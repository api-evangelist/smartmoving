# SmartMoving (smartmoving)

<!-- API-EVANGELIST-PROVENANCE:BEGIN -->
> ### About this repository
>
> **This is not our API.** This repository is an independent, third-party profile of a company's
> **publicly available** API surface, maintained by [API Evangelist](https://apievangelist.com).
> API Evangelist does not operate, host, resell, or support this company's APIs, and is not
> affiliated with or endorsed by the company unless stated on the profile.
>
> **Where the information came from.** Everything here is assembled from material a member of the
> public can reach with a browser and no credentials — the company's own website, developer portal
> and documentation, the specifications it publishes for public use (OpenAPI, AsyncAPI, JSON Schema,
> `apis.json`, `llms.txt` and similar), its public repositories, and its public status, pricing and
> changelog pages. **Nothing here is obtained by breaching a system, defeating an access control, or
> using credentials of any kind.**
>
> **The rating is an independent assessment.** The Kin Score and Agent Readiness rating are
> independently calculated scores of a company's *public* API artifacts, produced by API Evangelist
> against a published rubric. They are not certifications, endorsements, security assessments, or
> audits, and they score published artifacts — not the quality, safety, or security of the software.
>
> **Corrections, re-scores, and removal are free.** No partnership, contract, or purchase is
> required, and you do not need to justify the request.
>
> - **Something wrong?** Open an issue on this repository, or email
>   [info@apievangelist.com](mailto:info@apievangelist.com).
> - **Published something new?** Ask for a re-score and we will re-run the rating.
> - **Want the listing taken down?** Say so and we will honor it. The profile is reduced to your
>   company name, a factual description, and a link to your own site, and the company is recorded as
>   **unrated** — never scored zero for having asked.
>
> **Response times.** Acknowledgement within **one business day**; removal or restriction within
> **two business days**; corrections and re-scores within **five business days**.
>
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

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
