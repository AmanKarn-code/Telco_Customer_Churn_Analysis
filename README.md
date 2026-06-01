# Telecom Customer Churn & Revenue Risk Analysis

## 📌 Project Overview
This project delivers an end-to-end data analytics solution designed to identify operational friction points, segment customer attrition risk, and quantify financial leakages for a telecom enterprise. 

By employing a hybrid architecture—using **Python (Pandas)** for automated data hygiene and exploratory diagnostics, alongside **Power BI** for advanced star-schema data modeling and interactive visualization—this analysis uncovers actionable strategies to mitigate a **26.58% corporate churn rate**.

---

## 🛠️ Tech Stack & Architecture
* **Data Wrangling & Engineering:** Python 3.x, Pandas, NumPy
* **Data Modeling & Analytics:** Power BI Desktop, Power Query, DAX (Data Analysis Expressions)
* **Development Environment:** Jupyter Notebook (`.ipynb`), VS Code
* **Data Source:** Telco Customer Attrition Dataset (7,043 customer endpoints)

---

## ⚙️ Data Engineering & Pipeline Execution (`.ipynb`)
Before building executive dashboards, the raw data was audited and transformed within a Jupyter Notebook to ensure full production-grade accuracy:

1. **Type Rectification & Data Coercion:** Handled a critical data anomaly where the `TotalCharges` column contained hidden empty spaces (`' '`), forcing it to load as a string. Used `pd.to_numeric(..., errors='coerce')` to seamlessly convert and isolate missing values.
2. **Missing Value Management:** Identified and dropped records with null values in `TotalCharges` (representing new accounts with 0 months of tenure) to prevent statistical skewing.
3. **Feature Engineering:** Programmatically injected a binary matrix (`Churn_Binary`) to convert categorical attributes into mathematical metrics for precise group aggregations and average lifecycle trends.

---

## 📊 Executive Dashboard Architecture (Power BI)
The refined dataset was integrated into Power BI using a structured reporting layout optimized for business leaders. 

### 🔍 Key Metrics Captured:
* **Total Baseline Customers:** 7,032
* **Corporate Churn Rate:** 26.58% (1,869 Lost Accounts)
* **Direct Financial Impact:** ₹139K in immediate revenue leakage

<img width="1330" height="742" alt="Screenshot 2026-06-01 104455" src="https://github.com/user-attachments/assets/1f526980-0ab7-4674-bc19-1ab03347f851" />


---

## 📈 Strategic Business Insights & Analytical Breakdown

* **The Onboarding Vulnerability (Tenure Slicing):** Attrition is heavily aggressive in the initial customer lifecycle. Accounts in the **0–6 month tenure range exhibit a massive 53% churn rate**. This risk stabilizes sharply to 17% once a customer crosses the 12-month retention threshold.
* **The Contract Trap:** Rigid commercial structures heavily dictate customer loyalty. **Month-to-month contracts** are the primary operational failure point, driving **1,655 out of the total 1,869 churned cases**. Conversely, one-year (166) and two-year (48) commitments remain highly secure.
* **Payment Processing Friction:** Payment infrastructure strongly correlates with transactional drop-offs. **Electronic Checks** represent the highest risk vector, dominating the churn landscape across both male and female demographics with identical distribution trends.

---

## 💡 Commercial Recommendations
1. **Optimize Onboarding Strategy:** Deploy proactive engagement programs and loyalty milestones targeted explicitly at the high-risk 0–6 month subscriber cohort to recover original Customer Acquisition Costs (CAC).
2. **Incentivize Contract Migration:** Offer short-term subscription discounts or feature unlocks to migrate vulnerable month-to-month subscribers onto stable, longer-term annual contracts.
3. **Promote Automated Billing:** Implement payment-portal interventions pushing electronic check users toward automated banking channels (Credit Cards or Direct Bank Transfers), which statistically correlate with long-term retention.
