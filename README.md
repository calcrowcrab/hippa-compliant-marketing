# hipaa-compliant-marketing

An open-source, evidence-graded **HIPAA-compliant-marketing skill for healthcare providers** — therapists,
psychiatrists, physical therapists, dentists, clinics, and telehealth/behavioral-health practices — who
want to market their practice and use AI **without leaking patient data or getting fined.**

Built for [Claude skills](https://docs.claude.com); pairs with the `google-ads-ppc` skill for the ad
mechanics. Every claim is graded by evidence tier and cited to primary sources (HHS OCR, the HIPAA and 42
CFR Part 2 rules, FTC enforcement actions, and vendors' own BAA documentation).

## The one idea

**Using AI is not the violation. Putting patient data (PHI) into a tool that hasn't signed a Business
Associate Agreement is.** That yields two safe paths — de-identified data works with any tool, and real
patient data needs a BAA — and almost all marketing fits the first. The skill turns the fear into a
checklist.

## The three real risks

Every enforcement case traces to one of these, not to AI in the abstract:
1. A tracking pixel on a booking / intake / login page.
2. Sending patient data to a tool with no BAA.
3. Using a patient's story or review response without written authorization.

## What's inside

```
hipaa-compliant-marketing/
├── SKILL.md                              # orchestrator + the core thesis (read first)
└── references/
    ├── the-real-rules.md                 # PHI, "marketing" definition, de-identification, testimonials
    ├── tracking-and-pixels.md            # the #1 risk: pixels, Meta/GA, AHA v. Becerra, safe tracking
    ├── enforcement-and-state-laws.md     # FTC cases ($ figures), the "cash-pay isn't safe" trap, state laws
    ├── vendors-and-baas.md               # who signs a BAA, the compliant stack, de-identification methods
    ├── ai-and-behavioral-health.md       # the safe AI pattern, psychotherapy notes, 42 CFR Part 2
    └── sources.md                        # every source, by evidence tier
```

## Not legal advice

This is educational. HIPAA/FTC/state rules change, the online-tracking area is actively unsettled after
*AHA v. Becerra* (2024), and obligations depend on the specific practice and state. **Confirm compliance
decisions with a healthcare attorney or qualified compliance professional, and verify any vendor's BAA
terms directly with that vendor.**

## Companion guide

A provider-facing interactive guide (plain-English, with an "am I at risk?" self-check) is distributed
alongside this skill.

## License

MIT (see `LICENSE`).
