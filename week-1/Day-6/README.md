# Day 6 – SOQL, Apex Triggers, and Event-Driven Systems

## Q1. What is SOQL?

SOQL stands for Salesforce Object Query Language.

It is used to retrieve records from Salesforce objects. SOQL is similar to SQL, but it is specially designed for Salesforce data and relationships.

Developers use SOQL to:
- Retrieve records
- Filter data
- Access related objects
- Process business information
- Build automation logic

---

## Q2. Write Example SOQL Queries

### Find all students

```sql
SELECT Name FROM Student__c
```

### Find students with attendance below 75%

```sql
SELECT Name, Attendance__c
FROM Student__c
WHERE Attendance__c < 75
```

### Find students with pending fees

```sql
SELECT Name
FROM Student__c
WHERE Fee_Status__c = 'Pending'
```

### Find courses with available seats

```sql
SELECT Name
FROM Course__c
WHERE Available_Seats__c > 0
```

---

## Q3. What is an Apex Trigger?

An Apex Trigger is code that runs automatically when records are inserted, updated, or deleted in Salesforce.

Triggers help systems react automatically to business events.

---

## Q4. Explain Trigger Events

| Trigger Event | Description |
|---|---|
| Before Insert | Runs before saving records |
| After Insert | Runs after records are saved |
| Before Update | Runs before updating records |
| After Update | Runs after updating records |
| Before Delete | Runs before deleting records |
| After Delete | Runs after deleting records |

---

## Q5. Write a Before Trigger Example

```apex
trigger StudentBeforeTrigger on Student__c (before insert) {

    for(Student__c stu : Trigger.new) {

        if(stu.Age__c < 0) {

            stu.addError('Age cannot be negative');

        }

    }

}
```

### Explanation

This trigger validates student age before saving the record.

If the age is negative, Salesforce prevents the record from being saved.

---

## Q6. Write an After Trigger Example

```apex
trigger StudentAfterTrigger on Student__c (after insert) {

    for(Student__c stu : Trigger.new) {

        System.debug('Welcome Email Sent To: ' + stu.Name);

    }

}
```

### Explanation

This trigger runs after a student record is created.

In real systems, this can:
- Send welcome emails
- Notify admins
- Create related records automatically

---

## Q7. Difference Between Before Trigger and After Trigger

| Before Trigger | After Trigger |
|---|---|
| Runs before saving | Runs after saving |
| Used for validation | Used for automation |
| Can modify values before save | Used for notifications |

---

## Q8. Difference Between Flow and Trigger

| Flow | Trigger |
|---|---|
| No-code automation | Code-based automation |
| Easier to build | More flexible |
| Best for simple automation | Best for complex logic |
| Faster development | Handles advanced business rules |

---

## Q9. When Should We Use Flow?

Flows are suitable for:
- Sending emails
- Updating fields
- Creating tasks
- Approval automation

---

## Q10. When Should We Use Trigger?

Triggers are suitable for:
- Complex calculations
- Multi-condition logic
- External integrations
- Advanced business automation

---

## Q11. Real-World Trigger Use Cases

### Student Registration
- Event: After Student Insert
- Action: Send welcome email automatically

### Attendance Warning
- Event: After Attendance Update
- Action: Notify students if attendance falls below 75%

### Fee Pending Alert
- Event: After Fee Status Update
- Action: Restrict hall ticket generation

### Scholarship Eligibility
- Event: After Marks Update
- Action: Assign scholarship automatically

### Course Capacity Full
- Event: After Course Seats Filled
- Action: Block new registrations

---

## Q12. What are Event-Driven Systems?

Event-driven systems automatically react when events occur.

Examples:
- Sending notifications
- Updating related records
- Triggering approvals
- Processing transactions

This reduces manual work and improves efficiency.

---

## Q13. Query Thinking

```text
Find all students enrolled in Course A
Find all students with pending fees
Find all students with attendance below 75%
Find all courses handled by Faculty X
Find courses with available seats
```

---

## Q14. Why Do Enterprise Systems Need Event-Driven Behavior?

Enterprise systems handle large amounts of data and users.

Event-driven behavior helps systems:
- React instantly to changes
- Reduce manual work
- Improve automation
- Support scalability
- Improve real-time processing

Without automation, organizations would struggle to manage business operations efficiently.

---

## Q15. Key Learnings

- SOQL is used to retrieve Salesforce data.
- Apex Triggers automate actions when data changes.
- Before Triggers are mainly used for validation.
- After Triggers are mainly used for automation.
- Flows are useful for simple automation.
- Triggers are useful for advanced business logic.
- Event-driven systems improve enterprise automation.

---

## Q16. Conclusion

From Day 6 learning, I understood how Salesforce retrieves data using SOQL and how Apex Triggers help enterprise systems react automatically to business events.

I also learned the importance of event-driven architecture and how automation improves efficiency, scalability, and business productivity.
