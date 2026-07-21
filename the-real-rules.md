# Fundamentals (Verified)


## What is PHI (Protected Health Information)
Individually identifiable health information relating to a person's past/present/future physical or
**mental** health, care, or payment — including demographic data that identifies them or could
reasonably be used to. Held in any form (electronic, paper, oral). [HHS Privacy summary; de-id page]

## De-identification — the escape hatch (this is the key to safe AI use)
Two methods, and once data is de-identified it is **no longer PHI and the Privacy Rule places no
restrictions on its use** — you can use it with any tool, including non-BAA AI:
- **Safe Harbor** (45 CFR 164.514(b)(2)): remove **18 identifiers** — names; geographic units smaller
  than a state (except first 3 ZIP digits for areas >20,000); all date elements except year;
  phone/fax; email; SSN; MRN; account numbers; **IP addresses**; URLs; biometrics; full-face photos;
  and any other unique identifying number/characteristic/code.
- **Expert Determination** (164.514(b)(1)): a qualified statistician certifies the re-identification
  risk is "very small."

## What counts as "marketing" under HIPAA
"A communication about a product or service a purpose of which is to encourage recipients to purchase
or use" it (45 CFR 164.501). A covered entity **must get written patient authorization** to use PHI
for marketing — **except** face-to-face communications and promotional gifts of nominal value
(45 CFR 164.508(a)(3)). When marketing involves payment from a third party, extra rules apply.

**The bright line:** communications for **treatment** of the individual and **care coordination /
case management** are NOT marketing and need no authorization. General advertising that doesn't use
PHI (a billboard, a blog post about knee pain, an ad to a purchased non-patient list) is also fine —
because it doesn't touch PHI at all. The violation is using *patient data* to market.

## Minimum Necessary standard (45 CFR 164.502(b), 164.514(d))
Use/disclose only the minimum PHI needed for the purpose. Applied to marketing: don't pull more
patient data into a campaign tool than the task strictly requires.

## Open (not verified — flagged for follow-up / label as unconfirmed)
- **Testimonial/review OCR enforcement cases** (Elite Dental $10k 2019, US Dermatology-type cases):
  the *rule* is clear (responding to an online review with any patient-specific detail discloses PHI
  and needs authorization), but the specific fined-case citations did NOT survive verification — state
  the rule as solid, present specific case dollar amounts as "reported" until re-verified.
- **TCPA/CAN-SPAM specifics** for appointment reminders vs. marketing texts — not verified this run.

## Practical do/don't (from verified rules)
- **DO** market with de-identified or non-patient data freely (blog content, general ads, education).
- **DO** treat appointment reminders and care communications as permitted (not marketing).
- **DON'T** use identifiable patient info to target, retarget, or build testimonials without written
  authorization.
- **DON'T** respond to an online review with anything that confirms someone is your patient or reveals
  their condition/treatment — even to defend yourself. That's a disclosure of PHI.
