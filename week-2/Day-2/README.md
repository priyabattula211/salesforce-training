# Day 9 – Salesforce APIs, Integrations, and Postman Basics

## Introduction

Day 9 focused on understanding Salesforce APIs, external integrations, REST API basics, authentication methods, JSON data format, and API testing using Postman.

This session helped me understand how Salesforce communicates with external applications and how enterprise systems exchange data securely and efficiently.

I also learned how APIs are important for integrating Salesforce with payment gateways, websites, mobile applications, and third-party enterprise systems.

---

# Topics Covered

- Introduction to APIs
- What is Integration
- REST API Basics
- HTTP Methods
- Request and Response
- JSON Data Format
- API Authentication
- Salesforce API Concepts
- Postman Basics
- Real-World Integration Examples
- Enterprise Communication Systems

---

# Key Learnings

- APIs help different applications communicate with each other.
- REST APIs are widely used in Salesforce integrations.
- HTTP methods are used to perform different operations.
- JSON is used for sending and receiving structured data.
- Authentication provides secure API communication.
- Postman is used for testing APIs.
- Salesforce APIs help integrate external systems with Salesforce.

---

# What is an API?

API stands for Application Programming Interface.

An API allows two different applications or systems to communicate and exchange information.

---

## Real-World Example

When a payment is completed on a website:

- Website sends payment information
- Payment gateway processes transaction
- Response is sent back to Salesforce
- Salesforce updates payment status automatically

This entire communication happens using APIs.

---

# What is Integration?

Integration means connecting multiple systems so they can work together automatically.

---

## Examples of Salesforce Integrations

- Payment Gateway Integration
- SMS Notification System
- Email Service Integration
- College Portal Integration
- Attendance Management System

---

# REST API Basics

REST stands for Representational State Transfer.

REST APIs are commonly used because they are:
- Lightweight
- Fast
- Scalable
- Easy to use

Salesforce supports REST APIs for communication with external applications.

---

# HTTP Methods

| Method | Purpose |
|---|---|
| GET | Retrieve data |
| POST | Create new records |
| PUT | Update records |
| DELETE | Delete records |

---

# Example API Request

```http
GET /services/data/v58.0/sobjects/Student__c
```

This request retrieves student records from Salesforce.

---

# Request and Response

## Request
A request is sent from a client to the server.

It contains:
- Endpoint URL
- HTTP Method
- Headers
- Authentication details

---

## Response
A response is returned by the server.

It contains:
- Status code
- Response message
- Data

---

# JSON Data Format

JSON stands for JavaScript Object Notation.

JSON is commonly used for API communication because it is lightweight and easy to read.

---

## Example JSON

```json
{
  "StudentName": "Priya",
  "Department": "IT",
  "Attendance": 82
}
```

---

# API Authentication

Authentication is used to secure APIs and prevent unauthorized access.

---

## Common Authentication Methods

- Username and Password
- OAuth Authentication
- Access Tokens

---

# Salesforce API Usage

Salesforce APIs are used for:
- Creating records
- Updating records
- Retrieving data
- Connecting external systems
- Automating integrations

---

# Postman Basics

Postman is an API testing tool used by developers.

Using Postman, developers can:
- Send API requests
- Test APIs
- View responses
- Debug integration issues

---

# Steps to Test API Using Postman

1. Open Postman
2. Select HTTP Method
3. Enter API Endpoint URL
4. Add Authentication
5. Send Request
6. View Response

---

# Real-World Integration Examples

## Payment Gateway Integration

- Student pays fees online
- Payment gateway processes payment
- Salesforce receives confirmation
- Fee status updates automatically

---

## SMS Notification Integration

- Attendance falls below 75%
- SMS API sends warning message automatically

---

## Email Integration

- Student registration completed
- Welcome email gets triggered automatically

---

# Enterprise Communication Workflow

```text
Website → API → Salesforce → Database Update → Notification
```

This workflow helped me understand how enterprise systems communicate in real time.

---

# API Advantages

- Faster communication
- Real-time updates
- Automation support
- Better scalability
- Secure data exchange
- Integration flexibility

---

# Reflection – Why APIs are Important

Modern enterprise applications cannot work independently.

Businesses use multiple systems such as:
- Websites
- Mobile apps
- Payment systems
- ERP software
- CRM platforms

APIs help all these systems communicate efficiently and automate business operations.

Without APIs, enterprise automation and integration would become difficult and inefficient.

---

# Trailhead Modules Completed

- API Basics
- Postman API Fundamentals
- Salesforce Platform APIs

---

# Tools Used

- Salesforce Trailhead
- Salesforce Developer Edition
- Postman
- GitHub
- VS Code

---

# Overall Understanding After Day 9

After completing Day 9, I understood:
- Basics of APIs and integrations
- REST API concepts
- HTTP methods and requests
- JSON data format
- API authentication
- Salesforce API communication
- Postman basics
- Enterprise system integrations
- Real-time communication workflows
- Importance of APIs in enterprise applications

This session helped me understand how Salesforce integrates with external systems and how APIs enable secure and scalable enterprise communication.
