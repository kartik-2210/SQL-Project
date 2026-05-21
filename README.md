# Online Bookstore Analysis - SQL (PostgreSQL)

## Project Overview

This project focuses on analyzing sales, inventory, and customer purchasing behavior for an online bookstore using PostgreSQL. The objective is to solve real-world business problems related to book sales, customer activity, revenue generation, and stock management while demonstrating strong SQL fundamentals and relational database concepts.

The project simulates a bookstore management system containing books, customers, and orders data. Using SQL queries, the analysis uncovers purchasing trends, top-performing books, customer ordering patterns, and inventory insights that can support business decision-making.

---

# Dataset Information

| Property     | Detail                                                   |
| ------------ | -------------------------------------------------------- |
| Database     | PostgreSQL                                               |
| Project Type | Relational Database & SQL Analysis                       |
| Tables       | 3 (Books, Customers, Orders)                             |
| Key Metrics  | Revenue, Book Sales, Customer Orders, Inventory Tracking |

---

# Database Structure

## Database Name

`OnlineBookstore`

---

## Tables Used

### 1. Books
- <a href="https://github.com/kartik-2210/SQL-Project/blob/main/Books.csv">Books Dataset View</a>

Stores all book-related information including pricing, genre, publication details, and stock availability.

| Column Name    | Data Type          |
| -------------- | ------------------ |
| Book_ID        | SERIAL PRIMARY KEY |
| Title          | VARCHAR(100)       |
| Author         | VARCHAR(100)       |
| Genre          | VARCHAR(50)        |
| Published_Year | INT                |
| Price          | NUMERIC(10,2)      |
| Stock          | INT                |

---

### 2. Customers
- <a href="[https://github.com/kartik-2210/SQL-Project/blob/main/Books.csv](https://github.com/kartik-2210/SQL-Project/blob/main/Customers.csv)">Customers Dataset View</a>

Contains customer information used for order tracking and customer analysis.

| Column Name | Data Type          |
| ----------- | ------------------ |
| Customer_ID | SERIAL PRIMARY KEY |
| Name        | VARCHAR(100)       |
| Email       | VARCHAR(100)       |
| Phone       | VARCHAR(15)        |
| City        | VARCHAR(50)        |
| Country     | VARCHAR(150)       |

---

### 3. Orders
- <a href="[https://github.com/kartik-2210/SQL-Project/blob/main/Books.csv](https://github.com/kartik-2210/SQL-Project/blob/main/Orders.csv)">Orders Dataset View</a>

Stores transactional order data and connects customers with books using foreign keys.

| Column Name  | Data Type          |
| ------------ | ------------------ |
| Order_ID     | SERIAL PRIMARY KEY |
| Customer_ID  | INT (Foreign Key)  |
| Book_ID      | INT (Foreign Key)  |
| Order_Date   | DATE               |
| Quantity     | INT                |
| Total_Amount | NUMERIC(10,2)      |

---

# Entity Relationship

* One customer can place multiple orders
* One book can appear in multiple orders
* Orders table acts as a bridge between Customers and Books
* Foreign keys maintain relational integrity across the database

---

# Business Problems Solved

* Which genres generate the highest sales?
* Which books are ordered most frequently?
* Who are the highest spending customers?
* Which customers placed multiple orders?
* What is the total revenue generated?
* Which books have the lowest remaining stock?
* Which authors sold the highest quantity of books?
* Which cities generate high-value orders?
* Which books are the most expensive within specific genres?
* How much stock remains after fulfilling all orders?

---

# Process Walkthrough

## 1. Database & Table Creation

Designed a structured relational database using PostgreSQL with proper primary and foreign key relationships between books, customers, and orders tables.

This established an efficient database model capable of handling bookstore transactions and inventory management.

---

## 2. Data Import & Management

Imported CSV datasets into PostgreSQL using the `COPY` command.

Datasets imported:

* Books.csv
* Customers.csv
* Orders.csv

This enabled efficient querying and large-scale data analysis.

---

## 3. Sales & Revenue Analysis

Performed revenue-focused analysis to calculate:

* Total revenue generated
* Genre-wise sales
* Quantity of books sold
* Author-wise sales contribution

SQL operations used:

* `SUM()`
* `GROUP BY`
* `ORDER BY`
* `JOIN`

---

## 4. Customer Behavior Analysis

Analyzed customer purchasing behavior by identifying:

* Customers with multiple orders
* Highest spending customers
* Customers placing high-value orders
* City-based customer spending trends

This helps understand customer engagement and buying patterns.

---

## 5. Inventory & Stock Analysis

Tracked inventory movement and stock consumption by comparing available stock with ordered quantities.

Calculated:

* Remaining stock after orders
* Lowest stock books
* Inventory pressure on high-demand books

This analysis supports inventory planning and restocking decisions.

---

## 6. Advanced Query Analysis

Implemented advanced SQL operations using:

* Multi-table `JOIN`
* Aggregate Functions
* `HAVING`
* `DISTINCT`
* Aliasing
* Conditional Filtering
* Sorting & Limiting

These queries simulate real-world reporting and business analysis scenarios.

---

# Key Findings

* Fiction and Fantasy genres generated strong sales activity
* A small group of customers contributed significantly to overall revenue
* Some books were repeatedly ordered, making them top-performing products
* Certain books experienced rapid stock depletion due to high demand
* Revenue generation varied significantly across customers and cities
* High-value customers frequently placed larger quantity orders
* Popular genres showed higher inventory pressure compared to others

---

# SQL Concepts Demonstrated

## Database Design

* CREATE DATABASE
* CREATE TABLE
* DROP TABLE

## Data Import

* COPY Command
* CSV Integration

## Querying & Filtering

* SELECT
* WHERE
* BETWEEN
* DISTINCT

## Aggregation & Analysis

* SUM()
* AVG()
* COUNT()
* GROUP BY
* HAVING()

## Joins & Relationships

* INNER JOIN
* LEFT JOIN
* Foreign Keys

## Data Organization

* ORDER BY
* LIMIT
* Aliasing

---

# Sample Analyses Performed

### Basic SQL Queries

* Retrieve books by genre
* Find books published after a certain year
* Retrieve customers from specific countries
* View orders within a date range
* Calculate total stock available
* Find the most expensive book
* Identify low stock books
* Calculate total revenue

---

### Advanced SQL Queries

* Total books sold per genre
* Average price analysis by genre
* Customers with multiple orders
* Most frequently ordered books
* Top expensive books within genres
* Author-wise sales tracking
* High-value customer analysis
* Remaining stock calculation after fulfilling orders

---

# Business Impact / What This Solves

## Sales Analysis

Identifies genres, books, and authors contributing the highest revenue.

## Customer Insights

Helps identify repeat and high-value customers for retention strategies.

## Inventory Optimization

Tracks stock depletion and supports efficient inventory management.

## Revenue Tracking

Provides visibility into overall business performance and customer spending patterns.

## Decision Support

Enables data-driven decision-making for pricing, promotions, and stock planning.

---

# Technologies Used

* PostgreSQL
* SQL
* CSV Data Import
* pgAdmin / PostgreSQL Terminal

---

# Conclusion

This project demonstrates the practical application of SQL in solving real-world business problems using relational databases. Through sales analysis, customer behavior tracking, and inventory management, the project showcases how structured SQL queries can transform raw transactional data into meaningful business insights.

The project highlights strong understanding of:

* Relational database design
* PostgreSQL fundamentals
* SQL-based business analysis
* Joins and aggregations
* Inventory and revenue analysis

Overall, this project reflects the ability to design, manage, and analyze a relational database system using PostgreSQL and SQL for business-oriented problem solving.

# Author

## Kartik Srivastava

📧 Email: kartiksrivastava275@gmail.com

🔗 LinkedIn:  
[LinkedIn Profile](https://www.linkedin.com/in/kartik-srivastava-4a7850292)
