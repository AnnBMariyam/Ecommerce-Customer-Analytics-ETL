# Olist E-commerce ETL + Sales Analytics (Python)

## Project Overview
This project analyzes the Olist Brazilian E-commerce dataset using an end-to-end workflow including data loading, cleaning, feature engineering, and exploratory data analysis.  
The goal is to understand key revenue drivers, customer behavior, delivery performance, and review patterns to support data-driven business decisions.

---

## Dataset Description
The dataset contains multiple relational tables representing real e-commerce transactions:
- **Orders:** purchase timestamps, delivery status, delivery dates
- **Customers:** customer location details
- **Order Items:** product-level order details (price, freight)
- **Payments:** payment type and installment behavior
- **Products:** product category and metadata
- **Reviews:** customer ratings and feedback

---

## Tools & Skills Used
- **Python (Pandas, NumPy)**
- **Data Cleaning & Feature Engineering**
- **ETL-style folder structure (raw → cleaned)**
- **Data Aggregation + GroupBy Analysis**
- **Visualization (Matplotlib, Seaborn)**

---

## Key Business Questions Answered
- What is the total revenue, number of orders, and unique customers?
- Which product categories generate the highest revenue?
- How does delivery time impact review scores?
- What percentage of customers are repeat buyers?
- Which states face higher freight cost ratios?

---

## Key Insights Summary
- The dataset contains **98,666 orders** from **95,420 unique customers**, generating **~15.84M revenue**.
- **Health & Beauty** and **Watches & Gifts** are the top revenue-generating categories.
- Longer delivery times are associated with lower review scores, showing delivery speed impacts satisfaction.
- Customer retention is low, with most customers being one-time buyers.
- Freight cost ratios are significantly higher in certain states, indicating regional logistics challenges.

---

## Visualizations Included
- Top 10 categories by revenue  
- Monthly revenue trend  
- One-time vs repeat customers  
- Delivery days vs review score  
- Freight ratio by state  
- Review score distribution  

---
