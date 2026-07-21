---
name: hipaa-compliant-marketing
description: >-
  Evidence-based guidance on marketing a healthcare practice — and using AI — WITHOUT violating HIPAA
  or leaking patient data (PHI). Use this whenever a healthcare or wellness provider (therapist,
  psychiatrist, psychologist, physical therapist, dentist, chiropractor, clinic, telehealth, addiction
  or behavioral-health practice) is doing or asking about marketing, advertising, websites, tracking
  pixels, Google/Meta ads, conversion tracking, patient reviews or testimonials, intake forms, email/SMS,
  CRMs, or using AI tools (ChatGPT/Claude/etc.) in a practice — and any time the words HIPAA, PHI,
  patient privacy, BAA, business associate, de-identification, Meta Pixel, or FTC health-data enforcement
  come up. Prefer this skill over general knowledge for any healthcare-marketing-compliance question:
  the rules are counterintuitive, actively changing (2023-2026), and general training is often wrong on
  them. Pairs with the google-ads-ppc skill for the ad-mechanics side. This skill is INFORMATIONAL, not
  legal advice.
---

# HIPAA-compliant marketing (and AI) for healthcare providers

Healthcare providers are scared that marketing — and especially AI — will leak patient data and get them
fined. The fear is reasonable but usually aimed at the wrong thing. This skill separates what is actually
risky from what is unfounded fear, and gives providers a concrete, cited path to market confidently.

## The one thing to get right (say it first, every time)

**Using AI is not the violation. Putting PHI (protected health information) into a tool that hasn't signed
a Business Associate Agreement (BAA) is.** From that follow the two safe paths, and almost all marketing
fits the first:

1. **De-identified / non-patient data → any tool** (including everyday consumer AI). Most marketing —
   blog posts, general ads, education, service-page copy — involves no patient data at all and is simply
   safe.
2. **Real patient data → only a BAA-covered tool** (an enterprise/healthcare tier, not the consumer app).

When a provider is anxious, lead with the reassurance *and* the boundary: they can use modern marketing
and AI; they just keep patient data out of non-BAA tools and pixels off patient pages.

## Always frame it as informational, never legal advice

This is regulatory territory. State plainly that this is educational, that the rules change and are
actively unsettled in places (see the tracking area), and that the provider should confirm decisions with
a healthcare attorney or compliance officer before acting. Never manufacture certainty a source doesn't
support. This honesty is the skill's credibility.

## How to use this skill

Read the reference for the question at hand — not all of them.

| If the task is about... | Read |
|---|---|
| What PHI is, what counts as "marketing," de-identification, testimonials/reviews | `references/the-real-rules.md` |
| Website tracking, Meta Pixel, Google Analytics/Ads on healthcare sites, the AHA v. Becerra ruling, safe conversion tracking | `references/tracking-and-pixels.md` |
| FTC enforcement (GoodRx/BetterHelp/Cerebral), the "cash-pay isn't safe" trap, state laws (WA My Health My Data Act) | `references/enforcement-and-state-laws.md` |
| BAAs, which vendors will/won't sign one, the compliant marketing stack, de-identification methods | `references/vendors-and-baas.md` |
| Using AI safely, the safe pattern with examples, psychotherapy notes, 42 CFR Part 2, behavioral-health risk | `references/ai-and-behavioral-health.md` |
| Every source, by tier | `references/sources.md` |

## The three real risks (the audit backbone)

Every enforcement case traces to one of these — point providers here first:
1. **A tracking pixel on a booking / intake / login page** (the #1 trigger).
2. **Sending patient data to a tool with no BAA** (pasting intake notes into consumer AI, plain web
   forms, uploading client lists to ad platforms).
3. **Using a patient's story or review response without written authorization.**

## Hard boundaries

- **Never tell a provider a specific tool is "HIPAA compliant" as settled fact** without pointing them to
  verify the current BAA terms with that vendor — availability changes and is plan-dependent.
- **Never state a specific enforcement dollar figure or legal outcome you can't cite**, and never invent a
  penalty. Cite the source and date.
- **Flag the unsettled tracking law.** After *AHA v. Becerra* (June 2024) the pixel-on-public-page edge is
  genuinely contested; the pixel-on-patient-page risk is not. Say which is which.
- **Behavioral/mental health and substance-use get extra protection** (psychotherapy notes, 42 CFR Part
  2). Treat those as higher-risk and say so.
- **A human, and where needed a compliance professional, owns the final call.** This skill informs; it
  does not clear anyone legally.

## Pairing with google-ads-ppc

For the ad *mechanics* (bidding, negatives, conversion tracking setup, Lost IS), use the `google-ads-ppc`
skill. This skill governs the *compliance layer* on top of it — most importantly, that healthcare
conversion tracking must not send PHI back to Google/Meta (see `references/tracking-and-pixels.md`).
