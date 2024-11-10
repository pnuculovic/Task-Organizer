# Simple Task Organizer

**CSI2300 Course Project**

**Project Name**: Simple Task Organizer

**Team Name**: Logic Lab

**Member**: Peter Nuculovic


# Project Description

**Purpose**: The Simple Task Organizer is a desktop Java application that provides users with a means of organizing daily chores. Users can add, modify, and delete tasks and also mark them as done. Therefore, it's practical for personal organization and productivity.

**Why I Want to Build It**: With busy schedules and an increase in the number of responsibilities one has, being organized is key. This project will provide users with a light tool that provides the needed functionality to track activities without the overhead associated with larger task management applications. 

**Usage**: The application allows users to add tasks, check them off when completed, and delete tasks as needed. The data will be saved between sessions so users can continue where they left off.
```mermaid
classDiagram
    class Task {
        - String description
        - Date dueDate
        - boolean status
        + getDescription()
        + setDescription()
        + isCompleted()
        + setCompleted()
    }
    class TaskManager {
        - ArrayList~Task~ tasks
        + addTask(Task)
        + deleteTask(Task)
        + markTaskCompleted(Task)
    }
    class TaskOrganizerGUI {
        - JFrame frame
        - JList taskList
        + display()
        + updateTaskList()
        + addTaskButton()
        + deleteTaskButton()
    }

    TaskManager --> Task : manages >
    TaskOrganizerGUI --> TaskManager : uses >
    TaskOrganizerGUI --> Task : displays >
