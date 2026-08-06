# API Assignment — B19 Mobile Financial Service API Testing

Postman/Newman test suite for a Mobile Financial Service (MFS) style API (bKash/Nagad-like). Covers admin login, user onboarding (customer, agent, merchant), and money flows: system deposit to agent, agent deposit to customer, send money between customers, cash-out, and merchant bill payment.

## Test Flow

1. Admin Login
2. Customer Create
3. Agent Create
4. Merchant Create
5. System Login and Deposit to Agent
6. Agent Login and Deposit to Customer 01
7. Customer 01 Login and Send Money to Customer 02
8. Customer 02 Login, Cash Out and Pay Merchant Bill

## Technologies

- [Postman](https://www.postman.com/) — collection authoring
- [Newman](https://www.npmjs.com/package/newman) — CLI collection runner
- [newman-reporter-htmlextra](https://www.npmjs.com/package/newman-reporter-htmlextra) — HTML test report
- Node.js

## Prerequisites

- Node.js and npm installed
- API server running locally at `http://localhost:5000` (or update `baseUrl` collection variable)

## Clone

```bash
git clone https://github.com/rashadkhan97/dMoney_Postman-API-with-Newman_B19.git
cd dMoney_Postman-API-with-Newman_B19
```

## Install

```bash
npm install
```

Or install dependencies individually:

```bash
npm install newman
npm install newman-reporter-htmlextra
```

## Run

```bash
node report.js
```

Runs the Postman collection via Newman and generates an HTML report at `Reports/report.html`. Open it in a browser to view results.

## Project Structure

```
API-Assignment/
├── Collection/
│   └── B19-API_Assignment.postman_collection.json   # Postman collection
├── Reports/
│   └── report.html                                  # Generated Newman HTML report
├── report.js                                         # Newman runner script
└── package.json
```
