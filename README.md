<div align="center">

  <img 
    src="https://upload.wikimedia.org/wikipedia/commons/f/f9/Salesforce.com_logo.svg" 
    alt="Salesforce Banner"
    width="220"
  />

  <h1> Salesforce Summer Training Program</h1>

  <p>
    Building cloud-based enterprise solutions using Salesforce CRM, Apex,
    Lightning, Automation, SOQL, Triggers, APIs, LWC, Security,
    Integrations, Testing, Salesforce DX, and AI-powered technologies.
  </p>

</div>

---

# Salesforce Summer Training Program

## Overview

This repository contains my complete learning journey, hands-on practice, assignments, notes, mini-projects, workflows, and implementation activities completed during the Salesforce Summer Training Program.

The training focused on Salesforce CRM concepts, platform architecture, automation, Apex programming, Lightning Web Components, APIs, integrations, security models, testing strategies, asynchronous processing, Salesforce DX, and enterprise application development through Trailhead modules and real-world business scenarios.

---

# Topics Covered

## Salesforce Fundamentals
- Introduction to Salesforce
- CRM Basics
- Salesforce Platform
- Cloud Computing Concepts
- Multi-Tenant Architecture
- Salesforce Playground Setup
- Salesforce Developer Role
- Salesforce Admin vs Developer

---

## CRM Concepts
- Leads
- Accounts
- Contacts
- Opportunities
- Business Workflow
- Customer Lifecycle

---

## Data Modeling
- Apps
- Objects
- Tabs
- Fields
- Records
- Standard Objects
- Custom Objects
- Relationships
- Lookup Relationships
- Master-Detail Relationships
- Formula Fields
- Validation Rules

---

## Automation
- Salesforce Flow Builder
- Screen Flow
- Record-Triggered Flow
- Scheduled Flow
- Autolaunched Flow
- Workflow Automation
- No-Code Development

---

## Apex Programming
- Apex Basics
- Apex Classes
- Methods
- Constructors
- OOP Concepts
- Encapsulation
- Abstraction
- Inheritance
- Polymorphism
- Business Logic Development
- Exception Handling
- Collections

---

## Database & Querying
- SOQL
- SOSL
- Salesforce Query Language
- Data Retrieval
- Filtering Records
- Query Optimization

---

## Apex Triggers
- Before Triggers
- After Triggers
- Trigger Events
- Trigger Context Variables
- Event-Driven Systems
- Platform Events

---

## APIs & Integrations
- REST API
- SOAP API
- API Communication
- HTTP Callouts
- JSON Handling
- External Integrations
- Third-Party System Communication

---

## Lightning Web Components (LWC)
- Introduction to LWC
- Component-Based Architecture
- HTML Templates
- JavaScript Controllers
- Reactive Properties
- Event Handling
- Parent-Child Communication
- Data Binding
- UI Development

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
- Deployment Strategies
- Salesforce DX
- GitHub Integration
- Version Control

---

## Asynchronous Apex
- Future Methods
- Queueable Apex
- Batch Apex
- Scheduled Apex
- Background Processing

---

# Week 1 Learning Summary

# Day 1 – Salesforce CRM Basics

## Topics Covered
- Introduction to Salesforce
- CRM Basics
- Leads, Accounts, Contacts, Opportunities
- Salesforce Playground Setup

## Key Learnings
- Salesforce is a cloud-based CRM platform.
- CRM helps businesses manage customer relationships.
- Leads represent potential customers.
- Opportunities represent business deals.

## Business Workflow

```text
Lead → Contact → Opportunity → Customer
```

---

# Day 2 – Salesforce Platform Basics

## Topics Covered
- Apps
- Objects
- Tabs
- Multi-Tenant Architecture
- Configuration vs Coding

## Key Learnings
- Apps organize business functionalities.
- Objects store enterprise data.
- Salesforce supports both declarative and programmatic development.

---

# Day 3 – Data Modeling & Business Logic

## Topics Covered
- Objects
- Fields
- Records
- Relationships
- Formula Fields
- Validation Rules

## Key Learnings
- Relationships connect enterprise data.
- Validation Rules improve data quality.
- Formula Fields automate calculations.

---

# Day 4 – Salesforce Automation

## Topics Covered
- Flow Builder
- Workflow Automation
- Types of Flows

## Key Learnings
- Automation reduces manual work.
- Flows automate business processes without coding.

---

# Day 5 – Apex Programming Basics

## Topics Covered
- Introduction to Apex
- Business Logic
- Declarative vs Programmatic Development
- Flow vs Apex

## Key Learnings
- Apex handles complex business logic.
- Enterprise systems require programming.

### Example Pseudocode

```text
IF attendance < 75%
THEN notify student
```

---

# Day 6 – SOQL & Apex Triggers

## Topics Covered
- SOQL
- Apex Triggers
- Platform Events
- Event-Driven Systems

## Key Learnings
- SOQL retrieves Salesforce records.
- Triggers automate actions when records change.

### Example SOQL Query

```sql
SELECT Name
FROM Student__c
WHERE Attendance__c < 75
```

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

# Day 7 – Apex Testing & Salesforce DX

## Topics Covered
- Apex Testing
- Test Classes
- Test Coverage
- Salesforce DX
- Asynchronous Apex

## Key Learnings
- Testing improves deployment quality.
- Salesforce requires minimum 75% test coverage.
- Salesforce DX improves development workflow.

### Example Test Class

```apex
@isTest
private class StudentTest {

    @isTest
    static void testInsert() {

        Student__c stu = new Student__c(
            Name = 'Priya',
            Age__c = 20
        );

        insert stu;

        Student__c result = [
            SELECT Name
            FROM Student__c
            WHERE Name = 'Priya'
            LIMIT 1
        ];

        System.assertEquals('Priya', result.Name);

    }

}
```

---

# Week 2 Learning Summary

# Day 8 – Apex Classes & OOP Concepts

## Topics Covered
- Apex Classes
- Methods
- Constructors
- OOP Concepts
- Encapsulation
- Abstraction

## Key Learnings
- Apex follows object-oriented programming principles.
- Classes help organize business logic.

### Example Apex Class

```apex
public class StudentManager {

    public static String getMessage() {

        return 'Welcome Student';

    }

}
```

---

# Day 9 – Collections & Exception Handling

## Topics Covered
- Lists
- Sets
- Maps
- Exception Handling
- Try-Catch Blocks

## Key Learnings
- Collections help manage large datasets.
- Exception handling improves application stability.

### Example Collection

```apex
List<String> students = new List<String>();

students.add('Priya');
students.add('Rahul');
```

### Example Exception Handling

```apex
try {

    Integer result = 10 / 0;

} catch(Exception e) {

    System.debug('Error Occurred');

}
```

---

# Day 10 – APIs & Integrations

## Topics Covered
- REST API
- SOAP API
- HTTP Callouts
- JSON Parsing
- External Integrations

## Key Learnings
- APIs allow communication between systems.
- Salesforce integrates with external applications.

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

# Day 11 – Lightning Web Components (LWC)

## Topics Covered
- Introduction to LWC
- HTML Templates
- JavaScript Controllers
- Data Binding
- Event Handling

## Key Learnings
- LWC provides modern UI development.
- Components improve reusability.

### Example HTML File

```html
<template>

    <h1>Hello Salesforce</h1>

</template>
```

### Example JavaScript File

```javascript
import { LightningElement } from 'lwc';

export default class HelloWorld extends LightningElement {

}
```

---

# Day 12 – Advanced LWC & Component Communication

## Topics Covered
- Parent-Child Communication
- Reactive Properties
- Event Communication
- Component Reusability

## Key Learnings
- Components communicate using events and properties.
- Reusable UI improves scalability.

---

# Day 13 – Security & Access Management

## Topics Covered
- Profiles
- Roles
- Permission Sets
- Sharing Rules
- Field-Level Security

## Key Learnings
- Security controls user access.
- Salesforce protects enterprise data using role-based access.

---

# Day 14 – Deployment & Enterprise Workflow

## Topics Covered
- Deployment Process
- Sandbox Environment
- Change Sets
- GitHub Workflow
- Enterprise Architecture

## Key Learnings
- Deployment moves applications between environments.
- Version control improves collaboration.
- Enterprise workflows improve scalability.

---

# Real-World College Management System

## Objects Used
- Student
- Faculty
- Department
- Course
- Attendance
- Fees
- Examination

---

## Workflow Example

### Student Registration Workflow

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
- Salesforce Values: Quick Look
- Salesforce Developer: Quick Look
- Data Modeling
- Formulas and Validations
- Flow Builder Basics
- Automation Basics
- Apex Basics & Database
- Apex Testing
- Asynchronous Apex
- Salesforce DX Basics
- Search Solution Basics
- Platform Events Basics
- LWC Basics
- API Basics
- Security Basics

---

# Overall Learning

This Salesforce Summer Training Program helped me build a strong foundation in:

- CRM Concepts
- Salesforce Platform
- Data Modeling
- Automation
- Apex Programming
- SOQL & SOSL
- Apex Triggers
- APIs & Integrations
- Lightning Web Components
- Security & Access Management
- Testing Strategies
- Salesforce DX
- Enterprise Application Development

Through hands-on activities, Trailhead modules, mini-projects, and workflow implementations, I improved my understanding of how Salesforce developers and administrators build scalable, secure, and efficient enterprise business solutions.
