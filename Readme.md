## FinLedger Core - Secure Ledger-Based Banking Transaction API
FinLedger Core is a backend-focused banking transaction system built with Node.js, Express.js, MongoDB, Mongoose, JWT authentication, and Nodemailer. The project demonstrates a ledger-based account balance architecture, secure user authentication, transaction idempotency, immutable ledger entries, MongoDB session-based transaction handling, and email notifications.

## Key Features

# User Authentication
-User registration, login, and logout APIs
-JWT-based authentication
-Token blacklist support for logout handling
-Password hashing using bcryptjs

# Account Management
-Create user-linked accounts
-Fetch all accounts of the authenticated user
-Retrieve account balance from ledger entries instead of storing balance directly

# Ledger-Based Balance System
-Uses CREDIT and DEBIT ledger entries
-Balance is calculated dynamically as total credits minus total debits
-Ledger entries are treated as immutable records

# Transaction Processing
-Secure fund transfer between accounts
-Idempotency key support to prevent duplicate transaction processing
-Transaction statuses such as PENDING, COMPLETED, FAILED, and REVERSED
-MongoDB session-based transaction flow for debit and credit operations

# System User Flow
-Protected initial-funds endpoint for system-level users
-Middleware-based system user authorization

# Email Notifications
-Welcome email after registration
-Transaction success email after transfer
-Nodemailer with Gmail OAuth2 configuration

## Tech Stack

-Backend: Node.js, Express.js
-Database: MongoDB, Mongoose
-Authentication: JWT, Cookies, bcryptjs
-Email Service: Nodemailer, Gmail OAuth2
-Security Concepts: Password hashing, token blacklist, protected routes, idempotency key
-Architecture: MVC-style folder structure, controllers, models, routes, middleware, services

