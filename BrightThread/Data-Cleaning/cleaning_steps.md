# Data Cleaning Steps

**Tool:** Google Sheets
**Dataset:** Retail sales data, 300 rows (no data dictionary was provided)
**Goal:** Prepare reliable data so the business can see which products to keep and how to increase sales.

---

## 1. Setup before cleaning
- Made a **copy of the raw data** and worked only on the copy, so the original stays safe.
- Froze the header row and turned on filters.
- Added a **Flag column** to mark rows I changed.
- Kept a **change log** sheet that records what was changed and why.

## 2. Column-by-column cleaning

| Column | Issue found | What I did |
|---|---|---|
| Date | Checked format and range | Made all dates one consistent format |
| Order ID | Checked for blanks and repeats | Confirmed each order is recorded correctly |
| Customer ID | 12 blank values | Retrieve few from order id and remaining kept blank |
| Product Name | 29 blank values | Fixed by hand, because the formula method (VLOOKUP inside ARRAYFORMULA) was slower than checking 29 rows directly |
| SKU | Checked length | All SKUs have 10 characters, so no change needed |
| Price | Checked for wrong or odd values | Confirmed prices are valid numbers |
| Size | 71 values (small, medium, large) and 229 blank | Checked whether SKU could fill Size. It could not. Kept Blank |
| Quantity | Checked for wrong or odd values | Confirmed quantities are valid numbers |
| Product Line | Checked values | Only two values: dog and cat |
| Product Category | 145 blank values |  Retrived those using SKU |

## 3. Duplicate check
- Checked for **full-row duplicates** (rows where every column is the same).
- Result: No Duplicate Found

## 4. Final checks
- No unexpected blanks left in the columns used for analysis.
- Every column has one consistent format.
- Saved the result as the **clean dataset**, ready for SQL queries, Excel charts, and the Tableau dashboard.

## 5. Lessons learned
- Long formulas are not always faster. For a small number of fixes, checking by hand was quicker and safer.
- A Flag column and a change log make every edit easy to explain later.
- With no data dictionary, I checked each column on its own and did not guess missing values from other columns without proof.
