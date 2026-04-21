# AdventureWorks Sales — Tableau Story Dashboard

Tableau Public story analyzing the Sales schema of the AdventureWorks 2022 sample database: salesperson activity, order trends, currency flow, and customer hierarchy. Built to exercise LOD expressions, parameters, sets, and cross-dashboard actions.

## Live story

Published to Tableau Public. See `REPORT_LINK.txt` for the current URL.

## Stack

| Layer | Tools |
|---|---|
| Source | AdventureWorks 2022 Sales schema (SQL Server sample) |
| Modeling | Direct connection with relationship-based joins |
| Calculations | LOD expressions, parameter-driven sets, calculated fields |
| Delivery | Tableau Desktop authoring, Tableau Public hosting |

## What the story answers

- Which salesperson is most active by number of orders closed
- How revenue trends across `OrderDate` by month and year
- Top 5 and Bottom 5 products for 2011, driven by a user-controlled parameter and set
- Which currency pair sees the most exchange activity
- Latest expiration date for the most-used credit card type
- Tabular breakdown of monetary totals per `SalesOrder`, with a CustomerID to SalesPersonId hierarchy
- How many `SalesPersonId` records activate each month, computed with a fixed LOD

## Story structure

| View | Focus |
|---|---|
| 1. Sales Team Activity | Ranking salespeople by volume |
| 2. Order Date Trends | Monthly revenue line, year-over-year overlay |
| 3. Product Performance | Top and Bottom N products via parameter |
| 4. Currency Flow | Sankey or chord view of exchange direction |
| 5. Payment Methods | Credit card type usage and expiration timeline |
| 6. Customer Hierarchy | Drill-down from Customer to SalesPerson |
| 7. Monthly Activations | LOD-driven count of active salespeople per month |

## Repository structure

```
Tableau_Challenge_Solved.twb    # Tableau workbook, open with Tableau Desktop or Reader
REPORT_LINK.txt                 # Tableau Public story URL
screenshots/                    # view exports
```

## Notes

- Workbook connects to a local AdventureWorks 2022 database. Sample data is included in the workbook's cached extract; no live connection required to open and explore.
- No production data, no PII. AdventureWorks is Microsoft's public sample dataset.
