# Customer & Revenue Intelligence Report — E-Commerce Dataset

> A full-stack data analysis portfolio project using the **Olist Brazilian E-Commerce** dataset (100K+ orders). Covers data cleaning, SQL business queries, revenue trend analysis, RFM customer segmentation, and interactive Plotly dashboards.

---

## Project Overview

This project simulates a real analyst brief: *"Analyze our e-commerce data, identify revenue drivers, segment our customers, and recommend growth strategies."*

**Dataset:** [Olist Brazilian E-Commerce (Kaggle)](https://www.kaggle.com/datasets/olistbr/brazilian-ecommerce) — 100K+ orders from 2016–2018 across a Brazilian marketplace covering orders, customers, payments, reviews, products, and sellers.

---

## Key Findings

| Area | Insight |
|---|---|
| **Revenue Growth** | Steady growth from late 2016 to mid-2018; Black Friday 2017 was the peak month |
| **Top Categories** | Health & beauty, watches, and bed/bath/table generate the most revenue |
| **Customer Retention** | ~97% of customers placed only 1 order — retention is the biggest growth lever |
| **Delivery Impact** | Faster delivery strongly correlates with higher review scores (4.3 vs 2.5 avg) |
| **Payment Behavior** | 74% credit card usage with average 3–4 installments |
| **Geography** | São Paulo dominates volume; northern states face 20+ day delivery times |

---

## Analysis Modules

| # | Module | Notebook | Tools |
|---|---|---|---|
| 1 | **Data Cleaning & EDA** | [`01_data_cleaning.ipynb`](notebooks/01_data_cleaning.ipynb) | Pandas, NumPy, Matplotlib, Seaborn |
| 2 | **SQL Business Queries** | [`02_sql_analysis.ipynb`](notebooks/02_sql_analysis.ipynb) | SQLite3, Pandas |
| 3 | **Revenue Trends** | [`03_visualizations.ipynb`](notebooks/03_visualizations.ipynb) (Part A) | Matplotlib, Seaborn |
| 4 | **Customer Segmentation (RFM)** | [`03_visualizations.ipynb`](notebooks/03_visualizations.ipynb) (Part B) | Pandas, Plotly |
| 5 | **Interactive Dashboard** | [`03_visualizations.ipynb`](notebooks/03_visualizations.ipynb) (Part C) | Plotly |

---

## Project Structure

```
E-Commerce-Sales-Analysis/
├── data/                          # Raw CSVs from Kaggle (9 files)
│   ├── olist_customers_dataset.csv
│   ├── olist_orders_dataset.csv
│   ├── olist_order_items_dataset.csv
│   ├── olist_order_payments_dataset.csv
│   ├── olist_order_reviews_dataset.csv
│   ├── olist_products_dataset.csv
│   ├── olist_sellers_dataset.csv
│   ├── olist_geolocation_dataset.csv
│   └── product_category_name_translation.csv
├── notebooks/
│   ├── 01_data_cleaning.ipynb     # EDA, missing values, data wrangling
│   ├── 02_sql_analysis.ipynb      # 10 business questions via SQL
│   └── 03_visualizations.ipynb    # Revenue trends, RFM, Plotly dashboard
├── outputs/                       # Saved charts (.png) and interactive HTML
├── .gitignore
├── requirements.txt
└── README.md
```

---

## SQL Queries Covered (Module 2)

1. **Monthly Revenue Trend** — Are we growing?
2. **Top Product Categories** — Where does revenue come from?
3. **Customer Lifetime Value** — Who are our best customers?
4. **Seller Performance Ranking** — Which sellers drive revenue?
5. **Delivery Performance by State** — Where are logistics bottlenecks?
6. **Payment Behavior Analysis** — How do customers pay?
7. **Review Score vs Delivery** — Does speed impact satisfaction?
8. **Repeat Customer Rate** — What's our retention rate?
9. **Peak Sales Hours & Days** — When do orders come in?
10. **Revenue by State** — Which regions generate the most per customer?

---

## RFM Segmentation (Module 4)

Customers are scored on **Recency**, **Frequency**, and **Monetary** value, then assigned to segments:

| Segment | Description | Action |
|---|---|---|
| **Champions** | Recent, frequent, high spenders | Reward & upsell |
| **Loyal Customers** | Recent, high spenders | Loyalty program |
| **At Risk** | Used to spend but haven't returned | Win-back campaigns |
| **Lost** | Haven't purchased in a long time | Re-engagement or let go |
| **Promising** | Recent with moderate engagement | Nurture to loyalty |

---

## Actionable Recommendations

1. **Launch a loyalty/rewards program** — With ~97% one-time buyers, even a 5% retention improvement would significantly boost revenue
2. **Optimize logistics in northern states** — Delivery times of 20+ days hurt review scores; partner with regional carriers
3. **Focus ad spend on peak windows** — Weekday afternoons (10 AM – 4 PM) see the highest conversion
4. **Run win-back campaigns** — Target "At Risk" and "Lost" RFM segments with personalized offers
5. **Double down on top categories** — Health & beauty and watches have proven demand; expand selection

---

## Setup & Installation

```bash
# Clone the repository
git clone https://github.com/rushikeshwagh/E-Commerce-Sales-Analysis.git
cd E-Commerce-Sales-Analysis

# Install dependencies
pip install -r requirements.txt

# Download the dataset (requires Kaggle API key)
kaggle datasets download -d olistbr/brazilian-ecommerce -p data/ --unzip

# Run notebooks
jupyter notebook notebooks/
```

---

## Tech Stack

- **Python 3.11+**
- **Pandas / NumPy** — Data wrangling
- **SQLite3** — SQL analysis
- **Matplotlib / Seaborn** — Static visualizations
- **Plotly** — Interactive charts & dashboards

---

## License

Dataset provided under [CC BY-NC-SA 4.0](https://creativecommons.org/licenses/by-nc-sa/4.0/) by Olist.
