# Core MIS Dashboard Metric Definitions

Use these definitions consistently across Excel, SQL, and Power BI reports. Confirm the business meaning and source columns with the data owner before publishing results.

| Metric | Definition | Interpretation |
|---|---|---|
| Actual Sales | Sum of recorded sales for the selected period | Realized sales in the source data |
| Target Sales | Sum of assigned sales targets for the same scope | Planned sales benchmark |
| Achievement % | Actual Sales / Target Sales × 100 | Performance against target; handle zero targets explicitly |
| Sales Variance | Actual Sales − Target Sales | Positive means above target; negative means below target |
| Profit Margin % | Profit / Sales × 100 | Share of sales retained as profit; confirm profit definition |
| Return Rate % | Returned units or orders / eligible units or orders × 100 | State clearly whether the denominator is units, orders, or revenue |
| Delivery Rate % | Successfully delivered eligible orders / eligible orders × 100 | Define treatment of cancelled and pending orders |

## Reporting checks

- Use the same date range for actuals and targets.
- Document currency, time zone, and grain (order, item, or day).
- Do not divide by zero; show N/A when the denominator is zero.
- Reconcile headline KPIs to source totals before sharing a report.
- Label sample or synthetic datasets clearly.
