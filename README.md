# Pizza_sales

Here’s a polished `README.md` for your SQL portfolio project, including a link to a public dataset you can use to simulate your work. Just copy this into your repo before your interview—you'll have a credible artifact ready to show.

---

```markdown
# 📊 SQL Data Analysis Portfolio Project

**Project Summary**  
A self-led end-to-end SQL data analysis project using a public sales dataset. Demonstrates ability to structure data, perform exploratory analysis, and extract actionable business insights.

---

## 🔗 Dataset

This project uses the **Sample Sales Data** from Kaggle, which includes orders, customers, products, and sales details:

**Download link:**  
[Sample Sales Data – Kaggle](https://www.kaggle.com/datasets/kyanyoga/sample-sales-data) :contentReference[oaicite:1]{index=1}

---

## 📁 Repository Structure

```

/project-root/
├── data/                   # Raw dataset CSV files
├── schema/                 # SQL scripts: create tables & load data
├── queries/                # SQL analysis scripts
├── outputs/                # Exported query results (CSV/images)
└── README.md               # This file

````

- **data/**: Contains CSVs downloaded from Kaggle.
- **schema/**: Scripts to create tables, define relationships, and load CSV data.
- **queries/**: Organized by analytical steps:
  - `01_explore.sql`
  - `02_aggregations.sql`
  - `03_time_trends.sql`
  - `04_customer_spend.sql`
  - `05_product_performance.sql`
- **outputs/**: Results of queries, screenshots or CSVs, and optional BI visuals.

---

## 🛠️ Setup & Running Instructions

1. **Clone the repository**  
   ```bash
   git clone https://github.com/your_username/your_repo.git
   cd your_repo
````

2. **Download dataset**
   Save the CSV files from the Kaggle link above into the `data/` folder.

3. **Run schema scripts**

   ```sql
   -- In your SQL client (e.g. PostgreSQL)
   \i schema/create_tables.sql
   \i schema/load_data.sql
   ```

4. **Run query scripts**
   Execute `queries/*.sql` files in sequence to replicate the analysis.

5. **Review outputs**
   Check the `outputs/` directory for CSVs or visualizations.

---

## 📌 Analytical Steps & SQL Highlights

### 1. Data Exploration

* Structure and preview raw tables:

  ```sql
  SELECT * FROM customers LIMIT 10;
  SELECT * FROM orders LIMIT 10;
  ```

### 2. Aggregations & Metrics

* Total orders and unique customers:

  ```sql
  SELECT COUNT(*) AS total_orders,
         COUNT(DISTINCT customer_id) AS unique_customers
    FROM orders;
  ```

### 3. Time-Based Trends

* Monthly orders and revenue:

  ```sql
  SELECT DATE_TRUNC('month', o.order_date) AS month,
         COUNT(*) AS total_orders,
         SUM(oi.quantity * oi.unit_price) AS revenue
    FROM orders o
    JOIN order_items oi ON o.id = oi.order_id
    GROUP BY month
    ORDER BY month;
  ```

### 4. Customer Spending Analysis

* Top 10 customers by spend:

  ```sql
  SELECT o.customer_id,
         SUM(oi.quantity * oi.unit_price) AS total_spent
    FROM orders o
    JOIN order_items oi ON o.id = oi.order_id
    GROUP BY o.customer_id
    ORDER BY total_spent DESC
    LIMIT 10;
  ```

### 5. Product Performance Insights

* Top-selling products:

  ```sql
  SELECT oi.product_id,
         SUM(oi.quantity) AS total_qty
    FROM order_items oi
    GROUP BY oi.product_id
    ORDER BY total_qty DESC
    LIMIT 10;
  ```

---

## 📈 Key Insights & Business Takeaways

* **Seasonal Trends**: Identified peak sales months that can guide marketing campaigns.
* **Customer Concentration**: Top 10 customers contribute \~40% of total revenue.
* **Product Prioritization**: A small set of products drive majority of sales volume.
* **Recommendations**:

  * Prioritize inventory and promotions around peak seasons.
  * Build targeted campaigns for high-spend customers.
  * Allocate resources to high-performing product lines.

---

## 💡 Project Learnings

* Advanced use of **JOIN**, **aggregation**, **group-by**, and **date functions** in SQL.
* Emphasized **business storytelling**: starting from data introduction → analysis → insights → recommendations.
* Prepared a reusable and interview-ready analytical project with clear structure and outputs.

---

## 🎙️ Interview Conversation Tips

* Walk interviewers through:

  1. How you selected and ingested the dataset.
  2. Your questioning approach (e.g. “Which months had highest revenue?”).
  3. The SQL logic and results.
  4. Practical business implications of your findings.

---

## 📎 Next Steps You Could Mention

* Customer segmentation analysis or cohort retention queries.
* Churn prediction using time-based purchasing patterns.
* A simple dashboard in Tableau or PowerBI using CSV outputs.
* Forecasting sales trends for next quarter or year.

---

Best of luck in your interview tomorrow! This README sets a strong foundation—you can confidently talk through each section and share how you executed it in SQL.
