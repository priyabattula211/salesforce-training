#  Salesforce Training – Week 1

## Introduction

This repository contains my learning progress, hands-on practice, notes, assignments, and mini-project activities completed during Week 1 of the Salesforce Summer Training Program.

During this week, I learned the fundamentals of Salesforce CRM, platform architecture, data modeling, automation, Apex programming, SOQL querying, Apex Triggers, and event-driven systems through Trailhead modules, practical activities, and real-world business examples.

The training helped me understand how enterprise applications are designed using both declarative tools and programmatic development in Salesforce.

---

# Day 1 – Salesforce CRM Basics

## Topics Covered
- Introduction to Salesforce
- What is CRM
- Salesforce Developer role
- Salesforce Playground setup
- Leads, Accounts, Contacts, and Opportunities

---

## Key Learnings
- Salesforce is a cloud-based CRM platform used by businesses to manage customer relationships.
- CRM helps organizations track customers, sales activities, and communication efficiently.
- Salesforce provides tools for automation, application development, reporting, and data management.
- Salesforce Developers build custom applications and business logic on the Salesforce Platform.

---

## CRM Concepts

### Lead
A Lead represents a potential customer or inquiry.

### Account
An Account represents a company or organization.

### Contact
A Contact represents a person associated with an account.

### Opportunity
An Opportunity represents a potential business deal or sales process.

---

## Business Workflow

Lead → Contact → Opportunity → Customer

This workflow helps businesses track customer interactions from the initial inquiry to becoming a customer.

---

## Real-World Mapping (College Admission System)

| Salesforce Object | Example |
|---|---|
| Lead | Student Inquiry |
| Account | College |
| Contact | Student |
| Opportunity | Admission Process |

---

## Trailhead Modules Completed
- Salesforce Values: Quick Look
- Salesforce Developer: Quick Look
- Salesforce CRM
- Trailhead Playground Management

---

# Day 2 – Salesforce Platform Basics

## Topics Covered
- Salesforce Platform Overview
- Apps, Objects, and Tabs
- Salesforce Architecture
- Multi-Tenant Architecture
- Configuration vs Coding
- Salesforce Admin vs Developer
- Platform Development Basics

---

## Key Learnings
- Salesforce Platform allows businesses to build and manage applications on the cloud.
- Apps are collections of related objects and features designed for specific business purposes.
- Objects are database tables used to store information.
- Tabs help users access objects and records easily.
- Salesforce supports both no-code configuration and coding-based development.

---

## What is an App?

An App in Salesforce is a collection of tabs, objects, and functionalities designed for a specific business purpose.

### Examples
- Sales App
- Service App
- College Management App

---

## What is an Object?

An Object is used to store data in Salesforce.

### Types of Objects

#### Standard Objects
- Account
- Contact
- Opportunity
- Lead

#### Custom Objects
- Student
- Faculty
- Attendance

---

## Multi-Tenant Architecture

Salesforce follows multi-tenant architecture where multiple organizations share the same infrastructure securely.

### Advantages
- Secure
- Scalable
- Cost efficient
- Automatic updates

---

## Configuration vs Coding

### Configuration
Uses clicks instead of code.

Examples:
- Validation Rules
- Flows
- Reports

### Coding
Used for advanced requirements.

Technologies:
- Apex
- APIs
- Lightning Web Components

---

## Trailhead Modules Completed
- Agentforce 360 Platform Basics
- Agentforce 360 Platform Development Basics

---

# Day 3 – Salesforce Data Modeling and Business Logic

## Topics Covered
- Objects, Fields, and Records
- Standard vs Custom Objects
- Relationships in Salesforce
- Lookup Relationships
- Formula Fields
- Validation Rules
- Data Modeling Basics

---

## Key Learnings
- Objects store business data.
- Fields store specific information.
- Records represent individual entries.
- Relationships connect business data.
- Formula Fields automate calculations.
- Validation Rules improve data quality.

---

## Relationships in Salesforce

### Lookup Relationship
Used when objects are related but not fully dependent.

Examples:
- Student → Department
- Course → Faculty

---

## Formula Fields

Formula Fields automatically calculate values.

### Examples
- Percentage
- Remaining Seats
- Full Name

---

## Validation Rules

Validation Rules prevent invalid data entry.

### Examples
- Age cannot be negative
- Email cannot be blank
- Seats cannot exceed capacity

---

## Trailhead Modules Completed
- Data Modeling
- Formulas and Validations

---

# Day 4 – Salesforce Automation and Flows

## Topics Covered
- Automation Basics
- Salesforce Flow Builder
- Types of Flows
- Workflow Automation
- No-Code Automation

---

## Key Learnings
- Automation reduces manual work.
- Flow Builder automates processes without coding.
- Different flows solve different business requirements.
- Automation improves productivity and efficiency.

---

## Types of Flows

### Screen Flow
Used for user interaction.

### Record-Triggered Flow
Runs automatically when records change.

### Scheduled Flow
Runs at scheduled times.

### Autolaunched Flow
Runs automatically in the background.

---

## Real-World Workflow Examples

### Student Admission Automation
- Record creation
- Confirmation email
- Admin notification

### Fee Reminder Automation
- Scheduled reminders
- Daily checks
- Automated reports

---

## Trailhead Modules Completed
- Flow Builder Basics
- Automation Basics

---

# Day 5 – Introduction to Apex and Business Logic

## Topics Covered
- Introduction to Apex
- Declarative vs Programmatic Development
- Flow vs Apex
- Business Logic Design
- Enterprise Automation

---

## Key Learnings
- Apex is Salesforce’s programming language.
- Apex handles advanced automation.
- Enterprise systems require programming logic.
- Flows are useful for simple automation.
- Apex is better for complex business logic.

---

## Real Examples Where Apex is Needed

### Complex Fee Calculation
Uses multiple conditions and calculations.

### Payment Gateway Integration
Requires APIs and external communication.

### Eligibility Checking System
Checks attendance, marks, and fee status together.

---

## Pseudocode Examples

```text
IF attendance < 75%
THEN notify student
```

```text
IF seats are full
THEN block registration
```

---

## Trailhead Modules Completed
- Apex & .NET Basics
- Apex Basics & Database

---

# Day 6 – SOQL, Apex Triggers, and Event-Driven Systems

## Topics Covered
- SOQL Basics
- Salesforce Query Language
- Apex Triggers
- Before vs After Trigger
- Flow vs Trigger
- Event-Driven Systems
- Platform Events
- Search Systems
- CLI Basics

---

## Key Learnings
- SOQL is used to retrieve Salesforce records.
- Apex Triggers automate actions when data changes.
- Before Triggers are used for validation.
- After Triggers are used for automation.
- Event-driven systems improve enterprise automation.
- Platform Events support real-time communication.
- CLI tools improve developer productivity.

---

## What is SOQL?

SOQL stands for Salesforce Object Query Language.

It is used to retrieve data from Salesforce objects.

### Example

```sql
SELECT Name FROM Student__c
```

```sql
SELECT Name
FROM Student__c
WHERE Attendance__c < 75
```

---

## What is an Apex Trigger?

An Apex Trigger is code that runs automatically when records are inserted, updated, or deleted.

Triggers help automate business processes.

---

## Trigger Events

| Trigger Event | Description |
|---|---|
| Before Insert | Runs before saving |
| After Insert | Runs after saving |
| Before Update | Runs before updating |
| After Update | Runs after updating |

---

## Before Trigger Example

```apex
trigger StudentBeforeTrigger on Student__c (before insert) {

    for(Student__c stu : Trigger.new) {

        if(stu.Age__c < 0) {

            stu.addError('Age cannot be negative');

        }

    }

}
```

---

## After Trigger Example

```apex
trigger StudentAfterTrigger on Student__c (after insert) {

    for(Student__c stu : Trigger.new) {

        System.debug('Welcome Email Sent');

    }

}
```

---

## Flow vs Trigger

| Flow | Trigger |
|---|---|
| No-code automation | Code-based automation |
| Easier to build | More flexible |
| Best for simple tasks | Best for advanced logic |

---

## Event-Driven Systems

Event-driven systems automatically react when events occur.

Examples:
- Notifications
- Record updates
- Approval processing
- Automated workflows

---

## Platform Events

Platform Events allow systems to communicate automatically in real time.

### Example
When a student completes payment:
- Finance records update
- Receipt gets generated
- Notification gets sent

---

## Search Systems

Search functionality helps users quickly retrieve records from enterprise systems.

### Importance
- Saves time
- Improves productivity
- Improves user experience

---

## CLI Basics

CLI stands for Command-Line Interface.

Developers use CLI tools to:
- Execute commands faster
- Automate development tasks
- Improve workflow efficiency

---

## Trailhead Modules Completed
- Search Solution Basics
- Agentforce 360 Platform Events Basics
- Command-Line Interface Basics

---

# Overall Understanding After Week 1

After completing Week 1, I understood:
- Salesforce CRM fundamentals
- Salesforce Platform structure
- Apps, Objects, Fields, and Records
- Relationships and Data Modeling
- Formula Fields and Validation Rules
- Automation using Flow Builder
- Declarative vs Programmatic Development
- Apex programming basics
- SOQL querying
- Apex Triggers
- Event-driven systems
- Platform Events
- CLI tools and developer workflow
- Real-world enterprise business automation

This week helped me build a strong foundation in Salesforce development and understand how enterprise systems use automation, business logic, and scalable architecture to manage business operations efficiently.
```
