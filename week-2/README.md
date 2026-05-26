#  Salesforce Summer Training Program – Week 2

### Advanced Salesforce Development using LWC, Apex, APIs, Security, Testing, Deployment, and Enterprise Application Design

</div>

---

#  Overview

This repository contains my complete learning progress, practical tasks, notes, mini-projects, and hands-on implementation completed during Week 2 of the Salesforce Summer Training Program.

During this week, I explored advanced Salesforce development concepts including Lightning Web Components (LWC), Apex Controllers, API Integrations, Salesforce Security, Testing, Deployment, Asynchronous Apex, and Enterprise Application Architecture.

This week helped me understand how enterprise Salesforce applications are designed using frontend development, backend business logic, integrations, automation, testing, and deployment workflows.

---

#  Topics Covered in Week 2

- Lightning Web Components (LWC)
- Component-Based Architecture
- Event Handling in LWC
- Parent to Child Communication
- Child to Parent Communication
- Conditional Rendering
- Iteration in LWC
- Apex Classes and Controllers
- Apex Methods and Variables
- REST API Basics
- HTTP Methods
- API Integrations
- JSON Handling
- Apex Callouts
- Salesforce Security Model
- Profiles and Permission Sets
- Authentication and Authorization
- Role Hierarchy
- Sharing Rules
- Apex Testing
- Test Classes
- Debugging
- Asynchronous Apex
- Future Methods
- Batch Apex
- Queueable Apex
- Scheduled Apex
- Salesforce DX
- Deployment Concepts
- Git and GitHub
- Enterprise Application Workflow
- End-to-End System Design

---

#  Day 8 – Lightning Web Components (LWC)

##  Topics Covered
- Introduction to LWC
- Component-Based Development
- HTML, CSS, and JavaScript in LWC
- Data Binding
- Reactive Properties
- LWC Folder Structure

---

##  Key Learnings
- LWC is Salesforce’s modern frontend framework.
- Components are reusable and modular.
- LWC improves application performance.
- Reactive properties automatically update the UI.

---

##  LWC Folder Structure

```text
helloWorld/
│── helloWorld.html
│── helloWorld.js
│── helloWorld.js-meta.xml
```

---

##  Basic LWC Example

### helloWorld.html

```html
<template>

    <lightning-card title="Welcome">

        <h1>Hello Salesforce</h1>

    </lightning-card>

</template>
```

---

### helloWorld.js

```javascript
import { LightningElement } from 'lwc';

export default class HelloWorld extends LightningElement {

}
```

---

### helloWorld.js-meta.xml

```xml
<?xml version="1.0" encoding="UTF-8"?>

<LightningComponentBundle xmlns="http://soap.sforce.com/2006/04/metadata">

    <apiVersion>59.0</apiVersion>

    <isExposed>true</isExposed>

    <targets>

        <target>lightning__AppPage</target>

        <target>lightning__HomePage</target>

    </targets>

</LightningComponentBundle>
```

---

#  Day 9 – Advanced LWC and Event Handling

##  Topics Covered
- Event Handling
- Parent to Child Communication
- Child to Parent Communication
- Public Properties
- Custom Events
- Conditional Rendering
- Iteration in LWC

---

##  Key Learnings
- Components communicate using properties and events.
- Custom events improve component interaction.
- Conditional rendering improves UI flexibility.
- Iteration helps display dynamic data.

---

##  Button Click Example

### HTML

```html
<template>

    <lightning-button
        label="Click Me"
        onclick={handleClick}>
    </lightning-button>

</template>
```

---

### JavaScript

```javascript
import { LightningElement } from 'lwc';

export default class EventExample extends LightningElement {

    handleClick() {

        alert('Button Clicked');

    }

}
```

---

#  Day 10 – Apex Classes and Controllers

##  Topics Covered
- Apex Classes
- Methods
- Variables
- Access Modifiers
- Controllers
- Static Methods
- Business Logic Design

---

##  Key Learnings
- Apex Classes store backend business logic.
- Methods help organize reusable functionality.
- Controllers connect frontend and backend systems.
- Apex improves enterprise application flexibility.

---

##  Apex Class Example

```apex
public class StudentController {

    public static String getMessage() {

        return 'Welcome to Salesforce';

    }

}
```

---

#  Day 11 – API Integrations and Callouts

##  Topics Covered
- REST API Basics
- API Integrations
- HTTP Methods
- Apex Callouts
- JSON Handling
- External System Communication

---

##  Key Learnings
- APIs connect Salesforce with external systems.
- REST APIs are widely used for integrations.
- JSON is used for data exchange.
- Apex Callouts retrieve external data.

---

##  HTTP Callout Example

```apex
public class ApiCalloutExample {

    public static void fetchData() {

        Http http = new Http();

        HttpRequest request = new HttpRequest();

        request.setEndpoint('https://api.example.com/data');

        request.setMethod('GET');

        HttpResponse response = http.send(request);

        System.debug(response.getBody());

    }

}
```

---

#  Day 12 – Salesforce Security and Access Control

##  Topics Covered
- Salesforce Security Model
- Profiles
- Permission Sets
- Authentication
- Authorization
- Role Hierarchy
- Sharing Rules

---

##  Key Learnings
- Salesforce security protects sensitive data.
- Profiles control user permissions.
- Permission Sets provide additional access.
- Role hierarchy controls record visibility.
- Sharing rules improve data accessibility.

---

##  Security Layers in Salesforce

| Security Feature | Purpose |
|---|---|
| Profiles | Object-level permissions |
| Permission Sets | Additional permissions |
| Role Hierarchy | Record access |
| Sharing Rules | Data sharing |

---

#  Day 13 – Apex Testing and Debugging

##  Topics Covered
- Apex Testing
- Test Classes
- Assertions
- Debug Logs
- Code Coverage
- Error Handling

---

##  Key Learnings
- Testing improves software quality.
- Salesforce requires minimum test coverage.
- Assertions validate expected behavior.
- Debug logs help identify issues.

---

##  Test Class Example

```apex
@isTest

private class StudentTestClass {

    @isTest

    static void testStudentCreation() {

        Student__c stu = new Student__c(

            Name = 'Priya',

            Age__c = 20

        );

        insert stu;

        System.assertEquals(

            'Priya',
            stu.Name

        );

    }

}
```

---

#  Day 14 – Asynchronous Apex and Deployment

##  Topics Covered
- Asynchronous Apex
- Future Methods
- Batch Apex
- Queueable Apex
- Scheduled Apex
- Salesforce DX
- Deployment Concepts
- Git and GitHub

---

##  Key Learnings
- Asynchronous Apex processes background tasks.
- Batch Apex handles large data processing.
- Queueable Apex improves asynchronous execution.
- Scheduled Apex automates recurring tasks.
- Salesforce DX improves development workflow.
- GitHub helps manage source code versions.

---

##  Future Method Example

```apex
public class AsyncExample {

    @future

    public static void sendNotification() {

        System.debug('Notification Sent');

    }

}
```

---

##  Batch Apex Example

```apex
global class StudentBatchClass implements Database.Batchable<sObject> {

    global Database.QueryLocator start(Database.BatchableContext bc) {

        return Database.getQueryLocator(

            'SELECT Id, Name FROM Student__c'

        );

    }

    global void execute(

        Database.BatchableContext bc,

        List<Student__c> records

    ) {

        for(Student__c stu : records) {

            stu.Status__c = 'Processed';

        }

        update records;

    }

    global void finish(Database.BatchableContext bc) {

        System.debug('Batch Completed');

    }

}
```

---

#  Enterprise Workflow Understanding

##  Complete System Workflow

### Student Admission Workflow

1. Student submits admission form
2. LWC form collects user data
3. Apex Controller processes records
4. Validation rules verify data
5. Student record gets created
6. Confirmation email gets triggered
7. Admin receives notification
8. Data gets stored securely
9. Reports and dashboards update automatically

---

#  Declarative vs Programmatic Development

| Declarative Development | Programmatic Development |
|---|---|
| Uses clicks instead of code | Uses programming logic |
| Easier to maintain | More flexible |
| Faster implementation | Suitable for advanced requirements |
| Used for simple automation | Used for enterprise-level logic |

---

#  Flow vs Apex

| Flow | Apex |
|---|---|
| No-code automation | Code-based development |
| Easier to build | Requires programming knowledge |
| Best for simple workflows | Best for advanced logic |
| Limited flexibility | Highly flexible |
| Faster for small automation | Better for enterprise systems |

---

# 🛠️ Tools Used

- Salesforce Trailhead
- Salesforce Developer Edition
- VS Code
- Salesforce CLI
- Git
- GitHub

---

# Trailhead Modules Completed

- Lightning Web Components Basics
- Lightning Web Components and Salesforce Data
- Apex Basics
- Apex Database
- Apex Integration Services
- API Basics
- Salesforce Security Basics
- User Authentication Basics
- Apex Testing
- Asynchronous Apex
- Salesforce DX Basics
- Deployment Basics

---

# Key Learnings from Week 2

- Learned frontend development using LWC.
- Understood reusable component architecture.
- Learned Apex backend development.
- Understood REST APIs and integrations.
- Learned JSON handling and HTTP callouts.
- Understood Salesforce security architecture.
- Learned profiles, permission sets, and sharing rules.
- Learned testing and debugging concepts.
- Understood asynchronous processing.
- Learned deployment workflow using Salesforce DX.
- Improved understanding of enterprise application development.

---

#  Overall Understanding After Week 2

After completing Week 2, I understood how enterprise Salesforce applications are designed using frontend technologies, backend business logic, integrations, security mechanisms, testing strategies, deployment workflows, and asynchronous processing.

I learned how Lightning Web Components improve UI development, how Apex handles backend business logic, how APIs connect Salesforce with external systems, how security protects enterprise data, and how testing and deployment ensure software quality and maintainability.

This week significantly improved my understanding of full-stack Salesforce development and enterprise application architecture.

```
