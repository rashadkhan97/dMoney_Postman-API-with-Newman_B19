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
2. Admin creates a 2 Customer, 1 Agent, 1 Merchant.
3. System logs in and deposits money to the Agent.
   - **Hint**: fromAc: `SYSTEM`, toAc: `Agent`
   - `System Credentials - Email: system@dmoney.com; password:1234`
4. Agent logs in and deposits money to Customer 01.
   - **Hint**: fromAc: `Agent`, toAc: `Customer`
5. Customer 01 logs in and sends money to Customer 02.
   - **Hint**: fromAc: `Customer`, toAc: `Customer`
6. Customer 02 logs in, cashes out to Agent, and pays a Merchant bill.
   - **Hint**: fromAc: `Customer`, toAc: `Agent` / `Merchant`

## API Endpoint Details

- **User API Endpoints**: [_https://dmoney.roadtocareer.net/api-docs/user_](https://dmoney.roadtocareer.net/api-docs/user)

- **Transaction API Endpoints**: [_https://dmoney.roadtocareer.net/api-docs/transaction_](https://dmoney.roadtocareer.net/api-docs/transaction)
- **Partner Key**: X-AUTH-SECRET-KEY: `ROADTOSDET`

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

## Newman Report
<p align="center"> ### Report Summary </p>

<p align="center">
  <img src="https://github.com/user-attachments/assets/a9700e7b-1945-4834-976d-12864dfadbca" alt="Report Summary" width="700">
</p>

<p align="center"> ### Total Requests </p>
<p align="center">
  <img width="697" height="760" alt="image" src="https://github.com/user-attachments/assets/e53fb55e-210c-4f34-8557-9e95b243679a" />
</p>



