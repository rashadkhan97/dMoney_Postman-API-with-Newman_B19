# **API Assignment - DMoney Style REST API Testing with Newman**

## **Content**
- [Introduction](#introduction)
- [Test Cases Scenario](#test-cases-scenario)
- [API Endpoint Details](#api-endpoint-details)
- [How to run the project](#how-to-run-the-project)
- [Technology Used](#technology-used)
- [Project Structure](#project-structure)

## Introduction

This project is a Postman/Newman automated test suite for a Mobile Financial Service (MFS) REST API, simulating financial transactions where users transfer virtual/demo money between Admin, Agent, Customer, and Merchant accounts.

## Test cases scenario

1. Admin Login.
2. Admin creates a Customer.
3. Admin creates an Agent.
4. Admin creates a Merchant.
5. System logs in and deposits money to the Agent.
   - **Hint**: fromAc: `SYSTEM`, toAc: `Agent`
6. Agent logs in and deposits money to Customer 01.
   - **Hint**: fromAc: `Agent`, toAc: `Customer`
7. Customer 01 logs in and sends money to Customer 02.
   - **Hint**: fromAc: `Customer`, toAc: `Customer`
8. Customer 02 logs in, cashes out to Agent, and pays a Merchant bill.
   - **Hint**: fromAc: `Customer`, toAc: `Agent` / `Merchant`

## API Endpoint Details

- **Base URL**: `{{baseUrl}}` collection variable, default `http://localhost:5000`
- **Partner Key**: `X-AUTH-SECRET-KEY: ROADTOSDET`
- Endpoints grouped by folder in the Postman collection: Admin Login, Customer Create, Agent Create, Merchant Create, System Login and Deposit to Agent, Agent Login and Deposit to Customer 01, Customer 01 Login and Send Money to Customer 02, Customer 02 Login, Cash Out and Pay Merchant Bill.

## How to run the project

- Clone this project
   ```console
   git clone https://github.com/rashadkhan97/dMoney_Postman-API-with-Newman_B19.git
   ```
- Open with any code editor / Command Shell
- Give the following command ```npm i``` and ```node .\report.js```

## Technology Used
- Postman: If you haven't already, [download and install Postman.](https://www.postman.com/downloads/)
- Newman
- newman-reporter-htmlextra

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
