🏦 Bank IFSC Project

A project to clean, validate, and store Bank IFSC data using Python (Pandas) and PostgreSQL.

⚙️ Features

Cleans raw bank IFSC dataset (fixes NaN, .0, blanks)

Ensures unique IFSC codes

Stores data in PostgreSQL (bank_details table)

Provides SQL queries for analysis

🛠️ Tech Stack

Python (Pandas, Psycopg2)

PostgreSQL

Git/GitHub

🚀 How to Run

Clone repository

git clone [https://github.com/ShanBenny/Bank-IFSC-Project.git](https://github.com/ShanBenny/Bank.git)
cd Bank-IFSC-Project


Install requirements

pip install pandas psycopg2


Create PostgreSQL database Bank and run bank_details.sql

Insert cleaned data

python insert_data.py

📑 Example SQL Queries

Duplicate IFSC check

SELECT ifsc, COUNT(*) FROM bank_details GROUP BY ifsc HAVING COUNT(*) > 1;


Branches per state

SELECT state, COUNT(*) FROM bank_details GROUP BY state ORDER BY COUNT(*) DESC;

👤 Author

Shan Benny
