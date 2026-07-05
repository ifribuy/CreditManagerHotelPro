# 02_BusinessRules.md

# Business Rules

## Aging Buckets (Official)

The application shall use only these buckets:

-   0-30 JRS
-   31-60 JRS
-   61-90 JRS
-   91-120 JRS
-   AU DELÀ 120 JRS

## Collection Workflow

### 0-30 JRS

Status: Current Actions: - No reminder - Monitor account

### 31-60 JRS

Status: Reminder 1 Actions: - Reminder email - Collection task -
Dashboard notification

### 61-90 JRS

Status: Reminder 2 Actions: - Reminder email - Phone call - Payment
commitment request - Escalation to Credit Manager

### 91-120 JRS

Status: Escalation Actions: - Formal notice - Recommend credit block -
Daily monitoring - Financial Controller notification

### AU DELÀ 120 JRS

Status: Critical Actions: - Critical account - Credit blocked -
Litigation evaluation - Provision recommendation - Executive alert

# Credit Limit Rules

-   Credit limit configurable per customer.
-   Warning at 80%.
-   Critical at 100%.
-   Automatic block option.
-   Manual override with audit trail.

# Payment Promise

States: - Planned - Active - Due today - Overdue - Fulfilled - Cancelled

# Litigation

States: - Open - Under review - Waiting customer - Resolved - Closed

# Risk Score

Factors: - Aging - Outstanding amount - Credit limit usage -
Litigation - Payment behavior - Broken promises

Risk Levels: - Green - Yellow - Orange - Red - Dark Red

# Audit Rules

Every action must store: - User - Date - Time - Previous value - New
value - Device - Reason

# Executive Alerts

Notify when: - Customer exceeds credit limit - Customer reaches \>120
JRS - DSO increases - Recovery rate decreases - Cash forecast
deteriorates - High-value promise expires

# AI Recommendations

Recommend: - Customers to call today - Customers to block - Customers to
unblock - Collection priorities - Expected cash this week - High-risk
accounts
