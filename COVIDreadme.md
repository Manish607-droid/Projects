## COVID CASE

## Tools Used
- Google Colaboratory(libraries used: NumPy, Pandas, Matplotlib, Seaborn)
- Tableau (For Visualization)

## Project Objective
The major objective of this project was to analyze the number of people who were confirmed, deaths, and recovered from COVID-19 on April 29, 2020 which consists:
1) The top 10 region that has the highest confirmed and death cases
2) Which country has the highest recovery?

## Dataset Overview
This dataset contains the number of people from countries of COVID-19 cases recorded on April 29, 2020. This dataset contains the information of only one day (April 29, 2020).
It consists of 6 columns which are as follows:

1) Date : Represents the date when the data was recorded. In this dataset, all records are from April 29, 2020.

2) Region : The name of the country or territory for which COVID-19 data is recorded.

3) Confirmed : The total number of confirmed COVID-19 cases reported in that region as of April 29, 2020.

4) Deaths : The total number of deaths attributed to COVID-19 in that region as of April 29, 2020.

5) Recovered : The total number of individuals who recovered from COVID-19 in that region by the recorded date.

## Steps Performed
The steps performed on this dataset are as follows:

## 1. Data Cleaning
- The maximum values in the states column were empty. Hence, they were removed to make the data more clean
- Date were converted using Datetime. Here, the dates were separated to days, months and years.
- After the dates were separated into different columns. Then, the date column was further removed.

## 2. Featured Engineering
- To new columns Mortality rate and recovery rate were created. It was done to see which countriws had the highest recovery and mortality rate.
- Recovered rate = (Recovered/Confirmed) * 100
- Mortality rate = (Death/Confirmed) * 100

## 3).Analysis
- Through pandas some questions were analyzed for more depth:
1) The top 10 region that has the highest confirmed and death cases
2) Which country has the highest recovery?

## 4. Visualization
- Using the Matplotlib libraries various charts were created for visualzation of the data

- Horizontal Bar Charts were used for Top 10 Countries For Most Confirmed Cases
- Bar Charts were used for Top 10 COuntries for Most Deaths by COVID-19 and Top 10 Countries For Most Recovered Cases form CoVID-19.
- Heatmaps and Pairplots for Correlations.


## 5. Insights

-  USA had the most number of COVID-19 Cases reported on April 29,2020 (1039909).
-  USA had the most number of deaths from COVID-19 reported on APril 29, 2020 (60967).
-  Spain had the most number of recovered cases against COVID-19 on April 29, 2020 (132929).
-  There is a positive correlation between confirmed Cases and deaths (0.907).
-  There is a positive correlation between recovered cases and deaths (0.519).
-  There is a positive correlation between confirmed cases and recovered (0.596).

## 6. Recommendations
- Although countries like Italy and UK fall under one of the highest death and reported cases but in terms of recovery they are little behind. Hence,
  they should check healthcare responses and make more people aware about the cases.
- Since the data consists the information of only one day hence, more data should be collected to predict the long term trends in order to provide accurate insights.

- 
