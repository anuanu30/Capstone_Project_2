# Capstone_Project_2
RFM Segmentation & Retention Strategy
# Customer RFM Segmentation & Retention Strategy

## Project Overview

This project focuses on customer segmentation using the RFM (Recency, Frequency, Monetary) framework combined with additional behavioural signals. The objective is to identify customer groups that require retention attention before deploying a machine learning churn prediction model.

The analysis was performed using transaction-level customer order data and behavioural indicators such as returns, discount usage, ratings, and delivery experience.

---

# Objective

The goal of this project is to:

- Build RFM features from order data
- Create meaningful customer segments
- Combine RFM with behavioural indicators
- Recommend targeted retention strategies
- Prioritize customer groups under a limited campaign budget
- Analyze ambiguous customer cases manually

---

# Dataset Information

The dataset contains customer order-level transaction data with the following fields:

| Column Name | Description |
|---|---|
| order_id | Unique order identifier |
| customer_id | Unique customer identifier |
| order_date | Date of order |
| category | Product category |
| quantity | Quantity purchased |
| gross_amount | Total order amount |
| discount_pct | Discount percentage applied |
| delivery_days | Delivery completion time |
| returned | Whether the order was returned |
| rating | Customer rating |

---

# Features Created

## RFM Features

### Recency
Number of days since the customer’s most recent purchase.

### Frequency
Total number of unique orders placed by the customer.

### Monetary
Total amount spent by the customer.

---

# Additional Behavioural Signals

The project also includes additional customer behaviour indicators:

| Feature | Business Meaning |
|---|---|
| return_rate | Product dissatisfaction / churn risk |
| avg_discount_pct | Price sensitivity |
| avg_rating | Customer satisfaction |
| avg_delivery_days | Service quality experience |

---

# Customer Segments

The following customer segments were created:

| Segment | Description |
|---|---|
| Champions | High-value recent customers |
| Loyal Customers | Frequent repeat buyers |
| At Risk | Previously valuable but inactive customers |
| High Return Customers | Customers with high return behaviour |
| Dormant | Long inactive customers |
| New Customers | Recently acquired customers |

---

# Segmentation Logic

Customer segmentation was performed using:

- RFM metrics
- Return behaviour
- Discount usage patterns
- Customer ratings
- Delivery experience

Rule-based segmentation logic was implemented inside the notebook.

---

# Key Business Insights

## Champions
- Generate strong revenue
- Highly engaged and valuable

## Loyal Customers
- Consistent purchasing behaviour
- Good upsell potential

## At Risk
- Previously active customers becoming inactive
- High recovery opportunity

## High Return Customers
- Possible dissatisfaction or product mismatch
- Potential churn risk

## Dormant Customers
- Very low recent engagement
- Lower recovery probability

---

# Retention Strategy

Retention strategies were designed separately for each segment, including:

- VIP rewards
- Personalized campaigns
- Win-back offers
- Discount optimization
- Service improvement recommendations

Detailed strategies are provided in:

```text
retention_strategy.md
