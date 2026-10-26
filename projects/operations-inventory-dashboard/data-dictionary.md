# Inventory Sample Dataset: Data Dictionary

This document describes the sample inventory operations dataset included with the portfolio. Confirm field names and meanings against the CSV before using it in a report.

| Field | Intended meaning | Validation idea |
|---|---|---|
| SKU | Product identifier | Check blanks and duplicate keys at the intended grain |
| Product | Product name | Check blank labels and inconsistent spelling |
| Category | Product category | Compare values with the approved category list |
| Stock_On_Hand | Recorded stock quantity | Check for negative quantities and unit consistency |
| Reorder_Point | Threshold for replenishment | Confirm the business rule and non-negative values |
| Unit_Cost | Cost per unit | Confirm currency and non-negative values |
| Supplier | Supplier name or identifier | Standardize labels and check missing suppliers |
| Lead_Time_Days | Expected supplier lead time | Check non-negative numeric values |

## Before building visuals

- Verify the actual headers in the CSV; rename this dictionary if they differ.
- Confirm whether each row represents a SKU, SKU-location, or transaction.
- Do not sum repeated stock balances across transaction rows.
- Clearly label the dataset as synthetic/sample data if it is not from a real business system.
- Reconcile totals and test threshold boundary cases before publishing findings.
