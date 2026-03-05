# 💳 E-Wallet System

A **full-stack digital wallet application** built using **React, Spring Boot, and MySQL** that allows users to securely manage wallet balances, transfer money, and track transaction history.

This project simulates the basic functionality of modern **digital payment platforms**.

---

# 🚀 Features

### 👤 User Authentication

* User registration and login
* Password encryption
* Secure authentication using **JWT**

### 💰 Wallet Management

* Wallet created automatically for each user
* Add money to wallet
* Check wallet balance

### 🔁 Money Transfer

* Transfer money between users
* Balance validation before transaction
* Transaction status tracking

### 📜 Transaction History

* View sent and received transactions
* Timestamp and transaction details
* Track transaction status

### 📊 Transaction Filters

* Filter transactions by

  * Date
  * Amount
  * Transaction type

### 🛠 Admin Dashboard

Admin can view:

* Total users
* Total transactions
* Wallet balances

### 📧 Email Notification

Users receive email notifications after successful transactions.

---

# 🧰 Tech Stack

## Frontend

* React
* Axios
* React Router
* Bootstrap / Material UI

## Backend

* Java
* Spring Boot
* Spring Security
* JWT Authentication
* REST APIs

## Database

* MySQL

---

# 🗄 Database Design

## Users Table

| Column     | Description           |
| ---------- | --------------------- |
| id         | Primary Key           |
| name       | User name             |
| email      | User email            |
| password   | Encrypted password    |
| phone      | Phone number          |
| created_at | Account creation date |

## Wallet Table

| Column    | Description         |
| --------- | ------------------- |
| wallet_id | Primary Key         |
| user_id   | Foreign key (Users) |
| balance   | Wallet balance      |

## Transactions Table

| Column           | Description        |
| ---------------- | ------------------ |
| id               | Primary Key        |
| sender_id        | Sender user        |
| receiver_id      | Receiver user      |
| amount           | Transaction amount |
| transaction_type | Sent / Received    |
| timestamp        | Transaction time   |
| status           | SUCCESS / FAILED   |

---

# 📂 Project Structure

## Backend (Spring Boot)

com.walletapp

controller

* AuthController
* WalletController
* TransactionController

service

* UserService
* WalletService
* TransactionService

repository

* UserRepository
* WalletRepository
* TransactionRepository

model

* User
* Wallet
* Transaction

security

* JwtAuthenticationFilter
* JwtUtil

---

## Frontend (React)

src

components
pages

* Login
* Register
* Dashboard
* TransferMoney
* AddMoney
* TransactionHistory

---

# 🔌 API Endpoints

### Register User

POST /api/auth/register

### Login

POST /api/auth/login

### Add Money

POST /api/wallet/add-money

### Transfer Money

POST /api/wallet/transfer

### Check Balance

GET /api/wallet/balance

### Transaction History

GET /api/transactions

---

# ▶️ Running the Application

### Backend

1. Clone the repository
2. Configure MySQL in `application.properties`
3. Run Spring Boot application

### Frontend

1. Navigate to frontend folder
2. Install dependencies

npm install

3. Start React application

npm start

---

# 📈 Future Improvements

* QR Code payment simulation
* Mobile responsive UI
* Payment gateway integration
* Transaction analytics
* Multi-currency wallet support

---

# 👩‍💻 Author

Developed as a **full-stack learning project** to understand digital payment systems, secure backend APIs, and transaction management.
