**Project Delta – Library Management System**

**1. System Scope/Purpose**

This application is a library management tool that is meant to be used to effectively
manage the memberships, books, book loans, and other information and operations of a
library. Our application will be a web application for accessibility so
regular library customers and workers of the library can have easy
access to the tool. This will have a user-friendly interface that make it easy for members to browse, borrow, and return books. To guarantee returns that are done on time, it should have an integrated notice system for the late books and deadlines that are coming up.

**2. User Requirements**

A. Regular User

> -Must be able to make an account associated with the web app (account tracks user’s activities such as book-borrowing, borrowing history, wish list, membership dues, ...)
>
> \-Must be able to search for books using a search window
> - Should be able to have a search that filters by title, author, genre, and the availability.
>
> -Be able to enroll for a library membership in a separate window
> -The mebership enrollment should be able to gather members personal details, their membership type, and payment information.
>
> -Be able to reserve books for in-person reading (only within library)/loaning in a separate window.

B. Administrative User

> \-Must be able to login to a dashboard that can manage users and keep
> track of their activity, history, and fees within the system
>
> -The UI design:
> -Login page
> -A reservation window
> -A search window and filtering options
> -A membership enrollment form
> -Must be able to view a list of all registered users and their roles in the web app.

**3. System Requirements**

> -Must be able to store large quantities of various data (books, users, loans, return dates, etc..) likely within a database.
> -SQL database preferred
> -Loan records
> -Staff and Administrator records
> -Validation checks are needed for this to keep track of which books are being loaned out and which are physically available
>
> -Must have an automatic system that sends out email notification reminders to library users for active and overdue book loans.
>
> -Footer section of every window in web app must have references/links to all social media platforms/accounts related to the web app
>
> -Four separate windows related to a home, about, credits, and contact page.
>
>> I. Home: Introduces and addresses goal of the web app
>
> >II\. About: Chronological list of educational qualifications,
> professional/technical skills, recognition, and work experience gained by each team member.
>
> >III\. Credits: Tasks/Roles assigned and completed by each team member with a headshot photograph.
>
> >IV\. Contact: Fillable form with a name, email, and phone # field that when submitted by an end-user, sends an email notification to all team members.

### Additional System Requrements

> -All user accounts must have encrypted login credentials. Multi factor authentication should be added for an extra layer of security.
>
> -Ensure system can handle concurrent requests. No degradation in performance. Should be able to handle failures like rate limiting to make sure that data isn't lost during heavy loading situations.
>
> -System must be accessible the entire time during library hours. There should be backup systems to quickly restore service in case there are critical failures.

**4. Design Specifications**

> -Cross platform (Must work with various OS’s, like Windows, macOS, mobile app,)
>
> -Multiwindow Support: Application must support multiple windows being opened and used by end-users as well as the ability to drag and rearrange windows. Each window should have the ability to perform several tasks in parallel without interfering with the others.
>
> -Accessibility: 
>
> -Keyboard Shortcuts -> For all major functions
> -Various font options
> -Text fields like Windows must be resizable to accomodate the user needs and various screen sizes
> -Various color schemes must be included as features. Should agree with Web Content Accesibility Guidelines.
>
**5. Validations**

>\-Input Validation:
>\-Guarantee that the email input follows a solid format.
>\-Strong Password -> Password with 8 characters and with at leastone number and a special symbol.
>\-A confirm password section to confirm the users password.
>\-Ensuring that a new email is not already in the system.
>\-Guarantee that the name, details etc, information is completed.
>\-Validate the credit card information and check if it is formatted correctly.
>\-Data Validation:
>\-Check if certain books are duplicated and deal with that.
>\-Confirm that the genre assigned to a book belongs to the right genre.
>\-Email Validation:
>\-Be sure of sending email reminders when a book is overdue when loan record updates.
>\-Check if the email could be successfully sent.


**5. Technological Specifications**

>\- Platform: React

>\- Version Control: [GitHub](https://github.com/P-Delta)
