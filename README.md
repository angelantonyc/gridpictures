# gridpictures# TaskPlanner

A generation project


Aim:

Build a user-friendly website to schedule the tasks

Objectives:
Add  tasks with ease
Monitor progress by filtering the tasks
Advanced task tracker for teams of all sizes
Monitor progress with data-driven insights

The whole project was done using HTML5, CSS3, Bootstrap, JavaScript. 
Github used for collaboration.
The whole project was divided into 10 tasks. It was done in three sprints.

Initially, the project was designed using NinjaMock.

The bootstrap component selected was list-group.

HTML code is in index.html.
The CSS file is in styles.css
Totally, there are three JavaScript files. 
taskMangaerTable.js - class of taskManager dafined.
 index.js - all the event listeners in index.js
 api.js - The public holiday api code is in this file.

 > #### Tools
> - [HTML5](https://developer.mozilla.org/en-US/docs/Web/Guide/HTML/HTML5)
> - [Bootstrap](https://getbootstrap.com/)
> - [JavaScript](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference)


# Task 1: Design App Wireframes

Initially, the project was designed using NinjaMock. This really helps to get a clear idea about the design and looks of the website .

# Task 2: Implement wireframes using HTML5 and Bootstrap

All input fields are mapped in the Task Form (Name, Description, AssignedTo, DueDate, Status).

> #### Tools
> - [HTML5](https://developer.mozilla.org/en-US/docs/Web/Guide/HTML/HTML5)
> - [Bootstrap](https://getbootstrap.com/)

### Step 1: Create the page structure
 
In this step, we'll create a basic HTML structure and include [Bootstrap](https://getbootstrap.com/docs/4.5/getting-started/introduction/).
 
1. Created a new file called `index.html` inside the project folder.
2. Inside the project folder creatde a new folder called CSS and inside that created a new file called`styles.css`.
3. Included the `styles.css` file inside the `index.html` page.
 
### Step 2: Implemented Task Planner Wireframes
 
1. Add the selected components to the HTML page.
2. Implement Task planner form that contains the required fields:
* Name
* Description
* AssignedTo
* DueDate
* Status

# Task 3: Create a Task list layout and a Task List component

## Description

Implement the list layout bootstrap component that contains the task information:
* Name
* Description
* AssignedTo 
* DueDate
* Status

## Walkthrough

### Implementing the task list

In this step, we'll create a basic structure of a card with the task's information

1. Add a new sample [list](https://getbootstrap.com/docs/4.5/components/list-group/) to the `index.html`.
2. Add fields inside the list for task name, task description, assigned to, task due date, status.

# SPRINT 2

# Task 4: Task Form Inputs Validation

## Description

Implement a form that captures the fields required to create a task.

## Walkthrough

### Step 1: Add a task form

In this step, we'll add a form as a modal component to create a new task.

1. Add a new form inside the `index.html` page with all fields required to create a new task:
* Name
* Description
* AssignedTo 
* DueDate
* Status

2. Add a button to submit your form.

### Step 2: Implement a JavaScript function to validate your form fields

1. Create a `js` folder in the project 
2. Create a JavaScript file named `index.js` inside the `js` folder.
3. Add the `<script>` tag in `html` file to use the location of the `js/index.js` file.
4. Implement a JavaScript function named `validFormFieldInput(data)`
5. Add an ID attribute to each form field and implement the code needed to retrieve the each form field value

### Step 3: Showing errors to users

1. Add a [Bootstrap alert component](https://getbootstrap.com/docs/4.5/components/alerts/) inside the form to display the errors to the users.
2. Add the logic to display or hide the error message when the form is submited.
3. Display a meaningful error when a form filed is invalid and the user clicks the submit button.
4. Add the logic to hide the error message when the user clicks the submit button and the form data is valid.
    
# Task 5: Adding Tasks

## Description

For this task, creating a class to manage the tasks, adding a method to the class to keep track of tasks in our application, and connecting up the **New Task** form to create tasks.

## Walkthrough

### Step 1: The Setup

In this step, re-organise folder structure in preparation for the next few steps.

1.  Create a `taskManager.js` file in the `js` folder
2. Add a `<script>` tag pointing to the `js/taskManager.js` file _before_ the `<script>` tag pointing to the `js/index.js` file.

### Step 2: The TaskManager Class

In this step, create a `TaskManager` class that
will be responsible for managing the tasks in the application.

1. Create a `TaskManager` class in `js/taskManager.js`
2. Within the `constructor` of the `TaskManager` class, initialize a `this.tasks` property on the class equal to an empty array.

### Step 3: Adding A New Task Programmatically

In this step, add a method to the `TaskManager` class that will allow to add tasks to it's `tasks` property.

As part of this process, create a unique `id` for each task.

For each task for have a unique `id`, it need to keep track of what `id` the latest task was created with, so that it increment that `id` for the next task.


1. In the `TaskManager`'s `constructor`, accept a `currentId` parameter.
2. Assign the `currentId` to a new property on the class, `this.currentId`.
3. Create a method on the class, `addTask`. This method should accept all the nessecary information from the form to create a task as parameters.
    - `name`
    - `description`
    - `assignedTo`
    - `dueDate`
    - `status`
4. Within the `addTask` method, increment the `this.currentId`
5. `push` a new task into the `this.tasks` array, with the correct properties of the task, using the values passed in as parameters as well as the new `this.currentId`
    **Note** Make sure to include the `id` and a default `status` of `'TODO'`


### Step 4: Adding Tasks With The Form

In this final step, use the `TaskManager` class to keep track of tasks which added with the **New Task** form.

1. In `index.js`, add an event listener to the **New Task** form, listening to the `submit` event. 
2. When the `submit` event fires, if validation of the form is successful, use the values of each `input` in the form to call the `taskManager`'s `addTask` method.
    - **Note**: Make sure to prevent the default action of the form!
3. Clear the values from each form input, ready for the next submission.


# Task 6: Display The Tasks

## Description

For this task, write the code to display the `TaskManager`'s `tasks` array on the page.

## Walkthrough

### Step 1: Using Javascript to Create the Task HTML

> #### Useful Resources for this step
> - [Template literals (Template strings)](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Template_literals)

In this step, create a function using [template literals](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Template_literals) to return the HTML for each individual task.

1. In `js/taskManager.js`, above the `TaskManager` class definition, create a new function, `createTaskHtml`. The function should accept the following parameters:
    - `name`
    - `description`
    - `assignedTo`
    - `dueDate`
    - `status`

2. Within the `createTaskHtml` function, copying the HTML of a single task from the `index.html`

3. Using the template literal placeholders (`${}`), replace each section of the task HTML with the correct parameter

4. Return the HTML from the function


### Step 2: The render method


To display the tasks, create a new method on our `TaskManager` class called `render`.

1. In `js/taskManager.js`, within the `TaskManager` class, create a `render()` method. This method does not need any parameters.

2. Create a variable storing an empty array to hold the HTML of all the tasks' html, `tasksHtmlList`.

3. Loop over the `TaskManager`'s tasks, for each task:

    1. Store the current task in a variable
    
    2. Create a `taskHtml` variable to store the HTML of the current task, by calling the `createTaskHtml` function and using the properties of the current task.

    3. `push` the `taskHtml` into the `tasksHtmlList` array.

4. After looping through each task, create a `tasksHtml` variable, set the variable to a string of HTML of all the tasks by `join`ing the `tasksHtmlList` array together, separating each task's html with a newline.

5. Make sure the tasks list in `index.html` has an `id` so it can be selected.

6. Select the tasks list element and set its `innerHTML` to the `tasksHtml`.

### Step 3: Calling render

Now that the `TaskManager` class has a `render()` method, need to call it each time a new task is added, so that it is _rendered_ to the page!

After `addTask` is called, call the `TaskManager`'s `render` method.


# Task 7: Update A Task

## Description

For this task, write the code to update a task's status to "DONE" once a "Mark As Done" button on the task is clicked.

## Walkthrough

### Step 1: Adding the "Mark As Done" button

In this step, add a "Mark As Done" button to the tasks, so that a user can click the button to mark that specific task as done.

1. In `js/taskManager.js`, within the `createTaskHtml` function, add a button to the task html to mark the task as done.
2. Add a 'done-button' class to the "Mark As Done" button. use this later to check if the button has been clicked.

### Step 2: Adding an Event Listener to the Task List

In this step, add an Event Listener to our **Task List**, to check if one of our Task's buttons is clicked.

1. In `js/index.js`, at the bottom of the file, use `querySelector` to select the Task List id and store it in a variable.

2. Add an Event Listener to this, listening for the 'click' event. 

3. Using the `event.target`, using an `if` statement, check if the `target`'s `classList` contains the class we added to the button, `'done-button'`. If the `classList` contains `'done-button'`, "Mark As Done" button was clicked.

6. Use [DOM Traversal](https://developer.mozilla.org/en-US/docs/Learn/JavaScript/Client-side_web_APIs/Manipulating_documents#The_document_object_model), such as the `parentElement` property of the `target` ([Node.parentElement](https://developer.mozilla.org/en-US/docs/Web/API/Node/parentElement)) to _traverse_ the DOM and find the task's element.

7. Adding the Task id to the DOM

### Step 4: Adding getTaskById to the TaskManager class

Implement a `getTaskById` method on our `TaskManager` class to do just that. The `getTaskById` will compare a passed in `taskId` parameter to the ids of the `TaskManager` `tasks`. If it finds a matching task, it will return it from the method.


1. Add a new method, `getTaskById()`in the class, it should accept a `taskId` as a parameter.

2. In the `getTaskById()` method, create a `foundTask` variable to store the found task.

3. Loop over the `this.tasks` array, for each task in the loop:

    1. Store the current task in a variable called `task`

    2. Compare `task.id` to the passed in `taskId`, if its a match, store the `task` to the variable `foundTask`

4. After the loop, return the `foundTask` variable from the method.

### Step 5: Update the status of the selected Task to 'DONE'

1. After finding the `parentTask`, create a `taskId` variable, setting the value to the `taskId` `data-attribute` of the DOM element.

2. Using the `taskId` as it's parameter, call the `getTaskById()` method on the `taskManager`, storing the result in a `task` variable.

3. Change the `status` of the `task` to `'DONE'`.

4. Render the updated task by calling the `render()` method on the `taskManager`. 

### Step 6: Hiding the "Mark As Done" Button For Completed Tasks

In `js/taskManager.js`, in the HTML for each Task, add an `invisible` class to the "Mark As Done" button if the `status` parameter is `'TODO'`, and the `visible` class if it isn't.

### Step 7: Change the Styling of the Task Status.

For this, need to add specific badges to Task Status depending on the Status.

In `js/taskManager.js`, in the HTML for each Task, pass the color of the Task Status, depending on status.

> #### Useful Resources for this sprint
> - [Forms](https://getbootstrap.com/docs/4.5/components/forms/)
> - [Buttons](https://getbootstrap.com/docs/4.5/components/buttons/) 
> - [Modals](https://getbootstrap.com/docs/4.0/components/modal/)
> - [Query selector documentation](https://developer.mozilla.org/en-US/docs/Web/API/Document/querySelector)
> - [Bootstrap alert component](https://getbootstrap.com/docs/4.5/components/alerts/)
> - [Array.prototype.push()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/push)
> - [EventTarget.addEventListener()](https://developer.mozilla.org/en-US/docs/Web/API/EventTarget/addEventListener)
> - [Element.classList](https://developer.mozilla.org/en-US/docs/Web/API/Element/classList)
> - [DOM Traversal](https://developer.mozilla.org/en-US/docs/Learn/JavaScript/Client-side_web_APIs/Manipulating_documents#The_document_object_model)
> - [Node.parentElement](https://developer.mozilla.org/en-US/docs/Web/API/Node/parentElement)

# SPRINT 3

# Task 8: Persisting Tasks to LocalStorage

## Description

In this task, _persist_ tasks to LocalStorage, so that it can load the tasks again during the next visit of the webpage.

## Walkthrough

### Step 1: Adding the save method to TaskManager

In this step, add a `save()` method to TaskManager, that can call to save the current `this.tasks` to localStorage. Also need to save the `currentId` of the task, so that any new tasks after the application has loaded can continue off the `currentId`.

Because `localStorage` can only store strings, use [JSON.stringify()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/JSON/stringify), which can later on to convert back to an array using [JSON.parse()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/JSON/parse).

Also, since `currentId` is a number, need to convert that to a string too.

1. In `js/taskManager.js`, in the `TaskManager` class, create a `save` method.
2. In the `save` method, create a JSON string of the tasks using `JSON.stringify()` and store it to a new variable, `tasksJson`.
3. Store the JSON string in `localStorage` under the key `tasks` using `localStorage.setItem()`.
4. Convert the `this.currentId` to a string and store it in a new variable, `currentId`.
5. Store the `currentId` variable in `localStorage` under the key `currentId` using `localStorage.setItem()`.
4. In `js/index.js`, after both adding a new task and updating a task's status to done, call `taskManager.save()` to save the tasks to `localSorage`.

### Step 2: Adding the load method to TaskManager

Now saved the tasks to `localStorage`, need to load them back into `TaskManager`. 
For this, convert the array _stringified_ with `JSON.stringify()` back to an array, using `JSON.parse()`, before storing them back into the `TaskManager`'s `this.tasks`.

Also convert the `currentId` number that converted as a string, back to a number.

1. In `js/taskManager.js`, add a new method called `load`.
2. In the `load` method, check if any tasks are saved in localStorage with `localStorage.getItem()`.
3. If any tasks are stored, get the JSON string of tasks stored in `localStorage` with `localStorage.getItem()`. Store this string into a new variable, `tasksJson`.
4. Convert the `tasksJson` string to an array using `JSON.parse()` and store it in `this.tasks`.
5. Next, check if the `currentId` is saved in localStorage with `localStorage.getItem()`.
6. If the `currentId` is stored, get the `currentId` in localStorage using `localStorage.getItem()` and store it in a new variable, `currentId`.
7. Convert the currentId to a number before storing it to the `TaskManager`'s `this.currentId`
8. In `js/index.js`, near the top of the file, after _instantiating_ `taskManager`, `load` the tasks with `taskManager.load()` and render them with `taskManager.render()`.

# Task 9: Deleting Tasks

## Description

Need to delete old tasks so that they don't fill up the list over time.

## Walkthrough

### Step 1: Add A Delete Button to the Task HTML

In the the function `createTaskHtml`, add a `button` to delete the task, giving it a class `delete-button` that will use later to check if the button was clicked.

### Step 2: Create the deleteTask Method on TaskManager

Create a `deleteTask` method on our `TaskManager` class.

In this method, remove the task from the `this.tasks` array.

1. In `js/taskManager.js`, create a `deleteTask` method on the `TaskManager` class. It should take one parameter, `taskId`, the id of the task we want deleted.
2. In the `deleteTask` method, create an empty array and store it in a new variable, `newTasks`.
3. Loop over the tasks, in the loop
    - Get the current task in the loop, store it in a variable, `task`.
    - Check if `task.id` is **not** equal to the `taskId` passed as a parameter.
    - If the `task.id` is **not** equal to the `taskId`, push the `task` into the `newTasks` array.
4. Set `this.tasks` to `newTasks`.

### Step 3: Setting an EventListener to the Delete Button on Tasks

By using the `delete-button` class, check if the button is clicked. After the deleting the task, remember to `taskManager.save()` and `taskManager.render()` the tasks!

1. In `js/index.js`, find the `EventListener` for the `click` event on the list body.
2. At the bottom of the function, after our code that handles the "Mark As Done" button, create a new `if` statement to check if the `event.target.classList` `contains` the class `'delete-button'`.
3. If it does, get the `parentTask` and store it as a variable.
4. Get the `taskId` of the parent task from its `data-task-id` property.
5. Delete the task, passing the `taskId` to `taskManager.deleteTask()`
6. Save the tasks to `localStorage` using `taskManager.save()`
7. Render the tasks using `taskManager.render()`.

# Task 10: Test TaskManager

## Description

In the final task, test `TaskManager` class using Mocha.

## Walkthrough

### Step 1: Add Mocha to the project

> #### Useful Resources for this step
> - [Mocha - Getting Started](https://mochajs.org/#getting-started)

In this step, we'll add Mocha to our project.

1. Install Mocha as development dependency for your project:
    ```Javascript
      npm install --save-dev mocha
    ```
2. Create a new test directory and a test.js file to add your tests:
  - `mkdir test`
  - `$EDITOR test/test.js # or open with your favorite editor`


### Step 2: Testing TaskManager Methods

In this step, test some of the methods that exist on our `TaskManager` class.

1. Use testing to unit test the following methods on the `TaskManager` class:
  - `addTask`
  - `deleteTask`
  - `getTaskById`
2. Add a test case that tests how the `TaskManager` is initialized, ie: the `constructor` being called when a `new TaskManager()` is initialized.

>  Run the tests with `npm test`.

>  **Expected Result**
>  Should see the tests all pass, green! 


# EXTRA CHALLENGES


  > #### Useful Resources for this sprint
> - [Using the Web Storage API](https://developer.mozilla.org/en-US/docs/Web/API/Web_Storage_API/Using_the_Web_Storage_API)
> - [JSON.stringify()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/JSON/stringify)
> - [JSON.parse()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/JSON/parse)
> - [String](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String)
> - [Mocha - Getting Started](https://mochajs.org/#getting-started)
