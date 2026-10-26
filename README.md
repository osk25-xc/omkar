# Analytics & MIS Portfolio Projects

A collection of practical data-analysis and reporting projects using synthetic or project-provided datasets. Each project should be validated before presenting results as business findings.

## Featured projects

| Project | Focus | Tools | Status |
|---|---|---|---|
| [MIS Monthly Reporting Automation](README.md) | Monthly sales vs target, profit, region/department reporting, delivery and returns KPIs | Excel, CSV | Dataset and build guide available; workbook is a local starter file and still needs final verification |
| [E-commerce Customer & Revenue Deep Dive](https://github.com/osk25-xc/SQL-Business-Sales-Analysis/blob/main/sql/09_customer_revenue_deep_dive.sql) | Monthly revenue changes, customer ranking, category profitability, repeat-customer summary, quality checks | MySQL, SQL, CTEs, window functions | SQL script added; run against the repository schema/data and validate outputs |
| [Operations & Inventory Dashboard](projects/operations-inventory-dashboard/README.md) | Stock movement, closing stock, reorder risk, inventory value, warehouse/category comparisons | Power BI, Power Query, DAX | Project guide and synthetic sample CSV available; PBIX dashboard still needs to be built |
| [Data Cleaning & Quality Audit](projects/data-quality-audit/README.md) | Missing values, duplicates, invalid ranges, reconciliation checks | Python, Pandas | Reusable audit script available in the Retail Customer Segmentation repository |

## MIS project dataset
- `data/mis_monthly_data.csv`: synthetic monthly sales and operations practice data.
- `docs/excel-formulas.md`: formulas and dashboard build notes.
- `docs/data-dictionary.md`: field definitions and assumptions.

## Inventory sample data
- `data/inventory_operations_sample.csv`: 20 synthetic product/warehouse rows for Power BI practice.
- The dataset is fictional and should not be described as real company data.

## How to work with this portfolio
1. Read each project guide and confirm the dataset schema.
2. Recalculate KPIs from source data rather than copying unverified totals.
3. Document assumptions and data limitations.
4. Add screenshots, completed workbooks, PBIX files, and validated findings when available.
5. Do not claim business impact or finished dashboard features that have not been tested.

Maintained by [Omkar S. Kshirsagar](https://github.com/osk25-xc).
