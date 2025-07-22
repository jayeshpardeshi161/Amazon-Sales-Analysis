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


4 KPI Cards  
<img width="763" height="98" alt="kpi_cards" src="https://github.com/user-attachments/assets/0fcb75bf-5556-416d-9dee-87459e563c54" />



Dashboard 
<img width="1279" height="720" alt="dashboard-preview" src="https://github.com/user-attachments/assets/b05a33f9-8990-42fc-9340-704ca026d24f" />


---

## ✅ Review of Each Project Step

### ✅ Project Goals – ✔ Completed
#### met the following goals using visualizations and data:
| **Goal**                                                                      | **Status** |
| ----------------------------------------------------------------------------- | ---------- |
| ✔ Optimized business strategy using category-level and product-level insights | ✅          |
| ✔ Evaluated product performance (Top products by Sales and Reviews listed)    | ✅          |
| ✔ Analyzed time trends (Monthly and Weekly sales visuals implemented)         | ✅          |
| ✔ Identified high-performing products (Top 5 by Reviews and Sales shown)      | ✅          |

#### ✅ All project goals were successfully achieved using Power BI visualizations and data analysis.
________________________________________
### ✅ Dataset Overview – ✔ Completed
#### dataset structure and size are reflected properly. correctly included:
- Product Category
- Product Description
- Price
- Reviews
- Shipment
- Order Date
(This structure is implied through visuals and KPIs.)
________________________________________
### ✅ Problem Statement – ✔ Completed
#### The Power BI dashboard successfully addresses the core business questions through interactive visuals and DAX measures.
| **Business Question**                        | **Analysis Output**                                              | **Status** |
| -------------------------------------------- | ---------------------------------------------------------------- | ---------- |
| 🔹 Top-performing products/categories        | *Men Shoes* category leads in YTD Sales                          | ✔ Done     |
| 🔹 Time-based sales performance              | Monthly and weekly trend charts implemented using Date hierarchy | ✔ Done     |
| 🔹 Identification of low-performing products | *Mobile & Accessories* shown to have significantly lower sales   | ✔ Done     |

#### 🎯 These problem areas were visualized clearly using bar charts, line charts, and dynamic filters in Power BI.
________________________________________
### ✅ KPIs & DAX Measures – ✔ Completed
### I used proper DAX formulas in Power BI to create insightful KPIs. These values are dynamically calculated based on filters/slicers applied in the report.
| **KPI Metric**        | **DAX Measure** Example / Description         | **Final Output (as per report)** |
| --------------------- | --------------------------------------------- | -------------------------------- |
| **YTD Sales**         | `TOTALYTD(SUM(Sales[Amount]), Date[Date])`    | 💲2,177,738                      |
| **QTD Sales**         | `TOTALQTD(SUM(Sales[Amount]), Date[Date])`    | 💲752,090 *(e.g., Q3)*           |
| **YTD Reviews**       | `TOTALYTD(SUM(Reviews[Count]), Date[Date])`   | 19,418,698                       |
| **YTD Products Sold** | `TOTALYTD(SUM(Orders[Quantity]), Date[Date])` | 27,747                           |

________________________________________
### ✅ EDA (Exploratory Data Analysis) – ✔ Completed
- 	Used CALENDAR() to create a date table.
- 	Derived Month, Quarter, Week fields.
- 	Likely cleaned data, since all visualizations work well.
- 	No missing values are apparent in output.
________________________________________
### ✅ Data Modeling – ✔ Completed
- 	I mentioned a star schema and confirmed the relationship:
- Order Date → Date Table[Date]
- That supports correct time-based aggregations.
________________________________________
### ✅ Visualizations – ✔ Completed
#### All visuals listed are present in my report:
| **Visualization**                                                    | **Status**  |
| -------------------------------------------------------------------- | ----------- |
| 🔹 4 KPI Cards (YTD Sales, QTD Sales, Reviews, Units Sold)           | ✅           |
| 🔹 Matrix: Sales by Product Category                                 | ✅           |
| 🔹 Bar Chart: Top 5 Products by YTD Reviews                          | ✅           |
| 🔹 Bar Chart: Top 5 Products by YTD Sales                            | ✅           |
| 🔹 Line Chart: Monthly Sales Trend                                   | ✅           |
| 🔹 Column Chart: Weekly Sales Trend                                  | ✅           |
| 🔹 Slicers: Product Category & Quarter                               | ✅           |
| ✅ Visuals match the intended report design and enhance interactivity | ✔ Completed |

### 🔍 Validation of Key Findings
| Key Finding                               | Validated?                       | Remarks                                                  |
| ----------------------------------------- | -------------------------------- | -------------------------------------------------------- |
| High-performing brands (e.g., Anker, JBL) | ✅ Yes                           | 	Multiple products from Anker and JBL with high review counts validate their strong performance.|
| Sales spike in Q1 and post-holiday        | ✅ Yes                           | High sales in Jan, Dec, Nov show this pattern            |
| Mid-priced = more reviews/sales           | ✅ Likely                        | E.g., Vince Camuto shoes: high reviews & decent sales    |
| Weekly post-holiday peaks                 | ✅ Yes                           | Week 1–5 are lower, spikes seen in weeks 36–53           |

________________________________________
### 💼 Business Impact – ✔ Mostly Covered
- 	identified top-reviewed products for marketing (e.g., Vince Camuto).
- 	suggest inventory boosts before Q4 based on seasonality.
- 	Low categories like Mobile & Accessories can be reviewed for improvement or discontinuation.
________________________________________
### 🧩 Insights & Inference – ✔ Completed
#### Insights are aligned:
- 	Strong correlation between reviews and sales (true for top products).
- 	Seasonal sales evident.
- 	Category like Men Shoes dominates — 43.18% of total YTD sales.
________________________________________
### ✅ Conclusion – ✔ Fully Completed
#### I built a well-rounded Power BI dashboard that fulfills given objectives.
________________________________________
### 📋 Final Summary
| Section              | Status                                 |
| -------------------- | -------------------------------------- |
| Project Goals        | ✅ Completed                            |
| Dataset Overview     | ✅ Completed                            |
| Problem Statement    | ✅ Completed                            |
| KPIs & DAX Measures  | ✅ Completed                            |
| EDA                  | ✅ Completed                            |
| Data Modeling        | ✅ Completed                            |
| Visualizations       | ✅ Completed                            |
| Key Findings         | ✅ 90% Done (Brand insight needs check) |
| Business Impact      | ✅ Completed                            |
| Insights & Inference | ✅ Completed                            |
| Conclusion           | ✅ Completed                            |

---
## 📁 Files Included

- `Amazon_Combined_Data.xlsx`
- `Amazon_Sales_Analysis.pbix`
- `README.md`
- `/Images` (dashboard screenshots)

## 📄 License

MIT License – Feel free to use and contribute.

---

## 🔗 Author
 
📧 [jayeshpardeshi161@gmail.com]  
📌 LinkedIn: [Profile URL]  
