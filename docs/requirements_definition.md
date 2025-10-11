# Requirements Definition

### **System Scope/Purpose**

Client is requesting for an application that functions as a library management tool meant to be used by library users and workers. For library users, the 
application will appear as a normal application that lets them open various windows to make an account, sign up for a membership, search for books to loan, and 
other windows to track their history and fees for book loans. For library workers the application should appear differently with a dashboard that allows them to 
view a list as well as manage all of all their users, books, loans, overdue fees. Will be a web application so that regular library users and workers have easy 
accessibility to all library capabilites.

### **Waterfall model**

We are using waterfall model as the core/primary software process.
This plan driven approach will use feedback from one phase into another helping to ensure good coding habits, clear version control, and additional safety.

## Table of Contents
- [1. Requirements Elicitation & Analysis](#1-requirements-elicitation--analysis)
- [2. Requirements Specification](#2-requirements-specification)
- [3. Requirements Validation](#3-requirements-validation)


## 1. Requirements Elicitation & Analysis

Guest User: (Any user who wishes to view book selection or sign up)
- Must be able to make an account associated with the web app
  - Account will be made with a verified email and strong password (8 characters at least with a combination of numbers and upper/lower case letters)
- Be able to enroll for a library membership in a separate window
  -Attempts to use member capabilities like loaning or wishlisting a book without a membership will show a popup to activate a membership
- Must have a search window that allows users to search for books
  - Search filters will be added to sort by title, author, genre, and book availability
- Be able to enroll for a library membership in a separate window
  - Payment methods for membership must be verified before accepting
  - Auto-renew option will be asked to the user
- Able to log in

Member User: (Any library customer with an account and active membership)
- Reserve books for in-person reading/loaning in a separate window 
- Ability to wishlist books that are unavailable that sends out a email notification when it is available
- View current & past history records (books, loans, fees, etc.)
- Able to log out

Administrative User:
- Must be able to login to a dashboard that can manage users and keep track of their activity, history, and fees within the system
  - Option to allow for admin user to view the web application as a regular user
  - Capabilities of managing user include (add, modify, delete, etc.) books, loans, fees, etc.
- Must be able to view a list of all registered users and their roles in the web app
  - List must mention users membership status and/or administrative status

##  2. Requirements Specification
**Functional Requirements**
> -In addition to any user specfied requirement
- Must be able to store large quantities of various data (books, users, loans, return dates, etc..) likely within a database
  - Validation checks are needed for this to keep track of which books are being loaned out and which are physically available
- Must have an automatic system that sends out email notification reminders to library members for active and overdue book loans

- Footer section of every window in web app must have references/links to all social media platforms/accounts related to the web app

- Application must support multiple windows being opened and used by end-users as well as the ability to drag and rearrange windows

- Shortcuts, various fonts, resizable windows, and various color schemes must be included as features

**Non-Functional Requirements**
- *Performance*
  - Home page loads ≤ 3s  (disregarding backend build times)
  - Search results ≤ 2s

- *Scalability*
  - Supports ≥ 9 concurrent users for MVP

- *Availability & Reliability*
  - Cross platform (Must work with various OS’s)
  - 99.9% uptime accessibility during library hours (9:00 AM - 5:00 PM)
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

1. **Home**: Landing page, Introduces and addresses goal of the web app

2. **About**: Chronological list of educational qualifications, professional/technical skills, recognition, and work experience gained by each team member

3. **Credits**: Tasks/Roles assigned and completed by each team member with a headshot photograph

4. **Contact**: Fillable form with a name, email, and phone number field that when submitted by an end- user, sends an email notification to all team members

##  3. Requirements Validation

**Objectives**

- Serves as proof of final review
- Ensure all functional, non-functional, and any user requirements are valid and hold true to their designed purpose
  - Includes guest, member, adminstrative user, all windows needed, and any other functional/non-functional requirement

**Techniques/Methods for Signoff**

- Completeness for each functional requirement will be checked to make sure it lines up with what client asked for
- Consistency checks will be made to ensure all requirements are consistent
- Realism checks will be implemented for early feasibility and realism for development
  
**Criteria**

- &#x2611; Accepted: Requirements are feasible, testable, and ready for design phase
- &#x2610; Not-Accepted: Requirements are not feasible, testable, or cannot be implemented

**Schedule**

- All techniques/methods will be tested in order stated and will be reported as specified in the criteria
  - Completeness checks will be made to any functional requirement by design team when making class diagrams
  - Walkthrough checks will be made by programming team to ensure requirements are feasible
  - Consistency checks for all non-functional requirements will be made by quality control team with rigorous testing
  - Simulations can be made by anyone on the software team to check for multiple user experiences

**Requirements Signoff**

| Role            | GitHub User | Completeness | Consistency | Realism  | Date     |
|-----------------|-------------|--------------|-------------|----------|----------|
| Analyst         |             |   &#x2610;   |   &#x2610;  | &#x2610; | --/--/-- |
| Project Manager |             |   &#x2610;   |   &#x2610;  | &#x2610; | --/--/-- |
| Quality Control |             |   &#x2610;   |   &#x2610;  | &#x2610; | --/--/-- |
