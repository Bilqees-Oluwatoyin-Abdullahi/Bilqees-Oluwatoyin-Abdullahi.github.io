---
layout: default
title: Customer Churn Prediction
permalink: /projects/churn-prediction/
---

# Customer Churn Prediction

**Problem:** Low retention of existing customers due to high mothly customer churn rate, leading to stagnant revenue generation by the company.

**Solution:** Analysed how key attributes such as newsletter subscrition, loyalty score, region, and credit tier affects the life time value of customers.

## Approach

1. **Data Collection:** Extracted 3 years of customer data (200K+ records)
2. **EDA:** Analyzed patterns in customer behavior, identified key features
3. **ETL pipeline:** Ckeaned anprmalies in the data sets
4. **Analytics:** Used SQL and data visualizations to analyse trends.
5. **Evaluation:** Found the key attributes that causes customer churn and made appropaite recommendations.

## Results

- Amalytics correctly shows that 94% of customers will churn
- Idetified key attributes that led to custimer churn
- Enabled targeted retention campaigns

## Code Highlights

```python
# Feature engineering example
def create_features(df):
    df['days_since_active'] = (pd.Timestamp.now() - df['last_activity']).dt.days
    df['usage_trend'] = df['recent_usage'] / df['historical_usage']
    return df
