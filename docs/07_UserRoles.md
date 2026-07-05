# 07_UserRoles.md

# User Roles & Permissions

## Objective

Define access rights for every user profile in CreditManagerHotelPro.

## Roles

### 1. Credit Manager

Full operational access.

Permissions: - Import Excel balances - View all dashboards - Manage
customers - Edit credit limits - Block / Unblock credit - Approve
payment promises - Manage litigation - Generate all reports - Configure
KPI thresholds - Access AI assistant - Export PDF / Excel - View audit
logs

------------------------------------------------------------------------

### 2. Collection Officer

Permissions: - View assigned customers - Create reminders - Register
phone calls - Register payments - Create payment promises - Add notes -
View collection KPIs

Restrictions: - Cannot modify credit limits - Cannot block credit -
Cannot access administration

------------------------------------------------------------------------

### 3. Financial Controller

Permissions: - View financial dashboards - Review KPIs - Validate
reports - Review critical accounts - Recommend provisions - Monitor DSO
and Cash Forecast

------------------------------------------------------------------------

### 4. Finance Director

Permissions: - Executive dashboards - Portfolio analysis - Approve
credit limit changes - Approve credit blocks - Review AI
recommendations - Export executive reports

------------------------------------------------------------------------

### 5. General Manager

Read-only access.

Can view: - Executive Dashboard - Portfolio Health - Cash Forecast - Top
Debtors - Top Risks - Strategic Reports

------------------------------------------------------------------------

### 6. System Administrator

Permissions: - Manage hotels - Manage companies - Manage users - Manage
roles - Configure application - Manage themes - Configure
notifications - Backup / Restore - Audit management

------------------------------------------------------------------------

## Permission Matrix

  ---------------------------------------------------------------------------------------------
  Feature          Collector   Credit Manager Controller   Finance Director GM          Admin
  ---------------- ----------- -------------- ------------ ---------------- ----------- -------
  Import Excel     ✓           ✓              ✓            ✓                ✗           ✓

  View Dashboard   ✓           ✓              ✓            ✓                ✓           ✓

  Customer Details ✓           ✓              ✓            ✓                ✓           ✓

  Block Credit     ✗           ✓              Recommend    ✓                ✗           ✓

  Change Credit    ✗           ✓              ✗            ✓                ✗           ✓
  Limit                                                                                 

  Reports          Limited     ✓              ✓            ✓                Executive   ✓

  Administration   ✗           Limited        ✗            ✗                ✗           ✓
  ---------------------------------------------------------------------------------------------

## Audit Rules

Every sensitive action records: - User - Date - Time - Device - Previous
value - New value - Reason

## Future Roles

-   Group Credit Manager
-   Regional Finance Director
-   Internal Auditor
-   External Auditor
-   Read-only API User
