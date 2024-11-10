# Simple Task Organizer

**CSI2300 Course Project**

**Project Name**: Simple Task Organizer

**Team Name**: Logic Lab

**Member**: Peter Nuculovic


# Project Description

**Purpose**: The Simple Task Organizer is a desktop Java application that provides users with a means of organizing daily chores. Users can add, modify, and delete tasks and also mark them as done. Therefore, it's practical for personal organization and productivity.

**Why I Want to Build It**: With busy schedules and an increase in the number of responsibilities one has, being organized is key. This project will provide users with a light tool that provides the needed functionality to track activities without the overhead associated with larger task management applications. 

**Usage**: The application allows users to add tasks, check them off when completed, and delete tasks as needed. The data will be saved between sessions so users can continue where they left off.

# Plan and Estimate of Effort
In order to progressively add the necessary functionality and improve the program, I want to work on this project whenever I have free time. By adhering to the course objectives and making sure that every part functions properly, I hope to make the Simple Task Organizer as useful and easy to use as possible.

I'll concentrate on:

Putting in place essential functions such task addition, editing, and deletion.
constructing a straightforward, user-friendly GUI to efficiently handle jobs.
To guarantee dependability, the program is going to be constantly tested and debugged.
improving the usability of the application in light of user input and my personal observations.
Although the schedule is negotiable, I strive to finish every component with care and excellence.
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
