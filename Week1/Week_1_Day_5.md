# Data Engineer Journey

Hi, I have started my journey to become a Data Engineer. This file contains Week 1 Day 5 learning and inputs. Below are the topics I covered and what I learned today.

---

## 🔍 SQL Concepts

### 1. Window Functions

I learned how to use SQL window functions such as `RANK()`, `DENSE_RANK()`, and `ROW_NUMBER()` to assign rankings within a partition of data.

- **RANK()** – Assigns rank with gaps
- **DENSE_RANK()** – Assigns continuous ranks without gaps
- **ROW_NUMBER()** – Assigns a unique row number within a partition

#### 🧪 Example:
```sql
SELECT 
  employee_id,
  salary,
  DENSE_RANK() OVER (PARTITION BY department_id ORDER BY salary DESC) AS salary_rank
FROM employees;
```

---

## 🧠 Questions Solved

### 🔎 LeetCode:
1. **Rank Scores** – Practiced RANK()
2. **Nth Highest Salary** – Practiced subqueries and windowing
3. **Department Top Three Salaries** – Practiced DENSE_RANK with PARTITION BY

### 🔎 StrataScratch:
1. **Top Ranked Songs** – Practiced ROW_NUMBER()
2. **Top 3 Cities With Most Spend** – Practiced using SUM() with ranking

---

## 💬 Reflection

- **3 things I learned:**
  1. Difference between RANK, DENSE_RANK, and ROW_NUMBER
  2. How to partition data for per-group rankings
  3. Use of ORDER BY inside OVER() clause

- **1 mistake/challenge and how I fixed it:**  
  I initially used WHERE instead of filtering on the window function rank in an outer query. I corrected it by nesting the query and applying the condition in the outer SELECT.

---

## 📌 Bonus

### Interview Question from Interview Query:
**Second Highest Salary Per Department** – Learned how to use DENSE_RANK() with PARTITION BY to find this.

### Mode Analytics:
Practiced live SQL queries on Mode’s window function tutorial.

---

## 🧾 Note

By this, I end Week 1 Day 5. Looking forward to continuing the journey tomorrow!
