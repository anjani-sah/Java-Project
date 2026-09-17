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

## Technologies Used

- Java
- JSP
- Servlets
- JDBC
- MySQL
- HTML and CSS
- Apache Tomcat
- Eclipse or Spring Tool Suite
- MySQL Connector/J

## Project Architecture

The project follows a simple MVC-style structure.

### Model

`Employee.java` is the JavaBean or POJO representing an employee record. It contains fields for ID, name, email, phone, department, salary, and creation time.

### DAO

`EmployeeDAO.java` handles database operations such as inserting, retrieving, and deleting employee records.

### Servlets

- `EmployeeServlet.java` processes employee registration requests.
- `ListEmployeeServlet.java` retrieves and displays employee records.
- `DeleteEmployeeServlet.java` handles employee deletion.

### JSP

JSP pages provide the web interface for registration, success messages, employee lists, and related responses.

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

The database setup is available in `schema.sql`.

## Prerequisites

- JDK 8 or later
- Apache Tomcat 8.5
- MySQL 8.x
- Eclipse or Spring Tool Suite
- MySQL Connector/J

## Setup Instructions

### 1. Set up the database

Open MySQL Workbench or MySQL CLI and run:

```sql
source schema.sql;
```

Or execute the complete `schema.sql` file directly in MySQL.

This creates the `employee_db` database and the `employee` table. Sample employee records are also included for testing.

### 2. Configure database connection

Open:

```text
src/com/employee/util/DBConnection.java
```

Update the MySQL username and password according to your local MySQL configuration.

### 3. Import the project

Import the `EmployeeRegistration` folder into Eclipse or Spring Tool Suite as a Dynamic Web Project.

### 4. Add MySQL Connector/J

Add the MySQL Connector/J JAR to the Java Build Path and place the required JAR inside:

```text
WebContent/WEB-INF/lib/
```

### 5. Configure Apache Tomcat

Add Apache Tomcat 8.5 as the server runtime and deploy the project.

### 6. Run the application

Start the Tomcat server and open:

```text
http://localhost:8080/EmployeeRegistration/
```

## Main Application URLs

- `/` → Employee registration form
- `/registerEmployee` → Process employee registration
- `/listEmployees` → Display all employees
- `/deleteEmployee?id=N` → Delete an employee by ID

## Project Structure

```text
EmployeeRegistration/
├── schema.sql
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
List / Success / Error JSP
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

## Learning Objective

This project demonstrates how Java can be used to build a database-driven web application. It provides practical experience with JSP, Servlets, JDBC, MySQL, JavaBeans, DAO-based database operations, and basic web application architecture.

## Author

Anjani Sah

B.Tech CSE - Artificial Intelligence and Data Science
MIT World Peace University, Pune

GitHub: https://github.com/anjani-sah
