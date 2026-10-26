# Operations & Inventory Dashboard | Power BI

## Business scenario
A retail operations manager needs a clear view of stock availability, product movement, reorder risk, and estimated inventory value across warehouses.

## Project status
**Portfolio project specification and sample data.** The Power BI report (.pbix) is not included yet. Build the visuals in Power BI Desktop, validate the measures, then commit the finished .pbix and screenshots.

## Files
- `data/inventory_operations_sample.csv` — synthetic practice data; not company data.
- `projects/operations-inventory-dashboard/README.md` — this project guide.

## Suggested KPIs
- Total units sold
- Closing stock = Opening Stock + Stock In − Units Sold
- Products below reorder level
- Inventory value = Closing Stock × Unit Cost
- Estimated sales value = Units Sold × Unit Price
- Stock-out risk by warehouse/category

## Recommended visuals
1. KPI cards for units sold, closing stock, low-stock products, and inventory value.
2. Bar chart: closing stock by category.
3. Bar chart: units sold by warehouse.
4. Table: product, warehouse, closing stock, reorder level, and stock status.
5. Slicers: warehouse and category.

## Build steps
1. Import the CSV into Power BI Desktop.
2. Check column data types and confirm there are no unexpected blanks or duplicate product/warehouse rows.
3. Create measures using the formulas below.
4. Add the visuals and slicers.
5. Test filters and reconcile totals against the CSV before sharing.

### Example DAX measures
```dax
Units Sold = SUM(Inventory[Units_Sold])
```

```dax
Closing Stock =
SUM(Inventory[Opening_Stock])
    + SUM(Inventory[Stock_In])
    - SUM(Inventory[Units_Sold])
```

```dax
Inventory Value =
SUMX(
    Inventory,
    (Inventory[Opening_Stock] + Inventory[Stock_In] - Inventory[Units_Sold])
        * Inventory[Unit_Cost]
)
```

```dax
Low Stock Products =
COUNTROWS(
    FILTER(
        Inventory,
        Inventory[Opening_Stock] + Inventory[Stock_In] - Inventory[Units_Sold]
            <= Inventory[Reorder_Level]
    )
)
```

Replace `Inventory` with the actual table name if Power BI names it differently. This is synthetic sample data for practice; do not present it as real business performance.

## Tools
Power BI Desktop, Power Query, DAX, CSV.

Maintained by [Omkar S. Kshirsagar](https://github.com/osk25-xc).
