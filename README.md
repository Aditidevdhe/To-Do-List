# To-Do-List

# To-Do List Application

## Overview

The **To-Do List Application** is a console-based program that allows users to manage their daily tasks by adding, displaying, searching, deleting, and updating tasks. It provides a simple and efficient way to organize and track personal tasks, and stores the tasks in a text file, enabling persistence even after the application is closed. 

This project is an excellent example of file handling, basic CRUD operations (Create, Read, Update, Delete), and C++ programming concepts such as struct usage, loops, conditionals, and input/output handling.

---

## Features

- **Add Task**: Users can add new tasks to the to-do list with a task description.
- **Show Task**: Displays all saved tasks with their unique IDs.
- **Search Task**: Allows users to search for a task by its ID.
- **Delete Task**: Provides an option to delete a task by its ID.
- **Update Task**: Enables users to modify an existing task by updating its description.
- **Persistent Data**: Tasks are saved in a file called `todo.txt` so they persist between program runs.

---

## Project Structure

### `todolist` Struct

A **struct** is defined to represent each task:
- **id**: A unique integer identifier for the task.
- **task**: A string containing the description of the task.

### Key Functions

1. **`initializeID()`**: Initializes the global `ID` by counting the number of tasks in the `todo.txt` file. This ensures that the ID increments automatically with each new task.
2. **`addTask()`**: Allows users to add a new task. The task is saved in the `todo.txt` file with a unique ID.
3. **`showTask()`**: Displays all tasks in the to-do list, including their ID and description.
4. **`searchTask()`**: Searches for a task by its unique ID. If the task is found, it is displayed; otherwise, the user is informed that the task doesn't exist.
5. **`deleteTask()`**: Deletes a task by its ID. It creates a temporary file without the deleted task, then replaces the original file with the updated file.
6. **`updateTask()`**: Allows the user to update the description of an existing task based on its ID.
7. **`banner()`**: A helper function to display the program's title and heading at the top of each menu.

---

## How to Use

### 1. Clone the Repository

To use the **To-Do List Application**, start by cloning the repository to your local machine:

```bash
git clone https://github.com/your-username/todo-list-application.git
```

### 2. Compile and Run

Once you have cloned the repository, compile the program with a C++ compiler (e.g., `g++`):

```bash
g++ main.cpp -o todo_app
./todo_app
```

### 3. Use the Application

After running the program, you will be presented with a menu offering five options:
1. **Add Task**: Adds a new task to the to-do list.
2. **Show Task**: Displays all tasks stored in the `todo.txt` file.
3. **Search Task**: Allows you to search for a task using its ID.
4. **Delete Task**: Delete a task by providing its ID.
5. **Update Task**: Update the description of an existing task by its ID.

For example, to add a task, the program will prompt you to enter a task description. After you enter the description, it will ask if you'd like to save the task. Once saved, the task will be added to the file, and you can continue adding more tasks or return to the main menu.

---

## Code Walkthrough

1. **Task Structure**:
   The `todolist` struct holds the task details, including a unique ID and a description of the task. This struct is used to manage task information throughout the program.

2. **File Handling**:
   The program uses file I/O operations to persist the task data. Tasks are saved in the `todo.txt` file, and the program can read, update, and delete tasks based on the user's input.

3. **ID Management**:
   The global variable `ID` keeps track of the last used task ID. The `initializeID()` function ensures that the ID is set correctly when the program starts, and it is incremented as new tasks are added.

4. **Task Operations**:
   - **Add Task**: After collecting the task description from the user, the task is appended to the `todo.txt` file with a unique ID.
   - **Show Task**: The program reads the `todo.txt` file and displays each task along with its ID.
   - **Search Task**: The user is asked for a task ID, and the program searches the file for that ID. If found, the task details are displayed.
   - **Delete Task**: The task is searched for by ID and, if found, is deleted from the file by creating a new file excluding the task to be deleted.
   - **Update Task**: After searching for a task by ID, the user can update its description, and the file is rewritten with the updated task.

---

## Enhancements & Future Work

- **Input Validation**: Add checks to ensure valid input is provided for task IDs, especially during updates and deletions.
- **Multiple File Support**: Support for organizing tasks into categories or projects by saving them in separate files.
- **GUI Interface**: Implement a graphical user interface using a library like Qt or SFML for a more interactive experience.
- **Advanced Search**: Implement the ability to search tasks by keywords within the description.
- **Prioritize Tasks**: Add priority levels (e.g., High, Medium, Low) and allow sorting based on priority or due dates.

---
