# Superstore Sales Analysis — Power BI Dashboard

A Power BI dashboard exploring revenue, profit, and customer trends across regions, categories, and segments for a fictional US-based retail business.

**Author:** Patricia Fagbola | Data Analytics Intern, AnalystLab | 2026
**Tools:** Power BI, DAX

---

## Dataset

- **9,994** order records
- **21** columns
- **4 years** of transactions (2019–2022)
- Fields include Order ID/Date, Customer, Segment, Region, State, City, Category, Sub-Category, Sales, Quantity, Discount, and Profit

## Business Problem

The business generates millions in sales but lacks visibility into which products, regions, and customer segments actually drive profitability versus which erode it through discounting. Specific gaps:

- **Profitability gaps** — high-revenue products may carry negative margins, and discounting isn't evaluated against profit impact
- **Regional blind spots** — no clear view of underperforming states/cities relative to sales volume
- **Segment confusion** — Consumer, Corporate, and Home Office segments are treated the same despite different buying behavior
- **Category mix** — unclear contribution split between Technology, Furniture, and Office Supplies

## KPIs Tracked

| KPI | Formula | Purpose |
|---|---|---|
| Total Sales | `SUM(Sales)` | Overall revenue |
| Total Profit | `SUM(Profit)` | Net profit after discounts & cost |
| Profit Margin % | `Profit ÷ Sales × 100` | Sales efficiency / health indicator |
| Total Orders | `COUNT(Order ID)` | Demand volume |
| Avg. Discount | `AVG(Discount)` | Pricing discipline |
| Sales by Category | Sales per Category | Revenue breakdown by product line |

## Headline Numbers

- **$2.30M** total sales
- **$286K** total profit
- **12.47%** profit margin
- **9,994** total orders

## Key Insights

- **Technology leads revenue** — ~36% of total revenue, with Phones and Copiers as the strongest sub-categories
- **Furniture has the weakest margin** — despite being the second-highest category by sales, heavy discounting on Tables and Bookcases often sells at a loss
- **West region is the top performer** — highest sales and profit, with California alone driving a disproportionate share
- **Consumer segment dominates order volume** (~51%) but Corporate customers carry higher average order value and better margins
- **Discounts above 30% are consistently unprofitable** — the correlation between discount depth and negative profit holds across every category
- **Q4 is the peak sales period** — November and December spike every year, driven by holiday demand in Technology and Office Supplies

## Recommendations

1. **Cap discounts at 20%** — profit turns negative past 30% across all categories; review sales team pricing authority
2. **Invest more in Technology** — highest-margin category; increase inventory for Phones and Copiers ahead of Q4, and build bundled offers for Corporate customers
3. **Address Furniture losses** — audit Tables and Bookcases; re-price, renegotiate supplier cost, or stop discounting below margin thresholds
4. **Develop the South region** — lower sales and profit relative to other regions; targeted marketing/distribution could unlock growth
5. **Prioritize the Corporate segment** — higher order values; a loyalty or account management program could grow retention

## Challenges Faced

- **Data modeling** — ensuring correct fact/dimension relationships in Power BI to avoid ambiguous joins and incorrect filter context
- **DAX accuracy** — time-intelligence measures (YoY, MTD) and conditional aggregations required several iterations of validation
- **Discount vs. profit visualization** — communicating a non-linear relationship clearly for a non-technical audience
- **Dashboard UX** — balancing information density with readability across six KPIs, regional views, and category breakdowns on one canvas

## Repo Contents

```
Superstore-Sales-Analysis/
├── README.md
├── dashboard/
│   └── Superstore_Dashboard.pbix        # Power BI dashboard file
└── presentation/
    └── Superstore_Analysis_Presentation.pptx   # Project walkthrough deck
```

## How to View

- **Dashboard:** open `dashboard/Superstore_Dashboard.pbix` in [Power BI Desktop](https://powerbi.microsoft.com/desktop/) (free)
- **Presentation:** open `presentation/Superstore_Analysis_Presentation.pptx` in PowerPoint or Google Slides

