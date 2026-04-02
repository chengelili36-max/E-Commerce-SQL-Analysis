# 🛒 E-Commerce User Growth & Retention SQL Analysis

## 📝 Project Overview
In the e-commerce sector, understanding user retention and the repurchase cycle is critical for driving Customer Lifetime Value (LTV). This project utilizes advanced SQL to analyze a real-world dataset of 100,000+ orders from **Olist**, Brazil's largest department store marketplace. 

The goal of this analysis is to bypass standard BI tools and rely purely on raw SQL scripting to uncover behavioral patterns of repeat customers, providing data-driven recommendations for the CRM and Marketing teams.

## 🛠️ Tech Stack & SQL Techniques
* **Database Environment:** SQLite (Relational Database)
* **Core SQL Skills Demonstrated:**
  * **Common Table Expressions (CTEs):** Used for logical query structuring and step-by-step data aggregation.
  * **Window Functions:** Utilized `LAG()`, `OVER()`, and `PARTITION BY` to calculate time intervals between consecutive user actions.
  * **Date/Time Functions:** Utilized `strftime` and `julianday` for cohort and time-series analysis.
  * **Complex Joins & Aggregation:** Multi-table `JOIN`s and conditional logic (`CASE WHEN`) to calculate precise business metrics.

## 💡 Key Business Insights

### 1. User Retention Analysis (Cohort Churn)
* **Finding:** The platform's monthly repeat purchase rate remains low, averaging around **3.2%** during peak operational months. 
* **Business Implication:** This indicates that Olist operates primarily as a one-off transaction platform rather than a high-stickiness destination. Strategic focus should pivot from expensive "loyalty building" to "maximizing first-order Average Order Value (AOV)" and optimizing acquisition costs.

### 2. Repurchase Cycle (Time Between Orders)
* **Finding:** Through `LAG()` window function analysis, the average time between consecutive orders for repeat customers is exactly **79.2 days**.
* **Business Implication:** This directly informs the CRM team's trigger-based marketing efforts. Instead of wasting budget on immediate post-purchase retargeting, discount coupons or targeted email campaigns should be deployed around **Day 65 to Day 75** to intercept users just before their natural repurchase window.

## 📂 Repository Structure SQL script for calculating Monthly Active Users (MAU) and repeat purchase rates.
* `02_repurchase_intervals.sql`: SQL script for calculating Monthly Active Users (MAU) and repeat purchase rates and SQL script utilizing Window Functions to calculate the average days between orders.
* `monthly_retention.csv`: Query results for retention metrics.
* `repurchase_intervals.csv`: Query results for the 79.2-day interval calculation.

---
*Created by Chenge Li | Data Analyst*
