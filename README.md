# MIS Monthly Reporting Automation | Excel

A practical, portfolio-ready MIS reporting project built around a synthetic retail dataset. The goal is to turn monthly sales and operations data into a repeatable management report—not just a chart.

## Business scenario
A retail operations team needs one monthly report to compare actual sales with targets, review regional and department performance, and track order delivery, pending orders, and returns.

## Dataset
- **File:** `data/mis_monthly_data.csv`
- **Rows:** 240 monthly records (12 months × 5 regions × 4 departments)
- **Period:** January–December 2025
- **Data status:** Synthetic practice data created for this portfolio project; it is not real company data.

## KPIs to build in Excel
| KPI | Definition |
|---|---|
| Total Actual Sales | Sum of `Actual_Sales` |
| Total Target Sales | Sum of `Target_Sales` |
| Target Achievement % | Actual Sales ÷ Target Sales |
| Sales Variance | Actual Sales − Target Sales |
| Profit | Actual Sales − Cost |
| Profit Margin % | Profit ÷ Actual Sales |
| Delivery Rate % | Orders Delivered ÷ Orders Received |
| Pending Orders | Sum of `Pending_Orders` |
| Return Rate % | Returns ÷ Orders Delivered |

## Workbook build
1. Import the CSV into Excel and format it as a table named `SalesData`.
2. Add calculated columns using the formulas in [Excel formulas](docs/excel-formulas.md).
3. Create PivotTables for monthly trend, region performance, department performance, and order operations.
4. Add slicers for Region and Department, plus a Month timeline where available.
5. Build a one-page dashboard with KPI cards, monthly sales vs target, region comparison, department performance, and an operations summary.
6. Validate totals against the source data before sharing the report.

## Suggested report layout
- **Top:** Actual Sales, Target Sales, Achievement %, Profit, Pending Orders
- **Middle:** Monthly Actual vs Target line/column chart and sales by region
- **Bottom:** Department performance and delivery/returns summary
- **Filters:** Region, Department, Month

## Repository structure
```
data/
  mis_monthly_data.csv
docs/
  excel-formulas.md
  data-dictionary.md
```

## Tools
Microsoft Excel (Tables, formulas, PivotTables, charts, slicers). Power Query is optional for repeatable refresh.

## Important note
This repository currently provides the source dataset and build specification. Add screenshots of the completed workbook and verified findings after the dashboard is built; no business outcome is claimed before that validation.

Maintained by [Omkar S. Kshirsagar](https://github.com/osk25-xc).
