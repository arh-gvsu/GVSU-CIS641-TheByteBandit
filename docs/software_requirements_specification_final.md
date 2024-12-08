# Overview

The purpose of this Software Requirements Specification (SRS) document is to provide a detailed description of the functional and non-functional requirements for the Project Time Tracker system. This document outlines the intended features and behaviors of the system in order to help reduce ambiguity and acheive project goals and objectives. 

# Functional Requirements

1. Managing Time Entries
   1. The system shall allow users to create one time entry per task
   2. The system shall provide the option for a user to manually enter a start time and a stop time for each task in UTC
   3. The system shall provide an option to automatically record a time entry when a user selects a start recording option followed by a stop recording option
   4. The system shall provide an automatic calculation of the time duration when a user completes the stop time recording action
   5. The system shall prevent a Time Recording from having a stop time if it does not have a Start Time

2. Creating and Managing Projects
   1. The system shall allow any user to create a new project, update an existing project, or delete a project
   2. The system shall allow the Project to have one and only one Project Manager
   3. The system shall allow Resource users to be assigned to unlimited Projects
   4. The system shall allow users to create tasks and link them to a Project
   5. The system shall allow a Project to have an unlimited number of Project Resource users assigned to it
   6. The system shall allow Projects to be added, updated, or deleted from the Projects screen
  
3. Managing Tasks
   1. The system shall allow a task's status to be updated
   2. The system shall allow a user to create, update, and delete tasks from the Tasks screen
   3. The system shall allow Time Recording entries to have one and only one Task associated
   4. The system shall allow Tasks to have unlimited associated Time Recording Entries
   5. The system shall automatically calculate the total duration of the task based on the sum of all related Time Recording durations
   6. The system shall allow a Task to have an Estimated Duration and an Actual Duration

4. Managing Users
   1. The system shall allow a user record to be created, edited, or deleted from the Users screen
   2. The system shall allow a user to have a designation as either a Project Management User or a Project Resource User
   3. The system shall only permit a user with a Project Manager designation to be listed as a Project Manager on a Project
   4. The system shall allow a user to be linked to a Project in the Project Resource Assignments screen
  
5. Navigation
   1. The system shall allow a user to navigate to the Project Manager Dashboard from any of its child screens
   2. The system shall allow a user to choose either the Project Manager Dashboard or the Time Recording Portal when authenticated
   3. The system shall allow a user to return to the Home Page from the Project Manager Dashboard or the Time Recording Portal
   4. The system shall provide both an edit and a save button for records in each of the primary screens

# Non-Functional Requirements

1. Security
   1. The system shall ensure that only authenticated users with permission to the application can access the application
   2. The system shall ensure that only users designated as Co-Owners can make changes to the application
   3. The system shall ensure that only those within the same Microsoft Organization entity as the application can use the application
   4. The system shall log all access attempts, successful or failed, for auditing purposes
   5. The system shall encrypt all stored sensitive data, including user credentials and time entry data, using AES-256 encryption.
   6. The system shall leverage Microsoft's authentication and single sign-on
   7. The system shall only be available for users who are entered in Microsoft Entra as internal or external users to the Organization
   8. The system shall allow administrators to configure access controls based on user roles
   9. The system shall protect against common web vulnerabilities such as SQL injection, cross-site scripting (XSS), and cross-site request forgery (CSRF)

2. Performance
   1. The system shall provide the ability for a Project Manager to assign up to 10 project resources to a project without degraded performance
   2. The system shall display calculated recorded time after a user has performed the start and stop time recording sequence within 5 seconds
   3. The system shall update a Tasks Actual Duration time when a Duration is updated for a related Time Recording within 10 minutes
   4. The system shall maintain response times of under 2 seconds for navigation between screens under standard load conditions
   5. The system shall handle up to 10 concurrent users without significant performance degradation
   6. The system shall load the Project Manager Dashboard with all assigned projects within 3 seconds.
  
3. Maintainability
   1. The system shall retain a version history every time the application is saved
   2. The system shall provide comprehensive logging for errors, warnings, and critical events to facilitate troubleshooting
   3. The system shall follow a modular architecture to simplify updates or changes to individual components
  
4. Scalability
   1. The system shall allow the creation of up to 10 projects without requiring architectural changes
   2. The system shall support integration with all Microsoft Power Platform services
   3. The system shall accommodate future expansion to support additional roles, such as auditors or external stakeholders
   4. The system shall allow increasing the maximum number of project resource assignments per project from 10 to 50 without impacting performance.
