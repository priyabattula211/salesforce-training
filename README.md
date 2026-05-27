<div align="center">

  <img 
    src="https://upload.wikimedia.org/wikipedia/commons/f/f9/Salesforce.com_logo.svg" 
    alt="Salesforce Banner"
    width="180"
  />

# 🚀 Salesforce Summer Training Program

### Building Enterprise Solutions using Salesforce CRM, Apex, LWC, APIs, Automation, Security, and AI Technologies

</div>

---

# Overview

This repository contains my learning journey, hands-on practice, notes, assignments, mini-projects, and workflow implementations completed during the Salesforce Summer Training Program.

The training focused on understanding Salesforce CRM, automation, Apex programming, APIs, Lightning Web Components (LWC), security models, integrations, testing strategies, Salesforce DX, and enterprise application development using real-world business scenarios.

---

# Topics Covered

## Salesforce Fundamentals
- Salesforce CRM
- Cloud Computing
- Multi-Tenant Architecture
- Salesforce Platform
- Admin vs Developer

---

## CRM Concepts
- Leads
- Accounts
- Contacts
- Opportunities
- Customer Lifecycle
- Business Workflow

```text
Lead → Contact → Opportunity → Customer
```

---

## Data Modeling
- Apps, Objects, Tabs
- Fields & Records
- Standard vs Custom Objects
- Lookup & Master-Detail Relationships
- Formula Fields
- Validation Rules

---

## Automation
- Flow Builder
- Screen Flow
- Record-Triggered Flow
- Scheduled Flow
- Workflow Automation
- No-Code Development

---

## Apex Programming
- Apex Basics
- Classes & Methods
- OOP Concepts
- Exception Handling
- Collections
- Business Logic Development

### Example

```apex
public class StudentManager {

    public static String getMessage() {

        return 'Welcome Student';

    }

}
```

---

## Database & Querying
- SOQL
- SOSL
- Query Optimization
- Data Retrieval

### Example SOQL Query

```sql
SELECT Name
FROM Student__c
WHERE Attendance__c < 75
```

---

## Apex Triggers
- Before Triggers
- After Triggers
- Trigger Events
- Trigger Context Variables
- Event-Driven Systems

### Example Trigger

```apex
trigger StudentTrigger on Student__c (before insert) {

    for(Student__c stu : Trigger.new) {

        if(stu.Age__c < 0) {

            stu.addError('Age cannot be negative');

        }

    }

}
```

---

## APIs & Integrations
- REST API
- SOAP API
- HTTP Callouts
- JSON Handling
- Third-Party Integrations

### Example HTTP Callout

```apex
Http http = new Http();

HttpRequest req = new HttpRequest();

req.setEndpoint('https://api.example.com');

req.setMethod('GET');

HttpResponse res = http.send(req);

System.debug(res.getBody());
```

---

## Lightning Web Components (LWC)
- HTML Templates
- JavaScript Controllers
- Event Handling
- Reactive Properties
- Component Communication

### Example LWC

```html
<template>

    <h1>Hello Salesforce</h1>

</template>
```

```javascript
import { LightningElement } from 'lwc';

export default class HelloWorld extends LightningElement {

}
```

---

## Security & Access Management
- Profiles
- Roles
- Permission Sets
- Sharing Rules
- Field-Level Security
- Organization-Wide Defaults

---

## Testing & Deployment
- Apex Testing
- Test Classes
- Test Coverage
- Debugging
- Salesforce DX
- GitHub Integration
- Deployment Strategies

---

## Asynchronous Apex
- Future Methods
- Queueable Apex
- Batch Apex
- Scheduled Apex

---

# Week 1 Summary

### Day 1
- Salesforce CRM Basics
- Leads, Accounts, Contacts, Opportunities

### Day 2
- Apps, Objects, Tabs
- Multi-Tenant Architecture

### Day 3
- Data Modeling
- Relationships
- Validation Rules

### Day 4
- Flow Builder
- Automation & Workflows

### Day 5
- Apex Basics
- Business Logic

### Day 6
- SOQL
- Apex Triggers
- Platform Events

### Day 7
- Apex Testing
- Salesforce DX
- Asynchronous Apex

---

# Week 2 Summary

### Day 8
- Apex Classes
- OOP Concepts

### Day 9
- Collections
- Exception Handling

### Day 10
- APIs & Integrations
- HTTP Callouts

### Day 11
- Lightning Web Components
- UI Development

### Day 12
- Parent-Child Communication
- Reactive Properties

### Day 13
- Security & Access Management
- Sharing Rules

### Day 14
- Deployment Process
- Sandbox & GitHub Workflow

---

# Real-World Mini Project

## College Management System

### Objects Used
- Student
- Faculty
- Department
- Course
- Attendance
- Fees
- Examination

---

## Workflow

```text
Student Registration
        ↓
Validation Rules
        ↓
Automation Trigger
        ↓
Confirmation Email
        ↓
Attendance Tracking
        ↓
Fee Management
        ↓
Eligibility Verification
        ↓
Exam Registration
```

---

# Tools Used

- Salesforce Trailhead
- Salesforce Developer Edition
- VS Code
- Salesforce CLI
- GitHub

---

# Trailhead Modules Completed

- Salesforce CRM
- Data Modeling
- Automation Basics
- Apex Basics & Database
- Apex Testing
- Asynchronous Apex
- Salesforce DX Basics
- Platform Events Basics
- API Basics
- LWC Basics
- Security Basics

---

# Overall Learning

This Salesforce Summer Training Program helped me build strong knowledge in:

- Salesforce CRM
- Data Modeling
- Automation
- Apex Programming
- SOQL & SOSL
- Apex Triggers
- APIs & Integrations
- Lightning Web Components
- Security & Access Management
- Testing & Deployment
- Salesforce DX
- Enterprise Application Development

Through hands-on activities, mini-projects, and workflow implementations, I improved my understanding of how enterprise applications are built using Salesforce technologies.
