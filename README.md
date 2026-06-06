<div align="center">

  <img
    src="https://upload.wikimedia.org/wikipedia/commons/f/f9/Salesforce.com_logo.svg"
    alt="Salesforce Logo"
    width="190"
  />

# Salesforce Summer Training Program

### A consolidated learning portfolio covering Salesforce CRM, automation, Apex, LWC, integrations, security, testing, deployment, and enterprise data practices.

![Salesforce](https://img.shields.io/badge/Salesforce-CRM-00A1E0?style=for-the-badge&logo=salesforce&logoColor=white)
![Apex](https://img.shields.io/badge/Apex-Development-1798C1?style=for-the-badge)
![LWC](https://img.shields.io/badge/LWC-Frontend-2E844A?style=for-the-badge)
![Trailhead](https://img.shields.io/badge/Trailhead-Learning-032D60?style=for-the-badge)

</div>

---

## Portfolio Overview

This repository documents my Salesforce Summer Training journey through daily notes, hands-on tasks, Trailhead progress, examples, screenshots, and enterprise-style mini-project thinking.

The training focuses on how real Salesforce applications are designed: starting from CRM fundamentals and data modeling, then moving into automation, Apex programming, Lightning Web Components, APIs, security, testing, deployment workflows, and data governance.

## Learning Roadmap

| Phase | Focus Area | Outcome |
|---|---|---|
| Foundation | CRM, cloud platform, objects, fields, records | Understand Salesforce as an enterprise CRM platform |
| Configuration | Apps, tabs, validation rules, formulas, flows | Build no-code business automation |
| Development | Apex, SOQL, SOSL, triggers, async Apex | Write backend logic for advanced requirements |
| Frontend | Lightning Web Components | Build reusable Salesforce UI components |
| Integration | REST APIs, JSON, HTTP callouts | Connect Salesforce with external systems |
| Security | Profiles, permission sets, sharing rules | Protect data with layered access control |
| Delivery | Testing, Salesforce DX, GitHub, deployment | Follow a structured development workflow |
| Governance | Data quality, migration, duplicate prevention | Think like an enterprise data owner |

---

## Repository Structure

```text
salesforce-training/
|-- README.md
|-- week-1/
|   |-- README.md
|   |-- day-1/
|   |-- Day-2/
|   |-- Day-3/
|   |-- Day-4/
|   |-- Day-5/
|   |-- Day-6/
|   `-- Day-7/
|-- week-2/
|   |-- README.md
|   |-- Day-1/
|   |-- Day-2/
|   |-- Day-3/
|   |-- Day-4/
|   |-- Day-5/
|   |-- Day-6/
|   `-- day-7/
|-- week-3/
|   |-- Day-1/
|   |-- Day-2/
|   |-- Day-3/
|   |-- Day-4/
|   |-- Day-5/
```

## Weekly Highlights

### Week 1: Salesforce Foundations

[Open Week 1 README](./week-1/README.md)

Week 1 built the base of Salesforce development. It covered CRM concepts, platform architecture, apps, objects, relationships, validation rules, formulas, Flow Builder, Apex basics, SOQL, triggers, testing, asynchronous Apex, Salesforce DX, and command-line workflows.

| Day | Main Focus |
|---|---|
| Day 1 | CRM basics, Leads, Accounts, Contacts, Opportunities |
| Day 2 | Salesforce platform, apps, objects, tabs, multi-tenant architecture |
| Day 3 | Data modeling, relationships, formulas, validation rules |
| Day 4 | Flow Builder and no-code automation |
| Day 5 | Apex basics and business logic |
| Day 6 | SOQL, Apex triggers, platform events, CLI basics |
| Day 7 | Apex testing, async Apex, Salesforce DX |

### Week 2: Full-Stack Salesforce Development

[Open Week 2 README](./week-2/README.md)

Week 2 expanded into frontend, backend, integration, security, testing, and deployment. The focus moved from understanding the platform to building complete enterprise-style Salesforce solutions.

| Day | Main Focus |
|---|---|
| Day 8 | Lightning Web Components basics |
| Day 9 | LWC events, parent-child communication, rendering |
| Day 10 | Apex classes, methods, controllers, backend logic |
| Day 11 | REST APIs, HTTP callouts, JSON handling |
| Day 12 | Security model, profiles, permission sets, sharing rules |
| Day 13 | Apex testing, debugging, assertions, code coverage |
| Day 14 | Async Apex, deployment, Salesforce DX, GitHub workflow |

### Week 3: Data Management and Governance

[Open Week 3 Day 1 README](./week-3/Day-1/README.md)

| Debugging | Debug logs, Apex Replay Debugger, Developer Console, troubleshooting |
| Enterprise Engineering | Performance optimization, monitoring, maintainability, reliability |
| AI & Agentforce | AI agents, Agentforce, prompt workflows, AI governance |
| Architecture | System design, workflow integration, scalability planning |
| Analytics | Reports, dashboards, management insights |
| Project Design | End-to-end application architecture, approval workflows, failure handling |

| Day | Main Focus |
|---|---|
| Day 15 | Data management, Data Loader, data quality, migration, governance |
| Day 16 | Debugging, Developer Console, Apex Replay Debugger, LWC best practices |
| Day 17 | Agentforce, AI agents, AI workflows, AI governance |
| Day 18 | Final Project Phase 1, architecture design, workflow integration |
| Day 19 | Final Project Phase 2, scalability, analytics, architecture refinement |
---

## Core Skills Practiced

| Category | Skills |
|---|---|
| CRM | Leads, Accounts, Contacts, Opportunities, customer lifecycle |
| Data Modeling | Standard objects, custom objects, fields, records, lookup relationships |
| Automation | Screen flows, record-triggered flows, scheduled flows, validation rules |
| Apex | Classes, methods, triggers, collections, exceptions, async processing |
| Querying | SOQL, SOSL, filtering, record retrieval |
| LWC | Templates, JavaScript controllers, events, reactive properties |
| Integration | REST concepts, HTTP methods, callouts, JSON |
| Security | Profiles, permission sets, roles, sharing rules, field-level security |
| Testing | Apex test classes, assertions, test coverage, debug logs |
| Deployment | Salesforce DX, CLI, Git, GitHub, sandbox workflow |
| Data Governance | Data quality, duplicate rules, migration planning, bulk import risks |

---

## Mini Project Theme: College Management System

The learning examples are connected through a practical College Management System scenario.

### Business Objects

| Salesforce Object | Real-World Example |
|---|---|
| Lead | Student inquiry |
| Account | College or institution |
| Contact | Student |
| Opportunity | Admission process |
| Custom Object | Student, Faculty, Department, Course, Attendance, Fees, Examination |

### Workflow

```text
Student Inquiry
    -> Registration
    -> Validation Rules
    -> Flow or Apex Automation
    -> Confirmation Notification
    -> Attendance Tracking
    -> Fee Management
    -> Eligibility Verification
    -> Exam Registration
```
### Enterprise Enhancements

The College Management System was progressively enhanced using enterprise-level Salesforce concepts:

- Validation Rules for student registration
- Approval workflows for admissions and fee requests
- Apex automation for business logic
- Lightning Web Components for user interfaces
- Reports and dashboards for management insights
- Scalability planning for high-volume usage
- AI-powered enhancements using Agentforce concepts
- Failure-handling and monitoring strategies

## Sample Concepts

### SOQL Query

```sql
SELECT Name, Attendance__c
FROM Student__c
WHERE Attendance__c < 75
```

### Apex Trigger

```apex
trigger StudentTrigger on Student__c (before insert) {
    for (Student__c student : Trigger.new) {
        if (student.Age__c < 0) {
            student.addError('Age cannot be negative');
        }
    }
}
```

### LWC Component

```html
<template>
    <lightning-card title="Student Portal">
        <p>Welcome to Salesforce Training</p>
    </lightning-card>
</template>
```

---

## Tools and Platforms

- Salesforce Trailhead
- Salesforce Developer Edition
- Salesforce Data Loader
- Visual Studio Code
- Salesforce CLI
- Git and GitHub

## Trailhead Learning Areas

- Salesforce CRM
- Platform Basics
- Data Modeling
- Formulas and Validations
- Flow Builder
- Apex Basics and Database
- Apex Triggers
- Apex Testing
- Asynchronous Apex
- Salesforce DX
- Platform Events
- API Basics
- Lightning Web Components
- Security Basics
- Data Management
- Data Quality
-  Apex Replay Debugger
- Developer Console
- Lightning Web Component Best Practices
- Agentforce Fundamentals
- AI Agents and Prompt Workflows
- Enterprise Debugging
- Solution Architecture
- Scalability and Performance
- Reporting and Dashboards
- Enterprise Application Design

---

## Key Takeaways

This training helped me understand how Salesforce supports complete enterprise application development. I practiced both declarative and programmatic approaches, learned how data moves through CRM workflows, built logic using Apex and Flow, explored LWC for UI development, studied integration patterns, and understood why testing, security, deployment, and data quality matter in real-world systems.

As the program progressed, I expanded into enterprise debugging, performance optimization, maintainable architecture, Agentforce, AI-powered workflows, scalability planning, analytics, reporting, and complete application design. The final project phases emphasized thinking like a Salesforce Developer and Solution Architect rather than focusing only on individual platform features.

The repository represents a growing Salesforce learning portfolio: part study journal, part hands-on lab, part enterprise application design practice, and part exploration of future AI-powered business systems.
