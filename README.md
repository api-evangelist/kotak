# Kotak Mahindra Bank

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

Kotak Mahindra Bank Limited is an Indian private-sector bank headquartered in Mumbai, and the first non-banking finance company in India to convert into a full commercial bank. Alongside retail, corporate, and NRI banking it operates the **Kotak API Platform** ([api.kotak.com](https://api.kotak.com)), an enterprise open-banking developer portal offering a curated corporate banking API stack.

## API surface

The platform publishes **39 API products across 6 categories** (harvested from the portal's own public catalog at `https://api.kotak.bank.in/mapping/`):

| Category | Products |
|---|---|
| Account Services | Balance Enquiry, Account Statement |
| Payment Services | 24x7 payments (NEFT/RTGS/IFT), CMS Bulk Payments, Corporate Remittance (IMPS), Name Enquiry, NEFT-RTGS credit status, Merchant cashback (UPI pay) |
| Collection Services | UPI Web Collect, UPI Autopay, UPI manual refund, Merchant VPA verify, E-collection virtual accounts, NACH physical/e-mandate/Aadhaar e-mandate, BBPS agent + biller integration, direct debit queryback |
| Trade Finance | Import/export Letters of Credit, Standby LCs, Bankers Guarantees, Collections, Inward/Outward Remittance, Shipping Guarantee, Documents Upload, Finance Standalone, Miscellaneous |
| Onboarding | Application, Dedupe, Offers, OTP |
| Authorization Services | OAuth 2.0 access token |

Access is aimed at fintechs, ERP providers, and NBFCs via the **Connected Banking** partner program.

## What is public vs gated

- **Public:** the product catalog (including a machine-readable JSON catalog), category descriptions, FAQ, support desk, and API Terms of Use.
- **Gated (registration + corporate-domain email + login):** API specifications, the integrated sandbox testing environment, and per-product downloadable integration kits.

Kotak publishes **no** public OpenAPI/Swagger description, error reference, rate-limit documentation, versioning or deprecation policy, idempotency contract, API status page, changelog, CLI, SDKs, MCP server, or vulnerability-disclosure program as of 2026-07-19.

## Artifacts in this repo

- `well-known/kotak-api-catalog.json` — the harvested machine-readable API catalog
- `well-known/kotak-well-known.yml` — `/.well-known/` probe index
- `authentication/kotak-authentication.yml` — OAuth 2.0 profile
- `conventions/kotak-conventions.yml` — cross-cutting semantics (and the documented gaps)
- `conformance/kotak-conformance.yml` — UPI / NACH / BBPS / IMPS / NEFT-RTGS scheme conformance
- `sandbox/kotak-sandbox.yml` — integrated sandbox posture
- `packages/kotak-packages.yml` — registry sweep (no first-party SDKs found)
- `security/kotak-domain-security.yml` — TLS/HSTS/DNSSEC/CAA/SPF/DMARC probe
- `llms/kotak-llms.txt` — agent-facing index

Backed by: norwest-venture-partners — https://kotak.com
