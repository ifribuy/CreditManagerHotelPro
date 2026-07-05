# 09_KPI_Engine.md

# KPI Engine Specification

## Purpose

Define all Key Performance Indicators (KPIs) used throughout
CreditManagerHotelPro.

## Dashboard KPIs

### Portfolio KPIs

-   Total Accounts Receivable

-   Current Receivables (0--30)

-   Overdue Receivables

-   120 Days Receivables

-   Average Balance per Customer

-   Number of Active Customers

-   Number of Critical Customers

### Collection KPIs

-   DSO (Days Sales Outstanding) Formula: DSO = (Accounts Receivable /
    Credit Sales) × Number of Days

-   ADD (Average Days Delinquent) ADD = DSO − Best Possible DSO

-   Recovery Rate Recovery Rate = Collected Amount / Total Due × 100

-   Collection Effectiveness Index (CEI) CEI = (Beginning AR + Credit
    Sales − Ending Current AR) / (Beginning AR + Credit Sales − Ending
    Total AR) × 100

-   Promise Fulfillment Rate

-   Reminder Success Rate

-   Average Collection Time

### Credit KPIs

-   Credit Utilization
-   Credit Limit Usage %
-   Accounts Over Credit Limit
-   Blocked Accounts
-   Released Accounts

### Risk KPIs

-   Portfolio Risk Score
-   High-Risk Customers
-   Litigation Ratio
-   Bad Debt Ratio
-   Exposure Ratio
-   Concentration Risk

### Cash KPIs

-   Cash Forecast (7/15/30/60/90 days)
-   Expected Collections
-   Collected This Month
-   Outstanding Cash
-   Forecast Accuracy

### Operational KPIs

-   Excel Imports
-   Failed Imports
-   Processing Time
-   Report Generation Time
-   AI Recommendations Executed

## Trend Indicators

Each KPI shall display: - Current Value - Previous Period - Difference -
Percentage Change - Trend Arrow - Sparkline

## Threshold Colors

Green : Excellent Yellow : Attention Orange : High Risk Red : Critical
Purple : AI Insight

## Benchmarking

Compare: - Previous Month - Previous Quarter - Previous Year - Same
Month Last Year - Hotel vs Hotel - Company vs Company

## Dashboard Widgets

-   KPI Cards
-   Gauges
-   Heat Maps
-   Donut Charts
-   Trend Lines
-   Forecast Charts
-   Leaderboards
-   Risk Matrix

## AI KPIs

-   AI Risk Prediction
-   AI Collection Priority
-   AI Cash Forecast
-   AI Payment Probability
-   AI DSO Prediction
-   AI Portfolio Health Score
