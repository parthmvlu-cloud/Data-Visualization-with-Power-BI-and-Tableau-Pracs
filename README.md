# Jio Supermart Sales Dashboard (Tableau Final Project) 

This is my Tableau project for Data Visualization with Power BI and Tableau (B.Sc.IT Sem 5). I made a dashboard to look at Jio Supermart's sales from 2022 to 2025 and see what's making money and what isn't.

## What's in this repo

- `Jio_Supermart_Sales_Yearly_Sales_Analysis_Dashboard_Project.twbx` - the Tableau workbook
- `Jio_supermart sales.csv` - the dataset
- `dashboard_screenshot.png` - screenshot of the final dashboard

## About the data

The data isn't real company data. I generated it with Python, copying the layout of the Sample Superstore dataset but using Indian states and rupees.

It has 3,193 rows and 19 columns (about 1,700 orders from Jan 2022 to Dec 2025), covering 3 categories, 12 sub-categories, 48 products, 5 regions and 16 states.

Columns: Order ID, Order Date, Ship Date, Ship Mode, Customer ID, Customer Name, Segment, Country, City, State, Region, Product ID, Category, Sub-Category, Product Name, Sales, Quantity, Discount, Profit

## What the dashboard has

- 5 KPI cards: Total Sales, Total Profit, Total Quantity, Profit Ratio, Average Sales
- Line chart for the sales trend
- Lollipop chart for sales by category
- Pie chart for sales by region
- Bar chart for sales by state
- Waterfall chart for profit by sub-category
- Treemap for sales by sub-category
- Scatter plot for sales vs profit

Filters: Year, Category, Region and an AVG(Profit) slider. If you click a bar in Sales by State or the waterfall, the other charts filter too.

## Calculated fields

- Total Sales = `SUM([Sales])`
- Total Profit = `SUM([Profit])`
- Profit Ratio = `SUM([Profit]) / SUM([Sales])`
- Average Sales = `AVG([Sales])`
- Total Quantity = `SUM([Quantity])`
- Cumulative Profit = `RUNNING_SUM(SUM([Profit]))`
- Waterfall Size = `-SUM([Profit])`

## What I found

- Total sales are ₹4.52 crore and profit is ₹52.6 lakh, so the profit ratio is 11.6%
- Technology is the best category: 55% of sales and a 19.1% profit ratio
- Copiers sell the most, and the Multifunction Copier Pro is the top product
- Furniture loses a little money (-1.1%), mostly because of Tables (-10.3%)
- Sales go up every year, from ₹87.6 lakh in 2022 to ₹1.31 crore in 2025
- December is the best month and January is the worst
- West and South bring in about 57% of sales
- Orders with 20% or more discount lose money (-6.8%), the rest earn about 15.1%

## Opening it

Download the `.twbx` file and open it in Tableau Desktop or Tableau Public. Then go to the dashboard tab and try the filters or click on the charts.

Made with Tableau, Python and a CSV file.

Parth R. Kunkunkar
