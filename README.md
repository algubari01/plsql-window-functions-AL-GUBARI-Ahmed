# PL/SQL Window Functions Assignment

## Course Information
- **Course**: Database Development with PL/SQL (INSY 8311)
- **Instructor**: Eric Maniraguha | eric.maniraguha@auca.ac.rw
- **Assignment Date**: September 19, 2025
- **Deadline**: September 29, 2025 (11:59 PM)

---

## Problem Definition

### Business Context
This project focuses on a retail company analyzing its sales data to gain insights into customer behavior, product performance, and revenue trends.

### Data Challenge
The company needs to:
1. Identify top-performing products and customers.
2. Analyze sales trends over time.
3. Segment customers based on their lifetime revenue.

### Expected Outcome
The analysis will provide actionable insights for marketing strategies, inventory planning, and customer engagement.

---

## Success Criteria

The following measurable goals were defined:
1. **Top 5 products per region/quarter** → Using `RANK()`.
2. **Running monthly sales totals** → Using `SUM() OVER()`.
3. **Month-over-month growth** → Using `LAG()`/`LEAD()`.
4. **Customer quartiles** → Using `NTILE(4)`.
5. **3-month moving averages** → Using `AVG() OVER()`.

---

## Database Schema

### Tables
1. **Customers**: Stores customer information.
   - **Key Columns**: `customer_id (PK)`, `cust_name`, `region`, `email`, `join_date`.
2. **Products**: Stores product catalog information.
   - **Key Columns**: `product_id (PK)`, `product_name`, `category`, `price`.
3. **Transactions**: Stores sales records.
   - **Key Columns**: `transaction_id (PK)`, `customer_id (FK)`, `product_id (FK)`, `sale_date`, `quantity`, `amount`, `promo_flag`.

### ER Diagram
*(### ER Diagram
[![ER Diagram](Screenshots/er_diagram.png)](Screenshots/er_diagram.png))*

---

## Window Functions Implementation

### 1. Ranking Functions
#### Query
See the SQL script: [Ranking Queries](SQL_Scripts/Ranking%20sql03_queries_ranking.sql.txt).

#### Screenshot
*(Attach the screenshot of the query result here, e.g., `Screenshots/ranking_query_result.png`)*

#### Interpretation
This query ranks customers by their total revenue within each region and quarter. The `ROW_NUMBER()` function ensures unique rankings for each customer.

---

### 2. Aggregate Functions
#### Query
See the SQL script: [Aggregate Queries](SQL_Scripts/Aggregate%20sql04_queries_aggregate.sql.txt).

#### Screenshot
*(Attach the screenshot of the query result here, e.g., `Screenshots/aggregate_query_result.png`)*

#### Interpretation
This query calculates the running total of monthly sales, providing insights into cumulative revenue trends over time.

---

### 3. Navigation Functions
#### Query
See the SQL script: [Navigation Queries](SQL_Scripts/Navigation%20sql05_queries_navigation.sql.txt).

#### Screenshot
*(Attach the screenshot of the query result here, e.g., `Screenshots/navigation_query_result.png`)*

#### Interpretation
This query calculates the month-over-month percentage change in sales, helping identify growth or decline trends.

---

### 4. Distribution Functions
#### Query
See the SQL script: [Distribution Queries](SQL_Scripts/Distribution%20sql06_queries_distribution.sql.txt).

#### Screenshot
*(Attach the screenshot of the query result here, e.g., `Screenshots/distribution_query_result.png`)*

#### Interpretation
This query segments customers into quartiles based on their lifetime revenue, enabling targeted marketing strategies.

---

## Results Analysis

### Descriptive Analysis
- **Patterns**: Customers in the top quartile contribute significantly to revenue.
- **Trends**: Sales show consistent growth over the months.

### Diagnostic Analysis
- **Causes**: High revenue concentration in specific regions and product categories.
- **Comparisons**: Quartile analysis reveals disparities in customer spending.

### Prescriptive Analysis
- **Recommendations**: Focus marketing efforts on high-value customers and underperforming regions.

---

## References

1. [MySQL Documentation](https://dev.mysql.com/doc/)
2. [Window Functions Tutorial](https://www.sqltutorial.org/sql-window-functions/)
3. *(Add more references as needed)*

---

## Integrity Statement

All sources were properly cited. Implementations and analysis represent original work. No AI-generated content was copied without attribution or adaptation.
