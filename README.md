# AR aging & risk score analysis
Automated accounts receivable aging report built with Power Query in Excel. Drop a new monthly file into the folder, hit refresh, and get an updated aging analysis instantly.

## What it does
- Reads all `.xlsx` files from a folder automatically.
- Extracts the closing date from each filename.
- Calculates days past due per invoice.
- Classifies invoices into seniority buckets.
- Generates a pivot table by customer × seniority.
- Refreshes automatically when new monthly files are added.

## Seniority Buckets

| Bucket | Days Past Due |
|--------|--------------|
| Current | Not yet due |
| 0 – 30 | 0 to 30 days |
| 31 – 90 | 31 to 90 days |
| 91 – 365 | 91 to 365 days |
| Greater than 1 year | > 365 days |

## Power Query transformations applied
- Consolidate multiple files from folder.
- Promote headers and filter duplicates.
- Split filename to extract period (MM-YYYY).
- Calculate end of month as closing date.
- Date subtraction for days past due.
- Conditional column for seniority classification.
- Type conversions and column cleanup.

## Tools
Excel 365 · Power Query · Pivot Tables.

## How to use monthly
1. Drop the new month's `.xlsx` file into the AR_Aging folder.
2. Open `AR_Aging_Analysis.xlsx`.
3. Data → refresh all.
4. Pivot table updates automatically.

**Total validated:** 6,882,195,730 across 3,358 invoices (Jan–Mar 2021).

## Next Steps
- [ ] Add Risk Score (1–4) and Risk Label (low/medium/high/critical) columns.

## Author
**Mariano Jacquet** — [LinkedIn](https://www.linkedin.com/in/mariano-jacquet)

