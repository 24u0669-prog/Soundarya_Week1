# Banking Information System

A Core Java banking application prototype with a console-based banking workflow and a Swing dashboard interface. It demonstrates core banking operations such as registration, login, deposits, withdrawals, transfers, profile updates, balance checks, loan processing, and transaction history.

## Features

- User registration and login
- Admin login
- Deposit and withdrawal handling
- Fund transfer between accounts
- Balance enquiry and mini statement
- Account statement with transaction history
- Profile update
- Loan / EMI application flow
- GUI launch using Java Swing
- Temporary data storage for prototype use

## Project Overview

This project is designed as a banking system prototype to simulate real-world banking actions in a simplified Java application. It uses object-oriented design, collections, exception handling, and a menu-driven interaction model.

## Tech Stack

- Java SE
- Swing for desktop user interface
- Object-oriented programming
- Custom exception classes
- In-memory data persistence for prototype use

## Project Structure

```text
Soundarya_Week1/
├── bank_data.txt
├── index.html
├── README.md
├── README_BANKING.md
├── README_DASHBOARD.md
├── src/
│   └── com/
│       └── corejava/
│           └── banking/
│               ├── Account.java
│               ├── BankingAppGUI.java
│               ├── BankingSystem.java
│               ├── InsufficientFundsException.java
│               ├── InvalidTransactionException.java
│               ├── Loan.java
│               ├── Main.java
│               ├── Transaction.java
│               ├── User.java
│               └── dashboard/
│                   └── BankingDashboard.java
```

## Main Classes

- `Main` - console menu and user interaction
- `BankingSystem` - application logic for banking features
- `User` - user profile and login data
- `Account` - account details and balance management
- `Transaction` - transaction records
- `Loan` - EMI / loan details
- `BankingAppGUI` - Swing-based banking GUI
- `BankingDashboard` - dashboard UI screen

## Run the Console Application

### Windows PowerShell

```powershell
cd "C:\Users\USER\OneDrive\Documents\Soundarya_Week1"
New-Item -ItemType Directory -Force -Path out | Out-Null
$files = Get-ChildItem -Path src -Recurse -Filter *.java | ForEach-Object { $_.FullName }
javac -d out $files
java -cp out com.corejava.banking.Main
```

### Git Bash / Linux / macOS

```bash
cd /path/to/project
javac -d out $(find src -name "*.java")
java -cp out com.corejava.banking.Main
```

## Launch the GUI

### Windows PowerShell

```powershell
cd "C:\Users\USER\OneDrive\Documents\Soundarya_Week1"
$files = Get-ChildItem -Path src -Recurse -Filter *.java | ForEach-Object { $_.FullName }
javac -d out $files
java -cp out com.corejava.banking.BankingAppGUI
```

### Git Bash / Linux / macOS

```bash
cd /path/to/project
javac -d out $(find src -name "*.java")
java -cp out com.corejava.banking.BankingAppGUI
```

## Launch the Dashboard UI

```bash
javac -d out $(find src -name "*.java")
java -cp out com.corejava.banking.dashboard.BankingDashboard
```

## Typical Workflow

1. Register a new user
2. Log in with the generated user ID and password
3. Deposit or withdraw funds
4. Transfer money to another valid account
5. View account balance and statement
6. Apply for a loan or check EMI details
7. Update profile information
8. Log out or exit the system

## Notes

- This is a prototype for learning and demonstration.
- Data is stored temporarily in memory / local files for the prototype flow.
- The project is suitable for academic use, Java training, and object-oriented programming practice.

## Author
Soundarya Umesh Barigidad
Information Science Engineering Student
