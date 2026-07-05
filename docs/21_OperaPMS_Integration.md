# 21_OperaPMS_Integration.md

# Opera PMS Integration Specification

## Objective

Synchronize CreditManagerHotelPro with Oracle OPERA PMS to eliminate
manual data entry and maintain an up-to-date receivables portfolio.

## Integration Modes

-   Manual Excel import
-   Scheduled file import
-   REST API (future)
-   Secure file exchange (SFTP)

## Data Sources

-   AR Aging
-   Customer Accounts
-   Invoices
-   Payments
-   Credit Limits (if available)
-   Companies
-   Market Segments

## Import Workflow

1.  Receive OPERA export
2.  Validate format
3.  Map fields
4.  Detect duplicates
5.  Import changes
6.  Update KPIs
7.  Refresh dashboards
8.  Write audit log

## Field Mapping

OPERA Customer -\> Customer AR Balance -\> Aging Balance Invoice -\>
Invoice Payment -\> Payment Company -\> Company Market -\> Market
Segment

## Synchronization Rules

-   Preserve import history
-   Do not overwrite manual notes
-   Detect deleted customers
-   Flag mapping errors
-   Log every synchronization

## Error Handling

-   Invalid format
-   Missing mandatory fields
-   Duplicate customer code
-   Invalid currency
-   Import interruption recovery

## Security

-   Encrypted transfers
-   Authentication
-   Audit trail
-   Import validation

## Future Enhancements

-   Real-time synchronization
-   OPERA Cloud API
-   Automatic scheduled sync
-   Bi-directional updates where permitted
