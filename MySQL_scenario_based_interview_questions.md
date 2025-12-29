# 🧠 Scenario-Based SQL Interview Questions (MySQL)

A curated collection of **scenario-based SQL interview questions**.    
Perfect for **technical interviews, SQL revision, backend & data engineering prep**.   

---

## 🎯 Who Is This For?

- ✅ Beginners to Advanced SQL Developers  
- ✅ Technical Interviews & Coding Tests  
- ✅ SQL Revision & Practice  
- ✅ Backend / Data Engineering Prep  

---

## 📌 Table of Contents

1. Duplicate Records  
2. Second Highest Salary  
3. Employees Without Department  
4. Revenue Per Product  
5. Top Paid Employees  
6. Customers Without Returns  
7. Orders Per Customer  
8. Employees Joined in 2023  
9. Average Order Value  
10. Latest Order Per Customer  
11. Unsold Products  
12. Most Selling Product  
13. Revenue & Orders Per Region  
14. Customers With More Than 5 Orders  
15. Orders Above Average Value  
16. Employees Hired on Weekends  
17. Salary Range Filter  
18. Monthly Revenue & Orders  
19. Salary Ranking by Department  
20. Customers Ordering Every Month  
21. Moving Average of Sales  
22. First & Last Order Date  
23. Revenue Distribution %  
24. Consecutive Purchases  
25. Churned Customers  
26. Cumulative Revenue  
27. Top Performing Departments  
28. Above-Average Customers  
29. Revenue From New Customers  
30. Department Employee %  
31. Salary Difference per Department  
32. Pareto (80/20) Products  
33. Latest Order with Amount  
34. Avg Time Between Purchases  
35. Year-over-Year Growth  
36. 90th Percentile Orders  
37. Longest Gap Between Orders  
38. Bottom 10% Revenue Customers

---

## 1️⃣ Find Duplicate Records (Amazon)
```sql
SELECT column1, column2, COUNT(*) AS duplicate_count
FROM your_table
GROUP BY column1, column2
HAVING COUNT(*) > 1;
```

---

## 2️⃣ Second Highest Salary (Microsoft)
```sql
SELECT MAX(salary) AS SecondHighestSalary
FROM Employee
WHERE salary < (SELECT MAX(salary) FROM Employee);
```

---

## 3️⃣ Employees Without a Department (Uber)
```sql
SELECT e.*
FROM Employee e
LEFT JOIN Department d ON e.department_id = d.department_id
WHERE d.department_id IS NULL;
```

---

## 4️⃣ Total Revenue Per Product (PayPal)
```sql
SELECT product_id, SUM(quantity * price) AS total_revenue
FROM Sales
GROUP BY product_id;
```

---

## 5️⃣ Top 3 Highest-Paid Employees (Google)
```sql
SELECT *
FROM Employee
ORDER BY salary DESC
LIMIT 3;
```

---

## 6️⃣ Customers Who Purchased but Never Returned (Walmart)
```sql
SELECT DISTINCT o.customer_id
FROM Orders o
LEFT JOIN Returns r ON o.customer_id = r.customer_id
WHERE r.customer_id IS NULL;
```

---

## 7️⃣ Orders Per Customer (Meta)
```sql
SELECT customer_id, COUNT(*) AS order_count
FROM Orders
GROUP BY customer_id;
```

---

## 8️⃣ Employees Joined in 2023 (Amazon)
```sql
SELECT *
FROM Employee
WHERE YEAR(hire_date) = 2023;
```

---

## 9️⃣ Average Order Value Per Customer (Microsoft)
```sql
SELECT customer_id, AVG(total_amount) AS avg_order_value
FROM Orders
GROUP BY customer_id;
```

---

## 🔟 Latest Order Per Customer (Uber)
```sql
SELECT customer_id, MAX(order_date) AS latest_order_date
FROM Orders
GROUP BY customer_id;
```

---

## 1️⃣1️⃣ Products Never Sold (Generic)
```sql
SELECT p.product_id
FROM Products p
LEFT JOIN Sales s ON p.product_id = s.product_id
WHERE s.product_id IS NULL;
```

---

## 1️⃣2️⃣ Most Selling Product (Adobe / Walmart)
```sql
SELECT product_id, SUM(quantity) AS total_qty
FROM Sales
GROUP BY product_id
ORDER BY total_qty DESC
LIMIT 1;
```

---

## 1️⃣3️⃣ Revenue & Orders Per Region (Meta)
```sql
SELECT region,
       SUM(total_amount) AS total_revenue,
       COUNT(*) AS order_count
FROM Orders
GROUP BY region;
```

---

## 1️⃣4️⃣ Customers With More Than 5 Orders (Amazon)
```sql
SELECT COUNT(*) AS customer_count
FROM (
  SELECT customer_id
  FROM Orders
  GROUP BY customer_id
  HAVING COUNT(*) > 5
) t;
```

---

## 1️⃣5️⃣ Orders Above Average Order Value (PayPal)
```sql
SELECT DISTINCT customer_id
FROM Orders
WHERE total_amount > (SELECT AVG(total_amount) FROM Orders);
```

---

## 1️⃣6️⃣ Employees Hired on Weekends (Google)
```sql
SELECT *
FROM Employee
WHERE DAYOFWEEK(hire_date) IN (1,7);
```

---

## 1️⃣7️⃣ Salary Between 50K and 100K (Microsoft)
```sql
SELECT *
FROM Employee
WHERE salary BETWEEN 50000 AND 100000;
```

---

## 1️⃣8️⃣ Monthly Revenue & Orders (Google)
```sql
SELECT DATE_FORMAT(order_date, '%Y-%m') AS month,
       SUM(total_amount) AS total_revenue,
       COUNT(order_id) AS order_count
FROM Orders
GROUP BY month;
```

---

## 1️⃣9️⃣ Rank Employees by Salary per Department (Amazon)
```sql
SELECT employee_id, department_id, salary,
       RANK() OVER (PARTITION BY department_id ORDER BY salary DESC) AS salary_rank
FROM Employee;
```

---

## 2️⃣0️⃣ Customers Ordering Every Month in 2023 (Meta)
```sql
SELECT customer_id
FROM Orders
WHERE YEAR(order_date) = 2023
GROUP BY customer_id
HAVING COUNT(DISTINCT MONTH(order_date)) = 12;
```

---

## 2️⃣1️⃣ Moving Average of Sales (3 Days) (Microsoft)
```sql
SELECT order_date,
       AVG(total_amount) OVER (
         ORDER BY order_date
         ROWS BETWEEN 2 PRECEDING AND CURRENT ROW
       ) AS moving_avg_3day
FROM Orders;
```

---

## 2️⃣2️⃣ First & Last Order Date Per Customer (Uber)
```sql
SELECT customer_id,
       MIN(order_date) AS first_order,
       MAX(order_date) AS last_order
FROM Orders
GROUP BY customer_id;
```

---

## 2️⃣3️⃣ Revenue Distribution Percentage (PayPal)
```sql
WITH total AS (
  SELECT SUM(quantity * price) AS total_revenue FROM Sales
)
SELECT s.product_id,
       SUM(s.quantity * s.price) AS revenue,
       SUM(s.quantity * s.price) * 100 / t.total_revenue AS revenue_pct
FROM Sales s
CROSS JOIN total t
GROUP BY s.product_id;
```

---

## 2️⃣4️⃣ Consecutive Purchases (1-Day Gap) (Walmart)
```sql
WITH cte AS (
  SELECT customer_id, order_date,
         LAG(order_date) OVER (PARTITION BY customer_id ORDER BY order_date) AS prev_date
  FROM Orders
)
SELECT *
FROM cte
WHERE DATEDIFF(order_date, prev_date) = 1;
```

---

## 2️⃣5️⃣ Churned Customers (No Orders in Last 6 Months) (Amazon)
```sql
SELECT customer_id
FROM Orders
GROUP BY customer_id
HAVING MAX(order_date) < DATE_SUB(CURDATE(), INTERVAL 6 MONTH);
```

---

## 2️⃣6️⃣ Cumulative Revenue (Adobe)
```sql
SELECT order_date,
       SUM(total_amount) OVER (ORDER BY order_date) AS cumulative_revenue
FROM Orders;
```

---

## 2️⃣7️⃣ Top Performing Departments (Google)
```sql
SELECT department_id, AVG(salary) AS avg_salary
FROM Employee
GROUP BY department_id
ORDER BY avg_salary DESC;
```

---

## 2️⃣8️⃣ Customers With Above-Average Orders (Meta)
```sql
WITH customer_orders AS (
  SELECT customer_id, COUNT(*) AS order_count
  FROM Orders
  GROUP BY customer_id
)
SELECT customer_id, order_count
FROM customer_orders
WHERE order_count > (SELECT AVG(order_count) FROM customer_orders);
```

---

## 2️⃣9️⃣ Revenue From New Customers (Microsoft)
```sql
WITH first_orders AS (
  SELECT customer_id, MIN(order_date) AS first_order_date
  FROM Orders
  GROUP BY customer_id
)
SELECT SUM(o.total_amount) AS new_customer_revenue
FROM Orders o
JOIN first_orders f
ON o.customer_id = f.customer_id
AND o.order_date = f.first_order_date;
```

---

## 3️⃣0️⃣ Percentage of Employees per Department (Uber)
```sql
SELECT department_id,
       COUNT(*) * 100 / (SELECT COUNT(*) FROM Employee) AS emp_pct
FROM Employee
GROUP BY department_id;
```

---

## 3️⃣1️⃣ Salary Difference per Department (PayPal)
```sql
SELECT department_id,
       MAX(salary) - MIN(salary) AS salary_diff
FROM Employee
GROUP BY department_id;
```

---

## 3️⃣2️⃣ Pareto (80/20) Products (Walmart)
```sql
WITH sales_cte AS (
  SELECT product_id, SUM(quantity * price) AS revenue
  FROM Sales
  GROUP BY product_id
), total AS (
  SELECT SUM(revenue) AS total_revenue FROM sales_cte
)
SELECT product_id, revenue
FROM (
  SELECT s.product_id, s.revenue,
         SUM(s.revenue) OVER (ORDER BY s.revenue DESC) AS cumulative_revenue,
         t.total_revenue
  FROM sales_cte s
  CROSS JOIN total t
) x
WHERE cumulative_revenue <= total_revenue * 0.8;
```

---

## 3️⃣3️⃣ Latest Order with Amount (Google)
```sql
WITH ranked AS (
  SELECT customer_id, order_id, total_amount,
         ROW_NUMBER() OVER (PARTITION BY customer_id ORDER BY order_date DESC) AS rn
  FROM Orders
)
SELECT customer_id, order_id, total_amount
FROM ranked
WHERE rn = 1;
```

---

## 3️⃣4️⃣ Average Time Between Purchases (Meta)
```sql
WITH cte AS (
  SELECT customer_id, order_date,
         LAG(order_date) OVER (PARTITION BY customer_id ORDER BY order_date) AS prev_date
  FROM Orders
)
SELECT customer_id,
       AVG(DATEDIFF(order_date, prev_date)) AS avg_gap_days
FROM cte
WHERE prev_date IS NOT NULL
GROUP BY customer_id;
```

---

## 3️⃣5️⃣ Year-over-Year Growth (Microsoft)
```sql
WITH yearly AS (
  SELECT YEAR(order_date) AS yr, SUM(total_amount) AS revenue
  FROM Orders
  GROUP BY YEAR(order_date)
)
SELECT yr, revenue,
       revenue - LAG(revenue) OVER (ORDER BY yr) AS yoy_growth
FROM yearly;
```

---

## 3️⃣6️⃣ Top 10% Orders per Customer (Amazon)
```sql
WITH ranked AS (
  SELECT customer_id, order_id, total_amount,
         NTILE(10) OVER (PARTITION BY customer_id ORDER BY total_amount) AS bucket
  FROM Orders
)
SELECT *
FROM ranked
WHERE bucket = 10;
```

---

## 3️⃣7️⃣ Longest Gap Between Orders (Meta)
```sql
WITH cte AS (
  SELECT customer_id, order_date,
         LAG(order_date) OVER (PARTITION BY customer_id ORDER BY order_date) AS prev_date
  FROM Orders
)
SELECT customer_id,
       MAX(DATEDIFF(order_date, prev_date)) AS max_gap_days
FROM cte
WHERE prev_date IS NOT NULL
GROUP BY customer_id;
```

---

## 3️⃣8️⃣ Bottom 10% Revenue Customers (Google)
```sql
WITH cust_rev AS (
  SELECT customer_id, SUM(total_amount) AS revenue
  FROM Orders
  GROUP BY customer_id
), ranked AS (
  SELECT customer_id, revenue,
         NTILE(10) OVER (ORDER BY revenue) AS bucket
  FROM cust_rev
)
SELECT customer_id, revenue
FROM ranked
WHERE bucket = 1;
```

---

## 🧠 Interview Tips

- Always clarify **NULL handling** and edge cases  
- Prefer **JOINs over subqueries** where possible  
- Practice **window functions**  

