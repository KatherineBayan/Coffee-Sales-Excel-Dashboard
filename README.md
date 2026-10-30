# Coffee-Sales-Excel-Dashboard
<img width="1498" height="783" alt="image" src="https://github.com/user-attachments/assets/e323f339-4bc6-480e-995f-27a73c60a6d3" />

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
- **Data storytelling:** Turned the numbers into findings and recommendations.

### Results

- **Total sales were about $45.1K** across the period (US $35,639 + Ireland $6,697 + UK $2,799).
- **The US is the dominant market**, at about 79% of revenue. Ireland contributes about 15% and the UK about 6%.
- **Revenue is spread across all four coffee types.** No single type consistently leads, and each one swings sharply from month to month (roughly $50 to $850 per month).
- **Notable peaks:** Arabica spiked to about $840 in September 2021 and about $745 in early 2020. Liberica peaked at about $845 in January 2022.
- **There is no clear long-term growth trend.** Sales are volatile and flat across 2019–2022, and revenue appears to dip in the final months shown (2022 may be incomplete, since the data ends in August).
- **Customer revenue is not concentrated.** The top 5 customers (Allis Wilmore at $317, Brenn Dundredge at $307, Terri Farra at $289, Nealson Cutler at $282 and Don Flintif at $278) together account for only about 3% of total sales. That means low dependency risk, but also no standout “whale” accounts.

## Recommendations

Total sales of $45.1K and profit of $4.5K (10.0% margin) across 957 orders and 913 customers, Jan 2019 to Aug 2022.

#### 1. Shift the product mix toward higher-margin coffees

- **Evidence:** Profit margin varies by coffee type, from 13% for Liberica and 11% for Excelsa to 9% for Arabica and only 6% for Robusta. Liberica makes up 26.7% of sales but 34.7% of profit, while Robusta makes up 20.0% of sales but only 11.9% of profit. Roast type and bag size have almost no effect on margin (about 10% each).
- **Action:** Feature Liberica and Excelsa in promotions, bundles and homepage placement. Review Robusta pricing or costs, since it has the lowest sales and the thinnest margin.
- **KPI:** Blended profit margin (currently 10.0%) and profit share by coffee type.

#### 2. Build repeat purchasing, the largest gap in the data

- **Evidence:** Only 2.7% of customers ordered more than once, and the average customer placed 1.05 orders in nearly four years. Revenue relies almost entirely on one-time buyers.
- **Action:** Launch post-purchase follow-ups (reorder reminders timed to a bag’s usage), a subscription option, and a second-order incentive. Because coffee is a consumable, repeat purchase should be a core business model.
- **KPI:** Repeat customer rate, orders per customer, and customer lifetime value.

#### 3. Re-evaluate the loyalty program

- **Evidence:** Loyalty card members (443 customers) spend slightly less than non-members (470): $47.20 vs. $51.50 per customer, with a smaller average order ($45.10 vs. $49.10). Loyalty cards make up 46% of sales, in proportion to their share of customers, so the program is not driving higher spending or more repeat visits.
- **Action:** Redesign the program with tiers, points on larger bags or repeat orders, and member-only offers that reward frequency, not just sign-up. Track members vs. non-members as a controlled comparison.
- **KPI:** Spend per customer and repeat rate for members vs. non-members.

#### 4. Grow the Ireland and UK markets (medium priority)

- **Evidence:** The US generates 79% of sales (774 orders), Ireland 14.8% and the UK 6.2%. Margins are the same (about 10%) in all three, so growth in any market is equally profitable.
- **Action:** Run targeted campaigns in Ireland and the UK, with localized offers and shipping terms. Use the dashboard’s country view to measure results against a baseline.
- **KPI:** Share of sales outside the US, and new customers per market.

#### 5. Promote larger bag sizes and bundles (medium priority)

- **Evidence:** The 2.5 kg bag drives 52.7% of sales and 1.0 kg adds 24.4%, so larger sizes account for about 77%. Order counts are similar across sizes (236–268 each), so customers choosing larger bags generate far more revenue per order.
- **Action:** Make 2.5 kg the default highlighted option, and offer a volume discount or bundle that moves 0.2 kg and 0.5 kg buyers up a size. Check price-per-100g so larger bags remain attractive without cutting margin.
- **KPI:** Average order value (currently $47.16) and size mix.

#### 6. Stabilize demand and plan around seasonality (medium priority)

- **Evidence:** Monthly sales swing widely, and the Jan–Aug total was flat in 2019–2021 (about $8.0K each year). 2022 is lower at $7.1K, though part of that gap reflects data ending 19 August. Sales peak in March and June (about $4.8K each) and are weak in May and December ($3.2K and $3.1K).
- **Action:** Time campaigns to pre-empt soft months (May and December), and plan inventory for the March and June peaks. Run an A/B test to confirm what drives each peak before scaling.
- **KPI:** Month-over-month volatility, and sales in soft months.

#### 7. Maintain a broad customer base and avoid chasing a few accounts

- **Evidence:** The top 5 customers account for only 3.3% of sales, and the top 10% of customers (about 91) generate 35.6%. This is a healthy, low-concentration base, so there’s no dependency risk.
- **Action:** Identify the top 10% and offer them early access or bulk pricing, but prioritize acquisition and retention across the whole base.
- **KPI:** Share of sales from top 10% customers.
