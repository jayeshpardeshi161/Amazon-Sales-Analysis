# Amazon-Sales-Analysis
Amazon Sales Analysis - Power BI Dashboard
# 📊 Amazon Sales Analysis | Power BI Dashboard

## 📌 Project Summary

This project performs an in-depth sales analysis of Amazon product data using Power BI. It reviews product category trends, identifies top-performing products, uncovers seasonal patterns, and supports data-driven decision-making. KPIs such as total sales, product reviews, and units sold help stakeholders gain interactive insights over time.

---

## 🎯 Project Goals

- Optimize business strategy using sales analytics  
- Evaluate product performance and engagement  
- Analyze time-based trends (monthly/quarterly)  
- Identify high-revenue and high-review products  

---

## 📂 Dataset Overview

- **Source**: Excel file (`Amazon_Combined_Data.xlsx`)  
- **Rows**: 89,082  
- **Columns**: 6  

| Column Name         | Description                         |
|---------------------|-------------------------------------|
| Product Category    | Category of the product             |
| Product Description | Description of the product          |
| Price (Dollar)      | Product price in USD                |
| Number of Reviews   | Count of customer reviews           |
| Shipment            | Shipment information                |
| Order Date          | Date of product order               |

---

## ❓ Problem Statement

The business lacks visibility into:
- Top-performing products/categories
- Time-wise (monthly/quarterly) performance variation
- Low-performing products needing attention

This dashboard solves these with KPIs and visual trends.

---

## 📈 KPIs & DAX Measures

| KPI Name           | DAX Formula |
|--------------------|-------------|
| YTD Sales          | `TOTALYTD(SUM(Amazon_Data[Price(Dollar)]), 'Date Table'[Date])` |
| QTD Sales          | `TOTALQTD(SUM(Amazon_Data[Price(Dollar)]), 'Date Table'[Date])` |
| YTD Products Sold  | `TOTALYTD(COUNT(Amazon_Data[Product Category]), 'Date Table'[Date])` |
| YTD Reviews        | `TOTALYTD(SUM(Amazon_Data[Number of Reviews]), 'Date Table'[Date])` |

---

## 🔍 EDA (Exploratory Data Analysis)

- Cleaned date formats and verified data types
- Created `Date Table` using `CALENDAR()` function
- Derived columns: Month, Quarter, Week
- Handled missing/null values

---

## 🧠 Data Modeling

- One-to-many relationship:  
  `Amazon_Data[Order Date] → Date Table[Date]`
- Star schema design for optimized performance

---

## 📊 Visualizations

| Visualization                    | Details |
|----------------------------------|---------|
| 4 KPI Cards                      | YTD Sales, QTD Sales, YTD Products Sold, YTD Reviews |
| Matrix - Sales by Category       | Category-wise YTD & QTD sales, % YTD contribution |
| Bar - Top 5 by YTD Reviews       | Product vs. Reviews |
| Bar - Top 5 by YTD Sales         | Product vs. Sales |
| Line Chart - Monthly Sales       | Sales trend over months |
| Column Chart - Weekly Sales      | Sales volume over weeks |
| Slicers                          | Product Category, Quarter |

---

## 🔑 Key Findings

- Products like **Anker**, **JBL**, and **Amazon Basics** lead in sales and reviews.
- Sales spike notably in **Q1** and post-holiday weeks.
- Mid-priced products attract more reviews = higher sales velocity.
- Weekly sales show post-sale peaks (e.g., early January).

---

## 🧩 Business Impact

- Focus marketing on top-reviewed mid-priced products.
- Promote products more aggressively in high-performing weeks.
- Identify underperforming SKUs for revamp or discontinuation.

---

## 📌 Insights & Inference

- Strong correlation: product reviews ↔ sales.
- High-volume sales in lower-price categories.
- Seasonal sales patterns impact inventory and campaigns.

---

## ✅ Conclusion

The Power BI dashboard provides rich, interactive visuals and KPIs that empower teams to monitor sales, trends, and performance. These insights drive smarter decisions around product strategy, marketing focus, and inventory planning.

---

## 📷 Dashboard Preview

<img width="1165" height="651" alt="dashboard-preview" src="https://github.com/user-attachments/assets/72716b93-ce68-4a64-b39a-30084cc03a3e" />
<img width="414" height="237" alt="sales_by_category" src="https://github.com/user-attachments/assets/59061567-7d36-4f09-b219-fb399bc3aab8" />
<img width="763" height="98" alt="kpi_cards" src="https://github.com/user-attachments/assets/0fcb75bf-5556-416d-9dee-87459e563c54" />



## 📁 Files Included

- `Amazon_Combined_Data.xlsx`
- `Amazon_Sales_Analysis.pbix`
- `README.md`
- `/Images` (dashboard screenshots)

---

## 🔗 Author
 
📧 [jayeshpardeshi161@gmail.com]  
📌 LinkedIn: [Your Profile URL]  
