# Bank Customer Churn & Sales Analysis

## Project Overview:

### Introduction:
Power BI is a powerful business intelligence tool that enables interactive data visualization and insightful reporting. This project focuses on analyzing bank customer data across two key dimensions: **customer profiling and sales performance**, and **churn risk and financial analysis**. The goal is to uncover behavioral patterns, identify at-risk customer segments, and support data-driven decision-making.

The dataset contains 100,000 customer records sourced from a CSV file, covering demographics, financial behavior, product usage, and churn status across multiple geographies.

## Key Highlights:

##### Data Source & Model
A single CSV dataset of 100,000 bank customers was loaded into Power BI. The data model includes fields such as Age, AgeGroup, Balance, CardType, CreditScore, Geography, Gender, IsActiveMember, NumOfProducts, SatisfactionScore, Tenure, and Churn status. A date hierarchy was derived from the Tenure field to enable time-based analysis.

##### DAX Measures
Custom DAX measures were built to calculate core KPIs including Total Customers, Churned Customers, Churn Rate, Balance at Risk, and Average Credit Score. These measures power dynamic KPI cards and interact with all report slicers.

##### Interactive Slicers & Filtering
Each dashboard includes slicers for Geography, Gender, AgeGroup, and CardType, allowing users to drill into any customer segment and update all visuals simultaneously for a focused view.

##### Multi-Page Report Structure
The report is structured across three pages, each serving a distinct analytical purpose — customer profiling, churn analysis, and financial risk — allowing stakeholders to navigate between high-level overviews and granular insights.

## Dashboard Pages:

### Page 1 — Customer Analysis
This page provides a comprehensive overview of the customer base before any churn lens is applied. It covers demographic distribution, product adoption, activity levels, and satisfaction scores.

**Key KPI Cards:**
- Total Customers: 100,000
- Average Age
- Average Credit Score
- Average Satisfaction Score
- Active Member Rate

**Visuals include:**
- Customer distribution by Geography and Gender
- Age group breakdown
- Product count distribution
- Active vs. inactive member split
- Card type usage breakdown

![Customer Analysis Dashboard](Dashboards/customer_analysis.png)

---

### Page 2 — Customer Churn Dashboard
This page focuses on identifying which customer segments are most likely to churn. Slicers allow filtering by geography, gender, age group, and card type to isolate at-risk populations.

**Key KPI Cards:**
- Total Customers: 100,000
- Churned Customers: 5,575
- Churn Rate: 22%
- Average Credit Score: 599

**Visuals include:**
- Churn vs. retention donut chart (77.83% retained)
- Churn rate by country (horizontal bar)
- Churn rate by number of products
- Age group vs. churn distribution

![Customer Churn Dashboard](Dashboards/churn_dashboard.png)

---

### Page 3 — Risk & Financial Analysis
This page examines the financial implications of churn, with a focus on balance at risk, geographic exposure, and the relationship between activity level and churn.

**Key KPI Cards:**
- Total Customers: 25,000 *(filtered segment)*
- Churned Customers: 5,575
- Churn Rate: 22%
- Balance at Risk: $417M
- Average Credit Score: 599

**Visuals include:**
- Balance split: churned vs. retained donut (80.85% retained by balance)
- Churned customers by active membership status
- Customer count by age group and churn status
- Geographic breakdown table: balance, products, and churn per country

![Risk & Financial Analysis Dashboard](Dashboards/risk_financial.png)

---

## Key Findings:

#### Churn by Geography
Germany stands out with a disproportionately high churn rate relative to its customer count compared to France and Spain. This suggests a regional issue worth investigating — whether pricing, competition, or service quality is a contributing factor.

#### Activity & Churn
Inactive members churn at a significantly higher rate (~3,400 churned) compared to active members (~2,100 churned). Engagement and retention campaigns should prioritize inactive customers as a high-priority segment.

#### Product Count & Churn
Customers holding 3 or 4 products show notably higher churn rates than those with 1 or 2 products. This is counterintuitive and may suggest these customers are over-served, underperforming, or experiencing friction with the bank's multi-product offering.

#### Age Group Insights
The 75+ age group is the largest customer segment (5,950 customers) and also carries significant financial exposure. Tailored retention strategies for older demographics could protect a substantial share of the bank's total balance.

#### Balance at Risk
Of the $417M balance held by churned customers, the largest concentration is in Germany and among inactive members — highlighting where financial risk is most acute.
