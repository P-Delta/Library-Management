# Requirements Definition

**System Scope/Purpose**

Application is a fully functional library management tool to manage the memberships, books, book loans, and other information of a
library. 
Will be a modern web application for accessibility so
regular library customers and workers can have easy
access to library capabilities.

**Waterfall model**

We are using waterfall model as the core/primary software process.
This plan driven approach will use feedback from one phase into another helping to ensure good coding habits, clear version control, and additional safety.


## Table of Contents
- [1. Requirements Elicitation & Analysis](#1-requirements-elicitation--analysis)
- [2. Requirements Specification](#2-requirements-specification)
- [3. Requirements Validation](#3-requirements-validation)


##  1. Requirements Elicitation & Analysis

Regular User:
> - Must be able to make a member account associated with the web app (account
> tracks user’s activities such as book-borrowing, borrowing history,
> wish list, membership dues, ...)
> - Must be able to search for books using a search window
> - Be able to enroll for a library membership in a separate window
> - Able to log in


Member User:
> - Reserve books for in-person reading/loaning in a separate
> window
> - View current & history records (books, loans, fees, etc.)
> - Able to log out
>

Administrative User:
> - Must be able to login to a dashboard that can manage users and keep
> track of their activity, history, and fees within the system
> - Must be able to view a list of all registered users and their roles
> in the web app
> - Capable of managing user (add, modify, delete, etc.) books, loans, fees, etc.


##  2. Requirements Specification
**Functional Requirements**

- Must be able to store large quantities of various data (books, users,
loans, return dates, etc..) likely within a database

- Validation checks are needed for this to keep track of which books
are being loaned out and which are physically available

- Must have an automatic system that sends out email notification reminders to
library users for active and overdue book loans

- Footer section of every window in web app must have references/links to
all social media platforms/accounts related to the web app

- Application must support multiple windows being
opened and used by end-users as well as the ability to drag and
rearrange windows

- Shortcuts, various fonts, resizable windows, and various
color schemes must be included as features

**Non-Functional Requirements**
- *Performance*
  - Home page loads ≤ 3s  (disregarding backend build times)
  - Search results ≤ 2s

- *Scalability*
  - Supports ≥ 9 concurrent users for MVP

- *Availability & Reliability*
  - Cross platform (Must work with various OS’s)
  - 99.9% uptime accessibility
  - Data persistance after crashes

- *Security*
  - Passwords hashed  
  - Role-based privileges

- *Usability*
  - Responsive, accessible UI across devices

- *Maintainability*
  - Modular codebase  
  - Updated documentation per release

- *Portability*
  - Works on all modern browsers


**Window Requirements**

*Footer (included in all windows)*

I. **Home**: Landing page, Introduces and addresses goal of the web app

II\. **About**: Chronological list of educational qualifications,
 professional/technical skills, recognition, and work experience gained
 by each team member

III\. **Credits**: Tasks/Roles assigned and completed by each team member
 with a headshot photograph

IV\. **Contact**: Fillable form with a name, email, and phone \# field
 that when submitted by an end- user, sends an email notification
 to all team members


**Technological Specifications**

\- Platform: React

\- Version Control: [GitHub](https://github.com/P-Delta)

\- Database: MySQL


##  3. Requirements Validation
