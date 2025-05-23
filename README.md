# 🏥 Hospital Database SQL Project

A comprehensive SQL practice project using a simulated hospital database schema from [sql-practice.com](https://sql-practice.com), featuring real-world scenarios, complex queries, and advanced data logic. This project includes queries across **Easy, Medium, and Hard** levels, covering a wide range of SQL concepts.

---

## 📌 Objective

To enhance practical SQL skills through structured problem-solving on a normalized hospital database. The dataset mimics real-life healthcare records, enabling analysis and querying across patient demographics, doctor assignments, medical admissions, and provincial data.

---

## 💻 Tech Stack

- **Platform**: [sql-practice.com](https://sql-practice.com)
- **Language**: SQL (ANSI-compliant)
- **Tools Used**: Online SQL IDE, Microsoft Word (Documentation)
- **Database Schema**: `patients`, `admissions`, `doctors`, `province_names`

---

## 📂 Project Structure

| Level   | Topics Covered |
|---------|----------------|
| Easy    | Filtering, WHERE, LIKE, BETWEEN, JOIN, NULL handling, UPDATE |
| Medium  | Aggregation, HAVING, DISTINCT, Nested SELECTs, CASE statements, String & Date functions |
| Hard    | CTEs, Subqueries, Analytic Functions (LAG), Conditional Aggregation, Business Logic |

---

## ✅ Sample Queries

```sql
-- Get patients admitted on same day they were discharged
SELECT * FROM admissions
WHERE admission_date = discharge_date;

-- List doctors with total number of patients attended
SELECT d.first_name, d.last_name, COUNT(a.attending_doctor_id) AS total_patients
FROM doctors d
JOIN admissions a ON d.doctor_id = a.attending_doctor_id
GROUP BY d.doctor_id;
