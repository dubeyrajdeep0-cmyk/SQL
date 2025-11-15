# 📚 Database Files Summary (saitm_dep1.sql & saitm_groups_studentds.sql)

These two files contain SQL data dumps for tables within a database named `saitm`. Both tables appear to store student-related academic records.

## 📝 Tables Structure

Both `dep1` and `groups_studentds` tables share the same schema:

| Column Name | Data Type | Description |
| :--- | :--- | :--- |
| `name` | `varchar(30)` | Student's name. |
| `rollno` | `int` | Student's roll number (likely an identifier). |
| `class` | `varchar(30)` | The class/section the student belongs to (e.g., 'ds-a'). |
| `grade` | `varchar(10)` | The letter grade achieved (e.g., 'A', 'B+'). |
| `marks` | `int` | The numerical marks achieved. |

---

## 📊 Table Content Summary

Both tables contain records for students in the class `'ds-a'`.

### 1. `dep1` (from `saitm_dep1.sql`)

This table contains **9 records** in total.
* **Distinct Students:** 8 distinct students (the record for 'manik', rollno 131 is duplicated).
* **Class:** All records are for `'ds-a'`.
* **Grades:** All records are assigned an `'A'` grade.
* **Marks Range:** Marks range from 88 to 96.
    * *Note:* The data contains a duplicate entry: ('manik', 131, 'ds-a', 'A', 91) appears twice.

### 2. `groups_studentds` (from `saitm_groups_studentds.sql`)

This table contains **8 records** in total.
* **Distinct Students:** 8 distinct students.
* **Class:** All records are for `'ds-a'`.
* **Grades:** Records use multiple grades (`'A'` and `'B+'`).
    * Students with marks $\ge 90$ have grade `'A'`.
    * Students with marks $< 90$ (88, 89) have grade `'B+'`.
* **Marks Range:** Marks range from 88 to 96.

---

## 🛠️ SQL File Details

Both files are MySQL dumps created on **2025-11-14** and are configured for `utf8mb4` character set and `InnoDB` engine. They are ready to be imported into a MySQL database named `saitm`.

***

Would you like to analyze specific records, or perhaps generate a SQL query to compare the data between these two tables?
