# 📊 E-Commerce Profit Leakage & Payment Channel Analytics

[![Power BI](https://img.shields.io/badge/Power_BI-F2C811?style=for-the-badge&logo=power-bi&logoColor=black)](https://powerbi.microsoft.com/)
[![DAX](https://img.shields.io/badge/DAX-Data_Analysis_Expressions-blue?style=for-the-badge)](https://learn.microsoft.com/en-us/dax/)
[![Data Analytics](https://img.shields.io/badge/Analytics-Financial_%26_Operational-green?style=for-the-badge)]()

---

## 📌 Business Overview & Problem Statement

In high-volume e-commerce operations, top-line revenue often masks underlying operational inefficiencies, dynamic payment gateway charges, and seasonal margin compression. 

This Business Intelligence dashboard was engineered to analyze multi-quarter retail transaction data to **isolate profit leakage, evaluate payment gateway economics, track cumulative monthly P/L trajectory, and analyze product category shifts**.

By bridging raw transaction logs with executive-level financial reporting, this tool enables business leads to optimize checkout options, adjust category promotion budgets, and align marketing spend with high-margin quarters.

---

## 📸 Executive Dashboard Overview

![E-Commerce Profit Analytics Dashboard](dashboard_preview.png)
*(Note: Replace `dashboard_preview.png` with the exact image filename uploaded to your GitHub repository)*

---

## 🛠️ Data Architecture & Tech Stack

* **Business Intelligence:** Power BI Desktop (Data Modeling, DAX Engine, Visualizations)
* **ETL & Data Transformation:** Power Query (Data Type Casting, Missing Value Handling, Custom Columns)
* **Data Modeling:** Star Schema architecture linking Transaction Fact Tables with Date, Payment, and Product Dimensions.
* **Visual Techniques:** Dual-axis Combination Charts, Waterfall P/L Analysis, Ribbon/Flow Category Visuals, and Horizontal Bar Breakdowns.

---

## 📐 Key DAX Measures & Logic

Below are sample DAX formulas developed to power the analytical views in this dashboard:

### 1. Total Net Profit
```dax
Total Net Profit = 
SUM(Sales_Data[Profit])
