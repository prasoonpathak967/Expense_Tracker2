💰 Expense Tracker – Spring Boot REST API
📌 Project Overview

The Expense Tracker is a backend RESTful web application developed using Spring Boot that allows users to manage their daily expenses efficiently. The application provides APIs to create, read, update, and delete expenses while storing data in a relational database.

This project demonstrates the implementation of Spring Boot architecture with REST APIs, JPA persistence, and layered architecture, making it suitable for learning Java Full Stack development and backend API design.

🚀 Features

Add a new expense

View all expenses

Get expense details by ID

Update existing expense

Delete an expense

RESTful API architecture

Layered architecture implementation

Database persistence using JPA

Cross-Origin support for frontend integration

🏗️ Project Architecture

The project follows the Spring Boot layered architecture pattern.

Controller Layer
        ↓
Service Layer
        ↓
Repository Layer
        ↓
Database
1️⃣ Controller Layer

Handles HTTP requests and responses.

File:

ExpenseController.java

Responsibilities:

Accept client requests

Call service methods

Return API responses

Example API Endpoint:

POST /api/expenses
GET /api/expenses
GET /api/expenses/{id}
PUT /api/expenses/{id}
DELETE /api/expenses/{id}
2️⃣ Service Layer

Contains business logic of the application.

Files:

ExpenseService.java
ExpenseServiceImpl.java

Responsibilities:

Process application logic

Validate and manipulate data

Interact with repository layer

Example Service Methods:

addExpense()
getAllExpenses()
getExpenseById()
updateExpense()
deleteExpense()
3️⃣ Repository Layer

Handles database operations using Spring Data JPA.

File:

ExpenseRepository.java

This interface extends:

JpaRepository<Expense, Long>

This provides built-in methods like:

save()

findAll()

findById()

deleteById()

without writing SQL queries.

4️⃣ Entity Layer

Represents the database table structure.

File:

Expense.java

Fields:

Field	Type	Description
id	Long	Primary key
title	String	Expense title
amount	double	Expense amount
category	String	Expense category
date	LocalDate	Expense date

Example:

@Entity
public class Expense {

    @Id
    @GeneratedValue(strategy = GenerationType.IDENTITY)
    private Long id;

    private String title;
    private double amount;
    private String category;
    private LocalDate date;
}
🛠️ Technology Stack
Backend

Java

Spring Boot

Spring Web

Spring Data JPA

Database

MySQL / H2 (configurable)

Tools & Libraries

Lombok – Reduces boilerplate code

Maven – Dependency management

REST APIs – Communication layer

📂 Project Structure
Expense_Tracker2
│
├── Controller
│   └── ExpenseController.java
│
├── Service
│   ├── ExpenseService.java
│   └── ExpenseServiceImpl.java
│
├── Repository
│   └── ExpenseRepository.java
│
├── Entity
│   └── Expense.java
│
└── ExpenseTracker2Application.java
⚙️ How to Run the Project
1️⃣ Clone the Repository
https://github.com/prasoonpathak967/Expense_Tracker2
2️⃣ Open Project

Open the project in:

IntelliJ IDEA

VS Code

Eclipse

3️⃣ Install Dependencies

If using Maven:

mvn clean install
4️⃣ Run the Application

Run the main class:

ExpenseTracker2Application.java

or using Maven:

mvn spring-boot:run
5️⃣ Server Starts

🔗 API Endpoints
Method	Endpoint	Description
POST	/api/expenses	Add expense
GET	/api/expenses	Get all expenses
GET	/api/expenses/{id}	Get expense by ID
PUT	/api/expenses/{id}	Update expense
DELETE	/api/expenses/{id}	Delete expense
📌 Example API Request
Add Expense

POST /api/expenses

{
  "title": "Food",
  "amount": 250,
  "category": "Daily",
  "date": "2026-03-12"
}
🎯 Project Purpose

The main goal of this project is to demonstrate:

Spring Boot REST API development

Layered architecture design

CRUD operations with JPA

Backend development for Java Full Stack applications

This project can be integrated with a React, Angular, or Vue frontend to build a complete Full Stack Expense Management System.

📈 Future Improvements

User authentication (JWT / Spring Security)

Expense filtering by category

Monthly expense reports

Dashboard analytics

Pagination and sorting

Frontend integration (React / Angular)

👨‍💻 Author

Prasoon Pathak
