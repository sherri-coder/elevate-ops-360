# Elevate Ops 360: Hybrid Design System (Option C), Draft v0.1

Status: DRAFT for Sherri and Lexi review. Documentation only; no visual code changed.
Date: 2026-11-20. Basis: Notion hub "Approved brand decision, Option C" and the tokens currently in `redesign/styles.css`.

Items marked **(proposed)** are not in the current CSS and are not approved. Fonts, logo files and final asset usage still need verification per the hub.

## 1. Two modes, one identity

| | Corporate mode | Technology mode |
|---|---|---|
| Where | Solutions, How It Works, Industries, About/FAQ, footer-adjacent content | Hero product visual, Nexus, Technology We Work With, consult CTA |
| Background | Ivory / warm neutral **(proposed)** | Deep navy |
| Accent | Restrained gold (thin accents only) | Teal, plus gold as the shared accent |
| Headings | Serif **(proposed, font not chosen or verified)** | Manrope (current) |
| Body | Inter (current) | Inter (current) |
| Effects | Soft shadow only | Controlled teal glow, dimensional dashboard |
| Imagery | Professional photography (none exists yet) | Real product screenshots or labelled illustrative mockups |

Shared across both: gold as the common accent, the logo, spacing scale, radius, button shapes, focus ring, and the rule that every mockup is labelled illustrative with sample data.

## 2. Tokens

### Existing in `redesign/styles.css`
- Navy: 950 `#04111f`, 900 `#071c32`, 800 `#0a2745`, 700 `#0f3a5f`, 600 `#17517a`
- Neutrals: charcoal `#1c242c`, ink `#0c1a29`, slate `#4a5b6c`, mist `#eef3f6`, line `#d8e2e9`, white
- Teal: `#25d0c0` (on dark only), 500 `#14b3a4`, 700 `#0b7d74` (text on light), glow `rgba(37,208,192,.45)`
- Gold: `#c8a96b`, light `#e6cf9f`, deep `#a98654`
- Radius 18px; shadow `0 18px 50px rgba(5,20,38,.14)`
- Fonts: Manrope (headings), Inter (body), both self-hosted

### Proposed additions (corporate mode)
- Ivory background `#faf6ee` **(proposed)**, warm neutral line and text-muted values to be chosen with Lexi.
- Serif heading family: not selected. The Brand Kit lists DM Serif Display, Cormorant Garamond and Playfair Display as candidates. Self-hosting and licence check required before use.

## 3. Contrast reference (computed from the token hex values, WCAG 2.x)

| Foreground on background | Ratio | Use |
|---|---|---|
| ink on white | 17.57 | Body text, light sections |
| slate on white | 6.99 | Secondary text |
| slate on mist | 6.25 | Secondary text on tinted panels |
| teal-700 on white | 5.00 | Teal text or links on light |
| teal on navy-900 | 8.89 | Teal on dark |
| gold on navy-900 | 7.65 | Gold text on dark |
| white on navy-900 | 17.20 | Body on dark |
| navy-900 on gold | 7.65 | Gold buttons |
| ink on ivory (proposed) | 16.30 | Body on ivory |
| slate on ivory (proposed) | 6.48 | Secondary on ivory |
| teal-700 on ivory (proposed) | 4.64 | Passes for text, thin margin |
| gold-deep on white | **3.37** | Fails 4.5 for text; large text or decoration only |
| gold-deep on ivory (proposed) | **3.13** | Fails 4.5 for text; large text or decoration only |

Rules that follow: use gold as an accent line, rule, icon or button fill, not as small body text on light backgrounds. Use `gold-deep` only for text of 24px or larger, or 18.66px bold, which has a 3:1 requirement. Use teal-700, not the bright teal, for text on light backgrounds.

## 4. Mode boundaries
- Sections switch mode at full-width section edges only. No mixed backgrounds inside one section.
- The hero is the one deliberate blend: ivory or white copy side with a navy product panel is an option for Lexi to evaluate; today the hero is fully technology mode.
- Dark-mode sections carry the `on-dark` class in the current markup; a matching `on-ivory` class **(proposed)** would scope the corporate overrides.

## 5. Open questions for Sherri / Lexi
1. Approve ivory `#faf6ee` as the corporate background, or supply the Brand Kit's warm neutral values.
2. Choose the corporate serif from the Brand Kit list.
3. Photography source (client-owned, licensed stock or none at launch).
4. Official transparent logo file (still blocked).
5. Whether gold-deep text on light is acceptable at large sizes only, per section 3.

## 6. Suggested next step
Lexi builds one corporate section (Solutions) in ivory and serif as a sample for review before any site-wide change. No such change has been made.
