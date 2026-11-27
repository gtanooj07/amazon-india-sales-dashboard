# Amazon India Sales Dashboard

**Student:** [Your Name]  |  **Tool used:** Microsoft Excel

## 1. Project overview

This project analyzes Amazon India sales data to understand sales performance, profitability, product and category performance, order statuses, payment methods, fulfillment methods, and geographic trends.

The dashboard is designed to help business managers and decision-makers monitor key performance indicators, identify business trends, and make data-driven decisions.

## 2. Dataset

- **Number of records:** 10,000
- **Number of original columns:** 13
- **Date range:** January 2024 – August 2026
- **Source:** Amazon Sales Data India dataset

The dashboard covers the four main sections specified in the project brief:

1. **Overall Sales & Profit Performance:** Total sales, total profit, total orders, units sold, average order value, profit margin, and monthly sales and profit trends.
2. **Category & Product Performance:** Category-wise sales, profit, units sold, and top 10 products by sales.
3. **Order Status & Revenue Loss:** Delivered, shipped, returned, and cancelled orders; return and cancellation rates; and category-wise returns and cancellations.
4. **Payment, Fulfillment & Geographic Performance:** Sales and profit by payment method and fulfillment method, along with state-wise sales, profit, and orders.

## 3. Data preparation

**Checks performed:**
- Checked for missing values.
- Checked for duplicate records and duplicate Order IDs.
- Reviewed column data types.
- Checked the date range and date format.
- Verified that the dataset contained 10,000 records and 10,000 unique Order IDs.

**Fields created:**
- `Order_Date_Parsed` – converts the original date text into an Excel date value for analysis.
- `Month_Year` – groups orders by month and year for monthly trend analysis.
- `Year` – extracts the year for dashboard filtering.

The original `Order_Date` column was preserved.

**Treatment of cancelled and returned orders:**

Cancelled and returned orders were retained in the dataset and analyzed separately using order status. Return Rate and Cancellation Rate were calculated using the total number of orders as the denominator.

Sales and profit totals represent the values recorded in the dataset. They were not adjusted by subtracting returns or cancellations because the dataset does not provide separate refund or recovered-revenue amounts.

## 4. KPI definitions

- **Total Sales** = Sum of `Total_Sales_INR` = ₹15,57,89,893.89
- **Total Profit** = Sum of `Profit_INR` = ₹3,31,67,008.49
- **Total Orders** = Count of unique `Order_ID` = 10,000
- **Total Units Sold** = Sum of `Quantity` = 24,926
- **Average Order Value (AOV)** = Total Sales / Total Orders = ₹15,578.99
- **Profit Margin %** = (Total Profit / Total Sales) × 100 = 21.29%
- **Return Rate %** = (Returned Orders / Total Orders) × 100 = 4.85%
- **Cancellation Rate %** = (Cancelled Orders / Total Orders) × 100 = 5.00%

## 5. Dashboard preview

![Dashboard](screenshots/dashboard.png)

## 6. Key findings

1. The dataset contains **10,000 orders** with total recorded sales of **₹15.58 crore**.
2. The business generated approximately **₹3.32 crore in recorded profit**, resulting in a profit margin of **21.29%**.
3. The return rate is **4.85%**, while the cancellation rate is **5.00%** of total orders.

## 7. Recommendations

1. **Investigate returns:** Analyze categories and products with higher return counts to identify possible product-quality, description, or customer-expectation issues. This recommendation is supported by the 4.85% return rate.
2. **Reduce cancellations:** Review cancellation patterns across categories and fulfillment methods to identify opportunities to improve order processing and fulfillment. The cancellation rate is 5.00%.
3. **Monitor profitability:** Regularly compare sales and profit across categories, products, payment methods, and states to identify areas where profitability can be improved.

## 8. How to use the dashboard

Use the dashboard's PivotTable charts and slicers to explore sales performance across different dimensions.

**Slicers available:** [List the slicers actually added and connected to the dashboard, such as Year, Month-Year, Category, Payment Method, and Ship State.]

Select a slicer value to filter the connected PivotTables and charts. Clear the selection to return to the overall view.

## 9. Limitations

- The dataset covers only the period from January 2024 to August 2026.
- The dataset does not provide separate refund amounts or recovered revenue for returned orders.
- Sales and profit totals are based on the recorded dataset values and are not adjusted for cancelled or returned orders.
- The analysis is limited to the fields available in the dataset.
- The dashboard describes historical performance and does not predict future sales or profit.
