# Java Projects Collection

A collection of Java programs and mini projects covering object-oriented programming, exception handling, file handling, inheritance, method overloading and overriding, JDBC, Servlets, JSP, and MySQL.

## Projects

### 1. Banking System

Path: `BankingSystem/`

A console-based banking application that demonstrates account creation and basic banking operations.

Features:
- Create a customer account
- Validate customer ID from 1 to 20
- Enforce a minimum account balance of 1000
- Deposit money
- Withdraw money
- Check for insufficient balance
- Store customer records in a text file
- Handle custom exceptions

Java concepts demonstrated:
- Classes and objects
- Constructors
- Encapsulation basics
- Custom exception handling
- File handling with `FileWriter`
- `Scanner` for user input
- Menu-driven programming

Custom exceptions:
- `InvalidAmountException`
- `InvalidCIDException`
- `InsufficientBalanceException`

Main file: `BankingSystem/BankingSystem.java`

### 2. Employee Salary Calculation

Path: `Employee/`

A simple employee salary calculation program that demonstrates inheritance and different salary calculations for full-time employees and interns.

Features:
- Store employee salary
- Calculate a 50% salary increase for full-time employees
- Calculate a 25% salary increase for interns
- Display salary before and after the increase

Java concepts demonstrated:
- Inheritance
- Constructors
- `super()`
- Method implementation in subclasses
- Protected members

Main file: `Employee/Employee.java`

### 3. Employee Registration Web Application

Path: `EmployeeRegistration/`

A Java web application for registering, viewing, and deleting employee records using JSP, Servlets, JDBC, and MySQL.

Features:
- Employee registration form
- Employee data validation
- Email existence checking
- Store employee records in MySQL
- Display all registered employees
- Delete employee records
- Success and error pages

Technology stack:
- Java
- JSP
- Servlets
- JDBC
- MySQL
- Apache Tomcat 8.5
- HTML
- Eclipse or Spring Tool Suite

Architecture:
- Model: `Employee.java`
- DAO: `EmployeeDAO.java`
- Database utility: `DBConnection.java`
- Servlets: `EmployeeServlet.java`, `ListEmployeeServlet.java`, `DeleteEmployeeServlet.java`
- Views: `index.jsp`, `success.jsp`, `list.jsp`
- Database schema: `schema.sql`

Main URL when running locally:
`http://localhost:8080/EmployeeRegistration/`

The project includes a detailed setup guide in `EmployeeRegistration/README.txt`.

### 4. Method Overloading and Method Overriding

Path: `Overloading and Overriding/`

A Java program demonstrating compile-time and runtime polymorphism through method overloading and method overriding.

Method overloading examples:
- Multiple `Shapes` constructors for circle, rectangle, and triangle areas
- Multiple `area()` methods with different parameters

Method overriding examples:
- `Hillstations` as the parent class
- `Manali`, `Mussoorie`, and `Gulmarg` as subclasses
- Each subclass provides its own implementation of `famousfood()` and `famousfor()`

Java concepts demonstrated:
- Method overloading
- Constructor overloading
- Method overriding
- Inheritance
- Runtime polymorphism

Main file: `Overloading and Overriding/overloading_and_overriding.java`

### 5. Student Marks and Percentage Calculator

Path: `Student/`

A Java program that stores student information and calculates total marks and percentage.

Features:
- Store roll number and student name
- Store marks using an integer array
- Calculate total marks
- Calculate percentage
- Display student details

Java concepts demonstrated:
- Classes and objects
- Constructors
- Arrays
- Access modifiers
- Methods
- Basic data processing

Main file: `Student/Student.java`

## Repository Structure

```text
Java-Project/
│
├── BankingSystem/
│   ├── BankingSystem.java
│   └── customers.txt
│
├── Employee/
│   └── Employee.java
│
├── EmployeeRegistration/
│   ├── schema.sql
│   ├── README.txt
│   ├── src/
│   │   └── com/employee/
│   │       ├── dao/
│   │       ├── model/
│   │       ├── servlet/
│   │       └── util/
│   └── WebContent/
│       ├── index.jsp
│       ├── success.jsp
│       ├── list.jsp
│       └── WEB-INF/
│
├── Overloading and Overriding/
│   └── overloading_and_overriding.java
│
├── Student/
│   └── Student.java
│
└── README.md
```

## Concepts Covered

This repository provides examples of:

- Java fundamentals
- Object-oriented programming
- Classes and objects
- Constructors
- Encapsulation
- Inheritance
- Polymorphism
- Method overloading
- Method overriding
- Arrays
- Exception handling
- Custom exceptions
- File handling
- JDBC
- Servlets
- JSP
- MySQL database integration
- MVC-style application structure

## Requirements

For the standalone Java programs:
- JDK 8 or later

For the Employee Registration web application:
- JDK 8 or later
- Apache Tomcat 8.5
- MySQL 8.x
- MySQL Connector/J
- Eclipse or Spring Tool Suite

## How to Run Java Programs

Compile a Java source file using:

```bash
javac FileName.java
```

Run the compiled class using:

```bash
java ClassName
```

For example:

```bash
cd Student
javac Student.java
java Main
```

For the Employee Registration web application, follow the setup instructions in `EmployeeRegistration/README.txt`.

## Learning Goals

The projects in this repository are designed to practice Java programming and core object-oriented programming concepts through small, practical applications. The collection progresses from basic classes and arrays to inheritance, polymorphism, exception handling, file handling, and database-backed web applications.

## Author

Anjani Sah

GitHub: https://github.com/anjani-sah

Repository: https://github.com/anjani-sah/Java-Project
