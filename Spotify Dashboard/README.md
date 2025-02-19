# Spotify Dashboard 2024

## 📌 Project Overview

This project is a **Power BI Dashboard** that visualizes the most streamed **Spotify songs of 2024**. The dashboard includes **KPIs, slicers, bar charts, line charts, scatter plots, and categorical breakdowns** to provide insights into song popularity, artist influence, and streaming engagement across different platforms.

The dataset consists of multiple streaming metrics from **Spotify, YouTube, TikTok, SoundCloud, Deezer, and more**. The key focus of this dashboard is to analyze **song performance, artist ranking, and cross-platform engagement.**

## Dashboard Preview

Below is a snapshot of the interactive dashboard: ![Dashboard](https://github.com/CodeVistaPro/PowerBI_Projects/blob/main/Spotify%20Dashboard/Spotify%20Dashboard.png)


## 🛠️ **Project Workflow**

1. **Data Cleaning & Preparation (Power Query)**

   - Removed null values
   - Standardized column names
   - Ensured correct data types (e.g., converting text-based numbers to whole numbers for aggregations)

2. **Data Modeling & Measures (DAX in Power BI)**

   - Created calculated columns for better data categorization
   - Built **DAX measures** for KPIs & aggregations

3. **Dashboard Design**

   - KPI cards, filters, and interactive visuals were added for **better storytelling**
   - A clean, **high-contrast (black & neon green)** theme was applied for readability

4. **Final Enhancements**

   - Removed unnecessary slicers for a **minimalist and effective** user experience
   - Improved scatter plot readability by **reducing marker size, adding transparency & trend lines**

---

## 📊 **Dashboard Components**

### **1️⃣ KPI Cards**

These are **calculated DAX measures** to provide key summary insights:

#### **Total Songs**

```DAX
Total Songs = COUNT('Spotify Data'[Track])
```

#### **Total Spotify Streams**

```DAX
Total Spotify Streams = SUM('Spotify Data'[Spotify Streams])
```

#### **Average Spotify Popularity Score**

```DAX
Avg Popularity = AVERAGE('Spotify Data'[Spotify Popularity])
```

#### **Total YouTube Views**

```DAX
Total YouTube Views = SUM('Spotify Data'[YouTube Views])
```

#### **Explicit Songs Percentage**

```DAX
Explicit Percentage =
    DIVIDE(
        CALCULATE(COUNT('Spotify Data'[Explicit Track]), 'Spotify Data'[Explicit Track] = 1),
        COUNT('Spotify Data'[Track]),
        0
    ) * 100
```

---

### **2️⃣ Slicer - Release Year**

**Created a calculated column to extract Year from Release Date:**

```DAX
Release Year = YEAR('Spotify Data'[Release Date])
```

---

### **3️⃣ Visuals in Dashboard**

#### **🎵 Top 10 Songs by Streams (Bar Chart)**

- **X-axis:** Track
- **Y-axis:** Sum of Spotify Streams
- **Sorting:** Descending (Most streamed songs appear first)

#### **🎤 Top 10 Artists by Total Streams (Bar Chart)**

- **X-axis:** Artist
- **Y-axis:** Sum of Spotify Streams

#### **📊 Monthly Song Releases (Line Chart)**

- **X-axis:** Release Month
- **Y-axis:** Total number of songs released
- **Second Y-axis:** Distinct count of release years
- **Sorting Issue Fix:**

```DAX
Month Sort Order = SWITCH(
    'Spotify Data'[Month Name],
    "January", 1,
    "February", 2,
    "March", 3,
    "April", 4,
    "May", 5,
    "June", 6,
    "July", 7,
    "August", 8,
    "September", 9,
    "October", 10,
    "November", 11,
    "December", 12
)
```

- **Sort 'Month Name' by 'Month Sort Order'**

#### **📌 Rank Category Distribution (Bar Chart)**

- Shows how songs are classified by ranking (Extremely Popular, Moderately Popular, Least Popular)

#### **📌 Score Category Distribution (Bar Chart)**

- Displays how songs are categorized based on scoring criteria (Top 10%, Next 20%, Bottom 70%)

#### **📉 Spotify vs YouTube Engagement (Scatter Plot with Trend Line)**

- **X-axis:** Spotify Streams
- **Y-axis:** YouTube Views
- **Enhancements:**
  - **Marker transparency increased to 50%** for better visibility
  - **Trend line added using Power BI’s Analytics feature**

---

## 🔧 **Final Enhancements & Adjustments**

1. **Removed Extra Slicers**

   - Originally had filters for **Rank Category & Score Category**, but they were **not useful** since bar charts already displayed that info.
   - **Kept only 'Release Year' slicer** for better dashboard clarity.

2. **Improved Scatter Plot**

   - **Enabled trend line** to show correlation.
   - **Reduced marker size** for visibility.

3. **Overall Design Tweaks**

   - KPI cards text **left-aligned** for better readability.
   - Improved spacing between charts.

---

## 💾 **Files in Repository**

- `Spotify Dashboard.pbix` - Power BI dashboard file
- `Spotify Dataset.csv` - Source dataset
- `README.md` - Documentation (this file)
- `Spotify Dashboard.png` - Screenshot of final dashboard

---

## 🚀 **Conclusion**

This Power BI dashboard was built using **DAX calculations, interactive visuals, and refined design choices** to provide a **highly insightful, data-driven story** of **Spotify’s most streamed songs in 2024**.

It showcases **artist dominance, song popularity, and cross-platform streaming performance** in an **engaging and easy-to-navigate** format.

---

## 📌 **Next Steps (Future Enhancements)**

- Add **region-based filtering** to compare streams across different countries.
- Introduce **custom tooltips** to enhance user experience.
- Explore **ML-powered insights** (e.g., predicting song success using historical data).

---

###


