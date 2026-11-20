# Launch candidate and release plan (new homepage)

Date: 2026-11-20 (evening run). Author: Claude. Branch: feature/qa-a11y-responsive. DEV BRANCH ONLY. Nothing merged, deployed, or changed on production, DNS, or credentials.

## 1. Launch candidate
Candidate = the commit that contains this file (see Notion handoff for the SHA). Files changed this run:
- redesign/index.html: added a verified email fallback (hello@elevateops360.com, the same address already on production index.html) in the Consultation section and footer.
- redesign/qa-fixes.css: 5 lines styling that link (white underlined, visible focus ring).
- redesign/docs/launch-readiness-2026-11-20.md, redesign/docs/screenshots/release-candidate-1440.png and -390.png (real Playwright renders).

## 2. Every public link and CTA
| Link | Destination | Verified |
|---|---|---|
| Book a Demo (nav, hero, Nexus, footer) | #consult on same page | works |
| Book a Business Systems Assessment | calendly.com/sherriparsonsrealestate/elevate-ai-onboarding | HTTP 200. Event is the onboarding event, wording mismatch, needs Sherri |
| Email | mailto:hello@elevateops360.com | address already live on production |
| Marblism | www.marblism.com/agencies?type=agency | HTTP 200 |
| Nexus | ../nexus/ | 200 locally; existing page unchanged |
| Training | ../trainyourbrain/ | 200 locally |
| Live events | ../live/ | 200 locally |
No forms, no credential fields, no scripts loading third-party hosts on the redesign page.

## 3. Smoke test (served with python http.server, Chromium)
1440 and 390: 0 console errors, 0 failed or 4xx requests, 0 px horizontal overflow, 0 broken images (lazy Marblism wordmark checked after scroll). Earlier today: axe 0 violations at 390/768/1024/1440, Lighthouse a11y/best-practices/perf 100 (SEO 63 only because of intentional noindex).

## 4. What still blocks calling it publishable (not done by me, needs Sherri)
1. Footer literally says "Prototype for review. Not for publication." and "Privacy and accessibility pages to be added before launch." Both must change, and a privacy page needs to exist or the line be removed. I did not edit these because they are release-wording decisions.
2. `<meta name="robots" content="noindex, nofollow">` must be removed at release (Sherri's explicit call).
3. Six copy-audit flags (copy-audit-2026-11-20.md) are still unresolved. Proposed conservative wording:
   - "Nothing sends until you approve" -> "You review drafts before anything is sent."
   - Workflow strip / "Automations" -> label "Example workflow" and drop "Automations".
   - "Available now" on Real Estate -> "Now in beta".
   - CRM list -> name Follow Up Boss only as supported; others "more CRMs planned".
   - Marblism "training and implementation" claim -> "We work with a range of AI and automation tools, including Marblism. Approved Marblism agency and strategic partner." (Sherri's approved wording).
   - Assessment CTA -> confirm the right Calendly event; "no obligation" wording needs Sherri.
4. Production security (Christian): onboard.html password form and token rotation. Unresolved risk; the redesign does not touch it, but the site as a whole stays exposed until fixed.

## 5. Release plan (proposed, not executed)
1. Branch release/new-homepage off main (not main itself). Copy redesign/ assets, fonts, css to repo root paths; move current index.html to index-legacy.html; change relative `../nexus/`, `../live/`, `../trainyourbrain/` links to `/nexus/` etc.; apply the Section 4 copy and footer decisions.
2. Open PR titled DO NOT MERGE until Sherri approves. Check the GitHub Pages preview or local serve for /, /nexus/, /live/, /trainyourbrain/, /Updates.html, /onboard.html still returning 200.
3. After explicit approval: merge, wait for Pages build, smoke test www.elevateops360.com.
4. Rollback: revert the merge commit (single commit revert restores the old index.html; index-legacy.html stays as a fallback). No DNS change involved, so rollback is minutes.

## 6. Approval questions for Sherri
1. Authorize me, through this scheduled task or by telling me directly, to create the release branch and PR? (I will still not merge without a separate explicit yes.)
2. Approve the conservative wording in Section 4 item 3 or give your own.
3. Which Calendly event should the assessment button use?
4. Remove noindex at launch?
5. Privacy page: publish a simple one, or remove the footer line?
