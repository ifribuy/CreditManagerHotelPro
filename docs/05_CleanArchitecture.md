# 05_CleanArchitecture.md

# Clean Architecture

## Objective

Build a scalable, maintainable Android application using a strict
layered architecture.

## Layers

presentation/ - Screens - Navigation - Components - ViewModels - UI
State

domain/ - Models - Use Cases - Repository Interfaces - Business Rules -
KPI Engine - Risk Engine - Validation

data/ - Excel Parser - Local Database - Repositories - Mappers - Data
Sources

core/ - Constants - Extensions - Utilities - Logger - Date/Time -
Configuration

di/ - Dependency Injection modules

## Dependency Rule

Presentation ↓ Domain ↓ Data

No layer may access an upper layer.

## Main Use Cases

-   Import Aging Balance
-   Calculate KPIs
-   Compare Periods
-   Generate PDF
-   Generate Excel
-   Forecast Cash
-   Calculate Risk Score
-   Block Credit
-   Unblock Credit
-   Register Payment
-   Create Reminder
-   Create Promise To Pay

## Repository Interfaces

CustomerRepository ImportRepository ReportRepository KpiRepository
NotificationRepository SettingsRepository

## Principles

-   Single Responsibility
-   Dependency Inversion
-   Separation of Concerns
-   Immutable UI State
-   Reusable Components
-   Testable Business Logic

## Performance

-   Background imports
-   Lazy loading
-   Pagination
-   Cached calculations
-   Offline-first behavior

## Security

-   Role-based access
-   Audit logging
-   Encrypted local database
-   Secure session handling

## Future Ready

Architecture must support: - Web client - Desktop client - Cloud
synchronization - REST API - AI services - External PMS integrations
