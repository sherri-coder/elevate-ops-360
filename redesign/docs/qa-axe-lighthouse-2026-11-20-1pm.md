# QA run: axe + Lighthouse (2026-11-20, ~1 pm ET), commit a0cad0f
Local only (python http.server, Playwright Chromium, axe-core 4.10.2, Lighthouse).
- axe violations at 390 / 768 / 1024 / 1440: 0 at every width.
- Horizontal overflow (scrollWidth vs clientWidth): none at any width.
- Failed requests / console page errors: none.
- Lighthouse mobile: Performance 100, Accessibility 100, Best Practices 100, SEO 63. LCP 1.2 s, CLS 0, TBT 0 ms.
- Lighthouse desktop: 100 / 100 / 100 / 63. LCP 0.3 s, CLS 0, TBT 0 ms.
- SEO 63 is only "is-crawlable": the prototype intentionally carries `noindex, nofollow`. Remove only at launch (Sherri's gate).
- Contact sheet of the five review screenshots: screenshots/contact-sheet-2026-11-20-1pm.png
