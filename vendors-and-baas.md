# BAAs, Vendors & De-Identification (Verified)


## Business associate basics
- A **business associate** is a person/entity that creates, receives, maintains, or transmits PHI to
  perform a function for a covered entity (45 CFR 160.103). **Data analysis and data aggregation are
  explicitly listed** — so an analytics or ad platform that *uses* PHI is a business associate, not a
  mere pipe.
- **The conduit exception is narrow:** only entities that *merely transmit* PHI (USPS, couriers, ISPs)
  are exempt. An analytics/ad platform that uses the data does **not** qualify — a common
  misunderstanding.
- **A BAA is mandatory** (45 CFR 164.504(e)) before any vendor may handle PHI: it must limit uses,
  require safeguards, require breach reporting, and **flow down** the same terms to subcontractors.
- **No BAA, no PHI.** Using a vendor that handles PHI without a signed BAA is *itself* the violation.

## Which marketing vendors WON'T sign a BAA (so PHI must never reach them)
- **Google Ads** and **Google Analytics** — will **not** sign a BAA covering PHI. (Google Cloud /
  Workspace can, under specific terms — different products.)
- **Meta / Facebook** — will **not** sign a BAA. The Meta Pixel is the recurring enforcement culprit.
- **→ Rule:** these tools are fine for general, non-PHI advertising, but PHI (identifiable patient
  data, condition-specific booking info) must never be sent to them. If a tracking vendor won't sign a
  BAA, either drop it from PHI-touching pages or route through a BAA-covered intermediary that
  de-identifies first.

## Which vendors DO sign BAAs (the compliant stack)
- **CallRail** — signs a BAA for healthcare accounts (call tracking with a BAA). Verified from
  CallRail's own docs.
- Others commonly offering BAAs (mentioned; verify each against its current docs before relying):
  HIPAA-compliant email/forms/scheduling/CRM vendors (e.g., Paubox, Hushmail, and healthcare-specific
  CRMs). **Vendor BAA availability changes and is often plan/tier-dependent — always confirm the
  current terms and get the BAA in writing.**

## De-identification — the two methods (the freedom key)
- **Safe Harbor** (45 CFR 164.514(b)(2)): remove the **18 identifiers** (names, sub-state geography,
  dates except year, phone/fax, email, SSN, MRN, account #, **IP address**, URLs, biometrics,
  full-face photos, any other unique code).
- **Expert Determination** (164.514(b)(1)): a qualified expert certifies "very small"
  re-identification risk.
- **Once de-identified, it's no longer PHI** — the Privacy Rule imposes no restrictions, so it can go
  into any tool, including non-BAA AI. This is the mechanism behind the whole "safe AI pattern."

## The practical compliant small-practice marketing stack
| Function | Compliant approach |
|---|---|
| Website analytics / ads | Google Ads/GA/Meta = **general non-PHI pages only**; keep off authenticated/booking pages; de-identify server-side |
| Call tracking | BAA-covered vendor (e.g., CallRail healthcare) |
| Forms / scheduling / intake | HIPAA-compliant, BAA-covered form/scheduling vendor — never a plain non-BAA form that a pixel can read |
| Email / SMS | BAA-covered HIPAA email/SMS vendor for anything patient-identifiable |
| CRM | BAA-covered healthcare CRM if it stores PHI |
| Reviews / testimonials | No PHI without written authorization; respond to reviews without confirming patient status |
| AI (content/marketing) | **De-identified data only** with consumer AI; or an enterprise AI tier under a signed BAA (see `ai-and-behavioral-health.md`) |

**The one rule that ties it together:** for every tool, ask "does PHI reach this vendor?" If yes, you
need a signed BAA. If the vendor won't sign one, either the PHI must be removed before it gets there
(de-identification) or you don't use that vendor for that purpose.
