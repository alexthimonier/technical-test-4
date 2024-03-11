# Technical test

## Introduction

Fabien just came back from a meeting with an incubator and told them we have a platform “up and running” to monitor people's activities and control the budget for their startups !

All others developers are busy and we need you to deliver the app for tomorrow.
Some bugs are left and we need you to fix those. Don't spend to much time on it.

We need you to follow these steps to understand the app and to fix the bug : 
 - Sign up to the app
 - Create at least 2 others users on people page ( not with signup ) 
 - Edit these profiles and add aditional information 
 - Create a project
 - Input some information about the project
 - Input some activities to track your work in the good project
  
Then, see what happens in the app and fix the bug you found doing that.

## Then
Time to be creative, and efficient. Do what you think would be the best for your product under a short period.

### The goal is to fix at least 3 bugs and implement 1 quick win feature than could help us sell the platform

## Setup api

- cd api
- Run `npm i`
- Run `npm run dev`

## Setup app

- cd app
- Run `npm i`
- Run `npm run dev`

## Finally

Send us the project and answer to those simple questions : 
- What bugs did you find ? How did you solve these and why ? 
- Which feature did you develop and why ? 
- Do you have any feedback about the code / architecture of the project and what was the difficulty you encountered while doing it ?

---

## Solution
### What bugs did you find ? How did you solve these and why ?
#### Bug 1
The first bug was the inability to view the project when a project is unnamed. 
The solution involved using the "Optional Chaining" operator and assigning a default name, "Unnamed project", if not named, rather than leaving the text empty.

#### Bug 2
The second bug was the inability to update a user. 
The solution was to switch from using the `onChange` event to the `onClick` event on the LoadingButton. 

#### Bug 3
The third bug was an endless loading screen when trying to edit a project. 
The solution was to adjust how the backend's date data was processed, ensuring access to a single object rather than an array of a single object. This adjustment does not affect the backend, preventing issues with other applications that might rely on this backend.

### Which feature did you develop and why ?
#### Managing Other People's Activities
The idea was to enable viewing and updating other users' activity times, which could be particularly useful for a supervisor. This feature allows any user to update anyone's activities, but ideally, future versions would include permission restrictions.

### Do you have any feedback about the code / architecture of the project and what was the difficulty you encountered while doing it ?
#### Business Level:
##### Pros
* The app is intuitive and easy to understand.
##### Cons
* The project has too many bugs (making it hard to limit fixes to just three)

#### Technical Level:
##### Pros 
* Up-to-date and functional README

##### Cons 
* Poor file decomposition with multiple components per file, affecting maintainability.
* Insufficient separation of business logic and views, complicating updates.
* No component library, leading to unnecessary redundancy.
* Technical debts like poorly named, unused, or commented fields.
* Inappropriate or underused Redux.
* No translation files, impacting internationalization.
* Improper use of packages (e.g., fs at version 0.0.1-security) posing security risks.
