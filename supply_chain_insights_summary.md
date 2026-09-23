# Supply Chain and Inventory Analysis: Summary of Insights

**Data:** 15,000 order lines, Jan 2023 to Dec 2024, 10 products, 4 categories, 5 suppliers, 5 warehouses.
**Cleaning:** no duplicates, missing values, negative stock or date errors were found, so no rows were removed. 32 zero-stock rows and 49 zero-sales rows are valid and were kept.

## Headline numbers

| Measure | Value |
|---|---|
| Total revenue | ₹307.63 Cr |
| Total profit | ₹61.29 Cr (19.9% margin) |
| Units sold | 22,22,508 (against 37,63,769 units in stock; sell-through 37.1%) |
| Average shipping time | 5.50 days |
| Delayed orders (over 7 days) | 30.0% of lines |
| Year on year (2024 vs 2023) | Revenue -4.3%, profit -4.0%, units -3.5% |

Profit = units sold x (selling price - purchase cost). Currency is assumed to be rupees.

## Business questions

**1. Which products are frequently out of stock?**
Stock-outs are rare: 32 lines (0.2%). Phone (6), TV (5) and Laptop and Watch (4 each) lead. The larger exposure is stock below reorder level: 2,960 lines (about 20%), highest for Tablet (21.6% at risk) and lowest for Mixer (18.2%).

**2. Which suppliers have the highest delivery delays?**
Supplier E is highest at 30.9% of orders over 7 days, then B (30.4%), D (30.2%), A (29.8%) and C (28.9%). The best-to-worst gap is only 2 percentage points, so supplier choice alone does not explain delays.

**3. Which products generate the highest profit?**
Camera (₹6.73 Cr), Laptop (₹6.23 Cr) and Fan (₹6.16 Cr) lead. Shoes earns least (₹5.79 Cr) even though it has the best margin (20.4%), because it sells the fewest units. Camera is 16% ahead of Shoes in profit.

**4. How can inventory be optimized?**
- Restock what sells: 967 fast-moving lines (200+ units sold) are out of stock or below reorder level.
- Trim what sits: ₹13.11 Cr is tied up in 1,168 slow-moving lines holding more than 4x their reorder level. Total excess stock across all lines is ₹38.13 Cr.
- Fix the reorder rules: reorder level has no relationship with units sold (correlation -0.01). Set reorder points from daily demand x shipping days plus safety stock.

**5. What is the impact of delivery delays on sales?**
None is visible. Delayed orders sold 147.8 units per line against 148.3 for on-time orders (-0.3%). Correlation between shipping days and units sold is -0.007. The data records units sold, not sales lost while waiting for stock, so backorders and lost orders should be tracked to measure the real cost of delays.

## Other observations

- Revenue by category: Fashion ₹79.2 Cr, Home Appliances ₹77.4 Cr, Sports ₹75.4 Cr, Electronics ₹75.6 Cr.
- Revenue by warehouse: Bangalore ₹62.5 Cr highest, Chennai ₹60.4 Cr lowest.

## Read with care

- Differences between suppliers, warehouses and products are small (mostly a few percent). Treat rankings as directional, not decisive.
- The file has no promised delivery date, so "delayed" means shipping longer than a threshold (default 7 days, adjustable in the dashboard and workbook).
- Product names and categories do not line up (for example Tablet appears under Fashion). The data was left as supplied and products are compared by name.
