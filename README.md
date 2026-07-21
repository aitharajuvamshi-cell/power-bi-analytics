# ☕ Coffee Shop Sales Analysis — From Raw Data to Power BI Dashboard

### Turning a messy transactional dataset into a clear business recommendation

**By Vamshi Aitharaju**

`Power Query` `Data Cleaning` `Conditional Columns` `Star Schema` `Data Modeling` `Power BI` `DAX` `Dashboard Design` `Business Reporting`

---

## Getting the Data Ready

The project started with a coffee shop transactional dataset — orders, customers, products, locations, and payment methods across several hundred rows. Before any analysis, the data needed real cleanup, all handled in **Power Query**: filtering for inconsistent entries (spelling differences and extra spaces in city names), **splitting and trimming text columns**, correcting formats, and removing duplicates.

From there, new fields were derived using **conditional columns** where they'd actually support meaningful analysis — drink size categories, profit margin tiers, and customer age group (calculated from date of birth). Rather than transforming every possible column, only the variables that would lead to real insight were kept — a deliberate choice to keep the model clean and purposeful.

## Building the Model

The cleaned dataset was split into three related tables — **Orders, Customers, and Products** — each with its own primary key, joined using **merged queries** and connected through defined relationships. That structure became a proper **star schema** in Power BI — the fact/dimension foundation every visual in the dashboard was built on.

## The Dashboard, Chart by Chart

**1. Profit and Sales by Product Type**

<img src="assets/chart1_profit_by_product_type.png" width="600"/>

Basic drinks generated the highest profit — 1.32K, or 53.76% of total profit, from 1,729 sales. Premium drinks followed closely (1,016 profit, 1,653 sales). Affordable drinks barely registered — just 120 in profit from 22 sales. The takeaway: pricing low doesn't guarantee volume or profit. The business should stay focused on basic and premium products, which drive nearly all real value.

**2. Sales Volume by Coffee Type and Order Size**

<img src="assets/chart2_sales_by_coffee_order_size.png" width="600"/>

Drip coffee in large size led with 30 orders. Cold brew skewed medium, cappuccino skewed small. Layering in an age-group filter (built from that earlier conditional column) showed size preference actually shifts across customer segments — useful for targeted upselling rather than one-size-fits-all promotions.

**3. Sales Breakdown by Coffee Type and Drink Size (with Profit Margin)**

<img src="assets/chart3_treemap_drink_size.png" width="600"/>

The most-ordered combinations weren't always the most profitable ones. Drip coffee (medium) and mocha (large) sold the most — but the profit margin filter revealed many of these top-sellers actually sit in low-to-medium margin tiers. Popularity and profitability aren't the same thing, and this chart is the proof.

**4. Daily Trends in Sales Cost, Profit, and Order Volume**

<img src="assets/chart4_daily_trends.png" width="600"/>

A day-by-day view across January — the slowest day (Jan 16) saw just 3 orders and $17.75 profit; a strong day (Jan 12) hit 19 orders and $169.50 profit. This kind of daily pattern directly supports staffing decisions, promotion timing, and inventory planning.

**5. Orders and Average Profit by Payment Method**

<img src="assets/chart5_payment_method_profit.png" width="600"/>

Gift cards produced the highest average profit per order ($8.57), ahead of cash ($7.88, 68 orders) and Google Pay, which had both the most digital orders and the lowest average profit ($7.14). A clear, actionable insight: incentivizing gift card usage could measurably lift average profit per order.

**6. Sales by City and Customer Age Group**

<img src="assets/chart6_sales_by_city_age.png" width="600"/>

Flagstaff's sales came entirely from young professionals (760 total). Across nearly every city, young professionals were the dominant customer segment. That single pattern reframes the whole strategy — expansion, loyalty programs, and promotions should be built around this group first.

## The Conclusion

Not every high-selling product is a high-profit product — the combinations that balance both volume *and* margin are where the real opportunity sits. Size preference shifts by drink type and age group, payment method meaningfully affects profitability, and daily/city-level patterns both point back to the same core insight: **young professionals, buying high-margin drink combinations, paid for with incentivized gift cards, is the highest-leverage segment for this business to focus on.**

📄 [Read the full written analysis →](reports/Coffee_Shop_Sales_Analysis_Writeup.pdf) · [View the full dashboard export →](reports/Power_BI_Dashboard_Export.pdf)

---

## Tools & Skills

Power Query (data cleaning, column splitting, conditional columns, merged queries, grouping/aggregation) · Data Modeling & Star Schema Design · Power BI (DAX, dashboard design) · Business Insight Reporting · Data Storytelling

## Repository Map

```
├── assets/       → Real chart images from the Power BI dashboard
└── reports/       → Full written analysis + complete dashboard export, both as PDF
```

> **A note on file formats:** the original Power Query/Power BI working file is kept in a private archive. Every chart and finding it produced is shown here as real output — nothing in this repo is a mockup.

---
### 👤 About the Author
**Vamshi Aitharaju**
📧 aitharajuvamshi@gmail.com
🔗 [github.com/aitharajuvamshi-cell](https://github.com/aitharajuvamshi-cell)

Original individual coursework. © 2026 Vamshi Aitharaju. All rights reserved.
