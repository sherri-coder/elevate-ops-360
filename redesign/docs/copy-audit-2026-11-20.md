# Homepage copy audit (redesign prototype)

Date: 2026-11-20. Auditor: Claude (lead UI developer). Branch: feature/qa-a11y-responsive.
Scope: every product claim, service description and CTA on redesign/index.html.
Nothing was rewritten. Copy is unchanged. Rewrites below are suggestions for Sherri's approval.

Sources checked (Project docs): Nexus_Product_Spec_v1.0, Nexus_Platform_Marketing_Brief (pdf),
Nexus_Product_Marketing_Brief_Sonny (guardrails section), Nexus_V1_Launch_Plan_v2,
Nexus_Master_Roadmap and v3, Nexus_Complete_Tool_Reference, Notion hub (Nov 20 decisions).
Not available to me: the Notion page "Nexus Capabilities for Marketing (approved claims)" was not located
by search, and the Notion "Marketing Approval & Claims Register" is an empty planning stub. Treat the audit as
checked against product and marketing briefs, not against a formal approved-claims list.

Status key: SUPPORTED (a source says it), FLAG (conflicts with a source or overstates), UNVERIFIED (no source found).

## High priority

1. FLAG. "Nothing sends until you approve" (Nexus chat mockup) and "A person reviews and decides every next step."
   The product has direct email and messaging tools. Approval is a habit of how the agent prompts the AI, not a
   product-enforced gate that I can find in the spec. This is a behavioral guarantee. Confirm with Christian, or reword
   to "You review drafts before anything is sent."
2. FLAG. Workflow strip "Lead Captured, AI Engages, CRM Updated, Next Step Set" and the mockup items "Automations",
   "Lead response". These read as an automatic pipeline that starts when a lead arrives.
   Nexus is prompt driven (you ask your AI, it works in your CRM). V1 Launch Plan lists "persistent automations or
   background workflow engine" as NOT V1, and SMS/voice as Coming Soon. Suggest framing as "an example workflow you can
   run" and removing or relabeling "Automations".
3. FLAG. "Available now" tag on Real Estate Teams and Agents. Product Spec status is "Pre-launch beta"; the page's own
   FAQ says Nexus is in beta. Suggest "Now in beta" or "Real estate first".
4. FLAG. CRM list "Follow Up Boss, BoldTrail, Lofty, and GoHighLevel" (Industries bullet, Technology chips, disclaimer).
   Roadmap v3 item 1.2: market FUB as the V1 CRM; GHL and Lofty stay Beta/internal until certified.
   V1 Launch Plan: BoldTrail clients not ready (isolation not fixed). The marketing brief PDF lists FUB, BoldTrail, GHL
   (no Lofty). Sources disagree with each other and with the page. Decision needed: which CRMs are named as supported.
5. FLAG. CTA mismatch. "Book a Demo" (4 places) scrolls to #consult. "Book a Business Systems Assessment" opens the
   Calendly event "elevate-ai-onboarding", which the roadmap describes as the client onboarding flow. Visitors are told
   demo or assessment but land in an onboarding event. Also "no obligation" and the three assessment bullets have no source.
   Needs Sherri to confirm the right Calendly event and the offer wording (already tracked as pending).
6. UNVERIFIED. Marblism: "Elevate Ops 360 provides training and implementation support for teams that use it",
   "Tools our team trains and implements", "We train teams on it and help implement it", button "See our Marblism training".
   Roadmap says the Marblism partnership is deliberately parked until 5 to 10 paying clients. The only approved wording in
   the hub is "We work with a range of AI and automation tools, including Marblism...". Training/implementation claim
   is sourced only from the existing Train Your Brain page, which I could not tie to an approved doc.

## Medium priority

7. FLAG. Hero chips "Capture More Leads", "Convert More Clients". Sonny guardrails: do not promise leads will convert.
   Also "Faster, more consistent lead follow-up" and footer "Real Results". Suggest verbs about the work
   ("Respond faster", "Follow up consistently") rather than outcomes.
8. FLAG. "Perplexity" listed as an AI that works with Nexus (Nexus section, How It Works, chips). Roadmap says ChatGPT and
   Perplexity are connected via OAuth 2.1. Product Spec says ChatGPT OAuth was still being built. Sources conflict.
   Claude is the only AI both sources agree is working.
9. FLAG. "Secure, permissioned access" (How It Works). Per-tenant credential isolation is a stated design goal, but the spec
   and roadmap list open isolation and security blockers (Twilio, ElevenLabs, sector routing). Confirm before using "secure".
10. FLAG. Database revival bullet and mockup line "Checking ownership and equity data". Equity lookups come from the
    property data tier (Pro, via a data provider), not the V1 scope (FUB plus RentCast lookups). The brief says not to name infrastructure providers (page
    complies). Confirm equity is available to the audience the page targets.
11. UNVERIFIED. "Diagnose, Design, Implement, Support" service process and its four descriptions. No project doc describes
    this engagement model. Sherri to confirm it is how services actually run.
12. UNVERIFIED. Elevate Legal "In development" and its description ("Workflow automation and case tracking for legal
    practices"). Development status tracked as unresolved. Notion "Chris Technical Brief | Nexus Six Solutions + Elevate Legal"
    exists but was not read in this pass.
13. UNVERIFIED. Elevate Business and Elevate Academy one-line descriptions, and "Practical training for you and your team".
    Generic and low risk, but not tied to a source.

## Supported

- "Nexus connects the AI you already use to your CRM" and "so you stop copying and pasting between tools": matches the
  approved one-sentence message and Product Spec section 1.1.
- "Nexus is in beta": matches Product Spec status.
- Speed to lead and database revival as use cases: both are signature workflows in the spec (workflows 1 and 3).
- "Built from the day-to-day work of a working real estate team": matches the marketing brief (the team is the proof of concept).
- "Features vary by CRM and account permissions", "Illustrative mockup, sample data": accurate and consistent with the guardrail to
  separate demonstrations from guaranteed results.
- Marblism disclaimer "third-party product, not owned by Elevate Ops 360, no formal partnership": matches the hub decision.
- No pricing, trial terms, tool counts, statistics or testimonials appear on the page. The 26-year, 19-agent, 62,000-contact figures
  are not used (they remain unverified in the Notion hub).

## Needs a decision from Sherri
Items 1 to 6 before any copy goes to Lexi for the final visual pass. Items 7 to 13 can follow.
