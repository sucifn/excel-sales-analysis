# Data Quality & Preparation Log

## Objective

Prepare the sales dataset so revenue, profit, category performance, regional performance, and order quality can be analyzed more accurately.

| Issue Area | What Was Found | Business Risk | Action Taken |
|---|---|---|---|
| Missing values | Some rows had missing date, quantity, or revenue values. | Missing values can reduce the accuracy of trend, order count, and revenue analysis. | Marked affected rows for review and excluded non-clean rows from dashboard metrics. |
| Duplicate records | Some order IDs appeared more than once. | Duplicate records can overstate revenue, profit, and order count. | Flagged duplicate order IDs for business review. |
| Inconsistent categories | Some text fields used different casing or abbreviations. | PivotTables may split the same category into multiple labels. | Standardized region, channel, status, and category labels. |
| Date formatting | Some order dates used different formats or were blank. | Monthly trend analysis may become inaccurate. | Converted valid dates into a consistent date format and flagged missing dates. |
| Numeric fields | Some revenue values were stored as text with currency symbols. | Revenue and margin calculations may fail or return incorrect totals. | Converted valid numeric fields into analysis-ready values. |
| Order status | Cancelled and returned orders appeared in the dataset. | Including all statuses may distort clean sales performance. | Flagged cancelled and returned orders for separate review. |

## Data Quality Summary

| Quality Flag | Rows |
|---|---:|
| Clean | 611 |
| Review Status | 74 |
| Check Revenue | 10 |
| Check Date | 17 |
| Check Quantity | 8 |
| Duplicate Order | 5 |

## Summary

The dashboard focuses on clean rows so business decisions are based on reviewed data. Rows that require review are still documented because they may reveal process, data entry, or order management issues.
