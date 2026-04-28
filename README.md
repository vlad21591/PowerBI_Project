# Bank Sales Analysis & Customer Churn

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

Dashboards/1

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

---

## Key Insights & Recommendations:

##### 1. Germany Needs Urgent Attention
Germany has a churn rate far exceeding France and Spain despite having fewer customers. This market is underperforming and requires localized investigation. The bank should conduct customer exit surveys in Germany and benchmark against regional competitors to identify service gaps or pricing mismatches.

##### 2. Re-engage Inactive Members Before They Leave
With ~3,400 inactive members churning versus ~2,100 active ones, inactivity is one of the strongest churn predictors in the dataset. A proactive re-engagement strategy — such as personalized outreach, loyalty rewards, or product usage nudges — could significantly reduce churn volume among this group.

##### 3. Multi-Product Customers Are Surprisingly Fragile
The data reveals that customers with 3–4 products churn at a higher rate than those with just 1–2. Rather than assuming more products equals more loyalty, the bank should review whether bundled offerings are genuinely meeting customer needs or creating unnecessary complexity and dissatisfaction.

##### 4. The 75+ Segment is Both the Largest and Most Financially Exposed
At 5,950 customers, the 75+ age group is the single largest segment. Given their likely higher average balances, losing even a fraction of this group has outsized financial consequences. Dedicated relationship management and simplified digital experiences for this demographic are worth investing in.

##### 5. Credit Score is Not a Reliable Churn Predictor
The average credit score across churned customers (599) is very close to the overall average, suggesting creditworthiness alone does not distinguish loyal customers from those who leave. Behavioral signals — like activity status, product count, and geography — are far more actionable indicators.

##### 6. 80% of Total Balance is Retained — But the 20% at Risk is $417M
While the retention picture looks healthy on the surface (77.83% of customers stayed), the $417M in balance held by churned customers is a critical financial risk. Balance-weighted churn analysis should become a core metric tracked monthly, not just headcount-based churn rate.

##### 7. Card Type and Gender Show Minimal Churn Variance
After filtering across card types (Silver, Gold, Platinum, Diamond) and gender, the churn rate remains relatively stable. This means marketing segmentation by card type or gender is unlikely to yield differentiated retention results — resources are better directed at geography, activity level, and product count.
