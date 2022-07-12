# candidate-evaluation
An at home candidate evaluation for full stack engineers at Red Deer.

## Red Deer Candidate Evaluation
Your task is to create an application for managing a list of To Do items. There are two projects set up in this repository (see the [Overview of the Repository section](#overview-of-the-repository) for more information on these), a .Net API to handle requests and persist data and a React UI for a user to interact with the API.

Please document any assumptions, notes, or considerations that you make in the Assumptions.md file in the root of the repository. Please also document any libraries that you use to complete the task in this file, a note on why you chose some of the libraries over an alternative would be appreciated.

This task is only expected to take a few hours, but please commit regularly so we can see the approach you take to get to the end result.

This task should be completed in a public fork of this repository, and upon completion should be sent back to Phil at philippe.marti@reddeer.com

### Scope

A To Do Item should contain:
* Id
    * An identifier of the task
* Description
    * A short description of the task
* Is Complete
    * A flag that indicates the status of the task
* Created Date
    * The date that a task has been created
* Modified Date
    * The date in which the task has been modifided last

A user should be able to:
* see all of their To Do items
* add, edit, and remove their To Do items.
* flag a task as complete.
* remove the complete flag from the task.
* search for their To Do items, this should be done server side.
* sort their To Do items by Description or Created Date, this should be done on the front end.

Constraints:
* You do not need to consider multiple users for this task.
* You do not need to consider authorization or authentication for this task.
* Items that have been completed should be read only whilst the Is Completed flag is true.
* Items do not need to be persisted between sessions.
* The UI application should be styled, but this does not have to be anything extravagant. 
    * App layout and the use of spacing and colour are sufficient here. 
    * It would be prefered to demonstrate the use of Flex Box as a means of handling the layout, but this is not a requirement.
* Unit tests should be created for all public code, excluding Controllers.
    * You can use any any unit test framework that you like.

### Bonus Task
Persist your To Dos in a relational database of your choosing.

Constraints:
* For any infrastructure added, please use Docker containers using Docker Compose.
* You are free to use any ORM you like. 

## Overview of the Repository
This test comprises of two bootstrapped, but otherwise empty, that you must complete as part of your evaluation at Red Deer.

### Backend
There is a .Net 6 Web API project added to the `RedDeer.Todo` solution file, this contains configuration for CORS to allow communication between the UI project and an empty TODO controller.

Any new projects should be added to the `src/` folder of the repository.

### UI
There is a UI project bootstrapped using Create React App with the TypeScript template. You are welcome to use this as a starting point, but if you would prefer to use another framework, such as Angular, please feel free to do so.

This application can be started using `npm start` from the root of the `/ui` directory.
