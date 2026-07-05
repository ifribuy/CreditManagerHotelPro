# 15_ExcelExports.md

# Excel Export Specification

## Objective

Provide enterprise-grade Excel exports for operational analysis,
management reporting and executive decision-making.

## General Requirements

All exports shall: - Preserve formulas where applicable - Use
professional formatting - Include hotel logo (optional) - Include export
timestamp - Support XLSX format - Auto-size columns - Freeze header
row - Apply filters - Apply conditional formatting

------------------------------------------------------------------------

# Export Catalog

## 1. Aging Balance Export

Columns: - Customer - 0-30 JRS - 31-60 JRS - 61-90 JRS - 91-120 JRS - AU
DELÀ 120 JRS - Total - Risk Level - Credit Status

------------------------------------------------------------------------

## 2. Customer Portfolio

Includes: - Customer profile - Outstanding balance - Credit limit -
Utilization % - Risk score - Last payment - Last reminder

------------------------------------------------------------------------

## 3. KPI Export

KPIs: - DSO - ADD - Recovery Rate - CEI - Cash Forecast - Portfolio
Health - Collection Rate - Bad Debt Ratio

With: - Current value - Previous value - Difference - Trend

------------------------------------------------------------------------

## 4. Collection Report

Contains: - Calls - Emails - Promises - Payments - Status - Collector -
Outcome

------------------------------------------------------------------------

## 5. Credit Limit Report

Includes: - Credit Limit - Current Exposure - Available Credit - Block
Status - Approval History

------------------------------------------------------------------------

## 6. Litigation Report

Includes: - Open cases - Resolution status - Financial impact - Assigned
owner

------------------------------------------------------------------------

## 7. Cash Forecast Export

Forecasts: - 7 Days - 15 Days - 30 Days - 60 Days - 90 Days

------------------------------------------------------------------------

## 8. AI Recommendations

Columns: - Customer - Recommendation - Priority - Confidence Score -
Suggested Action

------------------------------------------------------------------------

# Formatting

Header: - Dark background - White text - Bold

Conditional Colors: - Green - Yellow - Orange - Red - Purple (AI)

Currency: - Local currency formatting

Dates: - ISO format (YYYY-MM-DD)

------------------------------------------------------------------------

# Pivot Tables

Optional generation: - Aging by Hotel - Aging by Market Segment - Aging
by Sales Manager - Risk by Customer - Monthly Collections

------------------------------------------------------------------------

# Charts Included

Optional worksheets with: - Line chart - Donut chart - Bar chart -
Stacked bar - KPI summary

------------------------------------------------------------------------

# Security

Exports may be: - Password protected - Read-only - Watermarked -
Digitally signed
