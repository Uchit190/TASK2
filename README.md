# Sales Dashboard - Power BI Project

## Overview

This project is a comprehensive Sales Dashboard created using Power BI to analyze and visualize key sales metrics like total sales, orders, customer insights, and product performance.

## Key Metrics

- **Total Sales:** 2.26M  
- **Total Orders:** 4922  
- **Unique Customers:** 793  
- **Average Sales per Order:** 459.48  
- **Repeat Customer %:** 0.99%

## Features

- **Time Series Analysis:**  
  Visualizes sales trends over time using line charts.

- **Category & Sub-Category Performance:**  
  Highlights top-selling product categories with bar charts.

- **Customer Insights:**  
  Shows unique customers and repeat customer percentage using DAX formulas.

- **Analytics Tools:**  
  - Min, Max, Average, and Median lines  
  - Anomaly detection (optional)  
  - Trend Line and Forecasting (enabled on line chart with date axis)

## DAX Measures

Repeat Customer % = 
DIVIDE(
 CALCULATE(DISTINCTCOUNT(Sales[CustomerID]), FILTER(Sales, Sales[Order_Count] > 1)),
    DISTINCTCOUNT(Sales[CustomerID])
)
