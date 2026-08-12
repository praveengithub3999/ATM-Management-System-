# ATM-Management-System-
# Smart ATM Card Management System

A simple **Python-based ATM Card Management System** built using **Object-Oriented Programming (OOP)** concepts.

This project simulates basic ATM operations such as creating ATM cards, checking balances, depositing and withdrawing money, changing PINs, performing cash withdrawals, and viewing mini statements.

## Features

* Add a new ATM card
* View all registered ATM cards
* Search for an ATM card
* Remove an ATM card
* Check account balance
* Deposit money
* Withdraw money
* Change ATM PIN
* Cash withdrawal in multiples of 100
* View mini statement
* Track transactions
* Validate PIN and balance
* Prevent duplicate ATM card numbers

## Concepts Used

This project demonstrates several Python programming concepts:

* Classes and Objects
* Constructors (`__init__`)
* Instance Variables
* Methods
* Lists
* Loops
* Conditional Statements
* Functions
* User Input
* Basic Input Validation
* Transaction Management
* Object-Oriented Programming

## Project Structure

```text
Smart-ATM-Card-Management/
│
├── atm.py
└── README.md
```

> Replace `atm.py` with the actual filename you use for your Python program.

## How It Works

The project uses an `ATM` class to represent each ATM card.

Each ATM card stores:

* Card Number
* Card Holder Name
* PIN
* Account Balance
* Transaction History

Transactions are stored in a list using the `transactions` attribute.

### ATM Class

The main class contains methods for performing ATM operations:

```python
class ATM:
    def __init__(self, card_no, name, pin, balance):
        self.card_no = card_no
        self.name = name
        self.pin = pin
        self.balance = balance
        self.transactions = []
```

## Available Operations

When the program starts, the following menu is displayed:

```text
================================
      SMART ATM CARD MANAGEMENT
================================

1. Add ATM Card
2. View ATM Cards
3. Search ATM Card
4. Remove ATM Card
5. Check Balance
6. Deposit Money
7. Withdraw Money
8. Change PIN
9. Cash Withdrawal
10. Mini Statement
11. Exit
```

### 1. Add ATM Card

Allows the user to create a new ATM card by entering:

* Card number
* Card holder name
* 4-digit PIN
* Initial balance

The program also checks whether the card number already exists.

### 2. View ATM Cards

Displays the details of all ATM cards currently stored in the program.

### 3. Search ATM Card

Searches for an ATM card using its card number and displays the card details if found.

### 4. Remove ATM Card

Removes an existing ATM card from the ATM card list.

### 5. Check Balance

Requires the correct PIN before displaying the current account balance.

### 6. Deposit Money

Allows the user to deposit money into their account.

The program checks that the entered amount is greater than zero.

### 7. Withdraw Money

Allows money to be withdrawn from the account.

The program checks:

* The withdrawal amount is valid
* The account has sufficient balance

### 8. Change PIN

Allows the user to change their existing PIN after entering the correct old PIN.

The new PIN must contain exactly 4 digits.

### 9. Cash Withdrawal

Simulates ATM cash withdrawal.

The withdrawal amount must:

* Be greater than zero
* Not exceed the available balance
* Be a multiple of 100

For example:

```text
100
500
1000
2500
```

are valid cash withdrawal amounts.

### 10. Mini Statement

Displays the ATM card details, transaction history, and available balance.

Example:

```text
=======================
ATM MINI STATEMENT
=======================
ATM Card Number: 12345678
Card Holder Name: John
Deposit: 5000
Withdrawal: 1000
ATM Cash Withdrawal: 500
-----------------------
Available Balance: 3500
=======================
```

## How to Run

### Step 1: Install Python

Make sure Python 3 is installed on your computer.

Check your Python version:

```bash
python --version
```

or:

```bash
python3 --version
```

### Step 2: Clone the Repository

```bash
git clone https://github.com/your-username/your-repository-name.git
```

### Step 3: Open the Project

```bash
cd your-repository-name
```

### Step 4: Run the Program

```bash
python atm.py
```

## Example

```text
SMART ATM CARD MANAGEMENT

1. Add ATM Card
2. View ATM Cards
3. Search ATM Card
4. Remove ATM Card
5. Check Balance
6. Deposit Money
7. Withdraw Money
8. Change PIN
9. Cash Withdrawal
10. Mini Statement
11. Exit

Enter Choice: 1

ADD ATM CARD

Enter ATM Card Number: 12345678
Enter Card Holder Name: John
Enter 4 Digit PIN: 1234
Enter Initial Balance: 10000

ATM Card Added Successfully
```

## Important Note

This is an **educational console-based project**. It does not use a database, encryption, authentication system, or real banking/ATM infrastructure.

ATM cards and transactions are stored only in memory, so all data will be lost when the program is closed.

The PIN is also stored as plain text in memory, which would **not be appropriate for a real banking application**.

## Future Improvements

Possible improvements include:

* Add a database such as SQLite or MySQL
* Encrypt or securely hash PINs
* Add login attempt limits
* Add transaction timestamps
* Add transaction IDs
* Generate ATM card numbers automatically
* Add account numbers
* Add fund transfer functionality
* Add interest calculation
* Add receipt generation
* Create a graphical user interface using Tkinter
* Build a web version using Flask or Django
* Add automated unit tests
* Improve input validation and error handling
