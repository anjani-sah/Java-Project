# Method Overloading and Method Overriding

## Overview

This Java project demonstrates two important concepts of Object-Oriented Programming:

1. Method Overloading
2. Method Overriding

The project uses two practical examples. The `Shapes` class demonstrates constructor and method overloading for calculating areas. The `Hillstations` class and its subclasses demonstrate method overriding and runtime polymorphism using different hill stations.

## Features

- Demonstrates constructor overloading
- Demonstrates method overloading
- Demonstrates method overriding
- Demonstrates inheritance
- Demonstrates runtime polymorphism
- Calculates areas of different shapes
- Displays famous food and attractions for different hill stations

## Java Concepts Demonstrated

### 1. Constructor Overloading

The `Shapes` class contains multiple constructors with different parameter lists:

- `Shapes(double radius)` calculates the area of a circle
- `Shapes(double length, double breadth)` calculates the area of a rectangle
- `Shapes(double base, double height, boolean isTriangle)` calculates the area of a triangle

This demonstrates constructor overloading because the same constructor name is used with different parameters.

### 2. Method Overloading

The `Shapes` class contains two `area()` methods:

```java
void area(int side)
void area(int length, int breadth)
```

The methods have the same name but different parameter lists. The first calculates the area of a square and the second calculates the area of a rectangle.

### 3. Inheritance

`Manali`, `Mussoorie`, and `Gulmarg` extend the parent class `Hillstations`.

```java
class Manali extends Hillstations
class Mussoorie extends Hillstations
class Gulmarg extends Hillstations
```

This allows the subclasses to inherit the methods of the parent class and provide their own implementations.

### 4. Method Overriding

The subclasses override the `famousfood()` and `famousfor()` methods of `Hillstations`.

Each hill station provides different information:

| Hill Station | Famous Food | Famous For |
|---|---|---|
| Manali | Siddu | Snow and Adventure |
| Mussoorie | Maggi | Hill Views |
| Gulmarg | Kashmiri Cuisine | Skiing |

### 5. Runtime Polymorphism

The program uses a `Hillstations` reference to create objects of different subclasses:

```java
Hillstations h;

h = new Manali();
h = new Mussoorie();
h = new Gulmarg();
```

The appropriate overridden method is selected at runtime based on the actual object.

## Project Structure

```text
Overloading and Overriding/
│
├── overloading_and_overriding.java
├── Gulmarg.class
├── Hillstations.class
├── Manali.class
├── Mussoorie.class
├── Shapes.class
├── overloading_and_overriding.class
└── README.md
```

## Source Code Components

### Shapes

The `Shapes` class demonstrates constructor overloading and method overloading.

Area formulas used:

- Circle: `π × radius × radius`
- Rectangle: `length × breadth`
- Triangle: `0.5 × base × height`
- Square: `side × side`

### Hillstations

`Hillstations` is the parent class containing general implementations of:

- `famousfood()`
- `famousfor()`

### Manali

Overrides the parent methods to display:

- Food: Siddu
- Famous for: Snow and Adventure

### Mussoorie

Overrides the parent methods to display:

- Food: Maggi
- Famous for: Hill Views

### Gulmarg

Overrides the parent methods to display:

- Food: Kashmiri Cuisine
- Famous for: Skiing

### overloading_and_overriding

This is the main class. It creates objects of `Shapes` and different `Hillstations` subclasses and demonstrates both overloading and overriding.

## Program Flow

### Part 1: Shapes

1. A circle object is created using the single-parameter constructor.
2. A rectangle object is created using the two-parameter constructor.
3. A triangle object is created using the three-parameter constructor.
4. The overloaded `area(int side)` method calculates the square area.
5. The overloaded `area(int length, int breadth)` method calculates the rectangle area.

### Part 2: Hillstations

1. A `Hillstations` reference is declared.
2. The reference points to a `Manali` object.
3. Overridden methods display Manali-specific information.
4. The reference then points to a `Mussoorie` object.
5. Overridden methods display Mussoorie-specific information.
6. The reference finally points to a `Gulmarg` object.
7. Overridden methods display Gulmarg-specific information.

## Sample Output

```text
---- Shapes ----
Area of Circle: 78.5
Area of Rectangle: 24.0
Area of Triangle: 6.0
Area of Circle: 3.14
Area of Square: 25
Area of Rectangle: 24

---- Hillstations ----
Siddu
Snow and Adventure
Maggi
Hill Views
Kashmiri Cuisine
Skiing
```

## Requirements

- Java Development Kit (JDK) 8 or later
- Command Prompt, Terminal, or any Java-supported IDE

## How to Run

Open a terminal in the project directory and compile the Java source file:

```bash
javac overloading_and_overriding.java
```

Run the program:

```bash
java overloading_and_overriding
```

## Learning Objective

This project helps understand how Java supports compile-time and runtime polymorphism through method overloading and method overriding. It also provides practical understanding of constructors, inheritance, subclasses, parent class references, and object-oriented programming principles.

## Author

Anjani Sah

B.Tech CSE - AI & Data Science
MIT World Peace University, Pune
