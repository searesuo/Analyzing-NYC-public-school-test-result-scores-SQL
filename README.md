# 🏫 Analyzing NYC Public School SAT Scores with SQL

This project explores SAT (Scholastic Aptitude Test) performance across New York City public schools using structured SQL queries. The goal is to uncover patterns in test scores, identify top-performing schools, and analyze borough-level trends. This intermediate SQL project combines reporting, filtering, and aggregating techniques for insightful education data analysis.

---

## 🎯 Project Objectives

In this project, we aim to answer:

1. ❓ **How many schools fail to report SAT scores?**
2. 🧠 **Which schools perform best/worst** in:
   - Reading
   - Math
   - Writing
3. 🏆 What are the **highest and lowest scores** in each SAT component?
4. 🏅 What are the **top 10 schools by average total SAT score**?
5. 🗺️ **How does SAT performance vary across NYC boroughs?**
6. 🔍 What are the **top 5 schools by average score** (across all components or a single one) **within a specific borough**?

---

## 🗃️ Data Overview

The SAT dataset is typically structured as follows:

### `sat_scores`
| Column          | Description                           |
|------------------|---------------------------------------|
| `school_name`    | Name of the public school             |
| `borough`        | Borough where the school is located   |
| `reading_score`  | SAT reading score                     |
| `math_score`     | SAT math score                        |
| `writing_score`  | SAT writing score                     |

> 📝 Note: Some rows may contain missing values, which must be accounted for in analysis.

---

## 🧾 SQL Highlights

### 🔍 1. Count Schools with Missing Data

```sql
SELECT COUNT(*) AS missing_schools
FROM sat_scores
WHERE reading_score IS NULL
   OR math_score IS NULL
   OR writing_score IS NULL;
