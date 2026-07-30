# Kotak Mahindra Bank

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
