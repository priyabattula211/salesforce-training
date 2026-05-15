<div align="center">

  <img 
    src="https://upload.wikimedia.org/wikipedia/commons/f/f9/Salesforce.com_logo.svg" 
    alt="Salesforce Banner"
    width="220"
  />

  <h1> Salesforce Project</h1>

  <p>
    Building cloud-based solutions using Salesforce CRM, Apex, Lightning,
    Automation, SOQL, Triggers, Testing, Salesforce DX, and AI-powered technologies.
  </p>

</div>

# Salesforce Summer Training Program

## Overview
This repository contains my learning progress, notes, assignments, hands-on practice, mini-project activities, and workflow implementations completed during the Salesforce Summer Training Program.

The training focuses on understanding Salesforce CRM concepts, platform architecture, business workflows, automation, Apex programming, SOQL querying, Apex Triggers, Testing, Salesforce DX, event-driven systems, and enterprise application development through Trailhead modules, practical tasks, and real-world business examples.

---

## Topics Covered
- Introduction to Salesforce
- Salesforce Platform Basics
- CRM Fundamentals
- Leads, Accounts, Contacts, and Opportunities
- Salesforce Playground Setup
- Apps, Objects, Tabs, Fields, and Records
- Standard vs Custom Objects
- Relationships in Salesforce
- Multi-Tenant Architecture
- Configuration vs Coding
- Salesforce Admin vs Developer
- Formula Fields and Validation Rules
- Data Modeling Basics
- Salesforce Automation
- Flow Builder
- Types of Flows
- Business Workflow Automation
- No-Code Automation
- Apex Programming Basics
- Declarative vs Programmatic Development
- Flow vs Apex
- Business Logic Design
- SOQL Basics
- Salesforce Query Language
- Apex Triggers
- Before vs After Triggers
- Event-Driven Systems
- Platform Events
- Search Systems
- CLI Basics
- Apex Testing
- Test Classes
- Test Coverage
- Asynchronous Apex
- Future Methods
- Queueable Apex
- Batch Apex
- Scheduled Apex
- Salesforce DX
- End-to-End Enterprise Workflow
- Enterprise System Architecture
- Basic System Design
- Business Workflow Understanding

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

## Platform Events

Platform Events allow systems to communicate automatically in real time.

### Example
When a student completes payment:
- Finance records update
- Receipt gets generated
- Notification gets sent

---

## Trailhead Modules Completed
- Search Solution Basics
- Agentforce 360 Platform Events Basics
- Command-Line Interface Basics

---

# Day 7 – Apex Testing, Asynchronous Apex, and Salesforce DX

## Topics Covered
- Apex Testing
- Test Classes
- Test Coverage
- Asynchronous Apex
- Future Methods
- Queueable Apex
- Batch Apex
- Scheduled Apex
- Salesforce DX
- Enterprise Workflow Design

---

## Key Learnings
- Testing ensures system reliability and bug-free deployment.
- Salesforce requires minimum test coverage for deployment.
- Asynchronous Apex improves scalability and performance.
- Future, Queueable, Batch, and Scheduled Apex handle background processing.
- Salesforce DX improves development workflow and collaboration.

---

## Why Testing Matters

Testing is important because it:
- Ensures business logic works correctly
- Reduces bugs and errors
- Improves deployment quality
- Maintains system stability
- Helps enterprise applications scale safely

Salesforce requires at least 75% test coverage for Apex deployment.

---

## Example Test Class

```apex
@isTest
private class StudentTriggerTest {

    @isTest
    static void testStudentInsert() {

        Student__c stu = new Student__c(
            Name = 'Priya',
            Age__c = 20
        );

        insert stu;

        Student__c result = [
            SELECT Name, Age__c
            FROM Student__c
            WHERE Name = 'Priya'
            LIMIT 1
        ];

        System.assertEquals(20, result.Age__c);

    }

}
```

---

## What is Asynchronous Apex?

Asynchronous Apex allows operations to run in the background instead of executing immediately.

### Advantages
- Better performance
- Faster processing
- Handles large data volumes
- Improves scalability

---

## Types of Asynchronous Apex

### Future Methods
Used for lightweight background processing.

### Queueable Apex
Used for advanced background jobs.

### Batch Apex
Processes large amounts of records in batches.

### Scheduled Apex
Runs jobs automatically at scheduled times.

---

## What is Salesforce DX?

Salesforce DX is a modern development environment used for Salesforce application development.

### Advantages
- Better collaboration
- Version control integration
- Faster deployments
- Improved development workflow
- Better project management

---

## Complete Enterprise Workflow

### Student Registration Workflow

#### Step 1 – Student Registration
- Student submits registration form
- Record gets created automatically

#### Step 2 – Validation
- System validates:
  - Age
  - Email
  - Required fields

#### Step 3 – Automation
- Confirmation email gets sent
- Admin receives notification

#### Step 4 – Attendance Tracking
- Attendance records update automatically

#### Step 5 – Fee Management
- Fee reminders get triggered

#### Step 6 – Eligibility Verification
System checks:
- Attendance percentage
- Pending fees
- Internal marks

#### Step 7 – Exam Registration
Eligible students can register for exams.

---

## Important Test Cases

### Test Case 1 – Negative Age Validation

Input:
- Age = -5

Expected Result:
- Record should not save

---

### Test Case 2 – Attendance Warning

Input:
- Attendance below 75%

Expected Result:
- Warning notification should trigger

---

### Test Case 3 – Fee Pending Validation

Input:
- Fee status = Pending

Expected Result:
- Exam registration should be blocked

---

### Test Case 4 – Successful Student Registration

Input:
- Valid student details

Expected Result:
- Record gets created successfully

---

## Reflection – Why Enterprise Software Needs Structured Workflows

Enterprise software systems handle large-scale business operations involving thousands of users, records, workflows, and transactions.

Without structured workflows:
- Data becomes inconsistent
- Automation becomes difficult
- Errors increase
- Scalability becomes challenging

Structured workflows help organizations:
- Maintain consistency
- Improve automation
- Reduce errors
- Improve scalability
- Support enterprise-level operations efficiently

---

## Trailhead Modules Completed
- Apex Testing
- Asynchronous Apex
- Salesforce DX Basics

---

# Tools Used
- Salesforce Trailhead
- Salesforce Developer Edition
- GitHub
- VS Code
- Salesforce CLI

---

# Overall Learning

This Salesforce Summer Training Program helped me build a strong foundation in:
- CRM concepts
- Salesforce Platform
- Data modeling
- Automation
- Apex programming
- SOQL querying
- Apex Triggers
- Event-driven systems
- Testing strategies
- Salesforce DX
- Enterprise application development

Through Trailhead practice, assignments, and mini-projects, I improved my understanding of how Salesforce developers and administrators work together to build scalable, secure, and efficient enterprise business solutions.
