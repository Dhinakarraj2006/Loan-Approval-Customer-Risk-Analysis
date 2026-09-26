# 🏦 Loan Approval & Customer Risk Analysis
> **An End-to-End Financial Data Analysis & Risk Assessment Project**

![Python](https://img.shields.io/badge/Python-3.x-blue?logo=python&logoColor=white)
![Pandas](https://img.shields.io/badge/Library-Pandas-150458?logo=pandas&logoColor=white)
![MySQL](https://img.shields.io/badge/Database-MySQL-4479A1?logo=mysql&logoColor=white)
![Power BI](https://img.shields.io/badge/BI-Power%20BI-F2C811?logo=powerbi&logoColor=black)
![Documentation](https://img.shields.io/badge/Report-10--Page%20PDF-red?logo=adobeacrobatreader&logoColor=white)
![Dataset](https://img.shields.io/badge/Dataset-52K%20Records-success)

---

## 📌 1. Project Metadata
* **Author:** Dhinakarraj S
* **Role:** Data Analyst
* **Domain:** Banking & Financial Services / Credit Risk Analytics
* **Tools & Technologies:** Python (Pandas), MySQL, Microsoft Power BI (DAX), WPS Office
* **Dataset Scale:** 52,000 Historical Loan Applications
* **Full Technical Documentation:** 📄 [Download / View 10-Page Master Case Study Report (PDF)](Loan_Approval_docs.pdf)

---

## 🎯 2. Project Objective & Business Problem
Financial lending institutions face the continuous challenge of expanding their loan portfolio while strictly managing credit risk and defaults. Manual underwriting often leads to operational bottlenecks, while rigid rule-based systems risk turning away creditworthy customers or approving hidden risks.

### Core Business Questions Addressed:
* **Risk Identification:** Which applicant parameters (Credit Score, Age, Income, Employment Status) act as true predictors for approval or rejection?
* **Portfolio Metrics:** What is the overall portfolio performance in terms of volume, approval rate, and average ticket size?
* **Demographic Patterns:** How do age brackets and credit tiers correlate with approval behavior?
* **Operational Parity:** Do factors like employment classification, existing loans, or outstanding debt significantly separate approvals from rejections?

---

## ⚙️ 3. Analytical Pipeline & Architecture

* **1. Data Ingestion & Hygiene (Python/Pandas):** Audited the 52,000 raw application dataset, validated schema data types, and confirmed zero null or duplicate records.
* **2. Relational Ingestion (SQLAlchemy/PyMySQL):** Programmatically exported and structured cleaned DataFrames into a production MySQL schema.
* **3. SQL Business Analytics (MySQL):** Formulated and solved 12 core business queries utilizing aggregations, window ranking (DENSE_RANK), and CTEs.
* **4. Interactive BI Intelligence (Power BI & DAX):** Designed an executive dark-themed analytics dashboard featuring customized DAX measures, dynamic KPI summaries, and automated risk color cues.
* **5. Strategic Framework & Technical Report:** Authored a comprehensive 10-page analytical report detailing methodology, SQL findings, and strategic underwriting recommendations.

---

## 📊 4. Interactive Power BI Dashboard
![Loan Approval Dashboard](loan_approval_dashboard.png)

### Dashboard KPI Summary:
* **Total Applications:** 52,000
* **Approved Loans:** 33,366 (64.17%)
* **Rejected Loans:** 18,634 (35.83%)
* **Average Loan Requested:** ₹21,102.70
* **Interactive Slicers:** Credit Score Tier, Age Group, City/Town, Education Level, Marital Status, Employment Status.

---

## 🔍 5. Key SQL & Analytical Insights

| Analysis Area | Key Metrics / Segmentation | Primary Finding |
| :--- | :--- | :--- |
| **Credit Score** | • Low (<600): **14.98% Approved** (85.02% Rejected)<br>• Medium (600–750): **85.37% Approved**<br>• High (>750): **84.80% Approved** | **Strongest Approval Gate:** Crossing the 600 mark increases approval rates by over **70%**. |
| **Age Demographic** | • 18–30 Years: **63.35% Approved**<br>• 31–50 Years: **72.58% Approved**<br>• Above 50 Years: **15.14% Approved** (84.86% Rejected) | Applicants over 50 face severe rejection rates due to conventional age thresholds. |
| **High-Approval Core Segment** | • **Criteria:** Credit Score $\ge$ 600 AND Age $\le$ 50<br>• **Volume:** 36,532 applications (**70.25% Portfolio Share**)<br>• **Approval Rate:** **84.99%** | The ideal target segment for automated, streamlined underwriting. |
| **Employment Parity** | • Self-Employed: **64.93%**<br>• Employed: **64.11%**<br>• Unemployed: **63.15%** | Employment category alone provides negligible predictive separation. |
| **Debt Exposure** | • Avg Debt (Approved): **₹14,965.69**<br>• Avg Debt (Rejected): **₹15,019.20** | Outstanding debt levels are practically identical across approval and rejection groups. |

---

## 💡 6. Strategic Business Recommendations
1. **Automated Fast-Track Workflows:** Formally deploy automated straight-through processing (STP) for the core low-risk segment (Credit Score $\ge$ 600 & Age $\le$ 50), which forms **70.25% of all applications**, drastically reducing acquisition costs.
2. **Alternative Underwriting for Low Credit (<600):** Instead of an 85% blanket rejection, evaluate cash flows, recurring utility payments, and collateral-backed credit options.
3. **Pensions & Wealth Evaluation for Mature Borrowers (>50):** Revise strict age-based rejections (84.86% rejection) by integrating post-retirement cash flows, assets, and fixed deposit holdings.
4. **Shift from Employment Titles to Repayment Capacity:** Focus on debt-to-income (DTI) and net disposable income rather than categorical labels (Employed vs Self-Employed).
## 📂 7. Repository Structure & Deliverables

- **Loan_Approval_docs.pdf** — 10-Page Master Technical Case Study & Documentation (WPS Office)
- **loan_approval.pbix** — Interactive Power BI Dashboard source file with DAX measures
- **loan_approval_dashboard.png** — High-resolution Executive Dashboard visual export
- **loan_approval_pandas.ipynb** — Python data cleaning, hygiene audit & MySQL ingestion pipeline
- **loan_approval_sql_analysis.ipynb** — 12 Business SQL queries & CTE/window implementations
- **cleaned_loan_approval.csv** — Preprocessed & validated dataset ready for analytics (52K records)
- **Loan Dataset.csv** — Original raw loan application source data

---
## 🛠️ 8. How to Replicate This Analysis

1. **Clone the Repository:**
[https://github.com/Dhinakarraj2006/Loan-Approval-Customer-Risk-Analysis.git](https://github.com/Dhinakarraj2006/Loan-Approval-Customer-Risk-Analysis.git)

2. **Clean Data & Ingest into Database:**  
Run `loan_approval_pandas.ipynb` to clean data and create the relational table in your local MySQL instance.

3. **Run SQL Queries:**  
Execute `loan_approval_sql_analysis.ipynb` to review the 12 business query implementations and results.

4. **Explore Interactive Dashboard:**  
Launch `loan_approval.pbix` in Microsoft Power BI Desktop to interact with the slicers and risk metrics.

5. **Review Master Documentation:**  
Open `Loan_Approval_docs.pdf` to read the complete 10-page analytical report.

---

