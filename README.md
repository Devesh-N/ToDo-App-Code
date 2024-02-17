# ToDo App Project Documentation

## Overview

This document outlines the architecture of the ToDo App, detailing the frontend and backend components, including services for user registration, task management, and additional utilities. Each component is linked to its respective repository for easy access.

## Frontend

- **Technology Stack:** HTML, Tailwind CSS, Vanilla JavaScript
- **Description:** The frontend interacts with the Rust ToDo service and Java user registration service. Requests are handled directly through JavaScript embedded within the HTML files.
- **Repository:** [Todo Frontend](https://github.com/Devesh-N/Todo-Frontend.git)

## Backend Services

### User Registration

- **Technology Stack:** Java Spring Boot
- **Description:** Handles user signup processes. It utilizes Spring Boot for the backend logic, sends the email ID to a Python API, which then forwards it to a Kafka topic.
- **Repository:** [SignUp Backend Java Spring Boot](https://github.com/Devesh-N/todo_register_java.git)

### Kafka API for Email Forwarding

- **Technology Stack:** Python Flask
- **Description:** Receives email addresses and sends them to a Kafka topic named `UserEmail`. It leverages MongoDB for data storage.
- **Repository:** [Java SignUp Backend Kafka API](https://github.com/Devesh-N/python_kafka_todo.git)

### Main ToDo App

- **Technology Stack:** Rust
- **Description:** The core backend service of the ToDo App, developed in Rust using Rocket.rs. It manages tasks and utilizes PostgreSQL as its database.
- **Repository:** [Main ToDo App Backend Rust](https://github.com/Devesh-N/rust-todo-app.git)

## Utility Services

### Proxy

- **Description:** A CORS proxy is essential for running the application due to the interconnected nature of all components. It should be run on port 9000 after modifying the `server.js` file.

### Go API Key Validation

- **Technology Stack:** Go
- **Description:** A new addition to the project, providing API key validation services.
- **Repository:** [Go API Key Validation Repo](https://github.com/Devesh-N/go-api-validation.git)

### Go Authentication Service

- **Technology Stack:** Go
- **Description:** Manages user Logins.
- **Repository:** [Go Authentication Service]([https://github.com/Devesh-N/go_todo_main)    

## Note

For the system to function correctly, ensure the proxy is running on port 9000, as all applications are interconnected and depend on this configuration.
