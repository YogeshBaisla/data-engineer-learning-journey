
# Data Engineer Journey

Hi, I have started my journey to become a data engineer. This file contains **Week 2 Day 1** learning and inputs. Below are the topics I covered and what I learned today:

# Advanced Window Functions

## LAG() and LEAD()
- I learned how to access previous (`LAG()`) and next (`LEAD()`) row values without performing a self-join.
- These functions help in calculating differences, session gaps, or comparing consecutive rows.
- **Example:**
```sql
SELECT user_id, event_date, 
       LAG(event_date) OVER (PARTITION BY user_id ORDER BY event_date) AS previous_event
FROM events;
```

## FIRST_VALUE() and LAST_VALUE()
- I learned how to fetch the first and last values within a partition (group).
- Useful for tracking changes, identifying first purchases, etc.
- **Example:**
```sql
SELECT user_id, 
       FIRST_VALUE(event_date) OVER (PARTITION BY user_id ORDER BY event_date) AS first_event
FROM events;
```

# Common Table Expressions (CTEs)

- I learned how to use the `WITH` keyword to create a CTE, making SQL queries easier to read and maintain.
- CTEs are often better than subqueries for readability, especially in complex queries.
- **Example:**
```sql
WITH ranked_employees AS (
  SELECT name, salary, RANK() OVER (ORDER BY salary DESC) AS rank
  FROM employees
)
SELECT * FROM ranked_employees WHERE rank <= 3;
```

# Questions Solved
I solved 3 questions today:
- **LeetCode:** [Consecutive Numbers](https://leetcode.com/problems/consecutive-numbers/)
- **StrataScratch:** [User Activity - Find Session Gaps](https://platform.stratascratch.com/coding/10176-find-the-number-of-times-the-users-logged-in-and-logged-out)
- **DataLemur:** [Rolling Average Tweet Volume](https://datalemur.com/questions/rolling-average-tweets)

# Reflection
- **Mistake/Challenge:** Initially struggled with understanding the frame used by `LAG()` and `LEAD()`.
- **How I Fixed It:** Carefully observed `PARTITION BY` and `ORDER BY` to control the row access.
- **Saving Today:** No extra notes today. Simple focus and execution!

# Note
This marks the completion of **Week 2 Day 1**.  
Excited to continue this journey toward becoming a Data Engineer 🚀!
