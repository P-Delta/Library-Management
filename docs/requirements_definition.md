**Project Delta – Library Management System**

**1. System Scope/Purpose**

This application is a library management tool that is meant to be used to effectively
manage the memberships, books, book loans, and other information and operations of a
library. Our application will be a web application for accessibility so
regular library customers and workers of the library can have easy
access to the tool.

**2. User Requirements**

A. Regular User

> -Must be able to make an account associated with the web app (account
> tracks user’s activities such as book-borrowing, borrowing history,
> wish list, membership dues, ...)
>
> \-Must be able to search for books using a search window
    - Should be able to have a search that filters by title, author, genre, and the availability.
>
> -Be able to enroll for a library membership in a separate window
     -The mebership enrollment should be able to gather members personal details, their membership type, and payment information.
>
> -Be able to reserve books for in-person reading (only within library)/loaning in a separate
> window

B. Administrative User

> \-Must be able to login to a dashboard that can manage users and keep
> track of their activity, history, and fees within the system
>
> -The UI design:
> -Login page
> -A reservation window
> -A search window and filtering options
> -A membership enrollment form
> -Must be able to view a list of all registered users and their roles
> in the web app
> 

**3. System Requirements**

> -Must be able to store large quantities of various data (books, users,
> loans, return dates, etc..) likely within a database
>    -SQL database preferred
>    -Loan records
>    -Staff and Administrator records
> -Validation checks are needed for this to keep track of which books
> are being loaned out and which are physically available
>
> -Must have an automatic system that sends out email notification reminders to
> library users for active and overdue book loans
>
> -Footer section of every window in web app must have references/links to
> all social media platforms/accounts related to the web app
>
> -Four separate windows related to a home, about, credits, and contact page
>
>> I. Home: Introduces and addresses goal of the web app
>
> >II\. About: Chronological list of educational qualifications,
> professional/technical skills, recognition, and work experience gained
> by each team member
>
> >III\. Credits: Tasks/Roles assigned and completed by each team member
> with a headshot photograph
>
> >IV\. Contact: Fillable form with a name, email, and phone \# field
> that when submitted by an end-user, sends an email notification
> to all team members

### Additional System Requrements

> -All user accounts must have encrypted login credentials
>
> -Ensure system can handle concurrent requests
>
> -System must be accessible the entire time during library hours

**4. Design Specifications**

> - Cross platform (Must work with various OS’s)
>
> - Multiwindow Support: Application must support multiple windows being
> opened and used by end-users as well as the ability to drag and
> rearrange windows
>
> - Accessibility: Shortcuts, various fonts, resizable windows, and various
> color schemes must be included as features

**5. Technological Specifications**

\- Platform: React

\- Version Control: [GitHub](https://github.com/P-Delta)
