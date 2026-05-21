# SQL Queries & Insights

---

# Q1: Retrieve all books in the Fiction genre

```sql id="s0a1q2"
SELECT *
FROM Books
WHERE Genre = 'Fiction';
```

### Insight

Filters and retrieves all books categorized under the Fiction genre.

---

# Q2: Find books published after 1950

```sql id="p4d7m8"
SELECT *
FROM Books
WHERE Published_Year > 1950;
```

### Insight

Identifies modern books published after 1950.

---

# Q3: List all customers from Canada

```sql id="x9k3l1"
SELECT *
FROM Customers
WHERE Country = 'Canada';
```

### Insight

Retrieves customer records belonging to Canada.

---

# Q4: Show orders placed in November 2023

```sql id="f2v6n0"
SELECT *
FROM Orders
WHERE Order_Date BETWEEN '2023-11-01' AND '2023-11-30';
```

### Insight

Filters orders placed within November 2023.

---

# Q5: Calculate total stock available

```sql id="r8w5b3"
SELECT SUM(Stock) AS Total_Stock
FROM Books;
```

### Insight

Calculates total inventory available across all books.

---

# Q6: Find the most expensive book

```sql id="u4t1c7"
SELECT *
FROM Books
ORDER BY Price DESC
LIMIT 1;
```

### Insight

Identifies the highest priced book in the bookstore.

---

# Q7: Show orders with quantity greater than 1

```sql id="n6y2h9"
SELECT *
FROM Orders
WHERE Quantity > 1;
```

### Insight

Retrieves orders where customers purchased multiple copies.

---

# Q8: Retrieve orders where total amount exceeds $20

```sql id="q3m8z5"
SELECT *
FROM Orders
WHERE Total_Amount > 20;
```

### Insight

Identifies high-value customer orders.

---

# Q9: List all unique genres available

```sql id="j7p4s1"
SELECT DISTINCT Genre
FROM Books;
```

### Insight

Displays all unique book genres available in the database.

---

# Q10: Find the book with the lowest stock

```sql id="e5x9k2"
SELECT *
FROM Books
ORDER BY Stock
LIMIT 1;
```

### Insight

Identifies books that may require restocking.

---

# Q11: Calculate total revenue generated

```sql id="v1n7d6"
SELECT SUM(Total_Amount) AS Total_Revenue
FROM Orders;
```

### Insight

Calculates total sales revenue generated from all orders.

---

# Q12: Retrieve total books sold for each genre

```sql id="c8r2m4"
SELECT b.Genre,
       SUM(o.Quantity) AS Total_Books_Sold
FROM Orders o
JOIN Books b
ON o.Book_ID = b.Book_ID
GROUP BY b.Genre;
```

### Insight

Analyzes sales performance across different genres.

---

# Q13: Find average price of Fantasy books

```sql id="t6q1w8"
SELECT AVG(Price) AS Average_Price
FROM Books
WHERE Genre = 'Fantasy';
```

### Insight

Calculates the average pricing within the Fantasy category.

---

# Q14: List customers with at least 2 orders

```sql id="h4z9u3"
SELECT o.Customer_ID,
       c.Name,
       COUNT(o.Order_ID) AS Order_Count
FROM Orders o
JOIN Customers c
ON o.Customer_ID = c.Customer_ID
GROUP BY o.Customer_ID, c.Name
HAVING COUNT(o.Order_ID) >= 2;
```

### Insight

Identifies repeat customers with multiple purchases.

---

# Q15: Find the most frequently ordered book

```sql id="m2x5f7"
SELECT o.Book_ID,
       b.Title,
       COUNT(o.Order_ID) AS Order_Count
FROM Orders o
JOIN Books b
ON o.Book_ID = b.Book_ID
GROUP BY o.Book_ID, b.Title
ORDER BY Order_Count DESC
LIMIT 1;
```

### Insight

Determines the most popular book based on order frequency.

---

# Q16: Show top 3 most expensive Fantasy books

```sql id="k7n1v4"
SELECT *
FROM Books
WHERE Genre = 'Fantasy'
ORDER BY Price DESC
LIMIT 3;
```

### Insight

Highlights premium books within the Fantasy genre.

---

# Q17: Retrieve total quantity sold by each author

```sql id="b5t8r0"
SELECT b.Author,
       SUM(o.Quantity) AS Total_Books_Sold
FROM Orders o
JOIN Books b
ON o.Book_ID = b.Book_ID
GROUP BY b.Author;
```

### Insight

Tracks author-wise sales contribution.

---

# Q18: List cities where customers spent over $30

```sql id="d9w3p6"
SELECT DISTINCT c.City,
       o.Total_Amount
FROM Orders o
JOIN Customers c
ON o.Customer_ID = c.Customer_ID
WHERE o.Total_Amount > 30;
```

### Insight

Identifies locations associated with high-value purchases.

---

# Q19: Find the customer who spent the most

```sql id="g1m6x8"
SELECT c.Customer_ID,
       c.Name,
       SUM(o.Total_Amount) AS Total_Spent
FROM Orders o
JOIN Customers c
ON o.Customer_ID = c.Customer_ID
GROUP BY c.Customer_ID, c.Name
ORDER BY Total_Spent DESC
LIMIT 1;
```

### Insight

Finds the highest spending customer in the bookstore.

---

# Q20: Calculate remaining stock after fulfilling all orders

```sql id="y4k7n2"
SELECT b.Book_ID,
       b.Title,
       b.Stock,
       COALESCE(SUM(o.Quantity), 0) AS Ordered_Quantity,
       b.Stock - COALESCE(SUM(o.Quantity), 0) AS Remaining_Stock
FROM Books b
LEFT JOIN Orders o
ON b.Book_ID = o.Book_ID
GROUP BY b.Book_ID, b.Title, b.Stock
ORDER BY b.Book_ID;
```

### Insight

Tracks inventory remaining after customer purchases.

---

# SQL Concepts Used

* SELECT Statements
* WHERE Clause
* Aggregate Functions
* GROUP BY & HAVING
* INNER JOIN & LEFT JOIN
* ORDER BY & LIMIT
* DISTINCT
* Aliasing
* Inventory Calculations
* Revenue Analysis

---

# Conclusion

This document demonstrates the SQL queries used to solve real-world business problems related to customer behavior, sales analysis, revenue tracking, and inventory management within the Online Bookstore database project.
