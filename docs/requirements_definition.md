# Requirements Definition

### **System Scope/Purpose**
Our client is requesting for a fully functional library management system used to manage library books, user memberships, book loans, etc. The software solution will be a modern web application so all library users and staff can have convenient accessibility to library capabilities.

## Table of Contents
- [Requirements Elicitation & Analysis](#1-requirements-elicitation--analysis)
- [Requirements Specification](#2-requirements-specification)
- [Requirements Validation](#3-requirements-validation)



## 1. Requirements Elicitation & Analysis

**Guest:** _(any user, not signed in)_
- Can make an account/log in
- Able to preview library book selection
- Be promted to make an account/sign in for more features

**Registered User**: _(signed in, might be member)_
- Able to begin/renew a membership
- Can manage membership
- Able to search through full selection of library books
- Reserve the physical books
- Recieve system notifications
- Leave reviews for books in the book selection
- Priority for new releases
- View checked out books/history of checked out books
- Can log out

**Administrator**: _(staff)_
- Has admin dashboard
- View and manage users, books, loans, fees, etc.
- The ability to back up/restore the library database



##  2. Requirements Specification

### **Functional Requirements (what the system must do)**

**Accounts/Membership**
- System must verify account is made with valid email

- Registered user accounts must automatically manage corresponding user activities (book borrowing, history, wishlist, membership dues, etc. )

**Book Management**
- Browse and search for library books
- filter by title, author, genre, and/or availability
- view information for each book
- Reserve available books
- Book wishlist

**Administrator Management**
- add, update, delete library books
- manage user accounts
- manage book metadata
- modify loans

**Loan/Fee Management**
- Loans must include full metadata regarding date/time and fees
- Users must be able to view current and prior loans
- Clear view of outstanding/overdue information

**Notifications**
- Automatic system that sends out email notification reminders to library registered users
  - for active and overdue book loans
  - renew their membership

**User Interface**
- Support multiple windows being opened/used
- Ability to drag and rearrange windows
- Shortcuts, various fonts, resizable windows, and various color schemes

**Window Requirements**
  1. **Home**: Landing page, introduces and addresses library goals to public
  2. **About**: Chronological list of educational qualifications, professional/technical skills, recognition, and work experience obtained by each team member
  3. **Credits**: Tasks/Roles assigned and completed by each team member with a headshot photograph
  4. **Contact**: Submittable form with a name, email, phone number, and message-box field for users (sends an email notification to all team members)
  5. **Footer**: included in all windows must have navigation to all social media platforms/accounts related to the library (at least 5)

### **Non-Functional Requirements (how the system must do 'it')**
- *Performance*
  - Home page loads ≤ 3s  (disregarding backend build times)
  - Search results ≤ 2s
  - Must be able to store large quantities of various data (books, users, loans, return dates, etc..)

- *Scalability*
  - Supports ≥ 9 concurrent users for MVP

- *Availability & Reliability*
  - Cross platform (Must work with various OS’s)
  - Works on all modern browsers
  - 99.9% uptime accessibility during library hours (9:00 AM - 5:00 PM)
  - Data persistance after crashes

- *Security*
  - password of at least 8 characters
  - password must contain at least one uppercase, lowercase, number, and special character
  - Passwords hashed
  - Role-based privileges
  - Ecnrypt users personal or sensitive information

- *Usability*
  - Responsive, accessible UI across devices
  - Smooth navigation between windows


- *Maintainability*
  - Modular codebase  
  - Updated documentation per release
  - Allowed to be easily updated and debugged when needed

##  3. Requirements Traceability

- Each functional requirement listed should be checked back to UML use case in order to maintain organization throughout
    the entirety of development phases, so that the requirements are represented in design, are implemented in the code,
    and to test the requirements. 

##  4. Requirements Validation

**Objectives**

Serves as final proof of review for the [Requirements Definition](requirements_definition.md) documentation

**Techniques/Methods for Signoff**
- Completeness for each functional requirement will be checked to make sure it lines up with what client asked for
  - Thoroughly ensure all requirements found in the [Requirements Elicitation & Analysis](#1-requirements-elicitation--analysis) section fulfills every requirement in the given client document
  - Repeat this process for [Requirements Specification](#2-requirements-specification)
  - Ensure there are no confusing elements that make it hard to understand purpose

- Consistency checks will be made to ensure [Requirements Elicitation & Analysis](#1-requirements-elicitation--analysis) corresponds with [Requirements Specification](#2-requirements-specification) through all functional and non-functional requirements
  - Make sure that requirements do not conflict with each other

- Realism will be considered helping predict feasibility and realism for development
  - All functional and non-functional requirements must be realistic and testable for later stages of development
  
**Criteria**
- &#x2611; Accepted: [Requirements Definition](requirements_definition.md) documentation has been thoroughly reviewed and ready for design phase
- &#x2610; Not-Accepted: Requirements are not feasible, testable, or cannot be implemented

**Requirements Signoff**

| Role            | GitHub User | Completeness | Consistency | Realism  | Date     |
|-----------------|-------------|--------------|-------------|----------|----------|
| Analyst         |             |   &#x2610;   |   &#x2610;  | &#x2610; | --/--/-- |
| Project Manager |             |   &#x2610;   |   &#x2610;  | &#x2610; | --/--/-- |
| Quality Control |             |   &#x2610;   |   &#x2610;  | &#x2610; | --/--/-- |
