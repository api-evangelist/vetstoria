# Vetstoria (vetstoria)

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
> **Not from the company, and here with a question?** You are welcome here — we would rather be the
> front line and point you the right way than have a good report go nowhere. What this repository
> can answer is narrow, though, so it is worth knowing who you are actually looking for:
>
> - **A question about how the API works, an account, billing, or a bug in the service** — that is
>   the company's own support, not us. We profile this API; we do not operate it and cannot see
>   your account.
> - **A bug in an open-source project we only catalog** — file it on that project's own repository.
>   This has happened with a real and correct bug report that reached us instead of the people who
>   could fix it, which helped nobody.
> - **Anything about this listing itself** — the description, the tags, the rating, a missing or
>   wrong artifact — is ours. Open an issue here.
> - **Not sure, or something general about API Evangelist or APIs.io** — open an issue on the
>   [APIs.io Inbox](https://github.com/api-search/inbox) and we will route it.
>
> **This repository contains no software, and we will never ask you to download anything.** There is
> no build, release, installer, or binary here — only text and machine-readable API descriptions, so
> there is nothing here that can be "corrupt" or need "repairing". Any issue, comment, or email
> claiming otherwise and offering a download link is not from us and is hostile. Do not follow the
> link; it is a lure. Report it to GitHub and, if you like, tell us at
> [info@apievangelist.com](mailto:info@apievangelist.com) so we can take it down.
>
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

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
