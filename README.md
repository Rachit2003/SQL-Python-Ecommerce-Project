# 🛒 SQL + Python E-Commerce Analysis Project

## 📌 Overview

This project focuses on extracting, analyzing, and visualizing key business insights from an e-commerce dataset using **MySQL** and **Python**. The goal is to support decision-making in areas like sales performance, customer behavior, product demand, and delivery operations.

---

## 🧰 Tools & Technologies

- **SQL (MySQL)** – For querying and data extraction  
- **Python (Jupyter Notebook)**  
  - **Pandas** – Data manipulation and EDA  
  - **Matplotlib & Seaborn** – Data visualization  
- **MySQL Workbench / Localhost** – SQL interface  

---

## 📊 Key Objectives

- Perform data cleaning and preprocessing
- Extract KPIs from the database using SQL
- Analyze customer behavior, order trends, and delivery delays
- Visualize insights through clear plots and dashboards

---

## 📁 Project Structure

| File | Description |
|------|-------------|
| `MYSQL_DATA.ipynb` | SQL-based extraction of KPIs like monthly sales, top-selling categories, customer distribution |
| `final.ipynb` | Python-based data cleaning, exploratory data analysis (EDA), and visualizations |

---

## 🔍 Key Insights

- 📈 Sales trends by month and product category  
- 👤 Top cities by order volume  
- ⏱️ Delivery time analysis and delays  
- 🛍️ Most purchased product categories  
- 📦 Seller performance and distribution

---

## 📌 Sample SQL Query

```sql
SELECT monthname(order_purchase_timestamp) AS month,
       COUNT(order_id) AS order_count
FROM orders
WHERE YEAR(order_purchase_timestamp) = 2018
GROUP BY month;
