# POE_Part3
 

# Task & Security Chatbot

## Overview

The **Task & Security Chatbot** is a desktop application built using **C#**, **WPF**, and **SQL Server**. It combines a simple task management system with basic cybersecurity awareness. Users can chat with the bot using normal language to create, view, complete, and delete tasks while also learning about common cybersecurity topics.

The goal of this project is to demonstrate how a chatbot can understand user requests, manage data in a database, and provide useful information through a conversational interface.

---

## Features

### Task Management

The chatbot allows users to manage their tasks through simple chat commands.

Users can:

* Add new tasks
* Add descriptions and reminders
* View all saved tasks
* Mark tasks as completed
* Delete tasks

If the user only provides the task title, the chatbot will continue the conversation by asking for the description and reminder before saving the task.

### Cybersecurity Assistant

The chatbot can answer questions about common cybersecurity topics such as:

* Phishing
* Password security
* Malware
* VPNs
* Two-Factor Authentication (2FA)

These responses are stored in a dictionary and matched against the user's message.

### Quiz

Users can also start a simple cybersecurity quiz by typing words like:

* quiz
* question
* test

The chatbot then displays a multiple-choice question.

### Chat Interface

The application uses a modern chat-style interface where:

* User messages appear on the right in blue chat bubbles.
* Bot responses appear on the left in grey chat bubbles.
* The conversation automatically scrolls to the newest message.

---

## Technologies Used

* C#
* Windows Presentation Foundation (WPF)
* SQL Server LocalDB
* ADO.NET
* Regular Expressions (Regex)

---

## Database

The application connects to a SQL Server LocalDB database named:

```
TaskChat
```

The project stores tasks inside a table called:

```
Task
```

Example columns:

* Id
* Title
* Description
* Reminder
* IsCompleted

---

## How the Chatbot Works

When the user sends a message, the chatbot checks what the user wants to do.

It looks for keywords to determine whether the user wants to:

* create a task
* view tasks
* complete a task
* delete a task
* ask a cybersecurity question
* start the quiz

If the chatbot cannot understand the request, it displays a helpful message showing the available commands.

---

## Example Commands

### Create a task

```
add task Buy groceries
```

The chatbot will then ask for:

* Description
* Reminder

or the user can provide everything in one message.

Example:

```
add task Buy groceries
description Buy milk and bread
reminder Tomorrow at 9 AM
```

---

### Show tasks

```
show tasks
```

or

```
display tasks
```

---

### Complete a task

```
done 2
```

---

### Delete a task

```
delete 3
```

---

### Ask security questions

```
What is phishing?
```

```
Tell me about VPNs
```

```
What is malware?
```

---

### Start the quiz

```
quiz
```

---

## Error Handling

The application includes error handling for database operations.

Examples include:

* Database connection failures
* Invalid task numbers
* Missing task information
* SQL errors

If an error occurs, the chatbot informs the user instead of crashing.

---

## Project Structure

```
MainWindow.xaml
MainWindow.xaml.cs
WindowGame.xaml
WindowGame.xaml.cs
Models/
Database/
```

The **MainWindow** contains most of the chatbot logic including:

* Chat interface
* Message processing
* Database operations
* Security responses
* Task management

---

## Future Improvements

Some features that could be added in future versions include:

* More cybersecurity questions and answers
* Multiple quiz questions with scoring
* Reminder notifications
* Natural Language Processing (NLP)
* Voice input
* User login system
* Task categories and priorities
* Search and filter tasks

---
#Here The Video Presention

* https://youtu.be/LenQefXxCh8

## Conclusion

This project demonstrates how a chatbot can combine task management with cybersecurity education in a simple desktop application. It uses conversational interactions instead of traditional menus, making the application easier and more engaging for users while demonstrating database integration, regular expressions, and WPF user interface development.
