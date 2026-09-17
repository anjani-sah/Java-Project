# Student Marks and Percentage Calculator

## Overview

This Java project demonstrates a simple Student Management program that stores student information and calculates the total marks and percentage obtained in five subjects.

The project also demonstrates Java access modifiers, constructors, arrays, methods, loops, and object-oriented programming concepts.

## Features

- Stores student roll number
- Stores student name
- Stores marks using an integer array
- Calculates total marks
- Calculates percentage
- Displays student details
- Uses a constructor to initialize student data
- Demonstrates different access modifiers

## Java Concepts Demonstrated

### Classes and Objects

The `Student` class represents a student and contains the student's roll number, name, and marks.

An object of the `Student` class is created in the `Main` class:

```java
Student student = new Student(101, "Anjani", marks);
```

### Constructor

The `Student` constructor initializes the roll number, name, and marks array:

```java
Student(int rollNo, String name, int[] marks)
```

### Arrays

The program stores marks for five subjects in an integer array:

```java
int[] marks = {78, 85, 69, 90, 88};
```

### Methods

The `Student` class contains three methods:

- `calculateTotal()` calculates the total marks
- `calculatePercentage()` calculates the percentage
- `displayDetails()` displays the student's information and percentage

### Access Modifiers

The project demonstrates three access levels:

| Member | Access Modifier | Purpose |
|---|---|---|
| `rollNo` | `private` | Restricts direct access to the class |
| `name` | `protected` | Allows access within the class and subclasses |
| `marks` | `public` | Allows direct access from other classes |

## Calculation

The program calculates the total marks by adding all values in the marks array.

For five subjects, the percentage is calculated as:

```text
Percentage = Total Marks / 5.0
```

For the current marks:

```text
78 + 85 + 69 + 90 + 88 = 410

Percentage = 410 / 5 = 82.0%
```

## Project Structure

```text
Student/
│
├── Student.java
├── Student.class
└── README.md
```

## Source Code Components

### Student Class

The `Student` class contains:

- `rollNo` for storing the student's roll number
- `name` for storing the student's name
- `marks` for storing subject marks
- Constructor for initializing student information
- `calculateTotal()` for calculating total marks
- `calculatePercentage()` for calculating percentage
- `displayDetails()` for displaying student details

### Main Class

The `Main` class contains the `main()` method. It creates the marks array, creates a `Student` object, and calls `displayDetails()`.

## Program Flow

1. The program creates an array containing marks for five subjects.
2. A `Student` object is created with roll number `101`, name `Anjani`, and the marks array.
3. The `displayDetails()` method is called.
4. The program calculates the total marks using `calculateTotal()`.
5. The percentage is calculated using `calculatePercentage()`.
6. The roll number, name, and percentage are displayed on the console.

## Sample Input Data

```text
Roll No: 101
Name: Anjani
Marks: 78, 85, 69, 90, 88
```

## Expected Output

```text
Roll No: 101
Name: Anjani
Percentage: 82.0
```

## Requirements

- Java Development Kit (JDK) 8 or later
- Command Prompt, Terminal, or any Java-supported IDE

## How to Run

Open a terminal inside the `Student` folder and compile the source file:

```bash
javac Student.java
```

Run the program:

```bash
java Main
```

## Learning Objective

This project provides practical understanding of Java classes and objects, constructors, arrays, loops, methods, access modifiers, and basic calculation logic. It is a simple example of applying object-oriented programming concepts to student marks processing.

## Author

Anjani Sah

B.Tech CSE - AI & Data Science
MIT World Peace University, Pune
