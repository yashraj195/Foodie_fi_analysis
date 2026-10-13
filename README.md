# Foodie-Fi Subscription Analysis (SQL)

A SQL data analysis project based on the Foodie-Fi subscription business case study.

The project analyses customer subscription behaviour, plan changes, free-trial conversions and churn to answer business questions using SQL.

## Project Overview

Foodie-Fi is a fictional subscription-based streaming service launched in 2020 that offers cooking-related video content through monthly and annual subscription plans.

The objective of this project is to analyse subscription data and understand customer behaviour throughout the subscription lifecycle.

## Tools & Technologies

- **SQL**
- **MySQL**
- Common Table Expressions (CTEs)
- Aggregate functions
- Joins and subqueries
- Window functions
- Date functions and conditional aggregation

## Database Schema

The analysis uses two tables:

**1. `plans`**

| Column | Description |
|---|---|
| `plan_id` | Unique plan identifier |
| `plan_name` | Name of the subscription plan |
| `price` | Plan price |

**2. `subscriptions`**

| Column | Description |
|---|---|
| `customer_id` | Customer identifier |
| `plan_id` | Associated subscription plan |
| `start_date` | Date the subscription plan starts or changes |

### Subscription Plans

| Plan ID | Plan Name | Price |
|---|---|---:|
| 0 | Trial | $0 |
| 1 | Basic monthly | $9.90 |
| 2 | Pro monthly | $19.90 |
| 3 | Pro annual | $199 |
| 4 | Churn | NULL |

## Business Questions

The project uses SQL to answer questions including:

- How many unique customers have subscribed to Foodie-Fi?
- What is the monthly distribution of free-trial sign-ups?
- How many subscription plan changes occurred after 2020?
- What percentage of customers churned?
- How many customers cancelled immediately after their free trial?
- What subscription plans did customers choose after their trial?
- What was the customer distribution across all plans at 31 December 2020?
- How many customers downgraded from Pro monthly to Basic monthly during 2020?

## Key Findings

Based on the results in the case-study analysis:

- **1,000 customers** subscribed to Foodie-Fi.
- **307 customers (30.7%)** churned.
- **92 customers (9.2%)** churned immediately after their initial free trial.
- After the free trial, 546 customers selected Basic monthly, 325 selected Pro monthly, and 37 selected Pro annual; 92 churned.
- No customers downgraded from Pro monthly to Basic monthly during 2020 in the analysed dataset.

## SQL Concepts Demonstrated

- `GROUP BY` and aggregate functions for customer and subscription summaries.
- `JOIN` operations to combine subscription and plan data.
- `CASE` expressions for conditional counting.
- CTEs and `ROW_NUMBER()` for analysing subscription sequences.
- `DENSE_RANK()` for ranking plans and identifying top customers.
- Date functions for monthly and year-based analysis.
- Percentage calculations for churn and plan distribution.

## Repository Structure

```text
foodie-fi-analysis/
├── README.md
└── foodie_fi.sql
```

*Adjust the SQL filename in this example to match the actual file in your repository.*

## Author

**Yash Raj**

- [GitHub](https://github.com/yashraj195)
- [LinkedIn](https://linkedin.com/in/yashraj195)
