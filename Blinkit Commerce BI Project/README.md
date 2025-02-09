# Blinkit Commerce BI Project

This project represents a Power BI dashboard created for Blinkit, aimed at analyzing sales, item performance, outlet characteristics, and customer trends. The dashboard provides valuable insights into the grocery business's operational and sales metrics, empowering stakeholders to make informed decisions.

---

## Dashboard Preview

Below is a snapshot of the interactive dashboard: ![Banking Churn Dashboard](https://github.com/CodeVistaPro/PowerBI_Portfolio/blob/main/Blinkit%20Commerce%20BI%20Project/blinkit.png)

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

## Project Objective
The primary goal of this project was to build a visually compelling and interactive dashboard that helps Blinkit analyze:
- Total sales and average sales by outlet type, size, and location.
- Customer purchasing behavior and trends.
- Outlet establishment growth over time.
- Performance metrics such as item fat content, item visibility, and ratings.

---

## Data Used
The data used for this project is stored in the `BlinkIT Grocery Data.csv` file, which includes the following columns:
- **Sales**: Total sales amount.
- **Average Sales**: Average sales per transaction.
- **Number of Items**: Total number of items sold.
- **Average Rating**: Average customer rating.
- **Item Fat Content**: Categorized as Low Fat, Regular, etc.
- **Item Type**: Types of items (e.g., Fruits and Vegetables, Dairy, etc.).
- **Item Visibility**: Visibility score of items in the store.
- **Outlet Establishment Year**: Year when the outlet was established.
- **Outlet Location Type**: Location type of outlets (e.g., Tier 1, Tier 2, Tier 3).
- **Outlet Size**: Size of the outlet (Small, Medium, High).
- **Outlet Type**: Outlet type (Grocery Store, Supermarket).
- **Total Sales**: Aggregate sales for each category.

---

## Dashboard Features
The dashboard has the following key components:

### Key Performance Indicators (KPIs):
- **Total Sales**: $1.20M
- **Number of Items**: 8,523
- **Average Sales**: $141
- **Average Rating**: 4

### Tabs for Metric Exploration:
- Total Sales
- Average Sales
- Number of Items
- Average Rating

### Insights at a Glance:
- **Item Type Contribution**: Distribution of sales across various item types.
- **Outlet Performance**: Analysis of total sales, number of items, and ratings by outlet type and size.
- **Location Performance**: Contribution of Tier 1, Tier 2, and Tier 3 locations to overall sales.
- **Fat Content Analysis**: Comparison of sales by low fat and regular fat items.

---

## Key Metrics
### Metrics Table:
A calculated table was created to organize and consolidate key metrics:
1. **Total Sales**
2. **Average Sales**
3. **Number of Items**
4. **Average Rating**

### Calculated Columns and Measures:
- **Sum of Sales**: Aggregates the total sales.
- **Average of Sales**: Computes the average sales per transaction.
- **Number of Items Sold**: Counts the total number of items sold.
- **Rating**: Average customer rating per outlet.

---

## Visualizations
### 1. **KPIs Section**:
- A card visual displays the four key performance indicators.

### 2. **Outlet Establishment Timeline**:
- Line chart showing the growth of outlet establishments over the years.

### 3. **Sales by Item Type**:
- Bar chart displaying total sales for each item type.
- Categories include Fruits, Snack Foods, Household, Frozen Foods, etc.

### 4. **Fat Content Contribution**:
- Donut chart showing the proportion of sales contributed by Low Fat and Regular items.

### 5. **Sales by Outlet Size**:
- Donut chart representing sales by Small, Medium, and High-sized outlets.

### 6. **Sales by Outlet Location**:
- 100% stacked bar chart showing sales distribution across Tier 1, Tier 2, and Tier 3 locations.

### 7. **Outlet Type Performance**:
- A table visual with conditional formatting showing:
  - Total Sales
  - Number of Items Sold
  - Average Sales
  - Average Rating
  - Item Visibility

---

## Filters and Interactivity
### Filters:
The dashboard provides dropdown filters for:
- **Outlet Location Type**: Select Tier 1, Tier 2, Tier 3, or All.
- **Outlet Size**: Small, Medium, High, or All.
- **Item Type**: Fruits, Snack Foods, Household, etc.

### Interactivity:
- Cross-filtering across visuals for real-time analysis.
- Dynamic switching between metrics (Total Sales, Average Sales, Number of Items, Average Rating).

---

## Data Modeling
### Simple Table:
- Since the dataset is compact and straightforward, data modeling involved using a single flat table named `BlinkIT Grocery Data`.
- Calculated columns and measures were used to enhance analysis.

---

## Technologies Used
- **Power BI**: For dashboard creation and interactivity.
- **DAX (Data Analysis Expressions)**: For creating calculated columns and measures.
- **Excel/CSV**: For storing and processing the input dataset.

---

## Business Outcomes
The Blinkit Commerce BI Dashboard provides the following actionable insights:
1. **High-Performing Item Categories**:
   - Fruits and Vegetables, Snack Foods, and Household items drive the highest sales.

2. **Outlet Size Efficiency**:
   - Medium-sized outlets generate the highest sales compared to Small and High-sized outlets.

3. **Location Trends**:
   - Tier 3 locations contribute the most to total sales, highlighting a strong customer base in less urbanized areas.

4. **Customer Preferences**:
   - Regular-fat items outperform low-fat items in terms of sales.

5. **Outlet Type Analysis**:
   - Supermarket Type 1 dominates sales and item count, while Grocery Stores have the lowest visibility.

---




