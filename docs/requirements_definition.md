## **Project Delta – Library Management System**  

### **1. System Scope/Purpose**  

Client is requesting for an application that functions as a library management tool meant to be used by library users and workers. For library users, the application will appear as a normal application that lets them open various windows to make an account, sign up for a membership, search for books to loan, and other windows to track their history and fees for book loans. For library workers the application should appear differently with a dashboard that allows them to view a list as well as manage all of all their users, books, loans, overdue fees. Our application will be a web application so that regular library users and workers have easy accessibility to the functions of the tool.

### **2. User Requirements**

A. Regular User

- Must be able to make an account associated with the web app (account tracks user’s activities such as book-borrowing, borrowing history, wish list, membership dues, etc.)

- Must have a search window that allows users to search for books

  - Search filters should be added to sort by title, author, genre, and book availability

- Be able to enroll for a library membership in a separate window

- Be able to reserve books for in-person reading/loaning in a separate window

B. Administrative User (Library workers)

- Login must take them to a dashboard that can manage users and keep track of their activity, history, and fees within the system.
  - Should also have an option that allows them to view the web application as a regular user

- Must be able to view a list of all registered users with an account in the application as well as any role they have
  - List must mention users membership status and/or administrative status

### **3. Application Requirements**

- Must be able to store large quantities of various data (books, users, loans, return dates, etc..) likely within a database
  - Validation checks are needed for loans to keep track of which books are being loaned out and which are physically available

- Must have an automatic system that sends out email notification reminders to library users for active and overdue book loans

- Footer section of every window in web app must have references/links to all social media platforms/accounts related to the web app

- Four separate windows related to a home, about, credits, and contact page

  1. Home: Introduces and addresses goal of the web app

  2. About: Chronological list of educational qualifications, professional/technical skills, recognition, and work experience gained by each team member

  3. Credits: Tasks/Roles assigned and completed by each team member with a headshot photograph

  4. Contact: Fillable form with a name, email, and phone number field that when submitted by an end-user, sends an email notification to all team members

### **4. Non-Functional Requirements**

- All user accounts must have encrypted login credentials

- Ensure system can handle concurrent requests
  
- System must be accessible the entire time during library hours (8:00 AM - 5:00 PM)

### **5. Design Specifications**

- Cross platform (Must work with various OS’s)

- Multiwindow Support: Application must support multiple windows being opened and used by end-users as well as the ability to drag and rearrange windows

- Accessibility: Shortcuts, various fonts, resizable windows, and various color schemes must be included as features

### **6. Technological Specifications**

- Platform: React

- Version Control: [GitHub](https://github.com/P-Delta)

- Database: MySQL
