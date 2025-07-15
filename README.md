# 🍕 Pizza Sales Analysis using SQL

## 📌 Project Overview
This project demonstrates end-to-end data analysis using SQL on a real-world **Pizza Sales** dataset. From data importing to complex queries, this project covers all essential steps required in the life cycle of a typical data analysis task performed by **Business Analysts** and **Data Analysts** in the food & beverage industry.

The goal was to extract meaningful insights from sales data to drive business decisions such as identifying popular pizza types, analyzing revenue trends, and understanding customer preferences over time.

---

## 🗂️ Dataset Details

### Tables Used:
- `orders` – Order date, time, and IDs  
- `order_details` – Order-specific pizza quantities and IDs  
- `pizzas` – Pizza names, categories, sizes, and prices  
- `pizza_types` – Additional metadata like ingredients and flavor category  

**Data Source**: Provided as `.csv` files and imported into an SQL database for analysis

---

## 🛠️ Project Workflow

### 🧱 Step 1: Database Setup & Data Import
- Created a SQL database for the project  
- Imported `.csv` files into corresponding SQL tables  
- Ensured proper data types and relationships across tables  

---

## 🔍 Analysis Stages

### ✅ Basic SQL Analysis
- ✅ Calculated the **total number of orders** placed  
- ✅ Computed **total revenue** generated from all pizza sales  
- ✅ Identified the **highest-priced pizza**  
- ✅ Found the **most common pizza size** ordered  
- ✅ Retrieved the **Top 5 most ordered pizza types** along with total quantities  

### 🟡 Intermediate SQL Analysis
- 🟡 Joined necessary tables to determine the **total quantity of each pizza category** ordered  
- 🟡 Analyzed **order distribution by hour of the day** to understand peak hours  
- 🟡 Grouped orders by category to find **category-wise sales distribution**  
- 🟡 Grouped orders by date and computed **average number of pizzas ordered per day**  
- 🟡 Identified **Top 3 most ordered pizza types based on revenue**  

### 🔴 Advanced SQL Insights
- 🔴 Calculated **percentage revenue contribution** of each pizza type to total revenue  
- 🔴 Analyzed **cumulative revenue over time** to observe growth trends  
- 🔴 Segmented **Top 3 pizza types by revenue within each category** using advanced joins and subqueries  

---

## 📈 Sample Insights Generated
- 🍕 **Most ordered pizza**: Classic Deluxe  
- 💰 **Top revenue generator**: BBQ Chicken Pizza  
- 🕒 **Peak order time**: 7 PM to 9 PM  
- 📊 **Category with highest order volume**: Classic  

---

## 🧠 What I Learned
- Practical use of **SQL joins, subqueries, groupings, and window functions**  
- Business-driven analysis techniques using **structured queries**  
- Query optimization and **real-time insight extraction**  
- Using **SQL as a standalone analysis tool** without needing BI tools  

---

> ✅ This project serves as a complete roadmap to performing structured SQL-based analysis, from importing raw data to deriving business-ready insights.
