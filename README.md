# ExpenseEase

ExpenseEase is a user-friendly and secure web application designed to help users manage their personal expenses. With features like Google OAuth integration, AI-driven expense descriptions, and multi-currency support, ExpenseEase streamlines the process of tracking daily financial activities and provides insights into spending habits.

[View the live project here](...)

## Table of Contents
- [User Experience (UX)](#user-experience-ux)
  - [Overview](#overview)
  - [User Stories](#user-stories)
  - [Developer Tasks](#developer-tasks)
  - [Agile](#agile)
- [Features](#features)
  - [Existing Features](#existing-features)
  - [Future Features](#future-features)
- [Design](#design)
  - [Wireframes](#wireframes)
  - [Database Schema](#database-schema)
- [Technologies Used](#technologies-used)
- [Testing](#testing)
- [Deployment](#deployment)
  - [How to Clone the Repository](#how-to-clone-the-repository)
  - [Create Application and Postgres DB on Heroku](#create-application-and-postgres-db-on-heroku)
- [Credits](#credits)
  - [Code](#code)
  - [Content](#content)
  - [Media](#media)
  - [Acknowledgments](#acknowledgments)
 



## User Experience (UX)

### Overview
The ExpenseEase project was created to offer a user-friendly and secure way to manage personal expenses. It aims to streamline tracking daily financial activities and includes advanced features like Google OAuth integration and AI-driven expense descriptions. This app is designed for anyone looking to take control of their finances and better understand their spending habits.

### Agile

The Agile methodology was employed to plan and manage the development of the ExpenseEase project. GitHub was used as the primary tool to demonstrate the Agile approach.

User Stories were then created as GitHub Issues, linked to the Epics. Custom issue templates were used to ensure consistency and clarity in describing the User Stories. Each User Story followed a specific format, including a title, and description.

A link to my Kanban board can be found [here](https://github.com/users/nathan-cool/projects/2/views/1?pane=issue&itemId=55533266)

![image](https://github.com/nathan-cool/ExpenseEase/assets/127421398/1a274d09-27e2-45f3-8314-7e9a6206226c)


### Epics
The following Epics were identified for this project:

- User Authentication and Account Management
- Expense Tracking Functionality
- Application Development and Deployment
- User Experience and Interface

### User Stories
Below are some of the key user stories implemented in this project:

- As a user, I would like to log in so that I can access my account
- As a user, I need the application to be responsive so that I can access and use it on various devices
- As a user, I need to be able to search for specific expenses and navigate through my expense history
- As a user, I would like to log out of my account
- As a user, I would like to know when I reach a page I don't have access to
- As a user, I need to receive clear feedback when I input data incorrectly or when errors occur
- As a user, I need to be able to set and update my preferences so that the application is tailored to my needs
- As a user, I would like to register for a new account so that I can create my profile and start using the application
- As a user, I would like the ability to add an expense to keep track of my expenses
- As a user, I want the ability to view my expenses
- As a user, I want the ability to edit my expenses
- As a user, I want the ability to delete an expense




## Features

### Existing Features

#### Authentication System and Security
- **Registration System**: Allows users to create a new account by providing their name, email, and password. The registration view splits the user's name into first and last names, validates the provided information, and if valid, sends a verification email to activate the account.
- **Login System**: Users can log in to their account using their email and password. The system checks if the account is active and has correct credentials before granting access.
- **Logout System**: Logged-in users can log out of their account, which redirects them to the login page with a success message.
- **Google OAuth Integration**: Users have the option to authenticate using Google, simplifying the login process without the need for a password.
- **Email Validation**: Validates email in real-time during registration to ensure they are not already in use and follow the correct format.
- **Password Validation**: Checks password strength to ensure it meets the required criteria for security.
- **Account Verification**: After registration, users receive an email with a link to verify their account, ensuring the email address belongs to them.

To restrict access to certain views and features, the Django `@login_required` decorator is used. This ensures that only registered and authenticated users can access these views. If an unauthenticated user tries to reach these views, they will be redirected to the login page.

#### Expense Management
- **View Expenses**: Users can view all their recorded expenses on the main expense dashboard.
- **Add Expenses**: Users can add new expenses by filling out a form that captures essential details such as the amount, date, category, and a description.
- **Edit Expenses**: Each expense can be edited using the edit functionality. Users can update the amount, date, category, description, and other relevant details.
- **Delete Expenses**: Expenses can be deleted with a confirmation step to prevent accidental deletions.
- **Generate Expense Descriptions Using AI**: Utilizes OpenAI's API to generate descriptive texts for expenses based on minimal input.
- **Multi-Currency Support**: Allow users to record expenses in different currencies, automatically converting them based on current exchange rates.
- **Search Expenses**: Users can easily find their recorded expenses by typing in keywords or amounts. The search feature lets you filter expenses based on different fields like amount, date, category, description, invoice number, and reference. This helps you quickly locate specific expenses without any hassle.
- **pagination**: To make it easier to browse through your expenses, the app uses pagination. This means your expenses are divided into smaller, more manageable pages, so you don't have to load everything at once. This keeps the app fast and user-friendly.


### Future Features
- **Password Reset**: Allows users to reset their password if forgotten, via a link sent to their registered email.
- **Two-Factor Authentication**: Adds an extra layer of security by requiring a second form of identification beyond just the username and password.
- **Expense Analytics**: Visual representations of expenses over time, categories, or other criteria to provide users with insights into their spending habits.
- **Budget Planning**: Tools to set monthly or annual budgets for various categories, with notifications for when spending approaches or exceeds these limits.
- **Expense Sharing**: Functionality for users to split and share expenses with others, useful for group activities or shared living arrangements.
- **Receipt Scanning**: Automatically populate expense entries by scanning receipts using OCR technology.



## The Skeleton Plain

### Wireframes

<details>
<summary>Main User Panel Wireframe</summary>
<br>
<img src="https://github.com/nathan-cool/django-expense-organizer/assets/127421398/bd58da71-5489-4f9f-a3ee-5acfe4f9a446" alt="Main User Panel">
</details>

<details>
<summary>Login Screen Wireframe</summary>
<br>
<img src="https://github.com/nathan-cool/django-expense-organizer/assets/127421398/aa88acc9-0e5f-45aa-80c9-d30c2b398442" alt="Login Screen">
</details>

<details>
<summary>Sign Up Screen Wireframe</summary>
<br>
<img src="https://github.com/nathan-cool/django-expense-organizer/assets/127421398/ea565ffb-fce8-40f4-8c36-68b1510cd27b" alt="Sign Up Screen">
</details>

<details>
<summary>Edit/Add Expense Screen Wireframe</summary>
<br>
<img src="https://github.com/nathan-cool/django-expense-organizer/assets/127421398/f1b00191-8bb1-4f60-b347-95b7e0aacde1" alt="Edit/Add Expense Screen">
</details>

## Site map 

To clarify the structure of the site and its navigation, I created a site map using Lucidchart:

![image](https://github.com/nathan-cool/ExpenseEase/assets/127421398/925a11f4-9812-4f68-bbf3-6db309e69f69)


### Database Schema

The database schema for this project is as follows: 

- **User Model (Built-in Django User Model)**
 - Fields:
   - `username`: CharField for storing the username (unique).
   - `email`: EmailField for storing the user's email address (unique).
   - `first_name`: CharField for storing the user's first name.
   - `last_name`: CharField for storing the user's last name.
   - `password`: CharField for storing the hashed password.
   - `is_active`: BooleanField indicating whether the user account is active.

- **Category Model**
 - Fields:
   - `name`: CharField for storing the name of the expense category.

- **Expenses Model**
 - Fields:
   - `owner`: ForeignKey relationship with the User model (on_delete=models.CASCADE).
   - `amount`: DecimalField for storing the expense amount.
   - `date`: DateField for storing the expense date.
   - `category`: CharField for storing the expense category.
   - `description`: TextField for storing the expense description.
   - `invoice_number`: CharField for storing the invoice number (optional).
   - `reference`: CharField for storing the reference (optional).

- **Preferences Model**
 - Fields:
   - `currency`: Allows users to change currency from the settings tab

  

## The Surface Plane

### Design

#### Colour Scheme

- **White (#FFFFFF)**: The main background color, offering a clean and bright look.
- **Dark Grey (#333533)**: Used for main text and key elements, providing high readability and contrast.
- **Violet (#712cf9)**: Adds vibrancy to buttons and interactive components.
- **Dark (#202020)**: Enhances visual feedback with button hover states.
- **Green (#1f7c4d)**: Signifies success messages and confirmations.
- **Purple (#5a23c8)**: Adds depth to design elements with shadow effects.

#### Typography

I've chosen **Nunito** as our primary font. It's clean, modern, and easy to read, making for a pleasant user experience.

#### Layout and Elements

- **Input Fields**: Rounded for a modern look.
- **Cards**: Custom widths and shadows enhance visual appeal.
- **Forms and Buttons**: Clean and simple, with hover effects to improve interaction feedback.
- **Responsive Design**: The app adapts to different screen sizes, ensuring a consistent experience whether you're on a phone, tablet, or desktop.

#### Special Elements

- **Alerts**: Success alerts are styled in green with white text to clearly indicate positive actions.
- **Password Toggle**: Conveniently placed for easy access, blending seamlessly with the form.
- **Navbar**: Simple and functional, with text styled for readability and a polished look.

#### Imagery

I've used background patterns and radial gradients to add depth and texture, creating a visually appealing and modern interface.

These design choices ensure the ExpenseEase looks great and is easy to use, no matter what device you're on.


## Planning

## Technologies Used

### Languages Used
- **Python 3**: The core backend programming language used for the application.
- **HTML5**: Used for structuring the web pages of the application.
- **CSS3**: Used to style the HTML content.
- **JavaScript**: Employed for adding interactive behaviors to web pages.

### Frameworks, Libraries & Programs Used
- **Django**: A high-level Python web framework used for developing the web application.
- **Python Standard Library**: Various modules such as `os`, `json`, and `re`.
- **dotenv**: Used for loading environment variables from a `.env` file.
- **OpenAI**: API used to generate descriptions for expenses.
- **Google OAuth**: Used for Google OAuth authentication.
- **JSON Web Tokens (JWT)**: Used for authentication and authorization.
- **Django Messages Framework**: Used to display success and error messages.
- **Django Authentication System**: For user registration, login, and logout functionality.
- **Django Email**: Used to send verification emails.

### Software & Web Applications Used
- **Git**: Used for version control.
- **GitHub**: For hosting Git repositories.
- **Visual Studio Code**: A code editor used for development.
- **Heroku**: Cloud platform used for deploying and hosting the web application.
- **PostgreSQL**: Used as the primary database.
- **Google Fonts**: Used for typography.
- **Balsamiq**: Used for creating mockups and prototypes.
- **Draw.io**: Used for creating visual representations of the application's architecture and user flows.


## Testing

### Validator Testing 

### Automated Testing

### Browser Compatibility


![Browser Testing](https://github.com/nathan-cool/django-expense-organizer/assets/127421398/803a96f7-b3be-4628-9c2b-2927e985ca0e)



### Manual Testing with User Storeys

<h3>Search and Pagination Functionality</h3>

<details>
<summary>Search Expenses</summary>

<table>
  <thead>
    <tr>
      <th>Test Case</th>
      <th>Procedure</th>
      <th>Expected Result</th>
      <th>Actual Result</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Search by amount (exact match)</td>
      <td>
        1. Log in to the application<br>
        2. Navigate to the expenses page<br>
        3. Enter a specific amount (e.g., '100') in the search field<br>
        4. Submit the search
      </td>
      <td>
        Only expenses with the exact amount of '100' are displayed<br>
        Only expenses belonging to the logged-in user are shown
      </td>
      <td>✅ Pass</td>
    </tr>
    <tr>
      <td>Search by amount (partial match)</td>
      <td>
        1. Enter a partial amount (e.g., '10') in the search field<br>
        2. Submit the search
      </td>
      <td>
        Expenses with amounts starting with '10' (e.g., '100', '105') are displayed<br>
        Only expenses belonging to the logged-in user are shown
      </td>
      <td>✅ Pass</td>
    </tr>
    <tr>
      <td>Search by date (exact match)</td>
      <td>
        1. Enter a specific date (e.g., '2024-06-11') in the search field<br>
        2. Submit the search
      </td>
      <td>
        Only expenses with the exact date of '2024-06-11' are displayed<br>
        Only expenses belonging to the logged-in user are shown
      </td>
      <td>✅ Pass</td>
    </tr>
    <tr>
      <td>Search by date (partial match)</td>
      <td>
        1. Enter a partial date (e.g., '2024-06') in the search field<br>
        2. Submit the search
      </td>
      <td>
        Expenses with dates starting with '2024-06' are displayed<br>
        Only expenses belonging to the logged-in user are shown
      </td>
      <td>✅ Pass</td>
    </tr>
    <tr>
      <td>Search by category</td>
      <td>
        1. Enter a category keyword (e.g., 'Travel') in the search field<br>
        2. Submit the search
      </td>
      <td>
        Expenses with categories containing the keyword 'Travel' are displayed<br>
        Only expenses belonging to the logged-in user are shown
      </td>
      <td>✅ Pass</td>
    </tr>
    <tr>
      <td>Search by description</td>
      <td>
        1. Enter a description keyword (e.g., 'dinner') in the search field<br>
        2. Submit the search
      </td>
      <td>
        Expenses with descriptions containing the keyword 'dinner' are displayed<br>
        Only expenses belonging to the logged-in user are shown
      </td>
      <td>✅ Pass</td>
    </tr>
    <tr>
      <td>Search by invoice number</td>
      <td>
        1. Enter an invoice number keyword (e.g., 'INV123') in the search field<br>
        2. Submit the search
      </td>
      <td>
        Expenses with invoice numbers containing the keyword 'INV123' are displayed<br>
        Only expenses belonging to the logged-in user are shown
      </td>
      <td>✅ Pass</td>
    </tr>
    <tr>
      <td>Search by reference</td>
      <td>
        1. Enter a reference keyword (e.g., 'REF456') in the search field<br>
        2. Submit the search
      </td>
      <td>
        Expenses with references containing the keyword 'REF456' are displayed<br>
        Only expenses belonging to the logged-in user are shown
      </td>
      <td>✅ Pass</td>
    </tr>
    <tr>
      <td>Failed search with no matching results</td>
      <td>
        1. Enter a search string that does not match any expense (e.g., 'nonexistent')<br>
        2. Submit the search
      </td>
      <td>
        No expenses are returned<br>
        An appropriate "No results found" message is displayed<br>
        No errors occur
      </td>
      <td>✅ Pass</td>
    </tr>
    <tr>
      <td>Search with multiple criteria</td>
      <td>
        1. Enter a complex search string that matches multiple fields (e.g., '100 2024-06 Travel')<br>
        2. Submit the search
      </td>
      <td>
        Expenses matching any of the criteria (amount, date, category) are displayed<br>
        Only expenses belonging to the logged-in user are shown
      </td>
      <td>✅ Pass</td>
    </tr>
  </tbody>
</table>

</details>

<details>
<summary>Pagination</summary>

<table>
  <thead>
    <tr>
      <th>Test Case</th>
      <th>Procedure</th>
      <th>Expected Result</th>
      <th>Actual Result</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Pagination with default page</td>
      <td>
        1. Log in to the application<br>
        2. Navigate to the expenses page without any query parameters
      </td>
      <td>
        The first 5 expenses are displayed<br>
        Pagination controls are visible and functional
      </td>
      <td>✅ Pass</td>
    </tr>
    <tr>
      <td>Pagination with specific page</td>
      <td>
        1. Load the expenses page with a specific page number (e.g., `?page=2`)
      </td>
      <td>The correct set of expenses for page 2 is displayed</td>
      <td>✅ Pass</td>
    </tr>
    <tr>
      <td>Pagination with invalid page number</td>
      <td>
        1. Load the expenses page with an invalid page number (e.g., `?page=999`)
      </td>
      <td>
        A valid page of expenses is displayed<br>
        No errors occur
      </td>
      <td>✅ Pass</td>
    </tr>
    <tr>
      <td>Pagination controls visibility</td>
      <td>
        1. Create more than 5 expenses<br>
        2. Navigate to the expenses page
      </td>
      <td>
        Pagination controls (next, previous, page numbers) are visible<br>
        Pagination controls are functional
      </td>
      <td>✅ Pass</td>
    </tr>
    <tr>
      <td>Pagination on boundary pages</td>
      <td>
        1. Navigate to the second page<br>
        2. Click to go to the first page<br>
        3. Navigate to the second-to-last page<br>
        4. Click to go to the last page
      </td>
      <td>
        Navigation to the first page from the second page works correctly<br>
        Navigation to the last page from the second-to-last page works correctly
      </td>
      <td>✅ Pass</td>
    </tr>
    <tr>
      <td>Currency display</td>
      <td>
        1. Set user preferences to a specific currency<br>
        2. View expenses on different pages
      </td>
      <td>The correct currency is displayed for all expenses based on user preferences</td>
      <td>✅ Pass</td>
    </tr>
    <tr>
      <td>Pagination without expenses</td>
      <td>
        1. Remove all expenses for the logged-in user<br>
        2. Navigate to the expenses page
      </td>
      <td>
        An appropriate "No expenses found" message is displayed<br>
        No errors occur
      </td>
      <td>✅ Pass</td>
    </tr>
    <tr>
      <td>Rapidly switching pages</td>
      <td>
        1. Navigate to the expenses page<br>
        2. Rapidly click through different page numbers
      </td>
      <td>
        The application handles rapid page switching gracefully<br>
        No performance issues or errors occur
      </td>
      <td>✅ Pass</td>
    </tr>
    <tr>
      <td>Adding expense on paginated view</td>
      <td>
        1. Navigate to a non-first page of expenses<br>
        2. Add a new expense
      </td>
      <td>
        The new expense is correctly added<br>
        Pagination adjusts accordingly
      </td>
      <td>✅ Pass</td>
    </tr>
    <tr>
      <td>Removing expense on paginated view</td>
      <td>
        1. Navigate to a non-first page of expenses<br>
        2. Remove an existing expense
      </td>
      <td>
        The expense is correctly removed<br>
        Pagination adjusts accordingly
      </td>
      <td>✅ Pass</td>
    </tr>
  </tbody>
</table>

</details>

<h3>User Authentication</h3>

<details>
<summary>Social Authentication</summary>

<table>
  <thead>
    <tr>
      <th>Test Case</th>
      <th>Procedure</th>
      <th>Expected Result</th>
      <th>Actual Result</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Successful Google OAuth authentication and user creation</td>
      <td>
        1. Click "Sign in with Google"<br>
        2. Select a Google account<br>
        3. Grant permissions
      </td>
      <td>New user account created and logged in</td>
      <td>✅ Pass</td>
    </tr>
    <tr>
      <td>Successful Google OAuth authentication with existing user</td>
      <td>
        1. Click "Sign in with Google"<br>
        2. Select a previously used Google account
      </td>
      <td>Existing user logged in successfully</td>
      <td>✅ Pass</td>
    </tr>
    <tr>
      <td>Failed Google OAuth authentication</td>
      <td>
        1. Click "Sign in with Google"<br>
        2. Cancel the Google authentication process
      </td>
      <td>User remains on login page with error message</td>
      <td>✅ Pass</td>
    </tr>
  </tbody>
</table>

</details>

<details>
<summary>User Registration</summary>

<table>
  <thead>
    <tr>
      <th>Test Case</th>
      <th>Procedure</th>
      <th>Expected Result</th>
      <th>Actual Result</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Successful user registration with valid data</td>
      <td>Enter valid name, email, and password</td>
      <td>Account created, verification email sent</td>
      <td>✅ Pass</td>
    </tr>
    <tr>
      <td>Registration with invalid password</td>
      <td>Enter valid name and email, but a password that doesn't meet requirements</td>
      <td>Error message displayed, registration prevented</td>
      <td>✅ Pass</td>
    </tr>
    <tr>
      <td>Registration with invalid name</td>
      <td>Enter invalid name (e.g., numbers or special characters)</td>
      <td>Error message displayed, registration prevented</td>
      <td>✅ Pass</td>
    </tr>
    <tr>
      <td>Registration with invalid email</td>
      <td>Enter an incorrectly formatted email address</td>
      <td>Error message displayed, registration prevented</td>
      <td>✅ Pass</td>
    </tr>
    <tr>
      <td>Registration with existing email</td>
      <td>Attempt to register with an email already in use</td>
      <td>Error message displayed, registration prevented</td>
      <td>✅ Pass</td>
    </tr>
  </tbody>
</table>

</details>

<h3>Input Validation</h3>

<details>
<summary>Email Validation</summary>

<table>
  <thead>
    <tr>
      <th>Test Case</th>
      <th>Procedure</th>
      <th>Expected Result</th>
      <th>Actual Result</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Email validation with empty email</td>
      <td>Submit registration form with empty email field</td>
      <td>Error message displayed, form submission prevented</td>
      <td>✅ Pass</td>
    </tr>
    <tr>
      <td>Email validation with existing email</td>
      <td>Enter an email address already registered</td>
      <td>Error message displayed, form submission prevented</td>
      <td>✅ Pass</td>
    </tr>
    <tr>
      <td>Email validation with invalid email format</td>
      <td>Enter an incorrectly formatted email (e.g., missing @ symbol)</td>
      <td>Error message displayed, form submission prevented</td>
      <td>✅ Pass</td>
    </tr>
    <tr>
      <td>Email validation with valid email</td>
      <td>Enter a correctly formatted, unused email address</td>
      <td>No error message, form submission allowed</td>
      <td>✅ Pass</td>
    </tr>
  </tbody>
</table>

</details>

<details>
<summary>Name Validation</summary>

<table>
  <thead>
    <tr>
      <th>Test Case</th>
      <th>Procedure</th>
      <th>Expected Result</th>
      <th>Actual Result</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Name validation with empty name</td>
      <td>Submit registration form with empty name field</td>
      <td>Error message displayed, form submission prevented</td>
      <td>✅ Pass</td>
    </tr>
    <tr>
      <td>Name validation with invalid characters</td>
      <td>Enter a name with numbers or special characters</td>
      <td>Error message displayed, form submission prevented</td>
      <td>✅ Pass</td>
    </tr>
    <tr>
      <td>Name validation with valid name</td>
      <td>Enter a name with only letters and spaces</td>
      <td>No error message, form submission allowed</td>
      <td>✅ Pass</td>
    </tr>
  </tbody>
</table>

</details>

<details>
<summary>Password Validation</summary>

<table>
  <thead>
    <tr>
      <th>Test Case</th>
      <th>Procedure</th>
      <th>Expected Result</th>
      <th>Actual Result</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Password validation with short password</td>
      <td>Enter a password shorter than the minimum required length</td>
      <td>Error message displayed, form submission prevented</td>
      <td>✅ Pass</td>
    </tr>
    <tr>
      <td>Password validation with missing required characters</td>
      <td>Enter a password without required elements (e.g., uppercase, lowercase, number)</td>
      <td>Error message displayed, form submission prevented</td>
      <td>✅ Pass</td>
    </tr>
    <tr>
      <td>Password validation with valid password</td>
      <td>Enter a password meeting all requirements</td>
      <td>No error message, form submission allowed</td>
      <td>✅ Pass</td>
    </tr>
  </tbody>
</table>

</details>

<details>
<summary>User Verification</summary>

<table>
  <thead>
    <tr>
      <th>Test Case</th>
      <th>Procedure</th>
      <th>Expected Result</th>
      <th>Actual Result</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Successful user verification</td>
      <td>Click verification link in email</td>
      <td>Account activated, user able to log in</td>
      <td>✅ Pass</td>
    </tr>
    <tr>
      <td>Verification with invalid token</td>
      <td>Modify verification link token and attempt to verify</td>
      <td>Error message displayed, account not activated</td>
      <td>✅ Pass</td>
    </tr>
    <tr>
      <td>Verification of already active user</td>
      <td>Attempt to verify an already verified account</td>
      <td>Redirected to login page with appropriate message</td>
      <td>✅ Pass</td>
    </tr>
  </tbody>
</table>

</details>

<details>
<summary>User Login and Logout</summary>

<table>
  <thead>
    <tr>
      <th>Test Case</th>
      <th>Procedure</th>
      <th>Expected Result</th>
      <th>Actual Result</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Successful user login</td>
      <td>Enter valid credentials and submit login form</td>
      <td>User logged in and redirected to dashboard</td>
      <td>✅ Pass</td>
    </tr>
    <tr>
      <td>Login with inactive account</td>
      <td>Attempt to log in with unverified account</td>
      <td>Error message displayed, login prevented</td>
      <td>✅ Pass</td>
    </tr>
    <tr>
      <td>Login with invalid credentials</td>
      <td>Enter incorrect email or password</td>
      <td>Error message displayed, login prevented</td>
      <td>✅ Pass</td>
    </tr>
    <tr>
      <td>Successful user logout</td>
      <td>Click logout button while logged in</td>
      <td>User logged out and redirected to login page</td>
      <td>✅ Pass</td>
    </tr>
  </tbody>
</table>
</details>

<h3>Expense Operations</h3>

<details>
<summary>Add Expense</summary>

<table>
  <thead>
    <tr>
      <th>Test Case</th>
      <th>Procedure</th>
      <th>Expected Result</th>
      <th>Actual Result</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Add expense with valid data</td>
      <td>
        1. Log in to the application<br>
        2. Navigate to the "Add Expense" page<br>
        3. Fill in all required fields with valid data<br>
        4. Click "Save" button
      </td>
      <td>
        Expense is successfully added to the database<br>
        User is redirected to the expenses page<br>
        Success message is displayed
      </td>
      <td>✅ Pass</td>
    </tr>
    <tr>
      <td>Add expense with missing required fields</td>
      <td>
        1. Navigate to the "Add Expense" page<br>
        2. Leave one or more required fields empty<br>
        3. Click "Save" button
      </td>
      <td>
        Expense is not added to the database<br>
        Error message is displayed for each missing required field<br>
        User remains on the "Add Expense" page
      </td>
      <td>✅ Pass</td>
    </tr>
    <tr>
      <td>Add expense with invalid amount format</td>
      <td>
        1. Navigate to the "Add Expense" page<br>
        2. Enter an invalid amount (e.g., "abc")<br>
        3. Fill in other required fields<br>
        4. Click "Save" button
      </td>
      <td>
        Expense is not added to the database<br>
        Error message is displayed for invalid amount<br>
        User remains on the "Add Expense" page
      </td>
      <td>✅ Pass</td>
    </tr>
  </tbody>
</table>

</details>

<details>
<summary>Edit Expense</summary>

<table>
  <thead>
    <tr>
      <th>Test Case</th>
      <th>Procedure</th>
      <th>Expected Result</th>
      <th>Actual Result</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Edit expense with valid data</td>
      <td>
        1. Navigate to the expenses page<br>
        2. Click "Edit" on an existing expense<br>
        3. Modify fields with valid data<br>
        4. Click "Save" button
      </td>
      <td>
        Expense is successfully updated in the database<br>
        User is redirected to the expenses page<br>
        Success message is displayed
      </td>
      <td>✅ Pass</td>
    </tr>
    <tr>
      <td>Edit expense with missing required fields</td>
      <td>
        1. Navigate to edit page for an existing expense<br>
        2. Remove data from one or more required fields<br>
        3. Click "Save" button
      </td>
      <td>
        Expense is not updated in the database<br>
        Error message is displayed for each missing required field<br>
        User remains on the edit expense page
      </td>
      <td>✅ Pass</td>
    </tr>
    <tr>
      <td>Edit expense category</td>
      <td>
        1. Navigate to edit page for an existing expense<br>
        2. Change the category to a different valid category<br>
        3. Click "Save" button
      </td>
      <td>
        Expense category is successfully updated in the database<br>
        User is redirected to the expenses page<br>
        Success message is displayed
      </td>
      <td>✅ Pass</td>
    </tr>
  </tbody>
</table>

</details>

<details>
<summary>Delete Expense</summary>

<table>
  <thead>
    <tr>
      <th>Test Case</th>
      <th>Procedure</th>
      <th>Expected Result</th>
      <th>Actual Result</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Delete existing expense</td>
      <td>
        1. Navigate to the expenses page<br>
        2. Click "Delete" on an existing expense<br>
        3. Confirm the deletion
      </td>
      <td>
        Expense is successfully removed from the database<br>
        User remains on the expenses page<br>
        Success message is displayed
      </td>
      <td>✅ Pass</td>
    </tr>
    <tr>
      <td>Attempt to delete non-existent expense</td>
      <td>
        1. Manually construct a URL to delete a non-existent expense ID<br>
        2. Navigate to this URL
      </td>
      <td>
        Error message is displayed indicating expense not found<br>
        User is redirected to the expenses page
      </td>
      <td>✅ Pass</td>
    </tr>
  </tbody>
</table>

</details>

<details>
<summary>Generate Expense Description</summary>

<table>
  <thead>
    <tr>
      <th>Test Case</th>
      <th>Procedure</th>
      <th>Expected Result</th>
      <th>Actual Result</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Generate description for existing expense</td>
      <td>
        1. Navigate to the edit page for an existing expense<br>
        2. Click "Generate Description" button
      </td>
      <td>
        A description is generated based on the expense details<br>
        The generated description is displayed in the description field<br>
        User remains on the edit expense page
      </td>
      <td>✅ Pass</td>
    </tr>
    <tr>
      <td>Generate description with missing expense details</td>
      <td>
        1. Create an expense with minimal details<br>
        2. Navigate to the edit page for this expense<br>
        3. Click "Generate Description" button
      </td>
      <td>
        A generic or partial description is generated<br>
        The generated description is displayed in the description field<br>
        User remains on the edit expense page
      </td>
      <td>✅ Pass</td>
    </tr>
    <tr>
      <td>Handle API error during description generation</td>
      <td>
        1. Temporarily invalidate the OpenAI API key<br>
        2. Navigate to the edit page for an existing expense<br>
        3. Click "Generate Description" button
      </td>
      <td>
        An error message is displayed indicating the description couldn't be generated<br>
        The original description (if any) remains unchanged<br>
        User remains on the edit expense page
      </td>
      <td>✅ Pass</td>
    </tr>
  </tbody>
</table>

</details>

<details>
<summary>Load Currency Data</summary>

<table>
  <thead>
    <tr>
      <th>Test Case</th>
      <th>Procedure</th>
      <th>Expected Result</th>
      <th>Actual Result</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Successfully load currency data</td>
      <td>
        1. Ensure the currencies.json file exists and is properly formatted<br>
        2. Navigate to the preferences page
      </td>
      <td>
        Currency data is loaded successfully<br>
        Preferences page is rendered with the list of currencies
      </td>
      <td>✅ Pass</td>
    </tr>
    <tr>
      <td>Handle missing currency data file</td>
      <td>
        1. Temporarily rename or remove the currencies.json file<br>
        2. Navigate to the preferences page
      </td>
      <td>
        Error message is displayed indicating the currency data file is not found<br>
        Preferences page is rendered with an empty currency list
      </td>
      <td>✅ Pass</td>
    </tr>
    <tr>
      <td>Handle invalid JSON in currency data file</td>
      <td>
        1. Modify the currencies.json file to contain invalid JSON<br>
        2. Navigate to the preferences page
      </td>
      <td>
        Error message is displayed indicating an error in decoding the currency data file<br>
        Preferences page is rendered with an empty currency list
      </td>
      <td>✅ Pass</td>
    </tr>
  </tbody>
</table>

</details>

<details>
<summary>Render Preferences Page</summary>

<table>
  <thead>
    <tr>
      <th>Test Case</th>
      <th>Procedure</th>
      <th>Expected Result</th>
      <th>Actual Result</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Render preferences page for user with existing preferences</td>
      <td>
        1. Log in as a user with existing preferences<br>
        2. Navigate to the preferences page
      </td>
      <td>
        Preferences page is rendered<br>
        Currency list is displayed<br>
        User's current currency preference is selected
      </td>
      <td>✅ Pass</td>
    </tr>
    <tr>
      <td>Render preferences page for user without existing preferences</td>
      <td>
        1. Log in as a new user without preferences<br>
        2. Navigate to the preferences page
      </td>
      <td>
        Preferences page is rendered<br>
        Currency list is displayed<br>
        No currency is selected by default
      </td>
      <td>✅ Pass</td>
    </tr>
  </tbody>
</table>

</details>

<details>
<summary>Update User Preferences</summary>

<table>
  <thead>
    <tr>
      <th>Test Case</th>
      <th>Procedure</th>
      <th>Expected Result</th>
      <th>Actual Result</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Update preferences for user with existing preferences</td>
      <td>
        1. Log in as a user with existing preferences<br>
        2. Navigate to the preferences page<br>
        3. Select a different currency<br>
        4. Submit the form
      </td>
      <td>
        User's preferences are updated in the database<br>
        Success message is displayed<br>
        User is redirected to the expenses page
      </td>
      <td>✅ Pass</td>
    </tr>
    <tr>
      <td>Create preferences for user without existing preferences</td>
      <td>
        1. Log in as a new user without preferences<br>
        2. Navigate to the preferences page<br>
        3. Select a currency<br>
        4. Submit the form
      </td>
      <td>
        New preferences are created for the user in the database<br>
        Success message is displayed<br>
        User is redirected to the expenses page
      </td>
      <td>✅ Pass</td>
    </tr>
    <tr>
      <td>Attempt to update preferences without selecting a currency</td>
      <td>
        1. Navigate to the preferences page<br>
        2. Submit the form without selecting a currency
      </td>
      <td>
        Error message is displayed indicating no currency was selected<br>
        User is redirected to the expenses page<br>
        No changes are made to the user's preferences
      </td>
      <td>✅ Pass</td>
    </tr>
  </tbody>
</table>

</details>

<h2>Test Results Summary</h2>
All manual tests passed successfully, demonstrating the robustness of our user authentication and management system. The application correctly handles various scenarios, including valid and invalid inputs, ensuring a secure and user-friendly experience.

### Device Testing
<details>
<summary>Responsivness</summary>

<table>
  <thead>
    <tr>
      <th>Device</th>
      <th>Test One</th>
      <th>Test Two</th>
      <th>Result One</th>
      <th>Result Two</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>iPhone SE</td>
      <td>Responsiveness</td>
      <td>Buttons/Features</td>
      <td>Pass</td>
      <td>Pass</td>
    </tr>
    <tr>
      <td>iPhone X</td>
      <td>Responsiveness</td>
      <td>Buttons/Features</td>
      <td>Pass</td>
      <td>Pass</td>
    </tr>
    <tr>
      <td>iPhone 14</td>
      <td>Responsiveness</td>
      <td>Buttons/Features</td>
      <td>Pass</td>
      <td>Pass</td>
    </tr>
    <tr>
      <td>iPhone 6</td>
      <td>Responsiveness</td>
      <td>Buttons/Features</td>
      <td>Pass</td>
      <td>Pass</td>
    </tr>
    <tr>
      <td>Galaxy Fold</td>
      <td>Responsiveness</td>
      <td>Buttons/Features</td>
      <td>Pass</td>
      <td>Pass</td>
    </tr>
    <tr>
      <td>24-inch Monitor</td>
      <td>Responsiveness</td>
      <td>Buttons/Features</td>
      <td>Pass</td>
      <td>Pass</td>
    </tr>
    <tr>
      <td>13-inch Laptop</td>
      <td>Responsiveness</td>
      <td>Buttons/Features</td>
      <td>Pass</td>
      <td>Pass</td>
    </tr>
  </tbody>
</table>
</details>




### Known bugs

#### Generate Expense Descriptions Using AI

- When attempting to create a new invoice, users are expected to be able to use AI to generate descriptive texts based on minimal input. However, this functionality does not trigger during the invoice creation process, although it operates correctly during the editing of invoices.

## Deployment

### How to Clone the Repository
<details>
<summary>Click to expand</summary>

To clone this repository and run the Django expenses app locally, follow these steps:

1. **Open Terminal**: Open your terminal if you are on macOS or Linux, or open CMD or PowerShell if you are on Windows.
2. **Install Git**: Ensure you have Git installed on your system. You can download and install it from [Git's official site](https://git-scm.com/downloads).
3. **Clone the Repository**:
    ```bash
    git clone https://github.com/yourusername/django-expenses-app.git
    ```
    Replace `yourusername` with your GitHub username or the username of the repository owner.
4. **Navigate to the Project Directory**:
    ```bash
    cd django-expenses-app
    ```
5. **Create a Virtual Environment** (Recommended):
    ```bash
    python -m venv venv
    ```
    Activate the virtual environment:
    - On macOS and Linux:
        ```bash
        source venv/bin/activate
        ```
    - On Windows:
        ```bash
        .\venv\Scripts\activate
        ```
6. **Install Dependencies**:
    ```bash
    pip install -r requirements.txt
    ```
7. **Set Environment Variables**: Create a `.env` file in the root directory of the project and add the necessary environment variables like `DJANGO_SECRET_KEY`, `DATABASE_URL`, and any other required API keys.
8. **Migrate Database**:
    ```bash
    python manage.py migrate
    ```
9. **Run the Development Server**:
    ```bash
    python manage.py runserver
    ```
    Once the server is running, you can access the Django expenses app at `http://127.0.0.1:8000` in your web browser.
10. **Access the Application**: Open a browser and go to `http://127.0.0.1:8000` to start using the Django expenses app.

</details>

### Create Application and Postgres DB on Heroku
<details>
<summary>Click to expand</summary>

1. **Sign Up or Log In to Heroku**:
    - Sign up at [Heroku's website](https://signup.heroku.com/) or log in if you already have an account.
2. **Create a New Application**:
    - Navigate to your Heroku dashboard.
    - Click on the "New" button and select "Create new app."
    - Enter a name for your application and select the region closest to your users.
    - Click on "Create app."
3. **Add a PostgreSQL Database**:
    - Go to the "Resources" tab in your Heroku dashboard.
    - In the "Add-ons" section, start typing "Heroku Postgres" and select it.
    - Choose the free "Hobby Dev" plan for development purposes.
    - Click "Submit Order Form" to add the PostgreSQL add-on to your application.
4. **Configure Environment Variables**:
    - Go to the "Settings" tab in your Heroku dashboard.
    - Under the "Config Vars" section, click on "Reveal Config Vars."
    - Add the necessary configuration variables such as `DJANGO_SECRET_KEY`, `DEBUG`, etc.
5. **Deploy Your Application**:
    - Connect your GitHub account under the "Deploy" tab by selecting "GitHub" as the deployment method.
    - Search for your repository and connect to it.
    - Enable Automatic Deploys or use the "Manual Deploy" section to deploy a specific branch.
6. **Run Migrations**:
    - After deploying, run your database migrations.
    - In the "More" dropdown menu, select "Run console."
    - Type `python manage.py migrate` and click "Run."
7. **Open Your App**: Click on the "Open app" button in the top right corner of the dashboard.

</details>

### Executing automated tests

### Final Deployment steps

## Credits 

### Code 

### Content 

### Media 

### Acknowledgments

I would like to express my gratitude to the Slack Community for their invaluable assistance. Stephen Seagrave for helping me throughout my coding. My mentor Brian Macharia.
