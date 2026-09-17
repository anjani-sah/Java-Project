# Employee Registration Web Application

A Java-based Employee Registration Web Application developed using JSP, Servlets, JDBC, and MySQL. The application allows users to register employee details, store them in a MySQL database, view registered employees, and delete employee records.

## Features

- Employee registration form
- Employee name, email, phone, department, and salary fields
- Input validation
- Duplicate email checking
- Store employee records in MySQL
- Display all registered employees
- Delete employee records
- Success and error pages
- Database connection using JDBC
- MVC-style project structure
- Search employees by name, email, or department
- Employee dashboard with total employees, payroll, and largest team

## Technologies Used

- Java
- JSP
- Servlets
- JDBC
- MySQL
- HTML and CSS
- JavaScript
- Apache Tomcat
- Eclipse or Spring Tool Suite
- MySQL Connector/J

## Project Architecture

The project follows a simple MVC-style architecture.

### Model

`Employee.java` is the JavaBean or POJO representing an employee record. It contains fields for ID, name, email, phone, department, salary, and creation time.

### DAO

`EmployeeDAO.java` handles database operations such as inserting, retrieving, checking duplicate emails, finding employees by ID, and deleting employee records.

### Servlets

- `EmployeeServlet.java` processes employee registration requests and validates form data.
- `ListEmployeeServlet.java` retrieves employee records and forwards them to the employee list page.
- `DeleteEmployeeServlet.java` handles employee deletion by ID.

### JSP Pages

- `index.jsp` provides the employee registration form.
- `success.jsp` displays registration confirmation and employee details.
- `list.jsp` displays all employees with dashboard statistics, search, and delete functionality.

## Database

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

The database setup and sample records are available in `schema.sql`.

## Validation

The application performs server-side validation for:

- Required employee name
- Valid email format
- Duplicate email prevention
- Valid 10-digit Indian mobile number
- Required department
- Valid salary value
- Prevention of negative salary values

## Main Application URLs

- `/` → Employee registration form
- `/registerEmployee` → Process employee registration
- `/listEmployees` → Display all employees
- `/deleteEmployee?id=N` → Delete an employee by ID

## Application Flow

```text
User
  ↓
JSP Registration Form
  ↓
EmployeeServlet
  ↓
Employee JavaBean
  ↓
EmployeeDAO
  ↓
JDBC
  ↓
MySQL Database
  ↓
Success / List / Error JSP
```

## Project Structure

```text
EmployeeRegistration/
├── schema.sql
├── README.md
├── README.txt
├── src/
│   └── com/employee/
│       ├── model/
│       │   └── Employee.java
│       ├── util/
│       │   └── DBConnection.java
│       ├── dao/
│       │   └── EmployeeDAO.java
│       └── servlet/
│           ├── EmployeeServlet.java
│           ├── ListEmployeeServlet.java
│           └── DeleteEmployeeServlet.java
└── WebContent/
    ├── index.jsp
    ├── success.jsp
    ├── list.jsp
    └── WEB-INF/
        ├── web.xml
        └── lib/
```

## Prerequisites

- JDK 8 or later
- Apache Tomcat with Jakarta Servlet support
- MySQL 8.x
- Eclipse or Spring Tool Suite
- MySQL Connector/J

## Setup Instructions

### 1. Set up the database

Open MySQL Workbench or MySQL CLI and execute the `schema.sql` file.

This creates the `employee_db` database and the `employee` table. Sample employee records are also included for testing.

### 2. Configure database connection

Open:

```text
src/com/employee/util/DBConnection.java
```

Update the MySQL username and password according to your local MySQL configuration.

Do not commit real database credentials to a public repository. Use environment variables or another secure configuration method for production applications.

### 3. Import the project

Import the `EmployeeRegistration` folder into Eclipse or Spring Tool Suite as a Dynamic Web Project.

### 4. Add MySQL Connector/J

Add the MySQL Connector/J JAR to the Java Build Path and place the required JAR inside:

```text
WebContent/WEB-INF/lib/
```

### 5. Configure the server

Configure a compatible Apache Tomcat server and deploy the project.

### 6. Run the application

Start the Tomcat server and open:

```text
http://localhost:8080/EmployeeRegistration/
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
- JDBC database connectivity
- DAO pattern
- MVC-style architecture
- Exception handling
- SQL database operations
- Form validation
- HTTP request handling

## Learning Objective

This project demonstrates how Java can be used to build a database-driven web application. It provides practical experience with JSP, Servlets, JDBC, MySQL, JavaBeans, DAO-based database operations, form validation, and basic web application architecture.

## Future Improvements

- Add employee update functionality
- Add authentication and role-based access
- Add pagination for large employee lists
- Move database credentials to environment variables
- Add REST API support
- Improve security with CSRF protection and stronger input sanitization

## Author

Anjani Sah

B.Tech CSE - Artificial Intelligence and Data Science
MIT World Peace University, Pune

GitHub: https://github.com/anjani-sah
