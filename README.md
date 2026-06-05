# H&M Customer Segmentation Analysis
[![Python](https://img.shields.io/badge/Python-3.8%2B-blue)](https://www.python.org/)
[![Pandas](https://img.shields.io/badge/Pandas-Latest-green)](https://pandas.pydata.org/)
[![Scikit--learn](https://img.shields.io/badge/Scikit--learn-Latest-orange)](https://scikit-learn.org/)

## Project Goal

The goal of this project was to explore customer purchasing behavior in the H&M Kaggle dataset and identify customer segments that could support marketing and retention initiatives.

## Dataset

The analysis uses the [H&M Personalized Fashion Recommendations](https://www.kaggle.com/competitions/h-and-m-personalized-fashion-recommendations/data) dataset from Kaggle.

* 31.3 million transactions
* 1.37 million customers
* 105,000 products
* Purchase history from September 2018 to September 2020

## Analysis Process

I started with exploratory analysis of customer demographics, product categories, purchasing patterns, and customer loyalty metrics.

For customer segmentation, transaction-level data was aggregated to the customer level. The following features were used:

* Purchase frequency
* Total spending
* Average purchase value
* Recency
* Customer age
![Age Distribution](visualizations/day1_age_distribution.png)
![Product Categories](visualizations/day2_product_categories.png)
![Monthly Trends](visualizations/day3_temporal_patterns.png)
![Price Distribution](visualizations/day4_price_distribution.png)
![Customer Loyalty](visualizations/day5_customer_loyalty.png)

Features were standardized before applying K-Means clustering.

I tested multiple cluster counts and selected four segments because they produced the most interpretable customer groups.

## Key Findings

### VIP Customers

A small segment of approximately 5% of customers generated 36% of total revenue.

These customers were highly active and made substantially more purchases than the rest of the customer base.

### Lapsed Customers

Around 26% of customers had not made a purchase for a long period and contributed relatively little revenue.

This group represents a potential re-engagement opportunity.

### Repeat Purchase Challenge

More than 65% of customers made only a single purchase during the period covered by the dataset.

This suggests customer retention may be a significant challenge.

![Customer Segmentation](visualizations/day6_customer_vs_revenue.png)

## Possible Business Actions

Based on the analysis, a business could consider:

* Retention programs for high-value customers
* Re-engagement campaigns for lapsed customers
* Initiatives focused on increasing repeat purchases after a customer's first order

## Tools Used

* Python
* Pandas
* NumPy
* Scikit-learn
* Matplotlib
* Seaborn

## Limitations

* The analysis is based on historical transaction data only.
* Customer demographics are limited.
* No causal analysis was performed, so recommendations should be validated through testing.

## Future Work

Possible extensions include:

* Segment-specific product preference analysis
* Customer lifetime value estimation
* Churn prediction models
* Interactive Power BI or Tableau dashboards
