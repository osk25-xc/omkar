# Data Cleaning & Quality Audit | Python / Pandas

## Objective
Create a repeatable data-quality check before a dataset is used for reporting. The audit reports missing values, duplicate customer IDs, invalid ranges, and inconsistent calculated fields without silently changing the source data.

## Current implementation
The reusable script is in [`data_quality_audit.py`](https://github.com/osk25-xc/Retail-Customer-Segmentation/blob/main/data_quality_audit.py) and is designed for the synthetic retail customer dataset in that repository.

## How to run
From the repository root:
```bash
pip install pandas
python create_dataset.py
python data_quality_audit.py
```

To audit another CSV with the same expected schema:
```bash
python data_quality_audit.py --input data/retail_customers.csv
```

## Checks included
- Required-column validation
- Missing values by column
- Duplicate customer IDs
- Age range checks
- Non-positive purchase frequency and item counts
- Negative spend or recency values
- Blank country/category fields
- Reconciliation of total purchases against frequency × average order value

## Business value
Catching quality issues before building a dashboard reduces the risk of reporting misleading KPIs. The audit reports potential issues; business owners should confirm business rules before treating any row as erroneous.

## Data note
The sample customer dataset is generated for practice and is not real customer data.

## Skills demonstrated
Python, Pandas, data validation, reproducible checks, exception reporting, and documentation.
