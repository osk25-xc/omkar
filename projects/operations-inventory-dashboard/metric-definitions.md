# Operations & Inventory Dashboard: Metric Definitions

Use these definitions as a starting point and align them with the business's actual policies before reporting.

| Metric | Definition | Notes |
|---|---|---|
| Stock on Hand | Current recorded available quantity | Confirm whether reserved or damaged stock is excluded |
| Reorder Point | Expected demand during lead time plus safety stock | Document the demand and lead-time assumptions |
| Low-Stock Items | Distinct items where available stock is below the agreed reorder threshold | Compare like-for-like units |
| Inventory Value | Quantity on hand multiplied by the agreed unit cost | State the valuation method and currency |
| Stockout Rate | Eligible item-periods with zero available stock / all eligible item-periods | Define the period grain and exclusions |
| Supplier Lead Time | Actual receipt date minus purchase order date | Specify calendar days versus business days |

## Validation checklist

- Confirm each row's grain (SKU, SKU-location, or transaction).
- Avoid summing a repeated product-level stock balance across transaction rows.
- Check duplicate SKU and supplier keys before joining tables.
- Validate quantity and unit-cost ranges.
- Test the low-stock threshold with boundary cases.
- Clearly label sample data and assumptions.
- Do not claim a live stockout alert unless refresh and alerting are actually configured.