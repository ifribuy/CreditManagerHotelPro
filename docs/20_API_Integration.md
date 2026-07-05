# 20_API_Integration.md

# API Integration Specification

## Objective

Expose and consume APIs for seamless integration with hotel and
enterprise systems.

## Architecture

Client (Android) \| REST / HTTPS \| API Gateway \| Business Services \|
Database

## Authentication

-   OAuth2
-   JWT Tokens
-   Refresh Tokens
-   Role-based authorization

## API Modules

### Customers

GET /customers GET /customers/{id} POST /customers PUT /customers/{id}
DELETE /customers/{id}

### Aging Balance

POST /imports GET /imports GET /imports/{id} GET /aging/current GET
/aging/history

### KPI

GET /kpis GET /kpis/dashboard GET /kpis/history

### Reports

POST /reports/pdf POST /reports/excel GET /reports/history

### Credit

GET /credit-limits PUT /credit-limits/{id} POST /credit/block POST
/credit/unblock

### Collections

POST /reminders POST /payments POST /promises GET /collections/tasks

### Litigation

GET /litigations POST /litigations PUT /litigations/{id}

### Notifications

GET /notifications PUT /notifications/read

### AI

POST /ai/analyze POST /ai/forecast POST /ai/recommendations POST
/ai/chat

## Response Format

JSON

{ "success": true, "message": "...", "data": {} }

## Error Codes

200 OK 201 Created 400 Bad Request 401 Unauthorized 403 Forbidden 404
Not Found 500 Internal Error

## Security

-   HTTPS only
-   JWT validation
-   Rate limiting
-   Audit logging
-   Request validation
-   Input sanitization

## Future APIs

-   GraphQL
-   WebSocket live updates
-   Webhooks
-   External partner APIs
