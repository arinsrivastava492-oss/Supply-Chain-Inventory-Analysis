# Supply Chain & Inventory Analysis (Project 3)

This is my third project for the Data Analyst program. The task was to take a supply chain dataset (15,000 order records) and figure out what's going on with stock levels, supplier delays, and which products are actually making money.

## Files in this repo

- **supply_chain_cleaned.csv** – the cleaned dataset. Checked it for duplicates, missing values, bad dates and negative stock numbers. Turned out the data was already pretty clean, so nothing major had to be removed.

- **supply_chain_analysis.xlsx** – this is the main file. It has the cleaned data, an analysis dashboard, and separate sheets breaking things down by product, supplier, warehouse and category. Also a monthly trend sheet and one comparing delivery delays to sales.

- **supply_chain_insights_summary.md** – a short writeup answering the business questions below.

## About the Excel file

Open the **Dashboard** sheet first — that's the main view. There are two dropdowns at the top (Year and Category) that filter everything on the sheet: the KPI numbers and all the charts update automatically when you change them.

Charts included:
- Inventory status (how much is overstocked/understocked/out of stock)
- Top selling products
- Supplier performance (delays + avg shipping time)
- Delivery delay trend by month
- Stock on hand vs units sold

Everything is built with formulas, nothing is a typed-in number, so if you change the delay/overstock thresholds on the Summary sheet the whole workbook recalculates.

## Business questions I was trying to answer

1. Which products are frequently out of stock?
2. Which suppliers have the highest delivery delays?
3. Which products generate the highest profit?
4. How can inventory be optimized?
5. What is the impact of delivery delays on sales?

Answers to all of these are in the insights summary file, with the actual numbers behind each one.

## A few notes / things I assumed

- The dataset doesn't have a "promised delivery date" column, so I used shipping time > 7 days as the definition of a "delayed" order. This is adjustable in the file.
- Overstock = more than 4x the reorder level. Also adjustable.
- Assumed the currency is rupees since nothing was specified.
- Product names and categories don't always match up in the raw data (e.g. some Tablets are tagged under Fashion) — left this as-is since it wasn't something I was told to fix, and compared products by name instead of category.
