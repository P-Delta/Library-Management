# Project Delta – UML Class Diagrams

---

| **User** |
|-----------|
| **Attributes**<br>+ id: UUID<br>+ name: string<br>+ email: string<br>+ phone: string (0..1)<br>– passwordHash: string<br>/ role: Role<br>+ createdAt: datetime<br>+ updatedAt: datetime |
| **Operations**<br>+ authenticate(password: string): bool<br>+ can(action: string): bool |

---

| **Member** |
|-------------|
| **Attributes**<br>+ membershipId: string<br>+ duesBalance: money<br>+ status: string<br>+ wishlist: Set<UUID> |
| **Operations**<br>+ addToWishlist(recordId: UUID): void<br>+ payDues(amount: money): void |

---

| **Admin** |
|------------|
| **Attributes**<br>+ permissions: Set<string> |
| **Operations**<br>+ assignRole(userId: UUID, role: Role): void |

---

| **CatalogueRecord** |
|----------------------|
| **Attributes**<br>+ id: UUID<br>+ title: string<br>+ authors: string[]<br>+ isbn: string (0..1)<br>+ publisher: string (0..1)<br>+ year: int (0..1)<br>+ subjects: string[] |
| **Operations**<br>+ availability(): string |

---

| **ItemCopy** |
|---------------|
| **Attributes**<br>+ barcode: string<br>+ recordId: UUID<br>+ status: CopyStatus<br>+ location: string (0..1)<br>+ condition: string (0..1) |
| **Operations**<br>+ markLost(): void<br>+ markDamaged(note: string): void |

---

| **Loan** |
|-----------|
| **Attributes**<br>+ id: UUID<br>+ memberId: UUID<br>+ barcode: string<br>+ startDate: date<br>+ dueDate: date<br>+ returnDate: date (0..1)<br>+ status: LoanStatus<br>+ renewalCount: int<br>/feesAccrued: money |
| **Operations**<br>+ renew(): bool<br>+ close(returnedOn: date): void |

---

| **Reservation** |
|------------------|
| **Attributes**<br>+ id: UUID<br>+ memberId: UUID<br>+ recordId: UUID<br>+ type: ReservationType<br>+ queuePosition: int<br>+ expiry: date<br>+ createdAt: datetime |
| **Operations**<br>+ cancel(): void |

---

| **Membership** |
|-----------------|
| **Attributes**<br>+ id: UUID<br>+ memberId: UUID<br>+ state: MembershipState<br>+ start: date (0..1)<br>+ end: date (0..1)<br>+ dues: money |
| **Operations**<br>(none) |

---

| **Notification** |
|-------------------|
| **Attributes**<br>+ id: UUID<br>+ userId: UUID<br>+ type: string<br>+ payload: text<br>+ sentAt: datetime (0..1)<br>+ status: string |
| **Operations**<br>(none) |

---

| **ContactSubmission** |
|-------------------------|
| **Attributes**<br>+ id: UUID<br>+ name: string<br>+ email: string<br>+ phone: string (0..1)<br>+ message: text<br>+ createdAt: datetime |
| **Operations**<br>(none) |

---

## Enumerations

| **Role** |
|-----------|
| MEMBER, ADMIN |

| **CopyStatus** |
|----------------|
| AVAILABLE, RESERVED, CHECKED_OUT, OVERDUE, LOST, DAMAGED |

| **LoanStatus** |
|----------------|
| ACTIVE, RENEWED, OVERDUE, CLOSED |

| **ReservationType** |
|---------------------|
| ReadingRoom, Loan |

| **MembershipState** |
|---------------------|
| Applied, Active, Suspended, Expired |

---

## Legend

`+` = public `-` = private `/` = derived (calculated) `(0..1)` = optional `*` = many

---

## Inheritance Hierarchy

User
<br>├─ Member
<br>└─ Admin

---

## Associations & Multiplicities

| From | Multiplicity | To | Multiplicity | Notes |
|------|---------------|----|---------------|--------|
| CatalogueRecord | 1 | ItemCopy | 0..* | A title has many physical copies |
| Member | 1 | Loan | 0..* | A member can have many loans |
| ItemCopy | 1 | Loan | 0..* | A copy can appear in multiple loans over time; at most one active at a time |
| Member | 1 | Reservation | 0..* | A member can reserve many books |
| CatalogueRecord | 1 | Reservation | 0..* | Reservations queue per record |
| Member | 1 | Membership | 0..* | At most one ACTIVE membership at any time |
| User | 1 | Notification | 0..* | System sends email messages to users |
| Member | 1 | CatalogueRecord | 0..* | Wishlist association (many-to-many logically) |

---

## Constraints / Business Rules

- A **Loan** can only reference an `ItemCopy` whose `status = AVAILABLE`.  
- Returning a copy sets `ItemCopy.status = AVAILABLE`; if late, compute `/feesAccrued`.  
- Each `Reservation.queuePosition` is unique per `recordId`; next ready copy → queuePosition 1.  
- Only **one active Membership** (`state = Active`) is allowed per `Member`.  
- Passwords are stored as `passwordHash` only (no plaintext).  
- Overdue loans trigger a `Notification`

