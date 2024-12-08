# Overview

The purpose of this Software Requirements Specification (SRS) document is to provide a detailed description of the functional and non-functional requirements for the Project Time Tracker system. This document outlines the intended features and behaviors of the system in order to help reduce ambiguity and acheive project goals and objectives. 

# Functional Requirements

1. Creating Time Entries
   1. The system shall allow users to create one time entry per task
   2. The system shall provide the option for a user to manually enter a start time and a stop time for each task in UTC
   3. The system shall provide an option to automatically record a time entry when a user selects a start recording option followed by a stop recording option
   4. The system shall provide an automatic calculation of the time duration when a user completes the stop time recording action

2. Creating and Managing Projects
   1. The system shall allow any user to create a new project, update an existing project, or delete a project
   2. The system shall allow the Project to have one and only one Project Manager
   3. The system shall allow Resource users to be assigned to unlimited Projects
   4. The system shall allow users to create tasks and link them to a Project
   5. The system shall allow a Project to have an unlimited number of Project Resource users assigned to it
  
3. Managing Tasks
   1. The system shall allow a task's status to be updated
   2. The system shall allow a user to create, update, and delete tasks
   3. The system shall allow Time Recording entries to have one and only one Task associated
   4. The system shall allow Tasks to have unlimited associated Time Recording Entries
   5. The system shall automatically calculate the total duration of the task based on the sum of all related Time Recording durations
   6. The system shall allow a Task to have an Estimated Duration and an Actual Duration

# Non-Functional Requirements

1. Security
   1. The system shall ensure that only authenticated users with permission to the application can access the application
   2. The system shall ensure that only users designated as Co-Owners can make changes to the application
   3. The system shall ensure that only those within the same Microsoft Organization entity as the application can use the application

2. Performance
   1. The system shall provide the ability for a Project Manager to assign up to 10 project resources to a project without degraded performance
   2. The system shall display calculated recorded time after a user has performed the start and stop time recording sequence within 5 seconds
   3. The system shall update a Tasks Actual Duration time when a Duration is updated for a related Time Recording within 10 minutes
