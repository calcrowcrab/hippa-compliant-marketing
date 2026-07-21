# Website Tracking & PHI Leakage (Verified)

**This is the single biggest current HIPAA-marketing risk.**

## The OCR tracking bulletin — timeline
- **Dec 1, 2022:** OCR's original bulletin on "Use of Online Tracking Technologies by HIPAA Covered
  Entities and Business Associates." Cookies/pixels/tracking that collect identifiable info may
  constitute PHI. Distinguished **authenticated pages** (patient portal — generally PHI) from
  **unauthenticated pages** (public info like visiting hours — generally not, but sometimes).
- **March 18, 2024:** updated bulletin. Kept the framework; clarified the IP-address question.
- **Content last reviewed June 26, 2024** (post-litigation).

## AHA v. Becerra — what got struck down (the law is genuinely unsettled)
**June 20, 2024:** the US District Court for the Northern District of Texas **vacated** the part of the
OCR bulletin treating **[IP address] + [visit to an unauthenticated public page about a health
condition/provider]** as automatically triggering HIPAA. OCR's March 2024 update had already conceded
an IP address tied to a health-condition page is **not** by itself PHI absent a connection to actual
healthcare.

**What still stands:** tracking on **authenticated pages** (patient portals, booking-after-login) is
still treated as touching PHI and must be configured to comply. And when an unauthenticated visit is
genuinely about the person's *own* healthcare, identifiable info can still be PHI. **→ The safe read
for a small practice: the pixel-on-the-booking-page problem did NOT go away.** The court narrowed one
edge (anonymous browsing of a public condition page); it did not bless pixels on pages where patients
identify themselves or book.

## The leakage mechanism (how a normal marketing setup leaks PHI)
- **A tracking vendor that meets the business-associate definition IS a business associate whether or
  not a BAA is signed** — and PHI disclosure to it **cannot** be cured by a privacy-policy notice or
  the vendor's promise to strip/de-identify *after* receipt. De-identification must happen *before*
  the data reaches a non-BAA vendor.
- **Meta Pixel "Advanced Matching"** transmits email, name, phone, city, state, ZIP, birthdate, and
  external IDs to Meta — **and can turn on automatically** in Events Manager without the practice
  writing any code. This is how appointment/intake data silently reaches Facebook.
- **Google Analytics / Google Ads conversion tags** on a booking or condition page can send URLs,
  form data, and IPs to Google. Google Ads and GA **will not sign a BAA** covering PHI (see
  `vendors-and-baas.md`), so PHI reaching them is a violation.
- The **FTC** independently treats this as its own violation (GoodRx $1.5M, BetterHelp, etc. — see
  `enforcement-and-state-laws.md`). FTC's own Office of Technology (Mar 16, 2023) documented that pixels are
  hidden and silently transmit form entries and behavioral data.

## How to configure marketing tracking safely (practical)
- **Never place Meta Pixel / GA / Google Ads tags on authenticated pages (patient portal, post-login
  booking) or on pages where patients submit identifiable info.** This is the core rule that survives
  AHA v. Becerra.
- **Keep PHI out of URLs and form-field names** — no `?condition=oncology` or appointment details in
  query strings that a pixel reads.
- **Use a BAA-covered intermediary** (a Customer Data Platform / server-side setup) that de-identifies
  *before* passing anything to non-BAA ad/analytics platforms.
- **General, unauthenticated informational pages** (homepage, a blog about knee pain) are lower risk —
  but audit what the pixel actually captures; Advanced Matching defaults are the trap.
- **When in doubt, remove the pixel from the sensitive pages entirely** — measure conversions offline
  instead (below).

## Conversion tracking for healthcare PPC without leaking PHI
The safe pattern: don't send patient identity back to Google/Meta. Track the *click* and reconcile
booked appointments **offline / server-side** using de-identified or hashed-under-BAA data, so the ad
platform learns "a conversion happened" without receiving who or what condition. Standard client-side
conversion pixels on a booking confirmation page are exactly the risk to avoid.

## Documented breaches (the scale — reported figures, verify before quoting exact numbers)
Hospital systems (Novant Health, Advocate Aurora, Kaiser in 2024) disclosed pixel-related breaches
affecting millions of patients. Specific patient counts were widely reported but not all re-verified
here — cite as "reported" with the year.

## The honest caveat
Post-AHA-v-Becerra, the law here is **genuinely unsettled** at the edges. The skill/guide should say
so: the authenticated-page and booking-page risk is solid; the anonymous-public-page edge is contested;
and OCR could re-issue guidance. When a decision hinges on the gray zone, that's a "check with your
attorney" moment.
