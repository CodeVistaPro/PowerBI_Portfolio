# E-Commerce Sales Analysis

## Project Overview
The E-Commerce Sales Analysis project leverages Power BI to provide an interactive and visually engaging dashboard that delves into the performance of an e-commerce platform. The dashboard offers insights into total sales, product performance, customer reviews, and pricing trends to help businesses make data-driven decisions and optimize their strategies.

---

## Key Features of the Dashboard

### 1. **Key Performance Indicators (KPIs)**
   - **Total Products**: `12K`
   - **Total Sales**: `6M`
   - **Average Review Score**: `3.03`

   These KPIs give a high-level summary of the platform's performance, including the number of products available, total revenue generated, and the average customer satisfaction rating.

### 2. **Visual Components**
   
   #### a. **Review by Category (Pie Chart)**
   - Shows the distribution of reviews across different categories (e.g., Sports, Books, Toys).
   - Key Insight: Categories such as Books and Toys receive the highest reviews, indicating customer interest in these segments.

   #### b. **Sales by Category (Bar Chart)**
   - Highlights total sales for each product category.
   - Key Insight: Books dominate with the highest sales, followed by Toys and Electronics.

   #### c. **Monthly Sales Trend (Line Chart)**
   - Displays the trend of monthly sales over the year.
   - Key Insight: Sales peak in February and gradually decline toward May.

   #### d. **Count of Reviews by Category (Bar Chart)**
   - Compares the number of reviews received by each category.
   - Key Insight: Books, Sports, and Toys lead in the number of reviews, showcasing customer engagement in these categories.

   #### e. **Average Price by Category (Bar Chart)**
   - Illustrates the average price of products in each category.
   - Key Insight: Health-related products have the highest average price, followed by Sports and Toys.

---

## Dataset Description
The dataset, `ecommerce_sales_analysis.csv`, contains the following key columns:

- **category**: Product categories such as Books, Sports, Toys, etc.
- **Month**: Numerical representation of the month.
- **Month Name**: Name of the month.
- **Monthly_sales**: Total sales for each month.
- **price**: Individual product prices.
- **product_id**: Unique identifier for each product.
- **product_name**: Names of the products.
- **review_count**: Number of reviews per product.
- **review_score**: Average review score.
- **Total Products**: Total number of products available.
- **Total Revenue**: Total revenue generated.
- **Total Sales**: Aggregate sales figures.

---

## Data Modeling
This project uses a single flat table for simplicity. Calculated columns and measures are created using **DAX** to enrich analysis.

### Key Measures:
1. **Total Products**: Count of unique products in the dataset.
2. **Total Revenue**: Sum of sales across all categories.
3. **Average Review Score**: Average of review scores for each product category.
4. **Monthly Sales Trend**: Aggregated sales per month.
5. **Category-Wise Sales**: Total sales by category.

---

## Business Insights
The dashboard reveals critical insights that can drive business decisions:

1. **Focus on High-Performing Categories**
   - Books and Toys contribute the most to sales and reviews.
   - Strategy: Increase inventory and marketing spend on these categories to capture more sales.
   - Expected Impact: **15-20% increase** in sales for these categories.

2. **Seasonal Trends**
   - Sales drop toward the mid-year months.
   - Strategy: Launch promotional campaigns or discounts in April and May to stabilize sales.
   - Expected Impact: **30-35% improvement** in sales during low-performing months.

3. **Optimize Pricing Strategies**
   - Categories like Health and Sports have higher average prices, indicating premium potential.
   - Strategy: Bundle high-priced items with lower-priced complementary products.
   - Expected Impact: **10-15% uplift** in revenue per transaction.

4. **Improve Review Engagement**
   - Books and Sports receive the highest reviews, but categories like Home & Kitchen have lower engagement.
   - Strategy: Offer incentives (e.g., discounts, reward points) for customers to leave reviews.
   - Expected Impact: **20% increase** in review count for underperforming categories.

5. **Drive Product Awareness**
   - Low-performing categories such as Home & Kitchen and Clothing require better visibility.
   - Strategy: Promote these categories through homepage features and email campaigns.
   - Expected Impact: **15% growth** in sales for these categories.

---

## Why This Dashboard Stands Out
1. **Interactive Visuals**: Users can explore data through dynamic filters, such as:
   - Category
   - Month
   - Price Range

2. **Actionable Insights**: The dashboard highlights areas of improvement and opportunities to maximize sales.

3. **Simplicity Meets Depth**: A single dataset and well-structured visuals provide a balance of simplicity and comprehensive analysis.

---


---



