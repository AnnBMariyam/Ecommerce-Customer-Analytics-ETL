# 🛒 E-Commerce Customer Analytics & ETL — Olist Brazil

![Python](https://img.shields.io/badge/Python-3.8+-blue?style=flat-square&logo=python)
![ETL](https://img.shields.io/badge/Pipeline-ETL-green?style=flat-square)
![Pandas](https://img.shields.io/badge/Pandas-Data%20Analysis-lightblue?style=flat-square)
![Status](https://img.shields.io/badge/Status-Completed-brightgreen?style=flat-square)

> **98,666 orders. 95,420 customers. ~$15.84M in revenue. What's actually driving — and hurting — the business?**
> This project builds a full ETL pipeline on Brazil's largest e-commerce dataset and extracts actionable insights on revenue, customer retention, delivery performance, and regional logistics.

---

## 📌 Project Overview

This end-to-end analytics project processes and analyzes the **Olist Brazilian E-Commerce dataset** — a real-world multi-table relational dataset covering orders, customers, products, payments, and reviews.

The workflow follows a structured ETL pipeline (raw → cleaned → analyzed), with a focus on answering real business questions around revenue performance, customer behavior, delivery impact, and freight cost disparities across Brazilian states.

---

## 📂 Repository Structure

```
Ecommerce-Customer-Analytics-ETL/
│
├── data/
│   ├── raw/              # Place downloaded Kaggle CSV files here (see Dataset section)
│   └── cleaned/          # Processed, analysis-ready datasets
│
├── notebooks/
│   └── olist_etl_eda.ipynb   # Full ETL + EDA notebook
│
├── images/               # All visualizations (charts, plots)
└── README.md
```

---

## 📊 Dataset

> ⚠️ **Due to file size limitations, raw datasets are not uploaded to GitHub.**
> Download from Kaggle and place files inside `data/raw/` to reproduce results.

**Source:** [Olist Brazilian E-Commerce — Kaggle](https://www.kaggle.com/datasets/olistbr/brazilian-ecommerce)

**Files used:**

| File | Contents |
|---|---|
| `olist_orders_dataset.csv` | Purchase timestamps, delivery status, delivery dates |
| `olist_customers_dataset.csv` | Customer location details |
| `olist_order_items_dataset.csv` | Product-level order details (price, freight) |
| `olist_order_payments_dataset.csv` | Payment type and installment behavior |
| `olist_products_dataset.csv` | Product category and metadata |
| `olist_order_reviews_dataset.csv` | Customer ratings and feedback |

---

## 🔧 Tech Stack

| Area | Tools |
|---|---|
| Language | Python 3.8+ |
| Data Processing | Pandas, NumPy |
| Visualization | Matplotlib, Seaborn |
| Pipeline Structure | ETL folder structure (raw → cleaned) |
| Environment | Jupyter Notebook |

---

## ⚙️ ETL Pipeline

```
Raw CSVs (6 tables) → Load & Merge → Clean & Validate → Feature Engineer → Analyze → Visualize
```

### Extract
- Loaded 6 relational CSV files from Kaggle
- Merged tables using order IDs and customer keys to build a unified analytical dataset

### Transform
- Handled missing values across delivery dates, review scores, and product metadata
- Engineered key metrics:
  - `delivery_days` = actual delivery date − order purchase date
  - `freight_ratio` = freight value / item price
  - `is_repeat_customer` = flag for customers with more than one order
- Parsed and extracted time-based features for monthly trend analysis
- Standardized product category names for consistent analysis

### Load
- Exported cleaned, merged dataset to `data/cleaned/` for reuse in analysis and reporting

---

## ❓ Business Questions Answered

1. What is the total revenue, order volume, and unique customer count?
2. Which product categories generate the highest revenue?
3. How does delivery time affect customer review scores?
4. What percentage of customers are repeat buyers?
5. Which states face disproportionately high freight cost ratios?

---

## 📈 Key Insights & Business Findings

### 📦 Scale
- **98,666 orders** from **95,420 unique customers** generating **~$15.84M in revenue**

### 🏆 Top Revenue Categories
- **Health & Beauty** and **Watches & Gifts** are the highest revenue-generating categories
- Strong opportunity for targeted promotions and inventory prioritization in these segments

### ⭐ Delivery Time vs. Review Score
- Clear negative correlation: **longer delivery times directly reduce customer review scores**
- Business implication: improving logistics speed is the highest-leverage lever for customer satisfaction — not discounts or promotions

### 🔄 Customer Retention Problem
- The vast majority of customers are **one-time buyers** — repeat purchase rate is critically low
- Signals an urgent need for loyalty programs, post-purchase engagement, and re-targeting campaigns

### 🚚 Regional Freight Disparity
- Certain states show **significantly higher freight cost ratios** (freight as % of item price)
- Customers in these states are effectively paying a "location tax" — a likely driver of cart abandonment and lower conversion in those regions

---

## 📸 Visualizations Included

| Chart | Insight |
|---|---|
| Top 10 categories by revenue | Which product lines dominate sales |
| Monthly revenue trend | Seasonality and growth patterns |
| One-time vs repeat customers | Customer retention breakdown |
| Delivery days vs review score | Delivery speed → satisfaction relationship |
| Freight ratio by state | Regional logistics cost disparities |
| Review score distribution | Overall customer satisfaction spread |

---

## 🚀 How to Run

```bash
# 1. Clone the repo
git clone https://github.com/AnnBMariyam/Ecommerce-Customer-Analytics-ETL.git
cd Ecommerce-Customer-Analytics-ETL

# 2. Download dataset from Kaggle
# https://www.kaggle.com/datasets/olistbr/brazilian-ecommerce
# Place all 6 CSV files inside data/raw/

# 3. Install dependencies
pip install pandas numpy matplotlib seaborn jupyter

# 4. Run the notebook
jupyter notebook notebooks/olist_etl_eda.ipynb
```

---

## 👩‍💻 Author

**Ann B Mariyam**
MS Data Analytics — University of Illinois Springfield
[LinkedIn](https://www.linkedin.com/in/ann-b-mariyam-a238a7275/) | [GitHub](https://github.com/AnnBMariyam) | annbijumariyam02@gmail.com
