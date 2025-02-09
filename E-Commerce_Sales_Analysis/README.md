# E-Commerce Sales Analysis

## Project Overview
The E-Commerce Sales Analysis project leverages Power BI to provide an interactive and visually engaging dashboard that delves into the performance of an e-commerce platform. The dashboard offers insights into total sales, product performance, customer reviews, and pricing trends to help businesses make data-driven decisions and optimize their strategies.

## Dashboard Preview

Below is a snapshot of the interactive dashboard: ![Banking Churn Dashboard](https://github.com/CodeVistaPro/PowerBI_Portfolio/blob/main/E-Commerce_Sales_Analysis/ecommerce.png)

---

## Table of Contents
1. [Project Objective](#project-objective)
2. [Data Used](#data-used)
3. [Dashboard Features](#dashboard-features)
4. [Key Metrics](#key-metrics)
5. [Visualizations](#visualizations)
6. [Filters and Interactivity](#filters-and-interactivity)
7. [Data Modeling](#data-modeling)
8. [Technologies Used](#technologies-used)
9. [Business Outcomes](#business-outcomes)

---

---

## Data Used
The dataset used for this analysis contains the following columns:
- **category**: Product categories such as Books, Sports, Health, etc.
- **Month**: The month in which sales were recorded.
- **Monthly_sales**: Total sales for the month.
- **price**: Price of individual products.
- **review_count**: Total number of customer reviews.
- **review_score**: Average score of customer reviews.
- **product_id**: Unique identifier for each product.
- **product_name**: Name of the product.
- **Total Products**: Aggregate count of products sold.
- **Total Revenue**: Revenue generated from sales.
- **Total Sales**: Total sales value for each product category.

---

## Dashboard Features
The dashboard comprises:

### **Key Performance Indicators (KPIs):**
- **Total Products**: 12,000 products analyzed.
- **Total Sales**: $6M in total sales.
- **Average Review Score**: 3.03.

### **Category and Sales Insights:**
- Breakdown of sales by product category.
- Monthly sales trends.
- Customer reviews and their relationship with sales.
- Average product prices by category.

---

## Key Metrics

### Metrics Table:
- **Total Sales**: Aggregate sales for each product category.
- **Monthly Sales**: Sum of sales for each month.
- **Average Review Score**: Mean review score for each product.
- **Review Count by Category**: Sum of customer reviews by product category.

### Calculated Measures:
- **Sum of Sales**: `SUM(Total Sales)`
- **Average of Sales**: `AVERAGE(price)`
- **Number of Products Sold**: `COUNT(product_id)`
- **Review Scores**: `AVERAGE(review_score)`

---

## Visualizations

### **1. KPI Section**
- Displays overall sales, product count, and average review score.

### **2. Monthly Sales Trend**
- A line chart showcasing monthly sales trends.

### **3. Review by Category**
- A pie chart representing the distribution of reviews across categories.

### **4. Count of Reviews by Category**
- A bar chart highlighting review counts by category.

### **5. Sales by Category**
- A bar chart comparing total sales for each category.

### **6. Average Price by Category**
- A bar chart showing the average price of products across categories.

---

## Filters and Interactivity

### Filters:
- **Category**: Select specific product categories to analyze.
- **Month**: Focus on sales trends for specific months.
- **Review Score**: Filter products by their review score.

### Interactivity:
- Cross-filtering across visuals for real-time updates.
- Dynamic visuals to switch between metrics such as sales, reviews, and pricing.

---

## Data Modeling
The dashboard relies on a flat table structure, with calculated measures and columns to support analysis. Since the dataset is straightforward, no complex star or snowflake schemas were required.

---

## Technologies Used
- **Power BI**: For data visualization and dashboard creation.
- **DAX (Data Analysis Expressions)**: To create measures and calculated columns.
- **CSV/Excel**: For data storage and preparation.

---

## Business Outcomes

### **1. Sales by Category**
- Books generate the highest revenue, followed by Toys and Electronics.
- Optimizing inventory for high-performing categories can boost revenue by **15%**.

### **2. Monthly Trends**
- Sales peak in October and February, highlighting the need for promotional campaigns during these months.
- Strategic marketing can improve sales by **20%** during these periods.

### **3. Review Insights**
- Average review score is **3.03**, suggesting room for improvement in customer satisfaction.
- Addressing low-rated products could enhance reviews and increase sales by **10%**.

### **4. Pricing Strategy**
- Books and Health categories have the highest average prices, which are well-accepted by customers.
- Competitive pricing in other categories could increase sales by **10-15%**.

### **5. Customer Engagement**
- Products in the Sports category receive the highest review counts, indicating strong customer interest.
- Leveraging customer feedback can drive better engagement and satisfaction.

---






