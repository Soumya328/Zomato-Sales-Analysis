📊 Zomato Sales Analysis 

This project presents a complete end-to-end analysis of Zomato’s sales and customer behavior using SQL, Excel, and Power BI.
It demonstrates strong skills in data cleaning, business analytics, data modeling, and visual dashboard creation.

📝 Project Summary

The objective of this project is to analyze Zomato’s sales data to uncover meaningful business insights.
Through this analysis, we identify high-value customers, fast-growing food categories, revenue trends, restaurant performance, and overall sales patterns.
The final output of the project is an interactive dashboard that summarises all major KPIs and business insights.

🎯 Key Objectives

Analyze customer purchase patterns

Identify top customers and high-value orders

Evaluate restaurant-level performance

Understand category-wise sales contribution

Analyze monthly and daily revenue trends

Build a KPI-driven interactive dashboard

Generate actionable business insights

🛠️ Tools & Technologies
Tool	Purpose
SQL	Data extraction, cleaning, and analysis
Excel	Data preprocessing and trend analysis
Power BI / Excel Dashboard	Interactive dashboard creation
Data Modeling	Building relationships between tables
📂 Dataset Details

The dataset consists of three major tables:

1. Customers

customer_id

customer_name

location

2. Orders

order_id

customer_id

restaurant_id

order_date

amount

3. Restaurants

restaurant_id

restaurant_name

category

📊 Measures & KPIs

The analysis focuses on the following KPIs:

Total Sales

Total Orders

Average Order Value (AOV)

Top 5 Customers

Top Restaurants by Revenue

Category-Wise Contribution

Monthly Revenue Trend

Daily Order Trend

🧮 Key SQL Queries Used
1. Top 3 Customers by Total Orders
SELECT 
    c.customer_id,
    c.customer_name,
    COUNT(o.order_id) AS total_orders
FROM order_detail o
JOIN customer c ON o.customer_id = c.customer_id
GROUP BY c.customer_id, c.customer_name
ORDER BY total_orders DESC
LIMIT 3;

2. Restaurant-wise Revenue Analysis
SELECT 
    r.restaurant_name,
    SUM(o.amount) AS total_revenue
FROM order_detail o
JOIN restaurant r ON o.restaurant_id = r.restaurant_id
GROUP BY r.restaurant_name
ORDER BY total_revenue DESC;

3. Monthly Sales Trend
SELECT 
    DATE_FORMAT(order_date, '%Y-%m') AS month,
    SUM(amount) AS monthly_sales
FROM order_detail
GROUP BY month
ORDER BY month;

📈 Dashboard Overview

The dashboard includes:

Regional performance

Total sales and revenue trends

Daily & monthly order analysis

Best-performing restaurants

Category-wise contribution

Customer segmentation

👉 Add your dashboard screenshot here:

![Zomato Dashboard](dashboard.png)

🧠 Business Insights

Fast Food category contributes the highest percentage of total sales.

Peak order time observed during evening hours.

Top 5 restaurants generate a significant share of revenue.

Customer loyalty increases overall business stability.

Weekend orders show a visible rise in volume.

