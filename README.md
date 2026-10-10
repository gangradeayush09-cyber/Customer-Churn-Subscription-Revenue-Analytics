# 📉 Customer Churn & Subscription Revenue Analytics Dashboard

An end-to-end data analytics and business intelligence project designed to analyze customer attrition, track Monthly Recurring Revenue (MRR), and identify key retention drivers for subscription-based business models.

Built using **SQL**, **Power Query**, **Power BI**, **DAX**, and **Generative AI**, this project delivers actionable strategies to reduce customer churn and maximize Customer Lifetime Value (CLV).

---

## 📌 Project Overview

Acquiring new customers is up to 5x more expensive than retaining existing ones. This project processes subscription datasets to analyze customer behavior, identify churn signals, evaluate revenue leakage, and segment user risk tiers.

### Key Objectives:
- **Revenue Performance Tracking:** Monitor Monthly Recurring Revenue (MRR), Average Revenue Per User (ARPU), and Net Revenue Retention (NRR).
- **Churn Driver Identification:** Analyze correlation between contract type, payment method, support tickets, and cancellation rates.
- **Customer Lifetime Value (CLV) Analysis:** Segment high-value customers and predict churn propensity to target proactive retention campaigns.

---

## 🛠️ Tech Stack & Tools

- **Data Querying & Processing:** SQL (Joins, CTEs, Window Functions), Advanced Excel, Power Query
- **Data Modeling & Visualization:** Power BI, Advanced DAX (Time Intelligence, Dynamic Measures)
- **AI Integration:** Generative AI for DAX optimization and automated executive summary generation
- **Dataset:** Subscription Customer Churn Dataset (10,000+ records)

---

## 📊 Key Metrics & DAX Measures Built

- **Total Active Subscribers:** `CALCULATE(COUNTROWS(Customer), Customer[Status] = "Active")`
- **Monthly Recurring Revenue (MRR):** `SUM(Subscriptions[Monthly_Fee])`
- **Customer Churn Rate %:** `DIVIDE([Churned Customers], [Total Customers], 0) * 100`
- **Average Revenue Per User (ARPU):** `DIVIDE([Total MRR], [Active Subscribers], 0)`
- **Customer Lifetime Value (CLV):** `[ARPU] * [Average Customer Lifespan]`

---

## 💡 Key Insights & Findings

1. **Contract Vulnerability:** Customers on **month-to-month contracts** exhibited a **42% churn rate**, compared to under 8% for annual plan subscribers.
2. **Support Ticket Signal:** Users logging **more than 3 support tickets** within 60 days had a 3x higher probability of canceling their subscriptions.
3. **Payment Method Risk:** Electronic check payments showed significantly higher payment failure and voluntary churn rates compared to automated credit card billing.

---

## 📁 Repository Structure

```text
├── Data/
│   └── Subscription_Churn_Data.csv
├── SQL/
│   └── Customer_Churn_Queries.sql
├── Dashboard/
│   └── Customer_Churn_Dashboard.pbix
├── .gitignore
└── README.md
# Power BI temporary files
*.pbix.lock
*.pbit.lock
*.tmp

# Microsoft Office temporary lock files
~$*.xlsx
~$*.xls
~$*.csv

# Operating System files
.DS_Store
Thumbs.db
desktop.ini

# Large files
*.zip
*.tar.gz
