# Credit-Card-Customer-Segmentation-Risk-Exploration
**Author:** S3renity1 | Sydney, NSW, Australia  
**Project Type:** Banking Analytics Portfolio Project  
**Tech Stack:** Python (Pandas, Scikit-learn), Power BI

## Dashboard Preview
![Executive Summary](https://github.com/S3renity1/Credit-Card-Customer-Segmentation-Risk-Exploration/blob/main/executive-summary.png)
![Risk Analysis](https://github.com/S3renity1/Credit-Card-Customer-Segmentation-Risk-Exploration/blob/main/risk-analysis.png)
![Actionable Insights](https://github.com/S3renity1/Credit-Card-Customer-Segmentation-Risk-Exploration/blob/main/actionable-insights.png)

## Project Overview
This project segments 30,000 credit card customers into behavioral risk profiles using K-Means clustering and identifies key default risk drivers. Built for banking graduate program applications.

**Business Value:**
- Identified 4 distinct customer segments with default rates ranging from 8% to 32%
- Discovered payment delays increase default odds by 2.8x
- Built Power BI dashboard for ongoing monitoring
- **Estimated Impact:** 15% default reduction could save NT$281 million annually

## Business Insights Summary

### 1. Segment Characteristics

**Premium Low-Risk Segment (11.26%% of customers)**
- Default Rate: ~9.64%%
- Avg Credit Limit: NT$244.83K+
- Profile: Older customers (40+), stable payment history
- **Recommendation:** Target for credit limit increases, premium card upselling

**High-Risk Delinquents (20.8%% of customers)**
- Default Rate: ~44.52%
- Avg Credit Limit: NT$84.88k
- Profile: Younger customers, frequent payment delays
- **Recommendation:** Proactive outreach, payment plan options, reduce limits

### 2. Risk Drivers (Correlation Analysis)

Top 3 predictors of default:
1. **Recent Payment Delays (PAY_0):** Correlation = 0.32
2. **Number of Delays (NUM_DELAYS):** Correlation = 0.29
3. **Maximum Delay Severity:** Correlation = 0.27

**Insight:** Customers with 3+ delays in past 6 months are 2.8x more likely to default.

### 3. Financial Impact

- **Total Estimated Loss from Defaults:** NT$281.91M million (assuming 50% loss severity)
- **Highest-Risk Segment Loss:** 89.28M NT$million (31.1% of total)
- **Potential Savings:** Reducing high-risk segment defaults by 15% could save NT$XX million annually

### Actionable Interventions
1. **Early Warning System:**
   - Flag customers with 2+ consecutive delays
   - Automated SMS/email reminders before due dates
   - Estimated impact: 10-15% reduction in defaults

2. **Risk-Based Credit Limit Management:**
   - Reduce limits for high-utilization + high-delay customers
   - Increase limits for low-risk, on-time payers
   - Estimated revenue gain: 5-8% from upselling

3. **Personalized Repayment Plans:**
   - Offer installment options to "Medium Risk" customers
   - Reduce default migration by 20%

4. **Segment-Specific Marketing:**
   - Premium Low-Risk: Travel rewards cards, higher limits
   - Stable Mid-Tier: Balance transfer offers
   - High-Utilizers: Financial literacy resources
   
### Model Performance

- **Logistic Regression ROC-AUC:** 0.72-0.76
- **Interpretation:** Model can identify 72-76% of defaults correctly
- **Business Use:** Integrate into credit decisioning pipeline for new applicants

##Dataset
**Source:** [UCI ML Repository - Default of Credit Card Clients](https://archive.ics.uci.edu/dataset/350/default+of+credit+card+clients)

**Details:**
- 30,000 records from Taiwan (2005)
- 23 features (demographics, payment history, bills)
- Binary target (default/no default)
- No missing values
