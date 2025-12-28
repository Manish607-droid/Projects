# Multiple Restaurant Sales Analysis

## Tools Used
- Google Colaboratory(libraries used: NumPy, Pandas, Matplotlib, Seaborn)
- Tableau (For Visualization)

## Project Objective
The major goal of this project was to analyze the restaurant, manager and customer insights in different locations of two months (November and December) which consists:
1) Most Preferred Payment Method
2) Most Selling Product - By Quantity & By Revenue ?
3) Which city had maximum revenue , or , Which Manager earned maximum revenue ?
4) Average Revenue of two months
5) Average Revenue of November & December month.
6) Is revenue increasing or decreasing over time?
7) Expensive and cheapest product
8)  Which city sells the most and least
9)  Most and least purchasing type

## About the dataset
This is the dataset of restaurants operating in different countries. This dataset contains information of sales of two months (November and December). 
There are 9 columns in this dataset which are as follows:

1) Order ID: A unique identifier for each sales order. This can be used to track individual transactions.

2) Order Date: The date when the order was placed. This column is essential for time-series analysis, such as identifying sales trends over time or seasonality.

3) Product: The name or type of the product sold. This column is crucial for analyzing sales performance by product category.

4) Price : The unit price of the product. This, along with 'Quantity Ordered', is used to calculate the total price of each order.

5) Quantity : The number of units of the product sold in a single order. This is a key metric for calculating revenue and understanding sales volume.

6) Purchase Type : The order was made online or in-store or drive-thru.

7) Payment Method : How the payment for the order was done.

8) Manager : Name of the manager of the store.

9) City : The location of the store. This can be used for geographical analysis of sales, such as identifying top-performing regions or optimizing logistics.

## Steps performed
The steps performed for this data are as follows:

## 1) Data Cleaning
- Unnecessary spaces were removed and text were standardized for understanding and to remove the duplicates.
-  Quantity was at float which was complex. Hence, it was converted to integer.
-  Date were converted using the function datetime. Additionally, the date were separated to day, month and year and made in separate columns.
-  Payment method was made more simple by replacing the term Credit Card with Card Payment.
-  Unnecessary columns were removed to avoid confusion.

 ## 2) Featured Engineering 
  - Revenue Column was created as it was required to see which products, Managers and Cities were generating more revenue.
  - Revenue = Price * Quantity

## 3) Analysis 
Through the pandas library the following questions were analyzed to gain more insights:

1) Most Preferred Payment Method
2) Most Selling Product - By Quantity & By Revenue ?
3) Which city had maximum revenue , or , Which Manager earned maximum revenue ?
4) Average Revenue of two months
5) Average Revenue of November & December month.
6) Is revenue increasing or decreasing over time?
7) Expensive and cheapest product
8)  Which city sells the most and least
9)  Most and least purchasing type

## 4) Visualization

- Bar Charts for top products by quantity, top managers, prices of products, avg revenue by month
- Horizontal Bar Chart for top products by revenue.
- Pie Chart for preferred purchase types and circle charts for payment method.
- Line graph to compare total revenue and quantity by month and total revenue per city
-  Box Plots have been used to review the outliers.
-  Heatmaps and pairplots for correlations.

## Key Insights

- Most purchases are done through online where customers mostly preferred to pay by cards.
- Beverages are sold most in quantity (34,938 units) whereas Burgers generate more revenue (376658.04).
- Lisbon is the city which generates maximum revenue (241,509.38) and Joao Silva generates maximum revenue as manager(241,509.38).
- There is a negative correlation between price and quantity. Positive correlation between quantity and revenue.
- There is a positive correlation between price and revenue(0.76).
- The revenue has increased in December (436,989.94) when compared to November (331,841.41).
- The outliers detected in the  revenue boxplot might be due to bulk orders.

## Recommendations

- Restaurant should focus more on online sales and keep customer convenience as top priority.
- Products like Burgers and Fries which generates high revenue should be promoted more often.
- Expensive Products like Chicken Sandwiches are sold less in quantity. Hence, the restaurant can experiment with different pricing strategies to increase the sales.
- Top performing managers and cities should be kept as a benchmark.
- More data should be collected to see and predict the long term trends.

