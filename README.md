# Analytics & MIS Portfolio Projects

A central portfolio repository for practical data-analysis, MIS reporting, and business-intelligence work. The projects use practice or synthetic datasets unless a source is explicitly identified.

## Project index

| Project | Business focus | Tools | Current scope |
|---|---|---|---|
| [MIS Monthly Reporting](README.md) | Sales vs target, profit, regions, departments, delivery and returns | Excel, CSV | Dataset and reporting guide |
| [E-commerce SQL Analysis](https://github.com/osk25-xc/SQL-Business-Sales-Analysis) | Revenue, customer contribution and category performance | MySQL | SQL scripts; run and validate against the project schema |
| [Operations & Inventory Dashboard](projects/operations-inventory-dashboard/README.md) | Stock, reorder risk and warehouse reporting | Power BI | Guide and sample data; dashboard completion should be verified |
| [Data Quality Audit](https://github.com/osk25-xc/Retail-Customer-Segmentation) | Missing values, duplicates and validation rules | Python, Pandas | Audit script in the linked repository |

## MIS practice data

- `data/mis_monthly_data.csv` — synthetic monthly sales and operations data.
- `docs/excel-formulas.md` — formula and dashboard build notes.
- `docs/data-dictionary.md` — field definitions and assumptions.

## Inventory practice data

- `data/inventory_operations_sample.csv` — fictional product and warehouse records for practice.
- See the linked project guide for intended analysis and limitations.

## Reproducibility checklist

1. Read the project guide and inspect the source columns.
2. Confirm metric definitions before calculating KPIs.
3. Reconcile summaries to the underlying records.
4. Record assumptions, exclusions, and data limitations.
5. Add screenshots and numerical findings only after verifying the actual output.

## Portfolio standards

This repository is a learning and portfolio workspace. Synthetic data must not be presented as real company data, and planned features must not be described as completed until they have been tested.

Maintained by [Omkar S. Kshirsagar](https://github.com/osk25-xc).
