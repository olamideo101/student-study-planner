Student Assignment & Study Planner
Requirements Specification
1. Customer Statement of Requirements

The Student Assignment & Study Planner is a web application designed to help college students organize their academic responsibilities in one place. Students often have assignments, projects, exams, and other responsibilities spread across multiple courses, which can make it difficult to keep track of deadlines and priorities.

The purpose of this application is to provide students with a simple and organized system for managing their courses and assignments. Users will be able to create an account, log in securely, add their courses, create assignments, enter due dates and priorities, and track whether assignments have been completed.

The first iteration of the application will focus on the core features needed for academic organization. The system will provide a web-based user interface connected to a database so that each student's information can be stored and accessed when they log back into the application.

The main scope of the first iteration includes:

User registration and login
Course management
Assignment management
Assignment due dates
Assignment priority levels
Assignment descriptions
Completion tracking
Student dashboard
Persistent database storage
2. Requirements Specification
Functional Requirements

FR-1: User Registration
The system shall allow a new user to create an account.

FR-2: User Login
The system shall allow registered users to log into their accounts.

FR-3: User Logout
The system shall allow users to securely log out of the application.

FR-4: Course Creation
The system shall allow users to add courses to their account.

FR-5: Course Management
The system shall allow users to view, edit, and delete their courses.

FR-6: Assignment Creation
The system shall allow users to create assignments and associate each assignment with a course.

FR-7: Assignment Information
The system shall allow users to enter information for an assignment, including its title, description, due date, and priority.

FR-8: Assignment Management
The system shall allow users to view, edit, and delete assignments.

FR-9: Assignment Completion
The system shall allow users to mark assignments as completed.

FR-10: Dashboard
The system shall provide a dashboard where users can view their courses and assignments.

FR-11: Due-Date Tracking
The system shall display assignment due dates so users can identify upcoming academic responsibilities.

FR-12: Priority Tracking
The system shall allow assignments to be assigned a priority level so students can identify which tasks require greater attention.

FR-13: User-Specific Data
The system shall display only the courses and assignments associated with the currently logged-in user.

FR-14: Data Storage
The system shall save user, course, and assignment information in a database.

Non-Functional Requirements

NFR-1: Usability
The application shall provide a simple and easy-to-understand interface that allows students to navigate the system without extensive training.

NFR-2: Performance
The application should respond to normal user requests within a reasonable amount of time.

NFR-3: Security
The application shall protect user account information and restrict personal course and assignment information to the appropriate authenticated user.

NFR-4: Reliability
Information stored by users should remain available after users log out and return to the application.

NFR-5: Maintainability
The application code should be organized so that additional features can be added in future iterations.

NFR-6: Compatibility
The application should function through commonly used modern web browsers.

NFR-7: Data Integrity
The application should validate required information before saving records to the database.

3. Data and Storage Blueprint
Data Input

Data will primarily be entered manually by users through forms in the web application's graphical user interface.

During registration and login, users will enter account information through authentication forms.

Users will also enter information through course and assignment forms. Assignment data may include:

Assignment title
Course
Description
Due date
Priority
Completion status

The Flask backend will receive the information submitted through the HTML forms and process it before storing it in the database.

For the first iteration, the application will not require an external dataset or information fetched from another website. The primary source of data will be information entered directly by the user.

Database or Storage

The application will use SQLite as its database.

SQLite was selected because it is lightweight, easy to integrate with Python applications, and appropriate for the initial version of the project.

The database will contain information related to:

Users

User ID
Username
Email
Password information

Courses

Course ID
Course name
User ID

Assignments

Assignment ID
Assignment title
Description
Due date
Priority
Completion status
Course ID
User ID

Relationships between the tables will allow courses and assignments to be associated with the correct user.

The application will use Python with Flask for the backend and HTML/CSS for the web interface. Flask will process requests between the user interface and the SQLite database.
