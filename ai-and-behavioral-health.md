# AI Safety & Behavioral-Health Extra Protections (Verified)


## The real rule on AI + PHI (the fear, corrected)
**Using AI is not a HIPAA violation. Putting PHI into a tool without a BAA is.** Verified from HHS:
a cloud service provider (the category enterprise AI runs on) that processes/stores ePHI is a business
associate and needs a BAA; using one *without* a BAA "is in violation of the HIPAA Rules." And
critically — **a provider that receives only properly de-identified data is NOT a business associate
and needs no BAA.** So there are exactly two safe ways to use AI:
1. **De-identified / non-patient data only** (works with any AI, including consumer tools), or
2. **An enterprise AI tier under a signed BAA** (for anything touching PHI).

## Which AI will sign a BAA (and which won't)
- **AWS** — requires a signed BAA before using any HIPAA-Eligible Service with PHI; **Amazon Bedrock**
  (its generative-AI service) is HIPAA-eligible. So enterprise AWS AI can process PHI under a BAA.
- **OpenAI** — offers a BAA, but **only for enterprise/API tiers** (Zero-Retention API with Modified
  Retention, ChatGPT Enterprise, ChatGPT for Healthcare/Clinicians). **Consumer ChatGPT and ChatGPT
  Business do NOT get a BAA.**
- General pattern (verify each currently): **consumer AI products = no BAA = de-identified data only.
  Enterprise cloud AI (Azure OpenAI, AWS Bedrock, Google Vertex) = BAA available.**

## The safe pattern for AI marketing (concrete do/don't)
The reassuring truth for a nervous provider: **almost all marketing work is safe with AI, because
marketing rarely needs patient data at all.**
- ✅ **SAFE:** "Write a blog post about recovery after knee surgery." "Draft 5 Instagram captions about
  managing anxiety." "Improve this general service-page copy." "Draft a professional reply to a
  negative Google review **without confirming the person is a patient or mentioning any detail**."
- ❌ **UNSAFE:** Pasting a patient intake form, chart, or session note. "Summarize this patient's story
  into a testimonial." Uploading a client list to generate targeted outreach. Anything with a name,
  DOB, condition tied to a person, photo, or contact detail — into a tool without a BAA.
- **Always keep a human reviewer** before anything publishes.

## Psychotherapy notes — heightened protection (45 CFR 164.508(a)(2))
Psychotherapy notes (a therapist's private session-analysis notes, kept separate from the record) get
**special protection**: a patient authorization is required for almost any use, and the narrow
exceptions (originator's own treatment, training, legal/oversight) **do not include marketing**. So
psychotherapy notes can essentially **never** be used in marketing. For therapists this is a hard wall.

## 42 CFR Part 2 — substance-use records (stricter than HIPAA)
SUD/addiction-treatment records are governed by a **separate, stricter** federal rule (42 CFR Part 2).
A 2024 final rule aligned Part 2 more closely with HIPAA, but it remains more protective — which is
why **addiction-treatment marketing is especially high-risk** (and why Monument, an alcohol-treatment
firm, was an FTC target).

## Why behavioral/mental health is the enforcement epicenter
The headline FTC actions — **BetterHelp, Cerebral, Monument** — are all mental-health or substance-use.
Mental-health status is among the most sensitive data, condition-based ad targeting/retargeting is
especially fraught, and **teletherapy intake forms and lead-gen are exactly where the pixel leaks
happen.** Behavioral health providers are right to be cautious — about the *pixel and the intake form*,
not about drafting a blog post with AI.

## The de-escalated bottom line for the guide
The fear ("AI will leak my patients' data") is aimed at the wrong thing. The real risks are concrete
and avoidable: pixels on intake/booking pages, sending patient data to non-BAA tools, and using
patient stories without authorization. Follow the two safe AI patterns and the tracking rules, and a
provider can use modern marketing (and AI) confidently. **When patient data genuinely must enter a
tool, get a BAA; otherwise, de-identify and proceed.**

## Open (not verified — flag)
State mental-health data laws stricter than HIPAA (e.g., Washington My Health My Data Act specifics)
did not fully verify — covered partly in the FTC/state gap. Note as "varies by state, confirm locally."
