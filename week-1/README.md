# 🚀 Salesforce Training – Week 1 

## Day 1 – Salesforce CRM Basics

### Topics Covered
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

Apps help users organize their work efficiently.

---

## What is an Object?

An Object is used to store data in Salesforce.

### Types of Objects

#### Standard Objects
Objects already provided by Salesforce.

Examples:
- Account
- Contact
- Opportunity
- Lead

#### Custom Objects
Objects created according to business requirements.

Examples:
- Student
- Faculty
- Attendance

---

## What is a Tab?

A Tab is a user interface element used to access objects and records quickly.

### Examples
- Accounts Tab
- Contacts Tab
- Opportunities Tab

Tabs improve navigation and user experience.

---

## Multi-Tenant Architecture

Salesforce follows multi-tenant architecture, where multiple organizations share the same infrastructure securely.

### Advantages
- Secure
- Cost efficient
- Automatic updates
- Scalable

---

## Configuration vs Coding

### Configuration
Configuration means building functionality using clicks instead of code.

#### Examples
- Validation Rules
- Flows
- Reports
- Dashboards

### Coding
Coding is used for advanced business requirements.

#### Technologies Used
- Apex
- Lightning Web Components
- APIs

#### Examples
- Payment Gateway Integration
- Complex Automation Logic

---

## Salesforce Admin vs Developer

### Salesforce Admin
- Works with configuration tools
- Manages users, reports, dashboards, and automation

### Salesforce Developer
- Writes code using Apex and Lightning Web Components
- Builds custom applications and integrations

---

## Real-Time System Design

### App Name
College Management App

### Objects
- Student
- Faculty
- Course
- Attendance
- Fees
- Examination

### User Interaction

#### Admin
Manages student records, fees, and reports.

#### Faculty
Updates attendance and marks.

#### Students
View attendance, marks, and course details.

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
- Structured Enterprise Data

---

## Key Learnings
- Objects are used to store business data in Salesforce.
- Fields store specific pieces of information inside objects.
- Records represent individual entries inside an object.
- Relationships connect related data between objects.
- Formula Fields automate calculations without coding.
- Validation Rules prevent invalid data entry and improve data quality.
- Structured data is important for enterprise systems and business automation.

---

## Objects, Fields, and Records

### Object
An Object is similar to a database table used to store information.

Examples:
- Student
- Faculty
- Course
- Department

---

### Field
A Field stores a specific piece of information.

Examples:
- Student Name
- Email
- Age
- Course Name

---

### Record
A Record is a single entry inside an object.

Example:

| Student Name | Age | Department |
|---|---|---|
| Priya | 19 | IT |

---

## Standard vs Custom Objects

### Standard Objects
Objects already provided by Salesforce.

Examples:
- Account
- Contact
- Opportunity
- Lead

### Custom Objects
Objects created according to business requirements.

Examples:
- Student
- Faculty
- Attendance
- Department

---

## Relationships in Salesforce

Relationships help connect related data between objects.

### Relationship Examples
- One Department can contain many Students
- One Department can contain many Faculty members
- One Faculty can teach multiple Courses

### Lookup Relationship
Lookup Relationships are used when objects are related but not fully dependent on each other.

Examples:
- Student → Department
- Course → Faculty

---

## Formula Fields

Formula Fields automatically calculate values without manual work.

### Examples
- Full Name
- Percentage
- Remaining Seats

### Advantages
- Reduces manual calculations
- Improves accuracy
- Saves time

---

## Validation Rules

Validation Rules prevent incorrect or invalid data from entering the system.

### Examples
- Email cannot be empty
- Student age cannot be negative
- Filled seats cannot exceed total seats

### Advantages
- Improves data quality
- Prevents business errors
- Maintains consistency

---

## Reflection – Why Structured Data Matters

Structured enterprise data is important because it helps organizations:
- Organize information properly
- Maintain relationships between data
- Reduce duplication
- Improve reporting
- Support automation
- Allow multiple users to work efficiently

Compared to spreadsheets, enterprise systems like Salesforce provide better scalability, security, and automation.

---

## Trailhead Modules Completed
- Data Modeling
- Formulas and Validations

---

# Day 4 – Salesforce Automation and Flows

## Topics Covered
- Introduction to Automation
- Salesforce Flow Builder
- Types of Flows
- No-Code Automation
- Manual vs Automated Systems
- Workflow Automation
- Business Process Automation

---

## Key Learnings
- Automation helps businesses reduce repetitive manual work.
- Salesforce Flow Builder is used to automate business processes without coding.
- Different types of flows are used for different business requirements.
- Automation improves productivity, accuracy, and efficiency.
- No-code automation allows businesses to build workflows quickly.

---

## What is Automation?

Automation means performing tasks automatically without continuous human effort.

Businesses use automation to:
- Save time
- Reduce manual work
- Improve productivity
- Reduce human errors
- Improve business efficiency

---

## What is a Flow?

A Flow is a no-code automation tool in Salesforce used to automate workflows and business processes.

Using Flow Builder, businesses can:
- Create records
- Update records
- Send notifications
- Automate approvals
- Collect user input

Flows use drag-and-drop components instead of coding.

---

## Types of Flows

### Screen Flow
Used when user interaction is required.

#### Example
Student Registration Form

---

### Record-Triggered Flow
Runs automatically when records are created or updated.

#### Example
Automatically sending a confirmation email when a student record is created.

---

### Scheduled Flow
Runs automatically at scheduled times.

#### Example
Sending daily fee reminder emails.

---

### Autolaunched Flow
Runs automatically in the background without user interaction.

#### Example
Automatically updating attendance percentage.

---

## Manual System vs Automated System

| Manual System | Automated System |
|---|---|
| Requires human effort | Tasks run automatically |
| Slower process | Faster process |
| More chances of errors | Improved accuracy |
| Difficult to scale | Easily scalable |

---

## Real-World Workflow Examples

### Student Admission Automation
- Student submits admission form
- Student record gets created automatically
- Confirmation email is sent
- Admin receives notification

### Fee Reminder Automation
- System checks pending fees daily
- Reminder emails are sent automatically
- Reports are generated for admin

### Course Registration Automation
- Student enters details using a form
- Flow validates data
- Registration records are created automatically

---

## Advantages of No-Code Automation
- Faster development
- Easy maintenance
- Reduces manual work
- Improves productivity
- Less coding required
- Better process management

---

## Trailhead Modules Completed
- Flow Builder Basics
- Automation Basics

---

# Overall Understanding After Day 1, Day 2, Day 3 & Day 4

After completing Day 1, Day 2, Day 3, and Day 4, I understood:
- Basics of Salesforce CRM
- CRM workflow and customer management
- Salesforce Platform structure
- Apps, Objects, Tabs, Fields, and Records
- Standard vs Custom Objects
- Relationships in Salesforce
- Difference between configuration and coding
- Formula Fields and Validation Rules
- Importance of structured enterprise data
- Salesforce automation and Flow Builder
- Different types of Flows
- No-code workflow automation
- Role of Salesforce Admin and Developer
- How Salesforce helps businesses automate processes and manage data efficiently
