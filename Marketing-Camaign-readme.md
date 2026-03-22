# Marketing Campaign Analysis

A data analysis project focused on understanding the performance of different marketing campaigns across channels, locations, and customer segments. The dataset is fictional but structured to reflect real-world marketing metrics, which made it useful for practising campaign performance analysis.

---

## Tools Used

- **Python** — data cleaning, feature engineering, exploratory analysis
- **Pandas / NumPy** — data manipulation and aggregation
- **Matplotlib / Seaborn** — statistical visualizations
- **Tableau** — interactive dashboard and final presentation

---

## Dataset Overview

The dataset covers multiple companies running different types of marketing campaigns across various locations, channels, and target audiences. Key columns include campaign type, channel used, target audience, customer segment, location, language, impressions, clicks, ROI, engagement score, acquisition cost, and conversion rate.

A few things were handled during cleaning and preparation:
- `Acquisition_Cost` was stored as a string with `$` and `,` symbols — stripped and converted to float
- Dates were converted using `datetime` and split into day, month, and year columns
- `All Ages` in the target audience column was replaced with `Age Not Revealed` for clarity
- Two new columns were engineered:
  - `Conversion_Rate_Percent` — conversion rate scaled to percentage (`× 100`)
  - `Click_Through_Rate` — calculated as `(Clicks / Impressions) × 100`
- The original `Conversion_Rate` and `Date` columns were dropped after extraction

---

## Objectives

1. Which campaign type generates the highest ROI?
2. Which marketing channel performs best in terms of ROI?
3. Which target audience has the highest conversion rate?
4. Which customer segment is the most profitable?
5. Which location delivers the highest ROI?
6. Which campaign type has the highest engagement score?

---

## Key Findings

- **Influencer** campaigns have the highest average ROI (5.011), followed by Search (5.008) and Display (5.006) — though the differences are marginal, likely due to the fictional nature of the data.
- **Facebook** is the top-performing channel by ROI (5.018), followed by Website (5.014) and Google Ads (5.003).
- **Men aged 18–24** have the highest conversion rate (8.023), particularly for food-related products.
- **Foodies** are the most profitable customer segment by ROI, followed by Tech and Health segments.
- **Miami** generates the highest ROI (5.012) across all locations — likely tied to its profile as a high-traffic tourist city.
- **Display** campaigns have the highest average engagement score, ahead of Email and Social Media.
- Outliers were found in the `Click_Through_Rate` boxplot — possibly unusually high-performing or low-performing individual campaigns.

---

## Correlations

| Variables | Relationship |
|---|---|
| Conversion Rate vs ROI | Near zero (-0.001) |
| Engagement Score vs ROI | Near zero (0.00058) |
| Clicks vs Conversion Rate | Near zero (0.000269) |

All three correlations are essentially flat, which is the most interesting finding in the dataset. Higher clicks don't lead to more conversions, higher engagement doesn't move ROI, and conversion rate has almost no bearing on ROI either. In a real dataset this would raise serious questions about campaign efficiency — here it's largely a reflection of the data being synthetic.

---

## Recommendations

1. **Influencer campaigns** show the highest ROI on average — worth prioritising in budget allocation, especially for food and lifestyle categories where the 18–24 male demographic is active.
2. **Facebook** consistently outperforms other channels and should remain the primary platform for paid campaigns.
3. **Miami and similar high-footfall locations** are strong performers — geographical targeting around tourist and urban hubs could yield better returns.
4. Since **clicks and engagement don't strongly predict conversions or ROI**, optimising purely for click volume or likes is not an effective strategy. Focus should shift toward conversion-focused metrics instead.
5. **Foodies and Tech segments** are the most responsive — campaigns tailored specifically to these groups are likely to see better returns than broad audience targeting.

---

## Limitations

The dataset is fictional, which is the primary limitation. The near-zero correlations between most variables and the very small differences in ROI across segments are a direct result of this — real campaign data would show much stronger patterns and variance. The findings here are useful for practising the analytical process, but should not be taken as representative of actual marketing performance.

---

## Files

| File | Description |
|---|---|
| `marketing_campaign_dataset.csv` | Raw dataset |
| `Cleaned_Marketing.csv` | Cleaned dataset after preprocessing |
| `analysis.ipynb` | Full Python notebook |
| Tableau Dashboard | Interactive visualizations (separate) |
