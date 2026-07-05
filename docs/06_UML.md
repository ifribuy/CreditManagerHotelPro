# 06_UML.md

# UML Specification

## Use Case Diagram

Actors: - Credit Manager - Collection Officer - Financial Controller -
Finance Director - General Manager - System AI

Main Use Cases: - Import Excel Aging Balance - View Dashboard - View
Customer - Search Customer - Calculate KPIs - Compare Periods - Generate
PDF Report - Export Excel - Register Payment - Create Reminder - Manage
Credit Limit - Block Credit - Unblock Credit - Create Promise to Pay -
Open Litigation - Close Litigation - Configure Settings - Manage Users -
Receive Notifications - Ask AI Assistant

------------------------------------------------------------------------

## Class Model

Customer ├── AgingBalance ├── Invoice ├── Payment ├── Reminder ├──
PromiseToPay ├── Litigation └── CreditLimit

ImportHistory └── KPIHistory

Hotel └── Company └── Customer

User └── Role

------------------------------------------------------------------------

## Sequence -- Excel Import

User → Select File → Validate Structure → Parse Workbook → Save Import →
Calculate KPIs → Refresh Dashboard → Save Audit Log

------------------------------------------------------------------------

## Sequence -- Credit Block

Credit Manager → Open Customer → Review Risk → Block Credit → Save
Decision → Notify Users → Update Dashboard → Audit Log

------------------------------------------------------------------------

## State -- Customer Credit

Active → Warning → Restricted → Blocked → Under Litigation → Closed

------------------------------------------------------------------------

## Activity -- Collection

Import → Identify Overdue → Prioritize → Reminder → Phone Call → Promise
→ Escalation → Litigation → Closed

------------------------------------------------------------------------

## Component Diagram

Presentation ↓ Domain ↓ Repositories ↓ Database / Excel Parser

------------------------------------------------------------------------

## Deployment

Android App ↓ Room Database ↓ Export Engine ↓ PDF Engine ↓ Excel Engine
↓ Notification Engine ↓ AI Engine

Future: REST API Cloud Sync Opera PMS Sage 1000
