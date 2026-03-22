# Multiple Restaurant Sales Analysis

A sales analysis project focused on restaurant operations across multiple cities, covering two months of transaction data (November and December). The goal was to understand what drives revenue, how customers behave, and where the business is performing well or falling short.

---

## Tools Used

- **Python** — data cleaning, feature engineering, exploratory analysis
- **Pandas / NumPy** — data manipulation and aggregation
- **Matplotlib / Seaborn** — statistical visualizations
- **Tableau** — interactive dashboard and final presentation

---

## Dataset Overview

The dataset contains 9 columns — order ID, order date, product, price, quantity, purchase type, payment method, manager, and city.

A few things were addressed during cleaning:
- Quantity was stored as float and converted to integer
- Dates were standardised using `datetime` and split into day, month, and year columns
- Inconsistent text casing and unnecessary spaces were cleaned to avoid duplicates
- Payment method entries were standardised (e.g. "Credit Card" → "Card Payment")
- A **Revenue** column was engineered as it was central to most of the analysis (`Revenue = Price × Quantity`)

---

## Objectives

1. What is the most preferred payment method?
2. Which product sells the most — by quantity and by revenue?
3. Which city and manager generated the highest revenue?
4. What is the average revenue across both months?
5. How does revenue compare between November and December?
6. Is revenue trending up or down over time?
7. What are the most and least expensive products?
8. Which city has the highest and lowest sales?
9. What is the most and least used purchase type?

---

## Key Findings

- **Online** is the dominant purchase channel and card payment is the most preferred method.
- **Beverages** lead in quantity sold (34,938 units) but **Burgers** generate the most revenue (Rs 376,658) — volume doesn't always translate to revenue.
- **Lisbon** is the highest revenue city (Rs 241,509) and is managed by **Joao Silva**, making him the top-performing manager in the dataset.
- Revenue grew from Rs 331,841 in November to Rs 436,989 in December — a notable increase, though the cause isn't entirely clear from two months of data alone.
- Outliers detected in the revenue boxplot are most likely bulk or catering orders.
- There is a **negative correlation** between price and quantity, meaning higher-priced items sell in lower volumes — expected, but worth monitoring.
- Strong positive correlations exist between quantity and revenue, and between price and revenue (0.76).

---

## Correlations

| Variables | Relationship |
|---|---|
| Price vs Quantity | Negative |
| Price vs Revenue | Strong positive (0.76) |
| Quantity vs Revenue | Strong positive |

The negative relationship between price and quantity is something the business should keep in mind when adjusting pricing — pushing prices too high on already slow-moving items could further reduce sales volume.

---

## Recommendations

1. **Online ordering** is the preferred channel and should be prioritised in terms of user experience and operational focus.
2. **Burgers** are the strongest revenue driver — consistent quality and targeted promotions here would have the most impact.
3. **Chicken Sandwiches** are among the priciest items but sell in low quantities. A revised pricing strategy or stronger marketing could help improve their contribution.
4. **Lisbon** is outperforming other locations — understanding what works there and applying it to lower-performing cities is worth exploring.
5. The November to December revenue increase is encouraging, but given this is a festive period, it may be seasonal. A longer dataset would confirm whether this is a genuine upward trend.

---

## Limitations

The dataset only covers two months, both of which fall in the festive season. This makes it difficult to distinguish between genuine business growth and seasonal spikes. Long-term trend analysis, forecasting, and seasonality assessment would require at least a full year of data.

---

## Files

| File | Description |
|---|---|
| `restaurant_sales.csv` | Raw dataset |
| `restaurant_cleaned.csv` | Cleaned dataset after preprocessing |
| `analysis.ipynb` | Full Python notebook |
| Tableau Dashboard | Interactive visualizations (separate) |
