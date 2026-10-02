# Python-SQL-Database-Connection

## 📌 Project Overview

This project demonstrates how to **connect Python with a SQL database**, load datasets into database tables, and execute SQL queries through Python.

The project was created to practice **Python, SQL, SQLite, Pandas, and database connectivity** using real-world Chicago datasets.

## 🎯 Objectives

* Connect Python with a SQLite database
* Load CSV datasets into database tables
* Execute SQL queries using Python
* Retrieve and analyze database results using Pandas
* Practice SQL filtering, grouping, sorting, and aggregation
* Understand the workflow between Python and a relational database

## 🗂️ Datasets

The project uses three Chicago datasets:

1. **Chicago Census Data** – Socioeconomic indicators for Chicago community areas
2. **Chicago Public Schools Data** – School-level information and performance data
3. **Chicago Crime Data** – Reported crime incidents in Chicago

## 🛠️ Technologies Used

* **Python**
* **SQL**
* **SQLite**
* **Pandas**
* **VS Code**

## 🔄 Project Workflow

```text
CSV Files
    ↓
Python / Pandas
    ↓
SQLite Database
    ↓
SQL Queries
    ↓
Python
    ↓
Pandas DataFrame
    ↓
Data Analysis
```

## 💻 Python-Database Connection

Python is connected to the SQLite database using the `sqlite3` library.

```python
import sqlite3

connection = sqlite3.connect("ChicagoCrimeData.db")
```

SQL queries can then be executed through Python:

```python
query = """
SELECT PRIMARY_TYPE, COUNT(*) AS total_crimes
FROM crime
GROUP BY PRIMARY_TYPE
ORDER BY total_crimes DESC
LIMIT 5;
"""

result = pd.read_sql_query(query, connection)

print(result.to_string(index=False))
```

## 📊 Example Analysis

The project includes SQL queries for:

* Counting records
* Grouping data
* Sorting results
* Filtering records
* Finding top crime categories
* Analyzing socioeconomic indicators
* Retrieving data from multiple database tables

Example:

```sql
SELECT community_area_name,
       community_area_number,
       per_capita_income
FROM census_data
WHERE per_capita_income < 11000;
```

## 📁 Project Structure

```text
Python-SQL-Database-Connection/
│
├── data/
│   ├── ChicagoCensusData.csv
│   ├── ChicagoPublicSchools.csv
│   └── ChicagoCrimeData.csv
│
├── ChicagoCrimeData.db
│
├── Chicago_Data_Analysis.ipynb
│
└── README.md
```

## 📚 Skills Practiced

* Python Database Connectivity
* SQL Queries
* SQLite Database Management
* Pandas DataFrames
* CSV Data Handling
* Data Filtering
* Data Aggregation
* `GROUP BY`
* `ORDER BY`
* `WHERE`
* SQL `COUNT()`
* Database and Table Operations

## 🚀 Key Learning

The main learning from this project was understanding how **Python can connect to a database and use SQL to retrieve and analyze data**.

This project helped build a practical understanding of the workflow:

**Python → Database → SQL → Results → Pandas → Analysis**

## 👤 Author

**Sunny Rai**

Aspiring Data Engineer | SQL | Python | Pandas | Data Analytics
