# UK E-Commerce Sales Dashboard 

This Power BI project analyzes UK-based e-commerce data to uncover key business insights on sales performance, customer behavior, and product segmentation. It demonstrates strong data modeling, cleaning, visualization, and storytelling skills.

 Project Overview

**Objective:**  
To explore sales trends, customer segmentation, and product-level performance using the UK e-commerce dataset. The goal is to provide valuable insights for decision-making around marketing and sales strategies.

**Tools Used:**  
- Power BI  
- Excel (for initial cleaning and calculations)  
- Power Query  
- DAX (Data Analysis Expressions)

 Dataset

**Source:** Kaggle – UK E-Commerce Dataset  
> Contains over 500,000 transactions from a UK-based online retailer between 2010 and 2011.

**Key Columns:**  
- InvoiceNo  
- StockCode  
- Description  
- Quantity  
- InvoiceDate  
- UnitPrice  
- CustomerID  
- Country

Report Pages

1. **O & G Trends**
- Sales by Country (Map Visual)
- Sales by Month and Year
- Total Sales KPI

 2. **Customer Behavior & Segmentation**
- Top-selling Products and Categories
- Monthly Sales Trends
- Quantity Sold by Product
- Year-based Sales Breakdown

 3. **Product & Time-Based Analysis**
- Orders per Customer
- Recency Calculation and Grouping
- Country-wise Performance Filter
- Customer Summary Table (Count, Sales, Recency)

 4. **Documentation Page**
- Project Summary
- Objectives
- KPIs Used
- Tools, Dataset Source, and Insights

* Key DAX Measures

```dax
LastPurchaseDate = 
CALCULATE(MAX(data[InvoiceDate]), ALLEXCEPT(data, data[CustomerID]))

Recency = 
DATEDIFF(data[LastPurchaseDate], TODAY(), DAY)

RecencyGroup = 
SWITCH(TRUE(),
    data[Recency] <= 30, "Active (0–30 Days)",
    data[Recency] <= 90, "Warm (31–90 Days)",
    "Inactive (90+ Days)"
)

Key Insights

. gb United Kingdom has the highest total sales.

. Peak months: January and November.

 . Top products: World War Posters, Jumbo Bags, Dotcom Postage.

 . 89% of customers are “Inactive” (Recency > 180 days) – opportunity for targeted re-engagement.

About Me
Madhuri Gubbala
Aspiring Data Analyst | Excel • Power BI • Python (in progress)
 madhurigubbala18@gmail.com
