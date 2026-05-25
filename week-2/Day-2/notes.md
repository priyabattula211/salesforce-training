# Day 9 Notes – Salesforce APIs, Integrations, and Postman Basics

## Introduction

Today’s session focused on understanding APIs, Salesforce integrations, REST API concepts, HTTP methods, JSON format, authentication, and API testing using Postman.

This topic helped me understand how Salesforce communicates with external applications and how enterprise systems exchange data automatically in real time.

---

# What is an API?

API stands for Application Programming Interface.

An API allows two different applications or systems to communicate with each other and exchange information.

---

## Simple Real-World Example

When a student pays fees online:

- Website sends payment request
- Payment gateway processes payment
- Salesforce receives confirmation
- Fee status gets updated automatically

This communication happens through APIs.

---

# What is Integration?

Integration means connecting multiple systems so they can work together automatically.

---

## Examples of Salesforce Integrations

- Payment Gateway Integration
- SMS Notification System
- Email Service Integration
- Student Portal Integration
- Attendance System Integration

---

# REST API

REST stands for Representational State Transfer.

REST APIs are widely used because they are:
- Fast
- Lightweight
- Scalable
- Easy to use

Salesforce supports REST APIs for external communication.

---

# HTTP Methods

| Method | Purpose |
|---|---|
| GET | Retrieve data |
| POST | Create records |
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

A request is sent from the client to the server.

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
- Message
- Data

---

# JSON Format

JSON stands for JavaScript Object Notation.

JSON is used to exchange data between systems because it is easy to read and lightweight.

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

Authentication is used to secure APIs.

It prevents unauthorized access to systems.

---

## Authentication Methods

- Username and Password
- OAuth
- Access Tokens

---

# Salesforce API Usage

Salesforce APIs are used for:
- Creating records
- Updating records
- Retrieving data
- External integrations
- Enterprise automation

---

# Postman Basics

Postman is a tool used to test APIs.

Developers use Postman to:
- Send requests
- Test APIs
- View responses
- Debug errors

---

# Steps to Test API in Postman

1. Open Postman
2. Select HTTP Method
3. Enter API URL
4. Add authentication
5. Click Send
6. View response

---

# Real-World Integration Examples

## Payment Integration

- Student completes payment
- Payment gateway confirms transaction
- Salesforce updates fee status

---

## SMS Notification System

- Attendance drops below 75%
- SMS notification gets sent automatically

---

## Email Automation

- Student registration completed
- Welcome email gets triggered automatically

---

# Enterprise Workflow Example

```text
Website → API → Salesforce → Database → Notification
```

This helped me understand how enterprise systems communicate automatically.

---

# Advantages of APIs

- Faster communication
- Real-time updates
- Automation support
- Better scalability
- Secure data transfer
- Easier integrations

---

# Reflection

Modern enterprise applications use multiple systems together such as:
- Websites
- Mobile applications
- Payment systems
- CRM platforms
- ERP software

APIs help these systems communicate efficiently and automate business operations.

Without APIs, enterprise-level automation would become difficult and inefficient.

---

# Trailhead Modules Completed

- API Basics
- Postman API Fundamentals
- Salesforce Platform APIs

---

# Overall Understanding

After completing Day 9, I understood:
- Basics of APIs
- Salesforce integrations
- REST API concepts
- HTTP methods
- Request and response handling
- JSON format
- API authentication
- Salesforce API communication
- Postman basics
- Enterprise system integrations
- Real-time communication workflows

This session improved my understanding of how Salesforce communicates with external systems and how APIs help businesses automate enterprise workflows efficiently.
