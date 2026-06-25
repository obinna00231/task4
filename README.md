# order performance center dashboard

## Project Overview
This repository hosts the order performance center Dashboard, an interactive Power BI solution designed to transform transactional e-commerce data into high-impact business intelligence. The dashboard allows stakeholders to dynamically filter data by Payment Method, Coupon Code, Year, and Customer ID to evaluate customer acquisition performance, revenue sustainability, and operational metrics.

## Key Performance Indicators (KPIs)
The top KPI ribbon tracks five high-level metrics crucial for assessing overall business health:
* pending orders:20%.
* Total Revenue: $1.26M in gross sales.
* Total Quantity: 3,535 total items sold.
* Total Orders: 1,200 transactions processed.
* Average Order Value (AOV): $1,054 spent per transaction.

## DAX Functions & Calculations
To build this dashboard, standard and advanced DAX (Data Analysis Expressions) formulas were utilized to aggregate transactional data, compute key ratios, and handle time-series intelligence. Below are the core functional definitions used in this model:

### 1. Total Revenue
Total Revenue = SUM('Cleaned data' [Total Price])

## 2. Total Orders
Counts the unique number of order IDS to establish the total transaction volume.

Total Orders = DISTINCTCOUNT('Cleaned data'[Order ID])

## 3. Average Order Value (AOV)
Calculates the average monetary amount spent every time a customer places an order.

Average Order Value = DIVIDE([Total Revenue], [Total Orders], 0)
## 4. pending order%
 to show what % of your total orders are still pending and not completed yet.
 pending order%=  DIVIDE(CALCULATE(COUNTROWS(Sheet1),Sheet1[OrderStatus] = "pending"),COUNTROWS(Sheet1))
## 5. pending alert
this is the early warning system for orders that are stuck too long.

pending alert =  IF([pending order %]>0.15,1,0)

## Key Insights
1. Revenue peaked in June ($171K), indicating a strong mid-year sales performance.
2. A noticeable decline in revenue and orders occurred from July to September, suggesting possible seasonal demand fluctuations.
3. Chair ($196K) and Printer ($196K) generated the highest revenue among all products, making them top-performing product categories.
4. Phone ($152K) generated the lowest revenue, presenting an opportunity for sales improvement.
5. Credit Card ($264K) and Online Payments ($262K) were the most preferred payment methods, contributing the highest revenue.
6. Instagram ($276K) emerged as the most effective referral source, outperforming Email, Google, Facebook, and direct referrals.
7. Order statuses are relatively balanced, indicating a stable order fulfillment process, though cancellations and returns still require attention.

## Recommendations
1. Increase marketing investments on Instagram campaigns since it generates the highest revenue.
2. Investigate factors behind the July–September sales decline and introduce targeted promotions during low-performing months.
3. Bundle or upsell high-performing products such as Chairs, Printers, and Laptops to maximize revenue.
4. Develop promotional campaigns for lower-performing products like Phones to improve sales contribution.
5. Encourage digital payment adoption through cashback offers and discounts, leveraging customer preference for online and card payments.
6. Monitor cancelled and returned orders closely to identify root causes and improve customer satisfaction.
7. Implement customer retention programs to increase repeat purchases and improve lifetime customer value.

## How to Run/View the project
Dashboard: Open the dashbord file in "order performance center Dashboard Project 4" to interact with the visualization.

## project gallery1
 ![alt text](https://github.com/obinna00231/task4/blob/fab03da0a494fd695aa9200e662350ab26b6bb11/decodelab%20project3/decodelab.pbix)

## Project Gallery

![alt text](https://github.com/obinna00231/task4/blob/f37c8849fcee4154bd58e12acfd250c1a211eee5/decodelab%20project3/Camera%20Roll/Capture.PNG)
