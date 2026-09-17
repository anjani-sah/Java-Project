# Employee Salary Calculation

## Overview

This project demonstrates employee salary calculation using Java inheritance. It models a general Employee class and extends it with FullTimeEmployee and InternEmployee classes.

The program calculates a salary increase based on the employee type and displays the salary before and after the increase.

## Features

- Store an employee's salary.
- Display the salary before the increase.
- Calculate a 50% salary increase for full-time employees.
- Calculate a 25% salary increase for interns.
- Display the updated salary.
- Reuse common employee functionality through inheritance.

## Java Concepts Demonstrated

- Classes and objects
- Inheritance
- Constructors
- `super()` keyword
- Protected access modifier
- Method implementation in subclasses
- Basic arithmetic operations
- Object-oriented programming

## Class Structure

### Employee

The `Employee` class acts as the parent class.

Property:

- `salary`: Stores the employee's current salary.

Methods:

- `Employee(double salary)`: Initializes the salary.
- `displaySalary(double newSalary)`: Displays the salary before and after the increase.

### FullTimeEmployee

`FullTimeEmployee` extends `Employee`.

Salary calculation:

```text
New Salary = Salary + 50% of Salary
```

Example:

```text
Original Salary: 40000
Salary after hike: 60000
```

### InternEmployee

`InternEmployee` extends `Employee`.

Salary calculation:

```text
New Salary = Salary + 25% of Salary
```

Example:

```text
Original Salary: 20000
Salary after hike: 25000
```

## Program Flow

```text
Start
  |
  v
Create FullTimeEmployee
  |
  v
Calculate 50% salary increase
  |
  v
Display salary
  |
  v
Create InternEmployee
  |
  v
Calculate 25% salary increase
  |
  v
Display salary
  |
  v
End
```

## Source File

```text
Employee/
└── Employee.java
```

The main program is located in `Employee.java`. It creates one full-time employee with a salary of 40000 and one intern with a salary of 20000. fileciteturn12file0

## Requirements

- Java Development Kit, JDK 8 or later
- Command line or any Java IDE such as IntelliJ IDEA, Eclipse, VS Code, or NetBeans

## How to Run

Open a terminal inside the `Employee` directory.

Compile the program:

```bash
javac Employee.java
```

Run the program:

```bash
java Employee
```

## Expected Output

```text
Full Time Employee
Salary before hike: 40000.0
Salary after hike: 60000.0

Intern Employee
Salary before hike: 20000.0
Salary after hike: 25000.0
```

## Learning Objective

This project provides a simple example of how inheritance can be used to share common properties and behavior between related classes while allowing subclasses to implement their own salary calculation logic.

## Author

Anjani Sah

GitHub: https://github.com/anjani-sah

Repository: https://github.com/anjani-sah/Java-Project
