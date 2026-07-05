# 03_ExcelImportEngine.md

# Excel Import Engine Specification

## Purpose

Import the official hotel aging balance Excel model and convert it into
validated business data.

## Supported Structure

Required columns:

-   Libellé
-   0-30 JRS
-   31-60 JRS
-   61-90 JRS
-   91-120 JRS
-   AU DELÀ 120 JRS
-   Total

## Import Workflow

1.  Select Excel file
2.  Validate workbook
3.  Detect header row
4.  Validate required columns
5.  Ignore empty rows
6.  Convert numeric values
7.  Replace empty amounts by 0
8.  Detect duplicates
9.  Save import history
10. Launch KPI engine

## Validation Rules

-   Missing mandatory column → Stop import
-   Invalid numeric format → Log error
-   Negative values → Allowed
-   Empty customer name → Ignore row
-   Total mismatch → Recalculate and flag

## Import History

Store: - Import ID - Date/time - Filename - User - Number of customers -
Portfolio total - Import duration - Validation errors

## Historical Comparison

Automatically compare with: - Previous import - Previous month - Same
month last year

Display: - Amount difference - Percentage change - New customers -
Removed customers - Customers with increased risk

## Performance Targets

-   10,000 rows \< 10 seconds
-   Progress indicator
-   Cancel import
-   Background processing

## Outputs

Generate: - Clean dataset - Error log - Import summary - KPI refresh -
Dashboard refresh - Audit entry

## Future Compatibility

Parser must support configurable column mapping to allow future imports
from different hotel PMS exports without code changes.
