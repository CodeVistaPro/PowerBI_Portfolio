# 📊 Credit Risk Assessment Dashboard 

## 📌 **Project Overview**

This Power BI dashboard is designed to assess **credit risk** by analyzing key financial indicators such as loan amounts, default rates, interest rates, and borrower characteristics. It helps businesses make **data-driven lending decisions** by identifying **risk factors** and **patterns** among different borrower segments.

---

## 📷 **Dashboard Preview**
Below is a snapshot of the interactive dashboard: ![Dashboard](https://github.com/CodeVistaPro/PowerBI_Projects/blob/main/Credit%20Risk%20Assessment/Credit%20Risk%20Assessment.png)


---

## 🔍 **Key Insights from the Dashboard**

1️⃣ **Credit Risk Score:** A gauge chart to evaluate the overall **creditworthiness of borrowers**.

2️⃣ **Loan Status Distribution:** A stacked bar chart displaying **default rates by loan grade**.

3️⃣ **Loan Amount Distribution:** Analyzes the **loan amount ranges** and their respective volume.

4️⃣ **Age Group Distribution:** Visualizes how different age groups contribute to the **total loan amount**.

5️⃣ **Credit History Distribution:** A pie chart showing borrower credit history categories.

6️⃣ **Home Ownership Impact:** Examines if homeownership affects **borrowing behavior and default risk**.


7️⃣ **Loan Intent Analysis:** A donut chart categorizing loans based on their **intended purpose**.

---

## 📌 **Data Fields Used**

### 🏦 **Loan & Borrower Details**

- `person_age` - Age of the borrower.
- `person_income` - Annual income.
- `person_home_ownership` - Homeownership status.
- `person_emp_length` - Employment length in years.

### 📊 **Loan Information**

- `loan_intent` - Purpose of the loan.
- `loan_grade` - Loan quality rating.
- `loan_amnt` - Loan amount.
- `loan_int_rate` - Interest rate applied.
- `loan_status` - Loan repayment status (Default/Non-default).
- `loan_percent_income` - Percentage of income allocated for the loan.
- `cb_person_default_on_file` - Any history of past loan defaults.
- `cb_person_cred_hist_length` - Length of credit history in years.

---

## 🛠 **Custom Columns & Measures Created**

### 📌 **Power Query (M Language) - Custom Columns**

#### 1️⃣ **Age Group Categorization**

```M
Age_group =
  if [person_age] >= 20 and [person_age] < 30 then "20-30"
  else if [person_age] >= 30 and [person_age] < 40 then "30-40"
  else if [person_age] >= 40 and [person_age] < 50 then "40-50"
  else if [person_age] >= 50 and [person_age] < 60 then "50-60"
  else if [person_age] >= 60 and [person_age] < 70 then "60-70"
  else if [person_age] >= 70 and [person_age] < 80 then "70-80"
  else if [person_age] >= 80 then "80+"
  else "Unknown"
```

#### 2️⃣ **Loan Amount Ranges**

```M
Loan_Amount_Range =
  if [loan_amnt] >= 500 and [loan_amnt] < 5000 then "500-5K"
  else if [loan_amnt] >= 5000 and [loan_amnt] < 10000 then "5K-10K"
  else if [loan_amnt] >= 10000 and [loan_amnt] < 15000 then "10K-15K"
  else if [loan_amnt] >= 15000 and [loan_amnt] < 20000 then "15K-20K"
  else if [loan_amnt] >= 20000 and [loan_amnt] < 25000 then "20K-25K"
  else if [loan_amnt] >= 25000 and [loan_amnt] < 30000 then "25K-30K"
  else if [loan_amnt] >= 30000 then "30K+"
  else "Unknown"
```

#### 3️⃣ **Credit History Length Ranges**

```M
Credit_History_Range =
  if [cb_person_cred_hist_length] >= 2 and [cb_person_cred_hist_length] < 5 then "2-5 Years"
  else if [cb_person_cred_hist_length] >= 5 and [cb_person_cred_hist_length] < 10 then "5-10 Years"
  else if [cb_person_cred_hist_length] >= 10 and [cb_person_cred_hist_length] < 15 then "10-15 Years"
  else if [cb_person_cred_hist_length] >= 15 and [cb_person_cred_hist_length] < 20 then "15-20 Years"
  else if [cb_person_cred_hist_length] >= 20 and [cb_person_cred_hist_length] < 25 then "20-25 Years"
  else if [cb_person_cred_hist_length] >= 25 then "25+ Years"
  else "Unknown"
```

---

### 📌 **DAX Measures**

#### 1️⃣ **Total Loan Amount**

```DAX
Total Amount = SUM(credit_risk[loan_amnt])
```

#### 2️⃣ **Average Loan Interest Rate (%)**

```DAX
Avg Interest Rate = FORMAT(AVERAGE(credit_risk[loan_int_rate]), "0%")
```

#### 3️⃣ **Default Rate (%)**

```DAX
Default Rate = FORMAT(DIVIDE(
    COUNTROWS(FILTER(credit_risk, credit_risk[loan_status] = 1)),
    COUNTROWS(credit_risk),
    0
), "0%")
```

#### 4️⃣ **Loan-to-Income Ratio**

```DAX
Loan to Income Ratio = AVERAGE(credit_risk[loan_percent_income]) * 100
```

#### 5️⃣ **Credit Risk Score (Gauge Chart)**

```DAX
Credit Risk Score = AVERAGE(credit_risk[loan_status]) * 100
```

---

## 📌 **How This Dashboard Helps in Decision-Making**

✅ **Identifies High-Risk Borrowers** based on **loan status, credit history, and employment length**.

✅ **Helps Financial Institutions** optimize their **loan approval strategy**.

✅ **Reveals Default Trends** based on **loan grade, amount, and intent**.

✅ **Provides Actionable Insights** to reduce risk and maximize returns.

---

## 📂 **Project Files & Resources**

📊 **Power BI Report:** `Credit_Risk_Assessment.pbix`\
📑 **Dataset Used:** `credit_risk.csv`\
📷 **Dashboard Image:** `Credit_Risk_Assessment.png`

---

## 🎯 **Final Thoughts**

This **Credit Risk Dashboard** is a powerful tool for **banks, lenders, and financial analysts** to assess loan risk and make **data-driven lending decisions**. 🚀📊


