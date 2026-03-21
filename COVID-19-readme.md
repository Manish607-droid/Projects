# COVID-19 Data Analysis

A data analysis project exploring COVID-19 trends across different countries using Python. The dataset was sourced from Kaggle and covers confirmed cases, deaths, and recoveries up to April 2020.

---

## Dataset

- **Source:** Kaggle
- **File:** `covid_19_data.csv`
- **Original columns:** Date, State, Region, Confirmed, Deaths, Recovered
- **Rows:** ~321 records after cleaning

---

## What This Project Does

- Cleans and preprocesses raw COVID-19 data (handles nulls, drops irrelevant columns, parses dates)
- Engineers new features: `Mortality_Rate` and `Recovery_Rate`
- Answers key questions about which countries were hit hardest
- Visualizes findings using Matplotlib and Seaborn
- Exports a cleaned dataset as `Cleaned COVID Dataset.csv`

---

## Questions Answered

1. Which 10 countries had the highest confirmed cases?
2. Which 10 countries had the most deaths?
3. Which countries had the highest recoveries?
4. How do confirmed cases, deaths, and recoveries correlate with each other?

---

## Key Findings

- **USA** had the highest confirmed cases and deaths as of the dataset period
- **Spain** led in recoveries, followed by the US and Germany
- **Italy and UK** had high case and death counts but lagged in recovery numbers
- There is a **strong positive correlation** between confirmed cases and both deaths and recoveries — meaning countries with more cases also tended to have more of both outcomes

---

## Libraries Used

| Library | Purpose |
|---|---|
| `pandas` | Data loading, cleaning, and manipulation |
| `numpy` | Sorting and array operations |
| `matplotlib` | Bar charts for top 10 countries |
| `seaborn` | Pairplot and correlation heatmap |

---

## How to Run

1. Clone this repository
2. Make sure you have the required libraries installed:
   ```
   pip install pandas numpy matplotlib seaborn
   ```
3. Place `covid_19_data.csv` in the same directory as the notebook
4. Open the notebook in Jupyter or Google Colab and run all cells

---

## Output

- Bar charts showing top 10 countries by confirmed cases, deaths, and recoveries
- A correlation heatmap across the three main metrics
- `Cleaned COVID Dataset.csv` — the processed version of the data ready for further analysis

---

## Notes

This project was done for personal learning and portfolio purposes. The data reflects a specific period early in the pandemic and does not represent the full timeline of COVID-19.
