# Introduction
### Purpose
The purpose of this document is to serve as a guide to designers, developers and testers who are responsible for the engineering of the *Medication Reminder App*. It should give the engineers all of the information necessary to design, develop and test the software.

### Scope
This document contains a complete description of the functionality of the *Medication Reminder App*. It consists of use cases, functional requirements and nonfunctional requirements, which, taken together form a complete description of the software.

### System Overview
The *Medication Reminder App* is an application designed to send reminders to patients so they do not forget to take their medication on time. It serves as a platform for patients to manage their medications and caregivers to oversee how medications are being administered.

# Definitions
| Term | Definition |
| ---- | ---------- |
|Medication|The name of the medication|
|Dosage|How much and how often the medication is to be administered|
|Prescriber|The doctor who prescribed the medication|
|QTY|The quantity of the bottle of medication|
|Usage|Reason the medication is being taken|

# Use Cases
|Name|UC-1: Accounts|
|---|---|
|Summary|The user will have an account that holds all of their information.|
|Rationale|Every time a patient needs to access their medication information, they will access their account so different users' medications don’t get mixed together.|
|Users|All users|
|Preconditions|The user is ready to login.|
|Basic course of events|<ol> <li>The user enters their username</li> <li>The user enters their password</li></ol>|
|Alternative Paths|<ol><li>The user creates an account</li></ol>|
|Postconditions|The user's account is open.|

|Name|UC-2: Medications|
|---|---|
|Summary|The users will be able to change their medications by either adding, removing, or changing their medication.|
|Rationale|After a doctor visit, a user may need to modify their medication list because something has changed.|
|Users|All users|
|Preconditions|The user is in their medication list/account
Basic course of events|<ol><li>Click on the plus sign</li> <li>Enter the information of the new medication (name, dosage, prescriber, usage).</li> <li>Click add</li></ol>|
|Alternative Paths|<ol><li>Click on a medication</li> <li>Edit the information or delete it</li></ol> <ol><li>Click checkmark next to medication</li> <li>Medication is marked as taken</li></ol>|
|Postconditions|The medication list has been updated to the most recent medication usage.|

|Name|UC-3: Reminders|
|---|---|
|Summary|The users will get sent a reminder when it is time to take their medication. |
|Rationale|They need to be reminded to take their medication. If they are unable to take the medication at that time, they will be able to snooze the reminder to go off at a later time.|
|Users|All users|
|Preconditions|A notification has been sent to the user’s phone|
|Basic course of events|<ol><li>Click on notification</li> <li>Opens app to patient’s name and a list of medication/s to be taken</li> <li>Click the check mark</li></ol>|
|Alternative Paths|<ol><li>Click on the notification</li> <li>Opens app to a patient's name and a list of medication/s to be taken</li> <li>Click the snooze button</li> <li>Select how long you would like to snooze the reminder</li></ol>|
|Postconditions|The medication is marked as taken.|

# Functional Requirements
|Name|FR-1: Sign-up|
|---|---|
|Summary|The user will sign-up for a medication reminder account.|
|Rationale|The user will create a username and password to login to their account.|
|Requirements|The user will enter a unique username and create an eight character password.|
|References|UC-1|

|Name|FR-2: Login|
|---|---|
|Summary|The user will login to their medication reminder account.|
|Rationale|The user will enter their username and password to login to their account.|
|Requirements|The user will enter their correct username and corresponding password.|
|References|UC-1|

|Name|FR-3: Add Patient Portal|
|---|---|
|Summary|The user will add patients to their account.|
|Rationale|The user will add patients to their account to keep the people they care for and their medication separate so the wrong patient doesn’t take the wrong medication at the wrong time.|
|Requirements|The user will add a patient portal by giving the patient a name. <ul><li>Click the ‘+’ button on the account</li> <li>Enter the patient name</li> <li>Click ‘add’ button</li></ul>|
|References|UC-1|

|Name|FR-4: Remove Patient Portal|
|---|---|
|Summary|The user will remove patients from their account.|
|Rationale|The user will remove patients from their account when they are no longer caring for that patient.|
|Requirements|The user will delete a patient portal from their account. <ul><li>Click on the patient</li> <li>Click the ‘x’ button</li> <li>Click ‘confirm’ button</li><ul>|
|References|UC-1|

|Name|FR-5: Add Medication|
|---|---|
|Summary|The user will add a medication to a patient's medication list.|
|Rationale|The user will add a medication every time a doctor prescribes a new medication.|
|Requirements|The user will add a medication to a patient medication list. <ul><li>Start in the patient portal</li> <li>Click on the ‘+’ button</li> <li>Enter the medication information</li> <li>Click ‘add’ button</li></ul>|
|References|UC-2|

|Name|FR-6: Remove Medication|
|---|---|
|Summary|The user will remove a medication from a patient's medication list.|
|Rationale|The user will remove a medication every time a doctor instructs the patient to stop taking that medication.|
|Requirements|The user will remove a medication from a patient's medication list. <ul><li>Start in the patient portal</li> <li>Click on the medication</li> <li>Click the ‘x’ button</li> <li>Click ‘confirm’ button</li></ul>|
|References|UC-2|

|Name|FR-7: Edit Medication|
|---|---|
|Summary|The user will edit a medication from a patient's medication list.|
|Rationale|The user will edit a medication every time the doctor changes the dosage of the medication a patient is already taking.|
|Requirements|The user will edit a medication from a patient's medication list. <ul><li>Start in the patient portal </li> <li>Click on the medication</li> <li>Click ‘edit’ button</li> <li>Change the dosage of the medication</li> <li>Click ‘confirm’ button</li></ul>|
|References|UC-2|

|Name|FR-8: Approve Medication|
|---|---|
|Summary|The user will be able to confirm a medication was taken.|
|Rationale|The user will confirm that they took their medication everytime they take a medication to keep a record of their medication intake.|
|Requirements|The user gets a notification. <ul><li>Click on the notification</li> <li>The app will open to a page where you can confirm or snooze the medication reminder</li> <li>Click the “check mark” to state that you have taken the medication/s that are listed.</li></ul> If they are taking the medication before the notification has happened, they can also open the app. <ul><li>Click the check mark next to the medication/s that has been taken</li> <li>The medication/s will take note that the medication is taken</li> <li>The app will not notify the patient to take it</li></ul>|
|References|UC-2, UC-3|

|Name|FR-9: Send Reminder|
|---|---|
|Summary|The user is sent a reminder.|
|Rationale|The user is sent a notification to remind them to take their medication/s.|
|Requirements|A notification pops up on the user's phone.
|References|UC-3|

|Name|FR-10: Snooze Reminder|
|---|---|
|Summary|The user will be able to snooze a reminder.|
|Rationale|The user might be unable to take the medication at the time the reminder goes off. If this is the case, the user can snooze the reminder to go off again soon.|
|Requirements|The user gets a notification. <ul><li>Click on the notification</li> <li>The app will open to a page where you can confirm or snooze the medication reminder</li> <li>Click the “snooze” to state that you have not taken the medication/s</li> <li>A drop down with options for snooze time will happen</li> <li>Pick the snooze time</li><ul>|
|References|UC-3|
