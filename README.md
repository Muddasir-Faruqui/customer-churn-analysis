# Customer Churn Analysis Portfolio Project

An end-to-end customer churn analysis project using Python, pandas, and SQLite. The project cleans relational customer data, builds a customer-level analytical dataset, explores churn drivers, and translates the findings into retention recommendations.

## Project Objective

The goal is to understand why subscription customers churn and identify which customers, plans, and support patterns deserve retention focus.

This project answers:

- What is the customer churn rate?
- Which plans, contract types, and acquisition sources have the highest churn?
- How are complaints, escalations, and CSAT related to churn?
- Which active customers should be monitored first?
- What business actions can reduce churn?

## Key Findings

- Total customers analyzed: 21
- Churned customers: 6
- Churn rate: 28.57%
- Retention rate: 71.43%
- Lost monthly revenue from churned customers: 73.94
- Monthly contracts and Basic plans show the highest churn risk in the sample.
- Complaint and escalation activity is strongly associated with churn.
- High churn-score customers are the best first group for retention outreach.

## Files

| File | Description |
| --- | --- |
| `Churn_Analysis_Portfolio.ipynb` | Main portfolio notebook with the full analysis workflow |
| `customer_churn.db` | SQLite database containing customer, subscription, and support tables |


## Dataset Overview

The SQLite database contains three source tables:

| Table | Rows | Purpose |
| --- | ---: | --- |
| `db_customer` | 21 | Customer profile information such as country, state, gender, and date of birth |
| `db_subscription` | 21 | Subscription plan, contract, renewal, cancellation, revenue, CLTV, and churn score |
| `db_support` | 9 | Support complaints, escalation flags, CSAT scores, and support comments |

## Analysis Workflow

1. Connect to the SQLite database.
2. Inspect database tables and schema.
3. Clean customer, subscription, and support data.
4. Standardize values such as gender and referral source.
5. Convert date fields to datetime format.
6. Engineer churn status, tenure, customer age, revenue, and risk features.
7. Merge tables into a customer 360 dataset.
8. Calculate churn KPIs and revenue impact.
9. Analyze churn by plan, contract, acquisition source, geography, and support behavior.
10. Build a retention watchlist and business recommendations.

## Tools Used

- Python
- pandas
- numpy
- SQLite
- Jupyter Notebook
- matplotlib, optional for visualizations

## How To Run

1. Clone or download this repository.
2. Open the project folder.
3. Install the core Python libraries:

```bash
pip install -r requirements.txt
```

4. Open the main notebook:

```bash
jupyter notebook Churn_Analysis_Portfolio.ipynb
```

5. Run the notebook cells from top to bottom.

## Business Recommendations

- Prioritize monthly-contract customers for retention offers and annual-plan conversion campaigns.
- Review Basic plan value perception, pricing, and content fit.
- Trigger customer success follow-up after support escalations.
- Use churn score, support activity, and CLTV together to rank outreach priority.
- Build cancellation-reason playbooks for competitor switching, price concerns, streaming quality, and content gaps.

## Project Status

Portfolio-ready analysis notebook with source data, KPI summary, segmentation, churn-risk interpretation, and business recommendations.



