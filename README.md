# Task-7-ElevateLABS
Get Basic Sales Summary from a Tiny SQLite Database using Python

Task 7: Basic Sales Summary from a Tiny SQLite Database


📌 Objective

The goal of this project is to demonstrate how to use Python with SQLite to pull simple sales insights such as total quantity sold and total revenue, and visualize the results with a basic bar chart.

🛠️ Tools Used

Python (sqlite3, pandas, matplotlib)

SQLite (built into Python — no setup required)

Jupyter Notebook / .py script

📂 Dataset

A small SQLite database sales_data.db is created with one table:

Table: sales

Column	Type	Description

id	INTEGER	Primary Key

product	TEXT	Name of the product

quantity	INTEGER	Quantity sold

price	REAL	Price per unit (₹)

Sample entries include Laptop, Smartphone, Headphones, Tablet with different sales values.

🚀 Steps Performed

Create Database & Table

Used sqlite3 to create a new database sales_data.db with a sales table.

Insert Sample Data

Added sales records for multiple products.

Run SQL Queries

Queried total sales quantity and revenue per product.

SELECT product, 
       SUM(quantity) AS total_qty, 
       SUM(quantity * price) AS revenue
FROM sales
GROUP BY product;


Load into Pandas

Fetched results into a DataFrame using pandas.

Print & Visualize

Printed summary in tabular format.

Plotted a bar chart of revenue per product using matplotlib.

📊 Output


Sales Summary Table
product	total_qty	revenue
Laptop	8	4,86,000
Smartphone	17	3,46,000
Headphones	25	53,000
Tablet	6	1,76,000
Revenue Bar Chart

The script generates a bar chart (sales_chart.png) that shows revenue distribution by product.

📑 Deliverables

task7_sales_summary.ipynb (Jupyter Notebook) or task7_sales_summary.py (Python script)

sales_data.db (SQLite database with sample sales data)

sales_chart.png (bar chart visualization)

README.md (project documentation)

✅ This project demonstrates SQL integration inside Python and basic data visualization.
