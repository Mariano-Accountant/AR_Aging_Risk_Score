# AR Aging & Risk Score Analysis
> Mariano Jacquet | Project 03 of 10

Automated AR aging report using **Power Query**. Consolidates monthly receivables data, calculates days past due, and classifies invoices by seniority buckets. Drop a new file → Refresh → done.

## Process

1. Power Query reads all `.xlsx` files from a folder automatically
2. Extracts closing date from filename
3. Calculates Days Past Due = Closing Date − Due Date
4. Classifies into buckets: Current, 0–30, 31–90, 91–365, >1 year
5. Outputs a Pivot Table by Customer × Seniority

**Total validated:** 6,882,195,730 across 3,358 invoices (Jan–Mar 2021).

## Tools

Excel 365 · Power Query

## Files

| File | Description |
|------|-------------|
| `data/AR_Aging_01-03_2021.xlsx` | Monthly AR extracts (×3) |
| `excel/AR_Aging_Analysis.xlsx` | Consolidated report with Pivot Table |
| `powerquery/AR_Aging_Query.m` | Power Query code |

## Next Steps

- [ ] Add Risk Score (1–4) and Risk Label columns
- [ ] Power BI dashboard with KPI cards and conditional formatting

## Author

**Mariano Jacquet** — Finance Data Analyst | International Accounting & Tax

GitHub: [github.com/Mariano-Accountant](https://github.com/Mariano-Accountant)
