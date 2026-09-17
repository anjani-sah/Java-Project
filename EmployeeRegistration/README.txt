# Employee Registration Web Application

A complete Java web application for managing employee records using JSP, Jakarta Servlets, JDBC, and MySQL. This folder contains the full Employee Registration project, including the registration module, employee listing module, employee deletion module, database setup, Java model, DAO layer, database connection utility, JSP pages, and web configuration.

## Project Modules

### 1. Employee Registration Module

Allows users to enter and register employee details through a JSP form.

Employee information includes:
- Full name
- Email address
- Phone number
- Department
- Salary

Validation is performed on the server side before the employee is stored in MySQL.

Main files:
- `WebContent/index.jsp`
- `src/com/employee/servlet/EmployeeServlet.java`
- `src/com/employee/model/Employee.java`
- `src/com/employee/dao/EmployeeDAO.java`

### 2. Employee Listing Module

Displays all registered employees in a structured dashboard and table.

Features:
- Total employee count
- Total payroll calculation
- Largest team display
- Search by name, email, or department
- Employee department badges
- Employee salary display
- Registration date
- Link to register a new employee

Main files:
- `src/com/employee/servlet/ListEmployeeServlet.java`
- `WebContent/list.jsp`

### 3. Employee Deletion Module

Allows an employee record to be removed from the database using the employee ID.

Main files:
- `src/com/employee/servlet/DeleteEmployeeServlet.java`
- `src/com/employee/dao/EmployeeDAO.java`

After deletion, the application redirects back to the employee list.

### 4. Registration Success Module

Displays a confirmation page after successful employee registration.

The page shows:
- Employee name
- Email
- Department
- Phone number
- Salary
- Active status
- Option to register another employee
- Option to view all employees

Main file:
- `WebContent/success.jsp`

### 5. Employee Model Module

`Employee.java` is the JavaBean or POJO used to represent employee data throughout the application.

Fields:
- `id`
- `name`
- `email`
- `phone`
- `department`
- `salary`
- `createdAt`

It uses private fields with constructors, getters, setters, and a `toString()` method.

Main file:
- `src/com/employee/model/Employee.java`

### 6. Database Access Module

`EmployeeDAO.java` centralizes all SQL operations for the employee table.

Operations include:
- Register employee
- Retrieve all employees
- Retrieve employee by ID
- Check whether an email already exists
- Delete employee

Main file:
- `src/com/employee/dao/EmployeeDAO.java`

### 7. Database Connection Module

`DBConnection.java` provides JDBC connections to the MySQL database.

It manages:
- MySQL JDBC driver loading
- Database URL
- Database username
- Database password
- JDBC connection creation

Main file:
- `src/com/employee/util/DBConnection.java`

Important: Configure your own local MySQL credentials in `DBConnection.java`. Do not commit real database passwords or other credentials to GitHub.

### 8. MySQL Database Setup Module

`schema.sql` creates the database and employee table and also contains sample records for testing.

Database:
- `employee_db`

Table:
- `employee`

Main file:
- `schema.sql`

## Features

- Employee registration
- Server-side validation
- Email format validation
- Duplicate email detection
- Indian 10-digit mobile number validation
- Salary validation
- MySQL database storage
- Employee listing
- Employee search
- Employee deletion
- Registration success page
- Dashboard statistics
- JDBC connectivity
- MVC-style architecture
- DAO-based database operations
- JSP-based user interface

## Technologies Used

- Java
- Jakarta Servlets
- JSP
- JDBC
- MySQL
- HTML5
- CSS3
- Apache Tomcat
- MySQL Connector/J
- Eclipse or Spring Tool Suite

## Architecture

The application follows a simple MVC-style architecture.

```text
Presentation Layer
        |
        v
      JSP Pages
        |
        v
  Jakarta Servlets
        |
        v
   Employee Model
        |
        v
   EmployeeDAO
        |
        v
   DBConnection
        |
        v
       JDBC
        |
        v
   MySQL Database
```

## Main Components

### Employee.java

Acts as the model and JavaBean for employee information. It contains constructors, private fields, getters, setters, and object representation.

### EmployeeDAO.java

Handles all SQL operations using `PreparedStatement` and JDBC.

### DBConnection.java

Creates JDBC connections to the `employee_db` MySQL database.

### EmployeeServlet.java

Handles employee registration requests. It reads form data, validates the input, creates an `Employee` object, and stores it through the DAO.

### ListEmployeeServlet.java

Retrieves all employees from the database and forwards them to `list.jsp`.

### DeleteEmployeeServlet.java

Reads the employee ID, deletes the corresponding database record, and redirects to the employee list.

### index.jsp

Provides the employee registration form.

### success.jsp

Displays registration confirmation and the newly registered employee details.

### list.jsp

Displays all employee records with dashboard statistics, search functionality, department labels, salary information, and delete actions.

### web.xml

Defines the web application configuration and sets `index.jsp` as the welcome page. Servlet URL mappings are handled using `@WebServlet` annotations in the servlet classes.

## Database Structure

The application uses a MySQL database named `employee_db`.

The `employee` table contains:

| Column | Type | Description |
|---|---|---|
| id | INT | Auto-increment primary key |
| name | VARCHAR(100) | Employee name |
| email | VARCHAR(150) | Unique employee email |
| phone | VARCHAR(15) | Employee phone number |
| department | VARCHAR(60) | Employee department |
| salary | DOUBLE | Employee salary |
| created_at | TIMESTAMP | Record creation time |

The complete database setup is available in `schema.sql`.

## Application URLs

```text
http://localhost:8080/EmployeeRegistration/
```

Available endpoints:

| URL | Purpose |
|---|---|
| `/` | Employee registration form |
| `/registerEmployee` | Register an employee |
| `/listEmployees` | View all employees |
| `/deleteEmployee?id=N` | Delete employee with the specified ID |

## Application Flow

### Employee Registration

```text
User opens registration page
        ↓
index.jsp
        ↓
EmployeeServlet
        ↓
Input validation
        ↓
Employee object created
        ↓
EmployeeDAO
        ↓
JDBC
        ↓
MySQL employee table
        ↓
success.jsp
```

### Employee Listing

```text
User opens All Employees
        ↓
ListEmployeeServlet
        ↓
EmployeeDAO
        ↓
MySQL
        ↓
List<Employee>
        ↓
list.jsp
```

### Employee Deletion

```text
User clicks Remove
        ↓
/deleteEmployee?id=N
        ↓
DeleteEmployeeServlet
        ↓
EmployeeDAO.deleteEmployee()
        ↓
MySQL DELETE
        ↓
Redirect to /listEmployees
```

## Validation

The registration module validates:

- Name cannot be empty
- Email cannot be empty
- Email must follow a valid format
- Email must be unique
- Phone number must be a valid 10-digit Indian mobile number
- Department must be selected
- Salary cannot be empty
- Salary must be numeric
- Salary cannot be negative

If validation fails, the user is returned to the registration form and previously entered values are preserved.

## Prerequisites

- JDK 8 or later
- MySQL 8.x
- Apache Tomcat compatible with Jakarta Servlet 5.0
- MySQL Connector/J
- Eclipse, Spring Tool Suite, or another Java web IDE

The project uses the Jakarta Servlet namespace and a Servlet 5.0 web application configuration.

## Setup Instructions

### 1. Clone the repository

```bash
git clone https://github.com/anjani-sah/Java-Project.git
```

Open the `EmployeeRegistration` folder in your IDE.

### 2. Create the MySQL database

Open MySQL Workbench or MySQL CLI and execute:

```sql
source schema.sql;
```

This creates the `employee_db` database, the `employee` table, and sample employee records.

### 3. Configure database credentials

Open:

```text
src/com/employee/util/DBConnection.java
```

Set your own MySQL username and password.

Do not publish real passwords in the repository.

### 4. Add MySQL Connector/J

Add the MySQL Connector/J JAR to the project build path.

Place the required JAR inside:

```text
WebContent/WEB-INF/lib/
```

### 5. Configure the server

Import the folder as a Dynamic Web Project and configure a Jakarta-compatible Apache Tomcat server.

### 6. Deploy and run

Start the Tomcat server and open:

```text
http://localhost:8080/EmployeeRegistration/
```

## Project Structure

```text
EmployeeRegistration/
│
├── README.txt
├── schema.sql
│
├── src/
│   └── com/
│       └── employee/
│           ├── model/
│           │   └── Employee.java
│           │
│           ├── dao/
│           │   └── EmployeeDAO.java
│           │
│           ├── util/
│           │   └── DBConnection.java
│           │
│           └── servlet/
│               ├── EmployeeServlet.java
│               ├── ListEmployeeServlet.java
│               └── DeleteEmployeeServlet.java
│
└── WebContent/
    ├── index.jsp
    ├── success.jsp
    ├── list.jsp
    │
    └── WEB-INF/
        ├── web.xml
        └── lib/
            └── MySQL Connector/J JAR
```

## Java Concepts Demonstrated

- Object-Oriented Programming
- Classes and objects
- JavaBeans
- Encapsulation
- Constructors
- Getters and setters
- Servlets
- JSP
- JDBC
- PreparedStatement
- ResultSet
- DAO pattern
- MVC-style architecture
- Exception handling
- SQL CRUD operations
- HTTP GET and POST requests
- Request forwarding
- HTTP redirection
- Server-side validation

## CRUD Operations

| Operation | Implementation |
|---|---|
| Create | `EmployeeDAO.registerEmployee()` |
| Read | `EmployeeDAO.getAllEmployees()` and `getEmployeeById()` |
| Update | Not implemented in the current version |
| Delete | `EmployeeDAO.deleteEmployee()` |

## Learning Objectives

This project provides practical experience in building a Java database-driven web application. It demonstrates how JSP pages communicate with Jakarta Servlets, how JavaBeans represent application data, how DAO classes manage SQL operations, and how JDBC connects the application to MySQL.

## Future Improvements

Possible future enhancements include:

- Employee record update functionality
- Authentication and login
- Role-based access control
- Pagination for large employee lists
- Advanced filtering and sorting
- Export employee data to CSV or PDF
- Improved password and credential management
- Connection pooling
- REST API integration

## Author

Anjani Sah

B.Tech CSE - Artificial Intelligence and Data Science
MIT World Peace University, Pune

GitHub: https://github.com/anjani-sah
