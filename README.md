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

## 💡 Key Business & Financial Insights

### 1. Payment Channel Profitability & Leakage
* **Credit Card Dominance:** Credit Card transactions served as the single largest net profit driver, contributing **~$12K+** in total net profitability.
* **UPI Profit Compression:** While alternative payment modes like Cash on Delivery (COD) (~$3.5K) and EMI (~$2K) remained profitable, **UPI transactions resulted in net negative profit (~ -$0.3K)**. This points to potential underlying payment processing overheads, micro-transaction fee structures, or elevated return rates associated with instant checkout modes.

### 2. Monthly P/L Waterfall & Seasonality (Total Net Profit: $16.4K)
* **Peak Profit Months:** August (**+$4.0K**) and October (**+$2.7K**) served as the primary growth engines for annual cumulative net profit ($16.4K).
* **Seasonal Margin Contraction:** Isolated two key deficit months—May (**-$0.3K**) and November (**-$0.9K**)—where operational costs/discounts offset gross earnings, signaling a need for promotional restructuring during mid-year and post-holiday lulls.

### 3. Sales vs. Profit Realization Disconnect
* **Quarterly Divergence:** High sales volume did not linearly convert to high profit. 
  * **Q1** generated **$60K in Sales** but yielded only **$3.9K in Profit**.
  * **Q3** generated **$47K in Sales** yet delivered the highest quarterly profit at **$7.2K** (driven by favorable product mix and reduced discount margins).

### 4. Product Category Dynamics
* Shifted category mix analysis across **Clothing**, **Electronics**, and **Furniture** revealed strong quarter-over-quarter volume transfers, highlighting seasonal shifts in consumer purchasing behavior across product lines.

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
