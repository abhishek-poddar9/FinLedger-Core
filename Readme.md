# FinLedger Core - Secure Banking Transaction Backend API

FinLedger Core is a backend-focused banking transaction system built with Node.js, Express.js, MongoDB, Mongoose, JWT authentication, and Nodemailer. The project demonstrates user authentication, account management, ledger-based balance calculation, duplicate transaction prevention using idempotency keys, and email notifications.

## Key Features

### User Authentication

- User registration, login, and logout APIs
- JWT-based authentication
- Token blacklist support for logout handling
- Password hashing using bcryptjs

### Account Management

- Create user-linked accounts
- Fetch all accounts of the authenticated user
- Retrieve account balance from ledger entries instead of storing balance directly

### Ledger-Based Balance System

- Uses CREDIT and DEBIT ledger entries
- Balance is calculated dynamically as total credits minus total debits
- Ledger entries are designed as immutable records

### Transaction Processing

- Authenticated fund transfer between accounts
- Client-provided idempotency key support to prevent duplicate transaction processing
- Transaction status tracking for pending and completed transfers
- Structured debit and credit ledger flow using MongoDB and Mongoose

### Email Notifications

- Welcome email after registration
- Transaction success email after transfer
- Nodemailer-based email notification service

## Tech Stack

- Backend: Node.js, Express.js
- Database: MongoDB, Mongoose
- Authentication: JWT, Cookies, bcryptjs
- Email Service: Nodemailer
- Security Concepts: Password hashing, token blacklist, protected routes, idempotency key
- Architecture: MVC-style folder structure, controllers, models, routes, middleware, services

