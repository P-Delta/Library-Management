# Requirements Definition

### **System Scope/Purpose**

Client is requesting for an application that functions as a library management tool meant to be used by library users and workers. For library users, the 
application will appear as a normal application that lets them open various windows to make an account, sign up for a membership, search for books to loan, and 
other windows to track their history and fees for book loans. For library workers the application should appear differently with a dashboard that allows them to 
view a list as well as manage all of all their users, books, loans, overdue fees. Will be a web application so that regular library users and workers have easy 
accessibility to all the library capabilites.

### **Waterfall model**

We are using waterfall model as the core/primary software process.
This plan driven approach will use feedback from one phase into another helping to ensure good coding habits, clear version control, and additional safety.


## Table of Contents
- [1. Requirements Elicitation & Analysis](#1-requirements-elicitation--analysis)
- [2. Requirements Specification](#2-requirements-specification)
- [3. Requirements Validation](#3-requirements-validation)


##  1. Requirements Elicitation & Analysis

Regular User: (Any library customer who wishes to use the web app for their library activities)
- Must be able to make an account associated with the web app
  - Account will be made with a verified email and strong password (8 characters at least with a combination of numbers and upper/lower case letters)
- Be able to enroll for a library membership in a separate window
  -Attempts to use member capabilities like loaning or wishlisting a book without a membership will show a popup to activate a membership
- Must have a search window that allows users to search for books
  - Search filters should be added to sort by title, author, genre, and book availability
- Be able to enroll for a library membership in a separate window
  - Payment methods for membership must be verified before accepting
  - Auto-renew option will be asked to the user
- Able to log in

Member User: 
- Reserve books for in-person reading/loaning in a separate window 
- Ability to wishlist books that are unavailable that sends out a email notification when it is available
- View current & past history records (books, loans, fees, etc.)
- Able to log out

Administrative User:
- Must be able to login to a dashboard that can manage users and keep track of their activity, history, and fees within the system
  - Should also have an option that allows them to view the web application as a regular user
  - Capabilities of managing user include (add, modify, delete, etc.) books, loans, fees, etc.
- Must be able to view a list of all registered users and their roles in the web app
  - List must mention users membership status and/or administrative status

##  2. Requirements Specification
**Functional Requirements**

- Must be able to store large quantities of various data (books, users, loans, return dates, etc..) likely within a database
  - Validation checks are needed for this to keep track of which books are being loaned out and which are physically available
- Must have an automatic system that sends out email notification reminders to library users for active and overdue book loans

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

- Platform: React
- Version Control: [GitHub](https://github.com/P-Delta)
- Database: MySQL

##  3. Requirements Validation
