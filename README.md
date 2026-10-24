# 🏦 Banking Management System

A console-based **Banking Management System** built using **Java, JDBC, and MySQL**. The application allows users to manage bank accounts and perform basic banking transactions through a command-line interface.

## ✨ Features

- 📝 User registration
- 🔐 User login and authentication
- 🏦 Create a new bank account
- 💰 Credit money
- 💸 Debit money
- 🔄 Transfer money between accounts
- 📊 Check account balance using a security PIN
- 🚪 Logout and exit the application

## 🛠️ Technologies Used

- **Java**
- **JDBC**
- **MySQL**
- **MySQL Connector/J**

## 🗄️ Database

The application uses a MySQL database named `banking_db` with two tables: `User` and `Accounts`.

```sql
CREATE DATABASE banking_db;
USE banking_db;

CREATE TABLE User (
    id INT AUTO_INCREMENT PRIMARY KEY,
    full_name VARCHAR(100) NOT NULL,
    email VARCHAR(100) UNIQUE NOT NULL,
    password VARCHAR(100) NOT NULL
);

CREATE TABLE Accounts (
    account_number BIGINT PRIMARY KEY,
    full_name VARCHAR(100) NOT NULL,
    email VARCHAR(100) NOT NULL,
    balance DECIMAL(15, 2) NOT NULL,
    security_pin VARCHAR(10) NOT NULL,
    FOREIGN KEY (email) REFERENCES User(email)
);
```

## 🚀 How to Run

1. Clone the repository.
2. Create the `banking_db` database and the required tables.
3. Configure your MySQL username and password in `BankingApp.java`.
4. Add the MySQL JDBC driver to the project.
5. Run `BankingApp.java`.

## 📚 Concepts Practiced

- Java Classes & Objects
- Constructors and Encapsulation
- Exception Handling
- JDBC Database Connectivity
- `Connection`
- `PreparedStatement`
- `ResultSet`
- SQL CRUD Operations
- Transaction Management using `commit()` and `rollback()`
- User Input using `Scanner`

## Usage 📋

Upon running the application, users can register or log in to access banking operations.

After logging in, users can open a bank account and perform transactions, including crediting money, debiting money, transferring funds, and checking their account balance.

## 👨‍💻 Author

**Priyanshu**

Built as a Java + JDBC learning project to practice database connectivity, SQL operations, and transaction management.