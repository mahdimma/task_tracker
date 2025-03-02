# Task Tracker CLI

Task Tracker is a simple command line interface (CLI) application to help you track and manage your tasks. It allows you to add, update, delete, and list tasks—all stored in a JSON file for persistence.

## Overview

The Task Tracker CLI enables you to:
- **Add tasks:** Create a new task with a unique ID, description, and default status (`todo`).
- **Update tasks:** Modify the description of an existing task.
- **Delete tasks:** Remove tasks that are no longer needed.
- **Change status:** Mark tasks as _in-progress_ or _done_.
- **List tasks:** Display all tasks or filter by status (`todo`, `in-progress`, `done`).


## Features

- **Task Management:** Add, update, and delete tasks.
- **Status Tracking:** Easily mark tasks as `todo`, `in-progress`, or `done`.
- **Filtering:** List all tasks or view tasks by status.
- **Persistent Storage:** Tasks are saved in a JSON file located in your current directory.
- **Error Handling:** Graceful management of edge cases and invalid user input.

## Requirements

- A terminal or command prompt environment
- No external libraries or frameworks are required (uses only native filesystem modules)

## Getting Started

### 1. Set Up Your Environment

- **Clone this repository:**  
  ```sh
  git clone https://github.com/mahdimma/task_tracker.git
  cd task_tracker
  ```

### 2. Installation

Since this project uses only native modules, no additional dependencies are required. simply run the script from the terminal.

### 3. Running the Application

The CLI accepts commands as positional arguments. Below are some example commands:

- **Add a new task:**
  ```sh
  task-cli add "Buy groceries"
  # Output: Task added successfully (ID: 1)
  ```

- **Update a task:**
  ```sh
  task-cli update 1 "Buy groceries and cook dinner"
  # Output: Task #1 updated successfully!
  ```

- **Delete a task:**
  ```sh
  task-cli delete 1
  # Output: Task #1 deleted successfully!
  ```

- **Mark a task as in-progress or done:**
  ```sh
  task-cli mark-in-progress 1
  task-cli mark-done 1
  ```

- **List all tasks:**
  ```sh
  task-cli list
  ```

- **List tasks by status:**
  ```sh
  task-cli list done
  task-cli list todo
  task-cli list in-progress
  ```

## Task Data Structure

Each task is stored with the following properties:
- **id:** Unique identifier for the task.
- **description:** A short description of what needs to be done.
- **status:** Current status of the task (`todo`, `in-progress`, or `done`).
- **createdAt:** Timestamp for when the task was created.
- **updatedAt:** Timestamp for when the task was last updated.

## Contributing

Contributions are welcome! If you have ideas for improvements or bug fixes, please:
1. Fork the repository.
2. Create a new branch:  
   ```sh
   git checkout -b feature/your-feature-name
   ```
3. Commit your changes and push the branch:  
   ```sh
   git push origin feature/your-feature-name
   ```
4. Open a pull request detailing your changes.

## License

This project is open source and available under the [MIT License](LICENSE).

---
