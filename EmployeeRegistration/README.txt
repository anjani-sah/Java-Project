# Java Project Collection

This repository contains a collection of Java projects created to practice Java programming, Object-Oriented Programming, exception handling, database connectivity, web development, and core Java concepts.

## Projects in This Repository

### 1. Banking System

A menu-driven console-based banking application that manages customer accounts and basic banking operations.

Features:
- Create customer accounts
- Customer ID validation from 1 to 20
- Minimum balance validation
- Deposit money
- Withdraw money
- Insufficient balance handling
- Custom exception handling
- File-based customer data storage using `customers.txt`

Java concepts:
- Classes and objects
- Constructors
- Encapsulation
- Exception handling
- Custom exceptions
- File handling
- Conditional statements and loops

Folder: `BankingSystem/`

---

### 2. Employee Salary Calculation

A Java program that calculates salary hikes for different types of employees using inheritance and method overriding.

Employee types:
- Full Time Employee: 50% salary hike
- Intern Employee: 25% salary hike

Java concepts:
- Inheritance
- Constructor usage
- Method overriding
- Protected members
- Classes and objects

Folder: `Employee/`

---

### 3. Employee Registration Web Application

A Java-based web application for registering, viewing, and deleting employee records using JSP, Servlets, JDBC, and MySQL.

Features:
- Employee registration form
- Employee data validation
- Duplicate email checking
- Store employee records in MySQL
- Display all registered employees
- Delete employee records
- Success and error pages

Technologies:
- Java
- JSP
- Servlets
- JDBC
- MySQL
- Apache Tomcat
- HTML/CSS

Architecture:
- Model: Employee JavaBean
- DAO: Database operations
- Servlet: Request processing
- JSP: User interface
- JDBC: Database connectivity

Folder: `EmployeeRegistration/`

#### Employee Registration Setup

Prerequisites:
- JDK 1.8 or later
- Apache Tomcat 8.5
- MySQL 8.x
- Eclipse or Spring Tool Suite
- MySQL Connector Java JAR

Setup steps:

1. Open MySQL Workbench or MySQL CLI.
2. Run `EmployeeRegistration/schema.sql`.
3. Open `src/com/employee/util/DBConnection.java`.
4. Configure the MySQL username and password.
5. Import the project into Eclipse or STS.
6. Add the MySQL Connector JAR to the Java Build Path.
7. Add the same JAR to `WebContent/WEB-INF/lib/`.
8. Configure Apache Tomcat 8.5.
9. Run the project on the Tomcat server.
10. Open:

`http://localhost:8080/EmployeeRegistration/`

Main URLs:
- `/` → Registration form
- `/registerEmployee` → Employee registration
- `/listEmployees` → Employee list
- `/deleteEmployee?id=N` → Delete an employee

Project structure:

```text
EmployeeRegistration/
├── schema.sql
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

---

### 4. Method Overloading and Method Overriding

A Java program demonstrating compile-time polymorphism through method and constructor overloading, and runtime polymorphism through method overriding.

Overloading examples:
- Shape constructors for different shapes
- `area()` methods with different parameters

Overriding examples:
- `Hillstations` parent class
- `Manali` child class
- `Mussoorie` child class
- `Gulmarg` child class

Java concepts:
- Method overloading
- Constructor overloading
- Method overriding
- Inheritance
- Polymorphism
- Runtime method dispatch

Folder: `Overloading and Overriding/`

---

### 5. Student Marks and Percentage Calculator

A Java program that stores student information and calculates total marks and percentage.

Features:
- Store student roll number
- Store student name
- Store marks for multiple subjects
- Calculate total marks
- Calculate percentage
- Display student details

Example marks used in the program:
- 78
- 85
- 69
- 90
- 88

Java concepts:
- Classes and objects
- Arrays
- Encapsulation
- Methods
- Access modifiers
- Basic arithmetic operations

Folder: `Student/`

---

## Repository Structure

```text
Java-Project/
│
├── BankingSystem/
│   ├── BankingSystem.java
│   └── README.md
│
├── Employee/
│   ├── Employee.java
│   └── README.md
│
├── EmployeeRegistration/
│   ├── README.txt
│   ├── schema.sql
│   ├── src/
│   └── WebContent/
│
├── Overloading and Overriding/
│   └── Java source files
│
├── Student/
│   └── Student.java
│
└── README.md
```

## Technologies and Concepts Covered

- Java
- Object-Oriented Programming
- Classes and Objects
- Encapsulation
- Inheritance
- Polymorphism
- Method Overloading
- Method Overriding
- Constructors
- Exception Handling
- Custom Exceptions
- File Handling
- Arrays
- JDBC
- MySQL
- JSP
- Servlets
- Apache Tomcat
- DAO Pattern
- MVC-based web application structure

## Requirements

For the core Java projects:
- JDK 8 or later
- Any Java IDE such as Eclipse, IntelliJ IDEA, or VS Code

For Employee Registration:
- JDK 8 or later
- Apache Tomcat 8.5
- MySQL 8.x
- Eclipse or Spring Tool Suite
- MySQL Connector Java

## Learning Objectives

These projects demonstrate practical implementation of Java fundamentals and Object-Oriented Programming concepts. The collection also introduces database-driven web application development using JSP, Servlets, JDBC, and MySQL.

## Author

Anjani Sah

B.Tech CSE - Artificial Intelligence and Data Science
MIT World Peace University, Pune

GitHub: https://github.com/anjani-sah
