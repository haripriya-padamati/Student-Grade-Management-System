# Student-Grade-Management-System
[![Python](https://img.shields.io/badge/Python-3.8+-blue)](https://python.org)
[![SQLite](https://img.shields.io/badge/SQLite-3.0+-green)](https://sqlite.org)
[![Pandas](https://img.shields.io/badge/Pandas-2.0+-yellow)](https://pandas.pydata.org)
SQLite + Python grade management system with GPA analytics, CRUD ops, and 10K-scale optimization

## Features
- **Normalized Schema**: Students, Courses, Enrollments, Grades, Departments (FKs, indexes)
- **CRUD Operations**: Python/sqlite3 for add/update/delete grades/enrollments
- **Analytics Queries**: GPA calc, top students (GROUP BY/AVR), course avgs, dept stats
- **Pandas Dashboard**: DataFrame summaries/exports
- **Scalable**: Optimized for 10K students (composite indexes)

## ERD
![ERD](ERD.png)

## Quick Start
1. Install: `pip install pandas`
2. Setup DB: `sqlite3 grades.db < schema.sql`
3. Load Data: `sqlite3 grades.db < sample_data.sql` (or run `python generate_data.py`)
4. Run: `python main.py` → See GPA dashboard

## Files
| File | Description |
|------|-------------|
| schema.sql | 5 tables + indexes |
| queries.sql | 10 SQL examples (GPA/top/avgs) |
| main.py | CRUD + `pd.read_sql_query` |
| generate_data.py | Insert 10K fake records |

## Demo Outputs
**GPA Summary (Pandas):**
![GPA](gpa_sample.png)
**Sample Query: Top Performers**