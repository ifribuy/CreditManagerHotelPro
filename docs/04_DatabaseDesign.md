# 04_DatabaseDesign.md

# Database Design

## Purpose

Define a scalable relational database supporting all Hotel Credit
Management operations.

------------------------------------------------------------------------

# Main Entities

## Hotel

-   HotelID (PK)
-   HotelName
-   Address
-   Currency
-   TimeZone
-   Active

------------------------------------------------------------------------

## Company

-   CompanyID (PK)
-   CompanyName
-   TaxNumber
-   Address
-   HotelID (FK)

------------------------------------------------------------------------

## Customer

-   CustomerID (PK)
-   CustomerCode
-   CustomerName
-   Company
-   MarketSegment
-   SalesManager
-   CreditLimit
-   CreditStatus
-   RiskScore
-   RiskLevel
-   HotelID (FK)

------------------------------------------------------------------------

## AgingBalance

-   AgingID (PK)
-   CustomerID (FK)
-   ImportID (FK)
-   Current_0_30
-   Aging_31_60
-   Aging_61_90
-   Aging_91_120
-   Aging_Over120
-   TotalBalance

------------------------------------------------------------------------

## ImportHistory

-   ImportID (PK)
-   ImportDate
-   FileName
-   ImportedBy
-   Duration
-   RowsImported
-   ErrorsCount
-   PortfolioValue

------------------------------------------------------------------------

## Payment

-   PaymentID (PK)
-   CustomerID (FK)
-   PaymentDate
-   Amount
-   Reference
-   Currency
-   Notes

------------------------------------------------------------------------

## Invoice

-   InvoiceID (PK)
-   CustomerID (FK)
-   InvoiceNumber
-   InvoiceDate
-   DueDate
-   Amount
-   Balance
-   Status

------------------------------------------------------------------------

## Reminder

-   ReminderID (PK)
-   CustomerID (FK)
-   ReminderType
-   ReminderDate
-   Status
-   Notes

------------------------------------------------------------------------

## PromiseToPay

-   PromiseID (PK)
-   CustomerID (FK)
-   PromiseDate
-   DueDate
-   Amount
-   Status

------------------------------------------------------------------------

## Litigation

-   LitigationID (PK)
-   CustomerID (FK)
-   OpenDate
-   Reason
-   Status
-   Resolution

------------------------------------------------------------------------

## CreditLimitHistory

-   HistoryID (PK)
-   CustomerID (FK)
-   OldLimit
-   NewLimit
-   ChangedBy
-   ChangedDate

------------------------------------------------------------------------

## KPIHistory

-   KPIID (PK)
-   ImportID (FK)
-   DSO
-   ADD
-   RecoveryRate
-   CEI
-   CashForecast
-   PortfolioRisk

------------------------------------------------------------------------

## Notification

-   NotificationID (PK)
-   UserID (FK)
-   Title
-   Message
-   Type
-   Status
-   CreatedAt

------------------------------------------------------------------------

## User

-   UserID (PK)
-   Name
-   Email
-   RoleID
-   Active

------------------------------------------------------------------------

## Role

-   RoleID (PK)
-   Name
-   Permissions

------------------------------------------------------------------------

## AuditLog

-   AuditID (PK)
-   UserID
-   Action
-   Entity
-   OldValue
-   NewValue
-   Timestamp
-   Device

------------------------------------------------------------------------

# Relationships

Hotel └── Company

Company └── Customer

Customer ├── AgingBalance ├── Invoice ├── Payment ├── Reminder ├──
PromiseToPay ├── Litigation ├── CreditLimitHistory

ImportHistory ├── AgingBalance └── KPIHistory

User ├── Notification └── AuditLog

Role └── User

------------------------------------------------------------------------

# Indexes

Indexes shall exist on:

-   CustomerCode
-   CustomerName
-   RiskScore
-   CreditStatus
-   ImportDate
-   InvoiceNumber
-   DueDate

------------------------------------------------------------------------

# Future Extensions

The schema must support:

-   Multi-hotel groups
-   Multi-company
-   Multi-currency
-   Opera PMS integration
-   Sage 1000 integration
-   REST API
-   Cloud synchronization
-   AI prediction engine
