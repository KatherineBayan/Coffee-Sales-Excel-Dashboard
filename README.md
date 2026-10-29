# Coffee-Sales-Excel-Dashboard

### Description

An interactive sales dashboard built from a three-table coffee retail dataset: 1,000 order lines, 1,000 customers and 48 products, covering January 2019 to August 2022. The dashboard tracks revenue over time by coffee type (Arabica, Excelsa, Liberica, Robusta), compares sales across countries, and ranks the top customers. A date timeline and slicers for roast type, bag size and loyalty card status let users filter every chart at once.

### Goal

Give a coffee retailer a single view of how the business is performing, so stakeholders can quickly answer:

- Which coffee types drive revenue, and how stable is that revenue over time?
- Which markets generate the most sales?
- Who are the most valuable customers?
- Do roast, size and loyalty membership change the picture?

### Skills Used

- **Data cleaning and preparation:** The `orders` sheet held only IDs and quantities. I enriched it with customer and product attributes (name, country, coffee type, roast, size, unit price) from the `customers` and `products` tables. I also checked ID integrity (no orphaned or duplicate keys) and flagged missing emails and phone numbers.
- **Data modeling:** Linked three related tables through Customer ID and Product ID.
- **Calculated fields:** Sales = Quantity × Unit Price.
- **Pivot tables and pivot charts:** Built the line chart (sales by coffee type by month), the bar chart (sales by country) and the Top 5 Customers ranking.
- **Interactive filtering:** Added a timeline and slicers (roast, size, loyalty card) connected to all visuals.
- **Dashboard design:** Used a consistent coffee-themed palette, a clear layout and readable labels, with filters on top and charts below.
- **Data storytelling:** Turned the numbers into findings and recommendations.

### Results

- **Total sales were about $45.1K** across the period (US $35,639 + Ireland $6,697 + UK $2,799).
- **The US is the dominant market**, at about 79% of revenue. Ireland contributes about 15% and the UK about 6%.
- **Revenue is spread across all four coffee types.** No single type consistently leads, and each one swings sharply from month to month (roughly $50 to $850 per month).
- **Notable peaks:** Arabica spiked to about $840 in September 2021 and about $745 in early 2020. Liberica peaked at about $845 in January 2022.
- **There is no clear long-term growth trend.** Sales are volatile and flat across 2019–2022, and revenue appears to dip in the final months shown (2022 may be incomplete, since the data ends in August).
- **Customer revenue is not concentrated.** The top 5 customers (Allis Wilmore at $317, Brenn Dundredge at $307, Terri Farra at $289, Nealson Cutler at $282 and Don Flintif at $278) together account for only about 3% of total sales. That means low dependency risk, but also no standout “whale” accounts.

### Recommendations

1. **Grow outside the US.** Ireland and the UK together make up about 21% of sales. Targeted promotions or shipping offers in these markets could reduce reliance on a single country.
2. **Investigate the spikes.** Look at what drove the Arabica (Sep 2021) and Liberica (Jan 2022) peaks, such as promotions, bulk orders or seasonal demand. If the cause can be repeated, it becomes a growth lever.
3. **Stabilize demand.** Monthly swings this large make inventory planning hard. Use demand forecasting or seasonal stock planning to avoid stockouts during peaks and overstock during dips.
4. **Build a stronger loyalty and retention strategy.** With spend spread thinly across many customers, focus on repeat purchases through subscriptions, bundles or tiered rewards. Compare loyalty and non-loyalty spend using the existing slicer to see whether the program pays off.
5. **Add profit to the analysis.** The products table includes profit per unit, but the dashboard shows revenue only. Adding margin by coffee type, roast and size would show which products to promote, since the highest-selling item is not always the most profitable.
6. **Extend the dashboard.** Add KPI cards (total sales, orders, average order value, repeat-customer rate) and a year-over-year comparison so performance is clear at a glance.
