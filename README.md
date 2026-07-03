# Vetstoria (vetstoria)

Vetstoria provides real-time online appointment booking, veterinary websites, and online payments for veterinary practices. It integrates in real time with 40+ practice management systems (PIMS) - including ezyVet, IDEXX Neo, IDEXX Cornerstone, IDEXX Animana, Covetrus Ascend, AVImark, RxWorks, visionVPM, Provet Cloud, and OpenVPMS - to sync availability, prevent double-bookings, and match booked clients and pets back into the PIMS. Founded in 2015, Vetstoria is used by more than 5,000 practices worldwide and operates as PetDesk Direct Booking in the United States.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/vetstoria/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/vetstoria/refs/heads/main/apis.yml)

## API Access Model (Important)

**Vetstoria does not publish a public, self-service developer API.** There is no developer portal, no public API reference, no OpenAPI definition, and no documented WebSocket or webhook API at the time of cataloging. This entry is intentionally a stub that documents the company and its access model honestly rather than fabricating an API surface.

How integration actually works:

- **Partner-gated.** Vendors integrate through a contact-based **Integrations Partner** program. There is no public documentation on how to become one; prospective partners submit a form and Vetstoria's team follows up. See [Partners](https://www.vetstoria.com/partners/).
- **PIMS-side driven.** In practice, each integration is configured from the practice management system, not from a Vetstoria developer console. For example, ezyVet exposes Vetstoria as an "API Partner" that continuously receives available calendar times, and IDEXX Neo auto-generates an API key when the Vetstoria connection is enabled under Administration > Integrations.
- **Client/pet matching is controlled by Vetstoria.** When a booking is made, Vetstoria cross-references email, phone number, and pet names against existing PIMS records to link (or flag) the appointment, rather than relying on the PIMS to deduplicate.

Because no public endpoints, request/response schemas, or authentication details are documented, no `openapi/`, `collections/`, `rate-limits/`, or `finops/` artifacts are included. If Vetstoria opens partner API documentation in the future, this entry can be expanded with real, sourced endpoints.

## Tags

- Veterinary
- Online Booking
- Appointment Scheduling
- Practice Management
- PIMS Integration
- Healthcare
- Payments
- Partner API

## Timestamps

- **Created:** 2026-07-03
- **Modified:** 2026-07-03

## Pricing

Vetstoria is sold as a fixed monthly per-practice subscription tiered by clinician count (no lock-in contracts, 30-day risk-free guarantee, one month free on annual billing). Representative published pricing:

- **Small Team** (up to 2 clinicians): £199 / €199 / A$199 per month
- **Medium Team** (up to 4 clinicians): £299 / €299 / A$299 per month
- **Large Team** (up to 7 clinicians): £399 / €399 / A$449 per month
- **Custom** (veterinary groups / unique setups): contact for quote; adds advanced analytics and quarterly reviews

All tiers include real-time online booking, secure online payments, reporting and analytics, and 24/7 support. Bundled website plans are available as an add-on. US pricing is handled via PetDesk Direct Booking (third-party sources cite from ~$230/month). See [Plans & Pricing](https://www.vetstoria.com/pricing/).

## Common Properties

- [LinkedIn](https://www.linkedin.com/company/vetstoria)
- [Website](https://www.vetstoria.com)
- [Documentation](https://www.vetstoria.com/integrations/)
- [Partners](https://www.vetstoria.com/partners/)
- [Plans](https://www.vetstoria.com/pricing/)

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
