# **Marketing Campaign Analysis**

## **📌 Project Overview**

This Power BI dashboard provides a comprehensive analysis of a **marketing campaign dataset**, helping businesses understand **customer behavior, revenue trends, and campaign effectiveness**. It enables data-driven decision-making by visualizing key performance indicators (KPIs), segmentation insights, and purchase patterns.


## Dashboard Preview

Below is a snapshot of the interactive dashboard: ![Dashboard](https://github.com/CodeVistaPro/PowerBI_Projects/blob/main/Marketing%20Campaign%20Analysis/Marketing%20Campaign%20Analysis.png)

---

## **📊 Dataset Description**

The dataset contains customer details, income, spending behavior, campaign engagement, and purchasing channels. Additionally, extra tables were created to structure and optimize analysis.

### \*\*Main Data Table: \*\***`market`**

- **Customer Demographics:** `ID`, `Year_Birth`, `Education`, `Marital_Status`, `Income`, `Income_range`
- **Customer Interaction:** `Kidhome`, `Teenhome`, `Dt_Customer`, `Recency`
- **Product Spending:** `Wines_amnt`, `Fruits_amnt`, `MeatProducts_amnt`, `FishProducts_amnt`, `SweetProducts_amnt`, `GoldProds_amnt`
- **Purchasing Behavior:** `NumDealsPurchases`, `NumWebPurchases`, `NumCatalogPurchases`, `NumStorePurchases`, `NumWebVisitsMonth`
- **Campaign Engagement:** `AcceptedCmp1` to `AcceptedCmp5`, `Response`, `Response Rate`
- **Retention & Complaints:** `Retention Rate`, `Complain`

### **Additional Tables Created**

1. **`UnpivotedData`** - Created by unpivoting product columns to analyze revenue per category:

   - **Columns:** `Product Category`, `Total Revenue`

2. **`Campaign`** - Summarizes campaign effectiveness:

   - **Columns:** `Campaign Category`, `Total Customers`

3. **`Channels`** - Provides insights into purchasing channels:

   - **Columns:** `Channel Category`, `Total Revenue`

## **📈 Dashboard Components & Insights**

### **🔹 KPI Cards**

- **Total Customers:** `2240`
- **Total Revenue:** `$1M`
- **Retention Rate:** `15%`
- **Avg Customer Spending:** `$606`

### **🔹 Revenue by Product Category (Bar Chart)**

- **Wines & Meat Products** generate the highest revenue.
- **Fruits & Sweet Products** underperform.

### **🔹 Customers by Income Range (Bar Chart)**

- Most customers fall within the **30K-80K** income range.
- **Higher-income (>100K) customers are fewer**.

### **🔹 Response Rate & Total Revenue by Income (Scatter Plot)**

- **Higher income customers respond more to campaigns.**
- **Best response & spending from 60K-100K income groups.**

### **🔹 Campaign Effectiveness (Bar Chart)**

- **Campaign 4 & 3 performed best.**
- **Campaign 2 was least effective.**

### **🔹 Top Channels for Purchases (Donut Chart)**

- **Web & Catalog purchases dominate.**
- **Store sales are lower.**

### **🔹 Revenue by Enrollment Year (Donut Chart)**

- **Older customers (2012) contribute the most revenue.**
- **Newer customers (2014) need better retention strategies.**

## **📌 DAX Measures Used**

### **🔹 Total Revenue Calculation**

```DAX
Total Revenue = SUM( market[Wines_amnt] ) + SUM( market[Fruits_amnt] ) +
                SUM( market[MeatProducts_amnt] ) + SUM( market[FishProducts_amnt] ) +
                SUM( market[SweetProducts_amnt] ) + SUM( market[GoldProds_amnt] )
```

👉 **Purpose:** Aggregates total revenue from all product categories.

### **🔹 Customer Retention Rate**

```DAX
Customer Retention Rate = DIVIDE( COUNTROWS(FILTER( market, market[Response] = 1 )), COUNTROWS(market), 0 )
```

👉 **Purpose:** Measures campaign engagement and retention.

### **🔹 Average Customer Spending**

```DAX
Avg Customer Spend = FORMAT(DIVIDE( [Total Revenue], COUNTROWS(market), 0 ), "$#,##0.00")
```

👉 **Purpose:** Calculates per-customer revenue contribution.

### **🔹 Income Range Categorization (Power Query M Language)**

```M
if [Income] >= 0 and [Income] < 10000 then "0-10K"
else if [Income] >= 10000 and [Income] < 20000 then "10K-20K"
else if [Income] >= 20000 and [Income] < 30000 then "20K-30K"
else if [Income] >= 30000 and [Income] < 40000 then "30K-40K"
else if [Income] >= 40000 and [Income] < 50000 then "40K-50K"
else if [Income] >= 50000 and [Income] < 60000 then "50K-60K"
else if [Income] >= 60000 and [Income] < 70000 then "60K-70K"
else if [Income] >= 70000 and [Income] < 80000 then "70K-80K"
else if [Income] >= 80000 and [Income] < 90000 then "80K-90K"
else if [Income] >= 90000 and [Income] < 100000 then "90K-100K"
else "100K+"
```

👉 **Purpose:** Groups customers into income brackets for better segmentation.

## **🚀 Conclusion**

- **Better Customer Targeting:** Income-based segmentation helps focus on high-value customers.
- **Optimized Marketing Strategies:** Campaign insights ensure future marketing is data-driven.
- **Revenue Maximization:** High-performing products and channels guide better business decisions.
- **Customer Retention Focus:** Older customers generate high revenue, indicating loyalty programs are crucial.

✔ **Better Customer Targeting:** Income-based segmentation helps focus on high-value customers.
✔ **Optimized Marketing Strategies:** Campaign insights ensure future marketing is data-driven.
✔ **Revenue Maximization:** High-performing products and channels guide better business decisions.
✔ **Customer Retention Focus:** Older customers generate high revenue, indicating loyalty programs are crucial.

**This dashboard provides actionable insights for data-driven decision-making and revenue growth.** 📊🔥


