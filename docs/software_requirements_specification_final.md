# Overview

The purpose of this Software Requirements Specification (SRS) document is to provide a detailed description of the functional and non-functional requirements for the Project Time Tracker system. This document outlines the intended features and behaviors of the system in order to help reduce ambiguity and acheive project goals and objectives. 

# Functional Requirements

1. Creating Time Entries
   1. The system shall allow users to create one time entry per task
   2. The system shall provide the option for a user to manually enter a start time and an end time for each task in UTC
   3. The system shall provide an option to automatically record a time entry when a user selects a start recording option followed by a stop recording option

2. Creating and Managing Projects
   1. The system shall allow any user with a Project Manager designation to create a new project
   2. The system shall allow the designated Project Manager of a Project to add other users as Project Resources
   3. The system shall allow the designated Project Manager of a Project to add tasks to a project
   4. The system shall allow the designated Project Manager of a Project to assign tasks to users allocated to the Project as Resources
  
3. Managing Tasks
   1. The system shall allow a task's status to be updated by either the user assigned to the task or the Project Manager of the associated Project

# Non-Functional Requirements

1. Security
   1. The system shall ensure that only assigned project resources and the project creator can view a project's tasks

2. Performance
   1. The system shall provide the ability for a Project Manager to assign up to 10 project resources to a project without degraded performance
   2. The system shall display calculated recorded time after a user has performed the start and stop time recording sequence within 5 seconds
  
3. Maintainability
   1. The system shall provide the ability for a Project Manager or System Administrator to archive projects
