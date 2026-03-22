# Superstore Sales – Exploratory Data Analysis

An end-to-end EDA project on a US-based retail superstore dataset. The goal was to uncover which regions, categories, and customer segments were driving sales and profit — and to give actionable recommendations based on the findings.

---

## Dataset

- **Source:** Sample - Superstore.csv (widely available retail dataset)
- **Rows:** 9,994 transactions
- **Columns:** 21 original columns covering orders, customers, products, sales, discounts, and profit
- **Period covered:** 2014 – 2017

---

## What This Project Does

- Checks for and confirms zero duplicates and zero null values
- Engineers new features: `Cost Per Unit`, `Profit Margin`, `Order Month`, `Order Day`, `Order Year`
- Renames `Same Day` shipping to `Premium First Class` to better reflect its business tier
- Drops columns not useful for analysis (Ship Date, Country, Postal Code, raw Date)
- Answers 5 core business questions through groupby analysis and visualizations
- Identifies and documents outliers in Sales and Quantity — and explains why they were kept
- Calculates correlations between key financial metrics
- Exports a cleaned file: `Cleaned Superstore.csv`

---

## Business Questions Answered

1. Which region has the highest sales and profit?
2. What are the most and least profitable categories and sub-categories?
3. Which customer segment drives the most revenue?
4. Which year had peak sales?
5. Which shipping mode is most used?

---

## Key Findings

- **West Region** led in both total sales (~$725K) and profit (~$108K)
- **Technology** was the most profitable category; **Furniture** was the least — with Tables and Bookcases operating at a loss
- **Consumer segment** drove the most revenue (~$1.16M), well ahead of Corporate and Home Office
- Sales grew consistently year over year, with **2017 being the peak year** (~$733K)
- **Standard Class** was by far the most used shipping mode (5,968 orders)
- Higher discounts are negatively correlated with profit (r = -0.22), while higher sales correlate positively with profit (r = 0.48)

---

## Recommendations

- **Central Region** likely gave heavier discounts to boost sales, which hurt profit margins. Discount strategy should be reviewed there.
- **Furniture** had the highest average discount (17%) across all categories. Reducing it to around 10–12% could improve profitability — the rough estimate from the correlation suggests ~1% improvement in profit per 5% discount reduction.
- **Tables** had the worst sub-category loss (-$17,725). Pricing and discount policy for tables specifically needs a re-evaluation.
- Technology and Office Supplies are performing well — focus should be on maintaining product quality and customer service in these categories.

---

## Libraries Used

| Library | Purpose |
|---|---|
| `pandas` | Data cleaning, feature engineering, groupby analysis |
| `numpy` | Quantile and outlier calculations |
| `matplotlib` | Bar charts, pie chart, line plot, box plots |
| `seaborn` | Scatter plot, line plot, heatmap |

---

## Visualizations Included

- Bar charts: Sales and profit by region, category, shipping mode
- Pie chart: Revenue share by customer segment
- Line plot: Total yearly sales trend and category-wise sales trend
- Scatter plot: Discount vs Profit relationship
- Box plots: Outlier detection for Sales and Quantity
- Heatmap: Correlation matrix for Sales, Quantity, Discount, and Profit

---

## Outlier Handling

Outliers were detected in both Sales and Quantity using the IQR method. They were intentionally kept because they represent genuine bulk business transactions — removing them would have distorted the analysis and led to misleading conclusions.

---

## Limitations

- The dataset only covers 4 years (2014–2017), which limits the reliability of long-term trend analysis.
- No customer demographics or external market data is available to explain regional performance differences.

---

