# SmartMoving (smartmoving)

SmartMoving is an all-in-one CRM and operations platform for moving companies, covering lead capture, sales and estimating, booking, dispatch and scheduling, storage, and customer follow-up. SmartMoving exposes a documented Open API (fronted by Azure API Management) to Growth Plan customers, authenticated with an `x-api-key` header, that reads and writes the platform's core CRM objects - customers, opportunities (quotes/estimates), leads, jobs (booked moves), payments, and follow-ups - plus a free, universally available Lead API for pushing new leads into an account from any lead provider or website. The API is offered in two tiers: Basic (read-only, for reporting and analytics) and Premium (read/write plus webhooks, for full integration and automation).

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/smartmoving/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/smartmoving/refs/heads/main/apis.yml)

## Tags

- Moving Software
- CRM
- Field Service
- Moving Company
- Operations
- Lead Management
- Dispatch

## Timestamps

- **Created:** 2026-07-04
- **Modified:** 2026-07-04

## APIs

### SmartMoving Customers API

List, retrieve, search, create, and update the customers (contacts / accounts) in a SmartMoving account, and read a customer's opportunities and storage accounts. Read operations are available on the Basic tier; create and update require the Premium tier.

- **Human URL:** [https://smartmoving-prod-api-management.developer.azure-api.net/](https://smartmoving-prod-api-management.developer.azure-api.net/)
- **Base URL:** `https://api.smartmoving.com/api`

#### Tags

- Customers
- CRM
- Contacts

#### Properties

- [Documentation](https://help.smartmoving.com/en/articles/9739804-smartmoving-s-open-api)
- [API Reference](https://smartmoving-prod-api-management.developer.azure-api.net/apis)
- [OpenAPI](openapi/smartmoving-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/smartmoving.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/smartmoving.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### SmartMoving Opportunities API

Retrieve opportunities (sales quotes / estimates) by ID or quote number, and read their associated jobs, payments, and follow-ups. Premium accounts can create follow-ups and jobs against an opportunity to automate the sales-to-booking workflow.

- **Human URL:** [https://smartmoving-prod-api-management.developer.azure-api.net/](https://smartmoving-prod-api-management.developer.azure-api.net/)
- **Base URL:** `https://api.smartmoving.com/api`

#### Tags

- Opportunities
- Quotes
- Estimates

#### Properties

- [Documentation](https://help.smartmoving.com/en/articles/9739804-smartmoving-s-open-api)
- [API Reference](https://smartmoving-prod-api-management.developer.azure-api.net/apis)
- [OpenAPI](openapi/smartmoving-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/smartmoving.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/smartmoving.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### SmartMoving Leads API

List and retrieve leads with pagination, read the set of available lead statuses, and (Premium) list leads assigned to a given salesperson - the read surface over the top of the sales pipeline that feeds reporting and routing integrations.

- **Human URL:** [https://smartmoving-prod-api-management.developer.azure-api.net/](https://smartmoving-prod-api-management.developer.azure-api.net/)
- **Base URL:** `https://api.smartmoving.com/api`

#### Tags

- Leads
- Sales
- Pipeline

#### Properties

- [Documentation](https://help.smartmoving.com/en/articles/9739804-smartmoving-s-open-api)
- [API Reference](https://smartmoving-prod-api-management.developer.azure-api.net/apis)
- [OpenAPI](openapi/smartmoving-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/smartmoving.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/smartmoving.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### SmartMoving Lead Provider API

Push new leads into a SmartMoving account from any website or third-party lead provider by POSTing to `/leads/from-provider/v2`. Authenticated by a per-source `providerKey` query parameter (not the Open API key) and free on every SmartMoving plan, with fields for contact, move details, origin and destination addresses, referral source, and UTM tracking.

- **Human URL:** [https://help.smartmoving.com/en/articles/3994387-smartmoving-lead-api-integration-guide](https://help.smartmoving.com/en/articles/3994387-smartmoving-lead-api-integration-guide)
- **Base URL:** `https://api.smartmoving.com/api`

#### Tags

- Lead Intake
- Webhook
- Ingestion

#### Properties

- [Documentation](https://help.smartmoving.com/en/articles/3994387-smartmoving-lead-api-integration-guide)
- [Documentation](https://help.smartmoving.com/en/articles/4547622-lookup-a-provider-key-api-link)
- [OpenAPI](openapi/smartmoving-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/smartmoving.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/smartmoving.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### SmartMoving Jobs & Moves API

Read the jobs (booked moves) attached to an opportunity and, on the Premium tier, create a job against an opportunity or delete a job - the surface that keeps external dispatch, project-management, and calendar tools in sync with SmartMoving's schedule.

- **Human URL:** [https://smartmoving-prod-api-management.developer.azure-api.net/](https://smartmoving-prod-api-management.developer.azure-api.net/)
- **Base URL:** `https://api.smartmoving.com/api`

#### Tags

- Jobs
- Moves
- Dispatch

#### Properties

- [Documentation](https://help.smartmoving.com/en/articles/9739804-smartmoving-s-open-api)
- [API Reference](https://smartmoving-prod-api-management.developer.azure-api.net/apis)
- [OpenAPI](openapi/smartmoving-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/smartmoving.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/smartmoving.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### SmartMoving Reference Data API

Read the lookup/reference data an account is configured with - branches (locations), users (staff / salespeople), service types, and referral sources - so integrations can resolve and route by branch, assign salespeople, and map external categories to SmartMoving values. Lead statuses are confirmed; the remaining reference collections are modeled from the documented data model pending developer-portal confirmation.

- **Human URL:** [https://smartmoving-prod-api-management.developer.azure-api.net/](https://smartmoving-prod-api-management.developer.azure-api.net/)
- **Base URL:** `https://api.smartmoving.com/api`

#### Tags

- Reference Data
- Branches
- Users

#### Properties

- [Documentation](https://help.smartmoving.com/en/articles/9739804-smartmoving-s-open-api)
- [API Reference](https://smartmoving-prod-api-management.developer.azure-api.net/apis)
- [OpenAPI](openapi/smartmoving-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/smartmoving.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/smartmoving.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### SmartMoving Webhooks API

Premium-tier outbound webhooks that POST event notifications to a URL you register when records change in SmartMoving - across leads, jobs, payments, documents, and customers - so external systems react in near real time instead of polling. Webhooks are server-to-endpoint HTTP callbacks, not a bidirectional WebSocket transport.

- **Human URL:** [https://smartmoving-prod-api-management.developer.azure-api.net/webhook-document](https://smartmoving-prod-api-management.developer.azure-api.net/webhook-document)
- **Base URL:** `https://api.smartmoving.com/api`

#### Tags

- Webhooks
- Events
- Automation

#### Properties

- [Documentation](https://smartmoving-prod-api-management.developer.azure-api.net/webhook-document)
- [Documentation](https://help.smartmoving.com/en/articles/9739804-smartmoving-s-open-api)
- [OpenAPI](openapi/smartmoving-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)

## Common Properties

- [Website](https://www.smartmoving.com)
- [LinkedIn](https://www.linkedin.com/company/smartmoving-software)
- [Documentation](https://help.smartmoving.com/en/articles/9739804-smartmoving-s-open-api)
- [Developer Portal](https://smartmoving-prod-api-management.developer.azure-api.net/)
- [Plans](plans/smartmoving-plans-pricing.yml)
- [Rate Limits](rate-limits/smartmoving-rate-limits.yml)
- [Fin Ops](finops/smartmoving-finops.yml)

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
