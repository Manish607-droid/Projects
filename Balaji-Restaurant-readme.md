# Balaji Fast Food Sales Analysis

This was a personal project I worked on to practice data analysis using a real-world restaurant dataset. The dataset contains 1000 transaction records from Balaji Fast Food covering 2022 and 2023. 

---

## What I Used

- **Python** — data cleaning, EDA, statistical analysis
- **Pandas / NumPy** — data manipulation
- **Matplotlib / Seaborn** — exploratory visualizations
- **Tableau** — final dashboard and interactive charts

---

## What the Data Looks Like

The dataset had 10 columns including item name, item type, item price, quantity, transaction amount, transaction type, received by, time of sale, and date. The date column was a bit messy — some entries used `-` as separator and others used `/`, so I standardised that before converting to datetime.

There was also a small issue with null values in the `transaction_type` column which I filled with `'Unknown'` rather than dropping the rows entirely.

---

## Questions I Tried to Answer

1. What is the total revenue generated in each year?
2. Which items bring in the most revenue?
3. What time of day sees the highest sales?
4. Which items are the most and least expensive?
5. Which items are sold the most by quantity?
6. What payment method do customers prefer?
7. Does gender affect transaction handling patterns?
8. Are there any outliers in transaction amounts?

---

## Key Findings

- **Sandwich** is the most expensive item (Rs 60) and also the top revenue generator (Rs 65,820) — but it's not the most sold.
- **Cold Coffee** is the most sold item (1,361 units) despite being priced lower. Sugarcane Juice and Panipuri follow closely.
- **Night** generates the most revenue (Rs 62,075), which is a bit surprising and might suggest a dinner crowd or bulk orders.
- **Cash** is still the preferred payment method (476 transactions), though online isn't too far behind (417).
- **Male** staff handled slightly more transactions (512 vs 488), though the gap is small enough that it's not really significant.
- Outliers were found in `transaction_amount` — likely from bulk or catering orders rather than data errors.

---

## Correlations

| Variables | Relationship |
|---|---|
| Price vs Quantity | Weak positive |
| Price vs Transaction Amount | Strong positive |
| Quantity vs Transaction Amount | Strong positive |

The strong correlation between quantity and transaction amount makes sense — more items ordered means a higher bill.
The weak correlation between price and quantity is interesting though — it suggests customers don't drastically change
how much they buy based on price alone, at least for this range.

---

## Recommendations

1. Sandwich has high revenue but isn't the most sold — worth testing a temporary price drop or running a promotion to push volume.
2. Cold Coffee, Sugarcane Juice and Frankie are consistent performers for both male and female-handled transactions. Quality here should be maintained.
3. Panipuri sells a lot but at Rs 20 it contributes little to revenue — a small price increase (Rs 25–30) could be tested to see if demand holds.
4. Aalopuri and Vadapav are the weakest sellers. A combo deal pairing them with popular items could help move them.

---

## Limitations

The dataset only covers parts of 2022 and 2023 — not full years. 
So any trend analysis (seasonal patterns, year-over-year growth) is limited.
A more complete dataset would allow for better forecasting.

---

## Files

| File | Description |
|---|---|
| `Balaji Fast Food Sales.csv` | Raw dataset |
| `Balaji Restaurant cleaned.csv` | Cleaned dataset after preprocessing |
| `analysis.ipynb` | Full Python notebook |
| Tableau Dashboard | Interactive visualizations (separate) |
