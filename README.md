# Flockjay

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

Flockjay is a sales enablement platform (LMS + sales content management + AI coaching), first
surfaced as a portfolio company of Lightspeed Venture Partners.

**This profile was previously recorded as having no developer API. That was wrong, and it has been
corrected.** A 2026-08-14 enrichment pass found two live API surfaces that Flockjay does not
document anywhere:

- **`https://api.flockjay.com/api/`** — a Django REST Framework API whose root is anonymously
  readable and enumerates 20 collections across two version trees. Every collection requires a
  Flockjay-issued token. There is no OpenAPI, no reference, and no developer portal.
- **`https://api.flockjay.com/mcp`** — a hosted Model Context Protocol server, announced on
  [Flockjay's own blog](https://flockjay.com/resources/blog/ai-enablement-mcp-server), protected by
  OAuth 2.1 authorization-code + PKCE with RFC 9728 protected-resource metadata and RFC 7591
  dynamic client registration. Anonymous `tools/list` returns HTTP 401, so the tool list is not
  public.

The authorization layer is genuinely standards-based and correctly cross-linked. The REST API
beneath it publishes no contract, no error vocabulary, no idempotency, no rate-limit signal and no
deprecation policy. See `conformance/`, `conventions/` and `mcp/` for the evidence.

Backed by: lightspeed-venture-partners
