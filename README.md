
# 📦 Vendor Performance Optimization Analysis

A comprehensive data analytics project to optimize profitability in retail & wholesale operations by uncovering inefficiencies in **pricing**, **inventory management**, and **vendor performance** using **Python**, **SQL**, and **Power BI**.

---

## 🚀 Project Objectives

🔍 The core goal of this project is to help businesses make smarter, data-driven decisions across inventory, pricing, and vendor relationships. Specifically, the analysis was conducted to:

- 📉 Identify underperforming brands that need pricing or promotional adjustments.
- 💰 Determine top vendors contributing to sales and gross profit.
- 📦 Evaluate inventory turnover to reduce holding costs and improve stock efficiency.
- 🛒 Assess the impact of bulk purchasing on cost savings.
- 📊 Analyze profit margin disparities between high and low-performing vendors using statistics.

---

## 🧰 Tech Stack & Tools

| Tool           | Purpose                                     |
|----------------|---------------------------------------------|
| **Python**     | Data cleaning, transformation, analysis     |
| **Pandas**     | Data manipulation                           |
| **SQLite**     | Database for structured querying            |
| **SQLAlchemy** | Python-DB interface for SQLite              |
| **Jupyter**    | EDA and business insight documentation      |
| **Power BI**   | Dashboarding and storytelling               |
| **Logging**    | Debugging and audit trails for pipelines    |

---

## 🗂️ Repository Structure

```

📦 Vendor-Performance-Analysis
├── data/                           # Raw CSV data (to be ingested into SQLite)
├── logs/                           # Debug and ETL logs
├── notebooks/
│   ├── Exploratory Data Analysis.ipynb
│   └── Vendor Performance Analysis.ipynb
├── reports/
│   └── Vendor Performance Report.pdf
├── scripts/
│   ├── ingestion\_db.py             # Script to load CSVs into SQLite
│   └── get\_vendor\_summary.py      # SQL + data transformation logic
├── vendor\_sales\_summary.csv       # Final merged dataset for analysis
├── vendor\_performance.pbix        # Power BI dashboard file
└── README.md                      # Project documentation

````
![image](https://github.com/user-attachments/assets/3b6471cc-4fc8-44a7-82b2-9f49385fb737)

---

## 🔧 How It Works

### 1️⃣ Data Ingestion  
Raw CSVs in the `/data` folder are ingested into a SQLite database using:
```bash
python scripts/ingestion_db.py
````

### 2️⃣ Vendor Summary Generation

A SQL + Pandas script joins purchases, invoices, and sales data to generate a clean summary:

```bash
python scripts/get_vendor_summary.py
```

### 3️⃣ Data Cleaning & Feature Engineering

The following calculated fields were added:

* **Gross Profit** = Sales Revenue - Purchase Cost
* **Profit Margin** = (Gross Profit / Sales Revenue) \* 100
* **Stock Turnover** = Total Sales Quantity / Total Purchase Quantity
* **Sales-to-Purchase Ratio** = Sales Value / Purchase Value

---

## 📈 Exploratory Data Analysis

Conducted in `Exploratory Data Analysis.ipynb`, covering:

* ❌ Negative or zero profit/margin products
* 📉 Zero-sales inventory (possible obsolete stock)
* 📦 Outlier detection in price, freight, and turnover
* 🔗 Correlation matrix:

  * Strong correlation between purchase and sales quantity
  * Weak correlation between pricing and profitability

---

## 📊 Business Insights

✅ Extracted from detailed EDA and statistics:

* **198 brands** show high margins but low sales — need pricing/promo adjustments
* **\$2.71M worth** of inventory remains unsold — impacting working capital
* **Top 10 vendors** = 65.7% of purchases — over-reliance risk
* **Bulk orders** reduce unit cost by **72%**
* **Statistical testing** confirms significant difference in margin behavior between top and low-performing vendors

---

## 📊 Power BI Dashboard

📁 `vendor_performance.pbix`

Includes:

* 💹 Vendor-level sales & margin analysis
* 📦 Inventory turnover metrics
* 🧾 Unsold inventory visualization
* 🏆 Vendor comparisons (high vs. low performing)

---

## 📐 Statistical Testing Summary

Performed hypothesis testing:

> **Null (H₀):** No significant margin difference
> **Alternative (H₁):** Margin difference exists between vendor groups

✅ **Result:** Rejected H₀ — confirming pricing strategy differences between top- and low-performing vendors.

---

## ✅ Recommendations

Based on the insights:

* 🎯 Promote high-margin, low-volume brands
* 🔀 Diversify vendor base to reduce risk
* 📦 Use bulk ordering for cost efficiency
* 🛍️ Run clearance sales for slow inventory
* 💡 Improve pricing & marketing for underperformers
* 🚚 Optimize freight/shipping cost strategies

---

## ⭐ Final Note

This project demonstrates strong capabilities in:

* 🧹 Data Cleaning & Transformation
* 📊 EDA & Correlation Insights
* 📐 Statistical Analysis (Hypothesis Testing)
* 📈 Visualization (Power BI)
* 💼 Business Strategy Recommendations

