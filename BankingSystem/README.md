# Banking System

A console based Java banking application that demonstrates object oriented programming, custom exception handling, user input, and file handling.

## Project Overview

The Banking System provides a simple menu driven interface for basic banking operations. Users can create an account, deposit money, withdraw money, and exit the application.

Customer account information is stored in `customers.txt` using Java file handling.

## Features

### 1. Create Account

Creates a new customer account after validating the customer ID and initial amount.

Validation rules:
- Customer ID must be between 1 and 20.
- Initial amount must be at least 1000.
- Customer details are saved to `customers.txt`.

### 2. Deposit

Allows the user to enter a deposit amount and calculates the updated balance.

Validation rule:
- Deposit amount must be greater than 0.

### 3. Withdraw

Allows the user to withdraw money from a specified current balance.

Validation rules:
- Withdrawal amount must be greater than 0.
- Withdrawal amount cannot exceed the current balance.

### 4. Exit

Terminates the menu driven application.

## Java Concepts Demonstrated

- Classes and objects
- Constructors
- Encapsulation basics
- Static members
- `Scanner` for user input
- File handling
- `FileWriter`
- Exception handling
- Custom exceptions
- Conditional statements
- Switch statements
- Loops
- Menu driven programming

## Custom Exceptions

The project defines three custom exceptions:

### InvalidAmountException

Used when an invalid deposit, withdrawal, or account opening amount is entered.

### InvalidCIDException

Used when the customer ID is outside the allowed range of 1 to 20.

### InsufficientBalanceException

Used when the withdrawal amount is greater than the available balance.

## Project Structure

```text
BankingSystem/
│
├── BankingSystem.java
├── BankingSystem.class
├── Customer.class
├── InvalidAmountException.class
├── InvalidCIDException.class
├── InsufficientBalanceException.class
├── customers.txt
└── README.md
```

The `.class` files are compiled Java files generated from the source code. The main source code is contained in `BankingSystem.java`.

## Program Flow

```text
Start
  |
  v
Display Menu
  |
  +---- 1. Create Account
  |          |
  |          +--> Validate CID
  |          +--> Validate Initial Amount
  |          +--> Save Customer Details
  |
  +---- 2. Withdraw
  |          |
  |          +--> Validate Amount
  |          +--> Check Balance
  |          +--> Calculate Remaining Balance
  |
  +---- 3. Deposit
  |          |
  |          +--> Validate Amount
  |          +--> Calculate Updated Balance
  |
  +---- 4. Exit
             |
             v
           End
```

## Requirements

- Java Development Kit, JDK 8 or later
- Command line terminal or Java IDE

## How to Run

Open a terminal in the `BankingSystem` directory.

Compile the program:

```bash
javac BankingSystem.java
```

Run the program:

```bash
java BankingSystem
```

## Example Menu

```text
1. Create Account
2. Withdraw
3. Deposit
4. Exit
Enter Choice:
```

## Data Storage

Customer records are appended to `customers.txt` when an account is created.

The stored format is:

```text
CID CustomerName Amount
```

For example:

```text
1 Anjani 5000.0
```

## Source File

The main source file is:

`BankingSystem.java`

It contains the `BankingSystem` class, `Customer` class, and the custom exception classes used by the application.

## Author

Anjani Sah

GitHub: https://github.com/anjani-sah
