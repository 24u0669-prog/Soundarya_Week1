# Banking Dashboard (Core Java Swing)

This is a simple Core Java Swing dashboard designed to showcase the banking system in a modern and attractive desktop form.

## Features

- Bank title and branding
- Balance panel with account number card design
- Summary cards for savings, income, and card count
- Quick action buttons
- Recent transaction list
- Professional dark blue banking theme

## Run

```bash
javac -d out $(find src -name "*.java")
java -cp out com.corejava.banking.dashboard.BankingDashboard
```

## Windows PowerShell

```powershell
cd "c:\Users\USER\OneDrive\Documents\Soundarya_Week1"
$files = Get-ChildItem -Path src -Recurse -Filter *.java | ForEach-Object { $_.FullName }
javac -d out $files
java -cp out com.corejava.banking.dashboard.BankingDashboard
```
