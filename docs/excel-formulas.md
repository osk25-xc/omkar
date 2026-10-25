# Excel formulas and build guide

Convert the imported data to an Excel Table named **SalesData** (Table Design → Table Name). Add these calculated columns to the table.

## Calculated columns
Use structured references so formulas fill down automatically.

- **Sales Variance**: `=[@Actual_Sales]-[@Target_Sales]`
- **Achievement %**: `=IFERROR([@Actual_Sales]/[@Target_Sales],0)`
- **Profit**: `=[@Actual_Sales]-[@Cost]`
- **Profit Margin %**: `=IFERROR([@Profit]/[@Actual_Sales],0)`
- **Delivery Rate %**: `=IFERROR([@Orders_Delivered]/[@Orders_Received],0)`
- **Return Rate %**: `=IFERROR([@Returns]/[@Orders_Delivered],0)`

Format percentage columns as Percentage (1 decimal place), and sales/profit as currency or number with thousands separators.

## PivotTables
Create each PivotTable from the **SalesData** table so new rows can be included after refresh.

1. **Monthly trend** — Rows: Month; Values: Sum of Actual_Sales, Sum of Target_Sales.
2. **Region performance** — Rows: Region; Values: Sum of Actual_Sales, Sum of Target_Sales, Sum of Profit.
3. **Department performance** — Rows: Department; Values: Sum of Actual_Sales, Sum of Profit, Sum of Orders_Delivered, Sum of Returns.
4. **Operations** — Rows: Region; Values: Sum of Orders_Received, Orders_Delivered, Pending_Orders, Returns.

Add calculated ratios next to PivotTables if necessary. Do not average row-level percentages to get an overall percentage; calculate the ratio from summed numerators and denominators.

## Dashboard checklist
- KPI cards: Actual Sales, Target Sales, Achievement %, Profit, Pending Orders.
- Chart 1: Actual vs Target by month.
- Chart 2: Actual Sales by Region.
- Chart 3: Actual Sales by Department.
- Small operations table: Received, Delivered, Pending, Returns, Delivery Rate.
- Slicers: Region and Department. Connect each slicer to all relevant PivotTables using Report Connections.
- Use consistent number formats and clear titles; avoid 3D charts.

## Quality checks
- Source row count should be 240.
- Each month should have 20 rows.
- There should be 5 regions and 4 departments.
- Check that Profit equals Actual Sales minus Cost.
- Check that Pending Orders equals Orders Received minus Orders Delivered.
- Refresh all PivotTables after changing source data.
