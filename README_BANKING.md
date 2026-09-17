## Compile and run

### Git Bash, WSL, or macOS/Linux

```bash
javac -d out $(find src -name "*.java")
java -cp out com.corejava.banking.Main
```

### Windows PowerShell

```powershell
New-Item -ItemType Directory -Force -Path out | Out-Null
$files = Get-ChildItem -Path src -Recurse -Filter *.java | ForEach-Object { $_.FullName }
javac -d out $files
java -cp out com.corejava.banking.Main
```

# Banking Information System Prototype

## Problem Statement

Develop a prototype of a Banking Information System in Core Java that provides a working preview of the key functionalities of a real banking system. The prototype demonstrates the core features and flow of the system, including user registration, account management, deposits, withdrawals, fund transfers, account statements, password protection, error handling, user interface, and temporary data persistence.

## Objective

The main objective is to build a practical and user-friendly banking system prototype that allows users to:

- create a bank account,
- log in securely,
- deposit and withdraw funds,
- transfer money to another account,
- view account details and statements,
- update personal information,
- handle invalid transactions properly.

## Requirements Covered

### 1. User Registration
- User enters personal details such as:
  - full name,
  - address,
  - contact number,
  - password,
  - initial deposit amount.
- The system creates a unique account number.
- On successful registration, the system confirms the account creation.

### 2. Account Management
- Users can view their account details.
- Users can update their profile information such as name, address, and contact number.
- Account balance is tracked and displayed.

### 3. Deposit and Withdrawal
- User can deposit money into their account.
- User can withdraw money from their account.
- The balance updates after every valid transaction.
- Insufficient funds are handled with a proper exception.

### 4. Fund Transfer
- User can transfer funds to another account number.
- The sender account is debited.
- The receiver account is credited.
- Transfer details are stored in the transaction history.

### 5. Account Statements
- The system displays transaction history with:
  - date and time,
  - transaction type,
  - transaction amount,
  - remaining balance,
  - description.

### 6. Password Protection
- Login requires a valid user ID and password.
- Unauthorized access is blocked.

### 7. Error Handling
- Invalid inputs are checked.
- Invalid transactions are rejected.
- Insufficient funds generate an error message.
- Invalid account numbers are handled.

### 8. User Interface
- Console-based menu driven UI is used.
- The user can navigate through banking operations easily.

### 9. Persistence
- The prototype stores user account information and transaction history temporarily in memory during the session.
- This is suitable for a prototype that demonstrates the application flow.

## Core Java Concepts Used

- Classes and Objects
- Encapsulation
- Data Hiding with private fields and getters/setters
- Collections (`HashMap` for users and account lookup)
- Exception Handling (`InvalidTransactionException`, `InsufficientFundsException`)
- Object-oriented design
- Console-based input/output

## System Features Implemented

1. Register new user
2. Login with password authentication
3. View account details
4. Update account profile
5. Deposit amount
6. Withdraw amount
7. Transfer funds between accounts
8. Display account statement
9. Logout and exit program

## Project Structure

- `com.corejava.banking.Main` – console menu and user interaction
- `com.corejava.banking.BankingSystem` – logic for registration, login, transactions, and statements
- `com.corejava.banking.User` – user information and password
- `com.corejava.banking.Account` – balance and transaction handling
- `com.corejava.banking.Transaction` – record for every banking event
- `com.corejava.banking.InvalidTransactionException` – custom invalid transaction error
- `com.corejava.banking.InsufficientFundsException` – custom insufficient funds error

## Run the Project

### Windows / PowerShell
```powershell
cd "c:\Users\USER\OneDrive\Documents\Soundarya_Week1"
New-Item -ItemType Directory -Force -Path out | Out-Null
$files = Get-ChildItem -Path src -Recurse -Filter *.java | ForEach-Object { $_.FullName }
javac -d out $files
java -cp out com.corejava.banking.Main
```

### Linux / macOS
```bash
cd /path/to/project
javac -d out $(find src -name "*.java")
java -cp out com.corejava.banking.Main
```

## Example Workflow

1. Register a user with name, address, phone number, password, and initial deposit.
2. Log in using the user ID and password.
3. Deposit money.
4. Withdraw money.
5. Transfer money to another valid account.
6. View statement to see all transactions and balances.

## Sample Output

```text
=== Banking Information System ===
1. Register User
2. Login
3. View Account Details
4. Deposit
5. Withdraw
6. Transfer Funds
7. View Account Statement
8. Update Profile
9. Logout
10. Exit
```

## Notes

This is a prototype designed for learning and demonstration. It uses in-memory storage, which meets the requirement for temporary persistence during the prototype session.
