# Task 6: Sales Trend Analysis Using SQL Aggregations

##  Objective
Analyze monthly and yearly sales trends using SQL by creating a database, inserting sample store transaction data, and applying aggregation functions to calculate total sales, average transaction value, and revenue by category.

##  Tools Used
- SQL (MySQL / SQLite)
- Aggregate Functions: `SUM()`, `COUNT()`, `AVG()`
- Time Functions: `YEAR()`, `MONTH()`
- String Functions: `CONCAT()`, `LPAD()`
- Clauses: `GROUP BY`, `ORDER BY`, `LIMIT`

##  Project Workflow

### 1. Database Creation
- Created a new database named **store_sales_data**.

### 2. Table Creation
- Created a table called **sales_transactions** with columns:
  - `transaction_id` (Primary Key)
  - `sale_date` (Date of transaction)
  - `quantity` (Number of units sold)
  - `unit_price` (Price per unit)
  - `category` (Product category)

### 3. Data Insertion
- Inserted 15 realistic transactions from 2022 and 2023 across multiple product categories.

### 4. Sales Trend Analysis
Executed the following SQL queries:
- Monthly Revenue Calculation
- Yearly Revenue by Category
- Top 3 Months by Revenue
- Average Transaction Value by Month

## Key Queries Explained

- **Monthly Revenue**:  
  Used `SUM(quantity * unit_price)` grouped by year and month.

- **Yearly Category Revenue**:  
  Aggregated by both year and product category.

- **Top 3 Revenue Months**:  
  Formatted month as `YYYY-MM` using `CONCAT()` and `LPAD()`, ordered by revenue.

- **Average Transaction Value**:  
  Used `AVG(quantity * unit_price)` grouped by month.

##  Files Included

- `task6_sales_friend_full.sql` — Full SQL script (DB, table, data, queries)
- `README.md` — This documentation

##  Key Learnings
- Created and populated a new transactional sales database from scratch
- Used arithmetic operations (`quantity * unit_price`) to calculate real-world sales value
- Grouped and analyzed sales by time and category
- Performed date formatting without `TO_CHAR()` (MySQL-compatible)
