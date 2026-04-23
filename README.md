---

## Tech Stack & Skills

![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![Power BI](https://img.shields.io/badge/Power_BI-F2C811?style=for-the-badge&logo=powerbi&logoColor=black)
![Pandas](https://img.shields.io/badge/Pandas-150458?style=for-the-badge&logo=pandas&logoColor=white)
![Matplotlib](https://img.shields.io/badge/Matplotlib-11557C?style=for-the-badge&logo=python&logoColor=white)
![Seaborn](https://img.shields.io/badge/Seaborn-3776AB?style=for-the-badge&logo=python&logoColor=white)
![Jupyter](https://img.shields.io/badge/Jupyter-F37626?style=for-the-badge&logo=jupyter&logoColor=white)
![DAX](https://img.shields.io/badge/DAX-0078D4?style=for-the-badge&logo=microsoft&logoColor=white)
![GitHub](https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white)

## Skills Demonstrated

`Churn Analysis` `Cohort Analysis` `Customer Retention` `Customer Lifetime Metrics` `Business Intelligence` `Data Storytelling` `Dashboard Design` `Statistical Analysis`

---
# RavenStack Customer Retention & Churn Analysis

**SaaS Analytics Portfolio Project | Future Interns Task 2**

Analyzed 500 SaaS customer accounts across 5 relational tables to identify churn patterns, retention drivers, and deliver actionable business recommendations using Python and Power BI.

---
## Introduction

### What is this study about?

This project analyzes customer churn and retention patterns for **RavenStack**, a fictional stealth-mode SaaS startup delivering AI-driven team collaboration tools. The company piloted their product with 500 coding bootcamp graduates, capturing every sign-up, feature interaction, support ticket, and churn event before their public launch.

### Business Problem

The goal was to help RavenStack's leadership answer:

- Why are customers leaving the platform?
- Which customer segments are most likely to churn?
- How long do customers typically stay active?
- What actions can improve customer retention?

---

## Methodology

### How was the analysis conducted?

#### Data Source

The **RavenStack Synthetic SaaS Dataset** contains 5 relational tables:

| Table | Records | Content |
|:---|:---|:---|
| accounts | 500 | Customer profiles, industry, plan tier, signup date |
| subscriptions | 5,000 | Billing history, plan changes, MRR |
| feature_usage | 25,000 | Product interaction events, errors, beta usage |
| support_tickets | 2,000 | Ticket priority, resolution time, satisfaction scores |
| churn_events | 600 | Churn dates, reasons, refunds, feedback |

#### Analytical Approach

**Phase 1: Data Preparation (Python - Pandas)**
- Parsed date fields across all tables
- Joined 5 tables using primary/foreign keys (`account_id`, `subscription_id`)
- Built a master analysis dataset with 30+ derived features
- Calculated customer lifetime metrics per account

**Phase 2: Metric Definition**
- Distinguished between **Ever Churned** (historical) and **Currently Churned** (inactive now)
- Defined cohorts by signup month
- Segmented customers by engagement level, ticket volume, and beta usage

**Phase 3: Analysis**
- Cohort retention analysis by signup month
- Churn rate comparison across plan tiers, industries, and segments
- Support ticket impact on churn probability
- Feature engagement correlation with customer lifetime
- Beta feature error rates and retention impact

**Phase 4: Visualization (Power BI)**
- 4-page interactive dashboard using DAX measures
- KPI cards, bar charts, donut charts, scatter plots, and matrix tables
- Cross-filtering for segment-level exploration

---

## Results

### What was found?

#### Key Metrics

| Metric | Value |
|:---|:---|
| Total Customers | 500 |
| Currently Active | 456 (91.2%) |
| Currently Churned | 44 (8.80%) |
| Historical Churn (Ever) | 352 (70.4%) |
| Total Support Tickets | 2,000 |
| Total Feature Events | 25,000 |

#### Finding 1: Current Churn is Healthy at 8.80%

Only 44 of 500 accounts are currently inactive. While 70.4% have churned at some point historically, the vast majority reactivated. This distinction was critical, using **ever churned** would have painted a misleading picture of a dying business.

#### Finding 2: Support Tickets Drive Churn

Customers with higher support ticket volumes showed consistently higher churn rates. The relationship was clear and progressive:

| Ticket Segment | Churn Impact |
|:---|:---|
| No Tickets | Lowest churn risk |
| 1-2 Tickets | Moderate increase |
| 3+ Tickets | Significantly higher churn |

#### Finding 3: Feature Engagement Increases Lifetime

Customers in higher engagement percentiles showed longer average lifetimes compared to low-engagement customers. Power users stay longer and churn less.

#### Finding 4: Beta Features Need Guardrails

Customers who used beta features experienced more errors, correlating with elevated churn risk compared to non-beta users.

#### Finding 5: Churn Varies by Plan and Industry

Certain plan tiers and industries showed higher churn rates, indicating potential product-market fit gaps in specific segments.

---

## Discussion

### What do these findings mean?

#### The Reactivation Story

The 70.4% historical churn rate initially seemed alarming. However, with only 44 accounts currently inactive, the real story emerged:

> **RavenStack doesn't have a retention problem - it has an onboarding problem.**

Customers leave early due to friction, but when they return, they stay. This means the core product delivers value. The opportunity is reducing initial drop-off so fewer customers leave in the first place.

#### Support as a Retention Lever

The correlation between ticket volume and churn suggests that unresolved issues erode customer confidence. Each additional ticket increases churn probability, making proactive support intervention a high-impact retention strategy.

#### Engagement as a Moat

The positive correlation between feature usage and customer lifetime validates a product-led growth approach. Driving early feature adoption creates stickiness that compounds over time.

---

## Recommendations

### Actionable Steps for RavenStack

| Priority | Action | Rationale |
|:---|:---|:---|
| **Immediate** | Flag accounts with 2+ support tickets in first 30 days for high-touch onboarding | Support tickets are the #1 churn predictor |
| **Short-term** | Gate beta features behind opt-in with clear expectations | Beta users face more errors and higher churn risk |
| **Short-term** | Implement 7-day activation email sequence | Drive early feature engagement to boost Month-1 retention |
| **Strategic** | Focus marketing on industries with lowest churn rates | Double down on segments with proven product-market fit |
| **Strategic** | Build engagement acceleration program for bottom 25% of feature users | Move low-engagement users to medium engagement within 30 days |

#### Metrics to Track Weekly

- Month-1 retention rate by cohort
- Average support tickets per new customer (first 30 days)
- 7-day feature activation rate
- Beta feature error rate

---

## Conclusion

This analysis transformed 5 relational tables into a clear, data-driven retention strategy for RavenStack.

**The headline:** Current churn is a healthy 8.80%. The high historical churn rate (70.4%) reflects onboarding friction, not product failure. Most customers who leave come back.

**The priority:** Fix the first 30 days. Proactive support outreach at 2+ tickets, guided feature activation, and beta feature guardrails will reduce early churn and increase long-term retention.

**The dashboard:** Delivered as a 4-page interactive Power BI report ready for stakeholder presentation.

---

## Project Structure

RavenStack_Retention_Analysis/

│

├── README.md

│

├── 01_Raw_Data/

│ ├── ravenstack_accounts.csv

│ ├── ravenstack_subscriptions.csv

│ ├── ravenstack_feature_usage.csv

│ ├── ravenstack_support_tickets.csv

│ └── ravenstack_churn_events.csv

│

├── 02_Visualizations/

│ ├── churn_reasons.png

│ ├── cohort_retention_heatmap.png

│ ├── support_impact_analysis.png

│ └── engagement_impact.png

│

├── 03_PowerBI_Dashboard/

│ ├── RavenStack_Retention_Dashboard.pbix

│ └── RavenStack_Dashboard_Report.pdf

│

├── Data_Cleaned.ipynb

├── ravenstack_cohort_analysis_ready.csv

├── ravenstack_master_analysis_final.csv

└── README.md


---

## Tools Used

| Category | Tool |
|:---|:---|
| Data Processing | Python (Pandas, NumPy) |
| Statistical Visualization | Matplotlib, Seaborn |
| Interactive Dashboard | Power BI Desktop, DAX |
| Development Environment | Jupyter Notebook |
| Version Control | Git, GitHub |

---
## How to Use

### Prerequisites
- Python 3.8+ with Pandas, NumPy, Matplotlib, Seaborn
- Power BI Desktop (free from Microsoft)
- Jupyter Notebook or VS Code

### Steps

**1. Clone the repository**
```bash: git clone https://github.com/Slyza13/FUTURE_DS_02.git, cd FUTURE_DS_02```

2. Explore the analysis notebook

bash
jupyter notebook 02_Processed_Data/RavenStack_Analysis.ipynb
3. Open the Power BI dashboard

Open 05_PowerBI_Dashboard/RavenStack_Retention_Dashboard.pbix

If prompted, update the data source path to 02_Processed_Data/ravenstack_master_analysis_final.csv

4. Navigate the dashboard

- Page 1: Executive Overview - KPIs, churn by plan/industry, churn reasons

- Page 2: Cohort Retention - Lifetime distribution, cohort trends

- Page 3: Support Impact - Ticket volume vs churn, satisfaction analysis

- Page 4: Feature Engagement - Engagement levels, beta impact

Future Suggestions
What could be done next?
1. Predictive Churn Model
Build a machine learning classification model using the existing features (ticket volume, engagement level, beta usage, plan tier) to predict which accounts are at highest risk of churning in the next 30 days.

2. Support Ticket Sentiment Analysis
Apply NLP to feedback_text in churn events and support ticket data to categorize customer sentiment and identify specific pain points mentioned by departing customers.

3. Revenue Impact Modeling
Quantify the dollar impact of churn reduction. Model scenarios showing how reducing current churn from 8.80% to 5% or 3% would affect Annual Recurring Revenue (ARR).

4. Customer Lifetime Value (LTV) Calculation
Calculate LTV by segment (plan tier, industry, acquisition channel) to identify which customer types deliver the highest long-term value and deserve disproportionate retention investment.

5. A/B Testing Framework for Onboarding
Design experiments to test onboarding improvements identified in this analysis:

Test high-touch vs standard onboarding for high-ticket accounts

Test gated vs open beta feature access

Measure impact on Month-1 retention

6. Time-to-Value Analysis
Identify the **-aha moment-** by analyzing which specific features, when used within the first 7 days, most strongly correlate with long-term retention.

7. Automated Reporting Pipeline
Schedule the Python script to run weekly, refresh the Power BI dataset automatically, and alert stakeholders when churn metrics exceed thresholds.

Author & Credits
Author
**Sifiso Sibiya**

**LinkedIn:** www.linkedin.com/in/sifiso-sibiya-8b2756334

**GitHub:** https://github.com/Slyza13/

Project Context
Completed as Task 2 of the Future Interns Data Analytics Program, focusing on customer retention and churn analysis for subscription-based businesses.

Dataset Credits
Dataset: RavenStack Synthetic SaaS Dataset

Author: River @ Rivalytics

License: MIT-like (fully synthetic, no PII)

Last Updated: April 2026

text

---

## Key Changes Made:

1. **Removed Literature Review section** - we didn't actually do research, we did analysis
2. **Removed comparison to benchmarks** - we didn't set formal targets before analysis
3. **Kept only our actual findings** - no fabricated numbers
4. **Added Future Suggestions section** - 7 concrete next steps that show strategic thinking
5. **Fixed TOC anchor links** - GitHub auto-generates anchors from lowercase headers with hyphens
6. **Cleaner, shorter, more honest** about what we actually did

**Analyzed with l.o.v.e by Sifiso SIbiya.**
