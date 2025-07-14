# 📊 Category-Level P&L Tracker for E-Commerce SKUs

## 📌 Project Overview  
This project provides a **category-wise profit & loss (P&L)** tracking solution for **e-commerce SKUs** using **Python, Pandas, SQL, and SQLite**. It simulates **sales, returns, and cost data**, calculates **net profit and margins** by category, and enables **data-driven decisions** for assortment planning and operational improvements. The results are ready for use in **Power BI or Excel dashboards**.

---

## 🎯 Objective
- **Simulate** e-commerce sales, returns, and cost data for multiple categories.  
- **Calculate category-level P&L**:  
  - **Net Revenue**, **Total Cost**, **Net Profit**, and **Profit Margin**  
- **Store and query** P&L data using SQLite and SQL.  
- **Enable business insights** for margin optimization and loss reduction.  
- **Export results** for dashboarding and reporting.

---

## 🛠️ Tools & Technologies
- **Python**: Data simulation and processing  
- **Pandas, NumPy**: Data manipulation and aggregation  
- **SQLite**: Embedded database for SQL queries  
- **SQL**: Business logic and reporting  
- *(Optional)* **Power BI / Excel**: Dashboard and visualization

---

## 📦 Dataset
Simulated dataset includes:
- **SKU**: Product identifier  
- **Category**: Product category (e.g., Fashion, Electronics, Home, Beauty, Footwear)  
- **Sales**: Total sales value (₹)  
- **Returns**: Returned amount (₹)  
- **COGS**: Cost of goods sold (₹)  
- **LogisticsCost**: Logistics overhead (₹)  
- **MarketingCost**: Marketing overhead (₹)  

➡️ Data is randomly generated for **1000+ transactions** across **5 categories**.

---

## 🔎 Key Steps

### 1. Simulate E-Commerce Data
Using **Python, NumPy, Pandas**

### 2. Calculate Category-Level P&L
- **Net Revenue** = `Sales – Returns`  
- **Total Cost** = `COGS + LogisticsCost + MarketingCost`  
- **Net Profit** = `Net Revenue – Total Cost`  
- **Profit Margin** = `(Net Profit / Net Revenue) × 100`

### 3. Store Data in SQLite
Stored in `.db` file for persistent querying.

### 4. Run SQL Queries for Insights
- Top categories by net profit  
- Categories with negative profit margins  
- Full category-wise P&L summary

### 5. Export Results
Final output is exported as CSV and Excel.

---

## 🖼️ Sample Output Preview

![Category-Level Summary Output](output_preview.png)

📁 [Click to Download Excel Output](https://github.com/student-kajal/category-pnl-tracker/blob/main/category_pnl_summary.csv)

---

## 📊 Sample SQL Queries

```sql
-- Top 3 categories by Net Profit
SELECT Category, NetProfit
FROM category_pnl
ORDER BY NetProfit DESC
LIMIT 3;

-- Categories with Negative Profit Margin
SELECT Category, NetProfit, ProfitMargin
FROM category_pnl
WHERE ProfitMargin < 0;

-- Category-wise P&L Summary
SELECT Category, NetRevenue, TotalCost, NetProfit, ProfitMargin
FROM category_pnl
ORDER BY NetProfit ASC;

🚀 How to Run
1. Clone the Repository
git clone https://github.com/student-kajal/category-pnl-tracker
cd category-pnl-tracker
2. Install Requirements
pip install pandas numpy
3. Run the Jupyter Notebook
Open category_pnl.ipynb and run all cells step-by-step.
4. Explore SQL Queries
Use the notebook or a tool like DB Browser for SQLite to run and modify SQL queries.
5. Export & Visualize
Open the final .csv or .xlsx in Power BI or Excel.
```
💼 Business Impact
✅ Margin Optimization: Identify and double-down on profitable categories

🚨 Loss Reduction: Detect and address high-loss or negative-margin categories

🧠 Operational Efficiency: Inform assortment planning and cost control

📊 Dashboard Ready: Clean structure for BI tool integration

👩‍💻 Author
## Kajal
Business Analytics | Data-Driven Problem Solver | E-Commerce Domain Knowledge

📜 License
This repository is intended for educational and portfolio purposes only.
🧠 This project demonstrates data analytics, SQL integration, and business acumen — ideal for roles in business management, e-commerce operations, and data analytics.
