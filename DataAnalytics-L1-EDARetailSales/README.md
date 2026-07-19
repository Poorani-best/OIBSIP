# Retail Sales EDA

Exploratory Data Analysis on a retail sales dataset covering customers, products, stores, and transactions — uncovering patterns in sales trends, customer demographics, product performance, and discount impact on profitability.

## Dataset

[Retail Sales Dataset](https://www.kaggle.com/datasets/buharishehu/retail-sales-dataset) (Kaggle) — 4 linked tables:
- **Customers** — demographics and membership details
- **Products** — pricing and category information
- **Stores** — store locations and regions
- **Transactions** — fact table with 5,000 sales records (Sep 2023 – Sep 2025)

## Repository Structure

```
DataAnalytics-L1-EDARetailSales/
├── retail_sales_eda.ipynb        # Main analysis notebook
├── data/
│   └── retail_sales_dataset.xlsx # Source dataset (Kaggle)
├── outputs/                      # Exported chart images from the analysis
│   ├── monthly_sales_trend.png
│   ├── quarterly_sales_trend.png
│   ├── customer_age_distribution.png
│   ├── customer_gender_breakdown.png
│   ├── top10_bestselling_products.png
│   ├── revenue_by_category.png
│   ├── correlation_matrix.png
│   ├── discount_vs_profit_margin_by_payment.png
│   └── payment_method_summary_table.png
├── README.md
└── .gitignore
```

## Tech Stack

Python, pandas, matplotlib, seaborn, Jupyter Notebook

## Analysis Covered

- Data cleaning and merge across 4 tables
- Descriptive statistics (mean, median, mode, std) for all numerical fields
- Monthly and quarterly sales trend analysis
- Customer demographics (age group and gender distribution)
- Top 10 best-selling products and revenue by category
- Correlation analysis across numerical variables
- Discount impact on profit margin by payment method

## Key Findings

1. Discounting shows a stronger negative correlation with profit (-0.24) than with revenue (-0.08) — discounts are eroding margin more than driving sales volume.
2. Revenue is more strongly driven by unit price (0.72 correlation) than by quantity sold (0.60) — Electronics and Fashion generate over 3.5x the revenue of Groceries despite comparable sales volume.
3. Customer age and tenure show near-zero correlation with spending behavior (-0.02 to 0.03) — demographic assumptions about "high-value" segments don't hold up statistically in this dataset.

## Business Recommendations

1. Cap discounting policy given its disproportionate impact on margin versus revenue lift
2. Prioritize inventory and marketing investment toward Electronics and Fashion; re-price or bundle Groceries
3. Validate age-based targeting using revenue-per-customer rather than raw headcount before investing in age-specific campaigns

## How to Run

1. Clone this repo
2. Install dependencies: `pip install pandas numpy matplotlib seaborn openpyxl jupyter`
3. Open `retail_sales_eda.ipynb` in Jupyter Notebook and run all cells
