DATA ANALYST PROJECT 3 - SUPPLY CHAIN & INVENTORY ANALYSIS
=============================================================

This folder contains all four required deliverables.

1. CLEANED DATASET
   supply_chain_cleaned.csv
   The 15,000 source rows after validation (no duplicates, missing
   values, or negative/incorrect stock were found in the source file).

2. ANALYSIS FILE (Excel)
   supply_chain_analysis.xlsx
   Sheets: Summary (KPIs and the 5 business questions), Cleaned_Data
   (raw data plus calculated columns), Product/Supplier/Warehouse/
   Category_Analysis, Monthly_Trend, Delay_vs_Sales, Cleaning_Log.
   All figures are live formulas - edit the blue input cells on the
   Summary sheet (delay threshold, overstock multiple, fast/slow
   movement cutoffs) and every sheet recalculates.

3. DASHBOARD
   supply_chain_dashboard.html
   Open this file in any web browser (double-click it, or drag it
   into a browser window). Dark, interactive dashboard with 6 tabs
   (Overview, Inventory, Suppliers and delivery, Products and profit,
   Insights, Records), clickable filters and charts, and two
   adjustable-threshold sliders.
   A live, shareable copy is also published at:
   https://claude.ai/artifact/BpYsZNxUrvcUsdcivnvVYA

4. SHORT SUMMARY OF INSIGHTS
   supply_chain_insights_summary.md
   One-page write-up answering the five business questions, with
   headline numbers and data-quality notes. Opens in any text editor;
   renders formatted on GitHub, in Claude, or in any Markdown viewer.

All four files use the same numbers, cross-checked against each other
and against an independent analysis in pandas.
