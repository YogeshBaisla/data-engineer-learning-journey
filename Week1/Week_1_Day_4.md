# Data Engineer Journey

Hi! This file contains my learning and progress from **Week 1 Day 4** of my Data Engineer journey.

---

## 🧠 Concepts Covered

### 🔁 Self Joins
- Learned how to join a table with itself.
- Useful for comparing rows within the same table (e.g., employee-manager relationships).

### 🔗 UNION vs UNION ALL
- `UNION`: Combines and removes duplicates.
- `UNION ALL`: Combines all, including duplicates.
- Learned when to use each based on performance and data needs.

### 🚫 EXCEPT / MINUS
- Filters out unmatched records from one result set.
- Very helpful in identifying what’s *missing* from one dataset compared to another.

### 🔁 INTERSECT
- Returns only common records between two result sets.

### 🎯 DISTINCT
- Eliminates duplicate rows.
- Useful for getting unique values from a column or combination of columns.

---

## ✅ Questions Solved

### 📍 LeetCode
🔹 **Employee Earning More Than Their Manager**
```sql
SELECT e.name AS Employee
FROM Employee e
JOIN Employee m ON e.managerId = m.id
WHERE e.salary > m.salary;
```

### 📍 StrataScratch
🔹 **Find the Difference Between Two User Datasets**  
*Practiced with `EXCEPT` / `MINUS` to compare records*

### 📍 DataLemur
🔹 **Duplicate Job Titles**  
*Used `DISTINCT` and joins to filter out non-unique titles*

---

## 📌 Reflection

### ✅ What I Learned
1. The real-world power of `EXCEPT` and `INTERSECT` in data auditing
2. `Self JOIN` is a game-changer for comparing hierarchical data
3. `UNION ALL` is often faster than `UNION` when duplicates are not an issue

### ❗ Challenge
I initially misunderstood the schema in the StrataScratch problem and missed the correct join keys.  
✅ Fixed it by carefully reviewing column relationships before writing queries.

---

🎉 Day 4 complete On to deeper concepts as we go.
