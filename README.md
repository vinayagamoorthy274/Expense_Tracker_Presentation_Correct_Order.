# Expense Tracker System

Console-based Java project using Java 17, Maven, Hibernate ORM, and MySQL.

## Features
- Add, view, search, update, and delete expenses
- Calculate total spending
- Summarize spending by category
- Filter expenses by month
- Store date, category, payment method, and notes

## Requirements
- JDK 17 or newer
- Maven (or Eclipse Maven support)
- MySQL Server

## Setup
1. In MySQL, run `CREATE DATABASE expense_tracker_db;`
2. Open `src/main/resources/hibernate.cfg.xml`.
3. Replace `YOUR_MYSQL_PASSWORD` with your MySQL password. Default username is `root`; change it if needed.
4. In Eclipse, choose **File → Import → Maven → Existing Maven Projects**, then select this folder.
5. Run `com.expensetracker.Main` as a Java Application, or run `mvn clean compile exec:java` in the project folder.

Hibernate creates/updates the table automatically once the database is available. This is an educational console application, not a banking/payment application.

## Structure
- `entity/Expense.java` — expense data model
- `repository/` — database operations
- `service/ExpenseService.java` — validation and application logic
- `util/HibernateUtil.java` — Hibernate SessionFactory
- `Main.java` — console menu
