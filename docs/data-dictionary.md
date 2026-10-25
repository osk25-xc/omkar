# Data dictionary

The CSV contains synthetic monthly retail reporting records. Each row represents one Month × Region × Department combination.

| Column | Type | Meaning |
|---|---|---|
| Month | YYYY-MM text | Reporting month in 2025 |
| Region | Category | North, South, East, West, or Central |
| Department | Category | Product department |
| Sales_Rep | Category | Synthetic sales representative name |
| Target_Sales | Integer | Planned sales target for that row |
| Actual_Sales | Integer | Actual sales recorded for that row |
| Cost | Integer | Associated cost used for a simple profit calculation |
| Orders_Received | Integer | Orders received during the reporting period |
| Orders_Delivered | Integer | Orders delivered |
| Pending_Orders | Integer | Orders still pending |
| Returns | Integer | Returned orders |

## Assumptions and limitations
- All records are generated for practice and are not real company records.
- Sales and cost values are illustrative; profit is a simplified calculation (Actual Sales − Cost).
- Order counts are operational measures, not customer-level transactions.
- Return Rate is calculated as Returns ÷ Orders Delivered in the reporting guide. Define a different denominator if your business uses another policy.
