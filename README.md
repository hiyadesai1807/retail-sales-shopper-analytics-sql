# Retail Sales & Shopper Analytics using SQL

Analysis of 541,909 e-commerce transactions (UCI Online Retail dataset) using SQL window functions, measuring the kinds of metrics used in retail measurement: market share, sales growth, top products and shopper behaviour.

## What I did
- Checked data quality first: found 9,288 cancellations, 135,080 rows without a customer ID, and invalid quantities and prices
- Cleaned the data in SQL, leaving 530,104 valid rows from 4,338 customers in 38 countries
- Calculated market share by country, month-on-month growth and top products per country using window functions (LAG, RANK, SUM OVER)
- Measured shopper metrics: repeat-purchase rate, basket size and basket value
- Flagged unusual sales weeks using rolling z-scores

## Key findings
- The United Kingdom accounts for 84.6% of revenue (about £9.0M of £10.7M)
- Revenue peaked in November 2011 (about £1.51M), showing strong pre-Christmas seasonality
- December 2011 appears to drop 57.7%, but it is a partial month (data ends 9 December), not a real decline
- 65.6% of customers bought more than once; the average basket of about 280 units suggests many customers are wholesalers
- About £395K (roughly 3.7% of revenue) came from non-product rows such as postage, Amazon fees and manual adjustments. Before removing them, "DOTCOM POSTAGE" ranked as the top-selling product
- After cleaning, the best-selling product is the Regency Cakestand 3 Tier (about £174.5K)

## Limitations
- Data from a single retailer, not a whole market
- About 25% of transactions lack a customer ID, so shopper metrics cover identified customers only

## Tools
Python, SQL, Pandas, Matplotlib
