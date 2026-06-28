1. Business Problem Summary
The business needed a way to understand what is driving sales and profit across its store portfolio. Leadership wanted answers to questions like: which regions and product categories are most profitable, whether discounts are helping or hurting the business, how returns are distributed across segments, and whether shipping speed affects performance.

This dashboard was built to answer those questions visually so leadership can make faster and better-informed decisions without having to read through raw data.

2. Dataset Description
The dataset contains one row per order with 20 columns covering sales transactions from January 2024 to December 2025.

Column	Description
order_id	Unique identifier for each order
order_date	Date the order was placed
ship_date	Date the order was shipped
customer_id	Unique identifier for each customer
customer_segment	Consumer, Corporate, or Home Office
region	East, North, South, or West
state	Indian state where the order was placed
city	City where the order was placed
category	Furniture, Office Supplies, or Technology
sub_category	13 product sub-categories
product_name	Name of the product ordered
ship_mode	First Class, Same Day, Second Class, or Standard Class
sales	Revenue from the order
quantity	Number of units ordered
discount	Discount applied (0 to 0.35)
profit	Profit from the order (can be negative)
return_flag	1 if the order was returned, 0 if not
delivery_days	Number of days between order and shipment
customer_rating	Customer satisfaction rating (1–5 scale)
campaign_channel	Email, Organic, Paid, Referral, or Social
Note: return_flag was converted to String type in Tableau. customer_rating has 32 missing values which Tableau handles automatically by excluding them from averages.

3. Tableau Workbook Description
The workbook contains 7 individual sheets and 1 executive dashboard:

Sheet	Purpose
Sales Trend View	Shows monthly sales trend by category over 2024–2025
Regional Performance View	Compares sales and profit across the 4 regions
Category Profitability View	Shows sales and profit margin by category and sub-category
Customer Segment View	Compares performance across Consumer, Corporate and Home Office
Shipping Performance View	Shows sales and profit by shipping mode and delivery speed
Discount vs Profit View	Scatter plot showing relationship between discounts and profit
Return Analysis View	Shows return rates by category, segment and region
Executive Dashboard	Combines all views with KPI cards and interactive filters
4. Calculated Fields Created
Five calculated fields were created in Tableau:

Field	Formula	Type
Profit Margin	SUM(profit) / SUM(sales)	Measure
Cost	sales - profit	Measure
Average Order Value	sales / quantity	Measure
Return Rate	SUM(IF return_flag = "1" THEN 1 ELSE 0 END) / COUNT(order_id)	Measure
Shipping Delay Bucket	IF delivery_days = 0 THEN "Same Day" ELSEIF delivery_days <= 2 THEN "Fast (1-2 days)" ELSEIF delivery_days <= 4 THEN "Standard (3-4 days)" ELSEIF delivery_days <= 6 THEN "Slow (5-6 days)" ELSE "Very Slow (7+ days)" END	Dimension
5. Dashboard Components
The executive dashboard includes:

3 KPI cards at the top showing Total Sales, Total Profit, and Return Rate at a glance
Sales Trend View — line chart showing monthly sales by category
Regional Performance View — bar chart comparing regions
Category Profitability View — horizontal bar chart with profit margin colour coding
Customer Segment View — grouped bar chart by segment and category
Shipping Performance View — stacked bar chart by shipping mode and delivery speed
6. Filters and Interactions Used
Filters added to the dashboard:

Region — filter by East, North, South, West
Category — filter by Furniture, Office Supplies, Technology
Customer Segment — filter by Consumer, Corporate, Home Office
Order Date — filter by date range
Ship Mode — filter by shipping type
All filters are set to apply to all worksheets using the same data source, so selecting any filter value updates every chart on the dashboard at the same time.

Action filter: A click-to-filter action was added so clicking on any data point in any chart automatically filters all other charts to match that selection. Clearing the selection restores all values.

7. Key Business Insights
Total sales of 217,017,652 and total profit of 33,306,313 across 4,200 orders
Overall profit margin is 15.3% and return rate is 4.5%
Technology is the most profitable category at 18.2% margin — Copiers, Accessories and Phones are the top three sub-categories by profit
Furniture has only a 6.9% margin and a 7.7% return rate — the weakest category on both measures
South region leads in sales (64,693,707) and profit (9,987,912)
Orders with discounts above 20% average only 2,915 in profit compared to 9,821 for lower-discount orders
288 of 4,200 orders are loss-making (negative profit)
Organic campaign channel generates the most profit (13,444,457) — more than double any other channel
Home Office segment has the highest return rate at 5.7%
8. Dashboard Story Summary
The dashboard tells a clear story across its seven views. Technology is carrying the business — it generates the majority of profit at strong margins while Furniture generates volume but little return. The South region consistently outperforms others. High discounts are hurting profitability, with a clear negative relationship visible in the scatter plot. Furniture also has the highest return rate which compounds its already thin margins. The Organic channel is the most efficient revenue source and should be prioritised. Sales grew modestly from 2024 to 2025 indicating a stable but not rapidly growing business.

9. Assumptions and Limitations
Assumptions made:

return_flag values of "1" are treated as returned orders and "0" as not returned
delivery_days of 0 means the order was shipped on the same day it was placed
Profit figures are gross profit — overhead costs like rent and salaries are not included
customer_rating missing values (32 out of 4,200) are excluded from rating averages
Limitations:

Only two years of data are available — long-term seasonal patterns cannot be confirmed
Return reasons are not recorded — we can see which orders were returned but not why
Campaign channel cost data is not included — so true marketing ROI cannot be calculated
The dashboard was built and tested in Tableau Public which has some feature limitations compared to Tableau Desktop
Geographic analysis is limited to region level — state and city level maps could provide more granular insights