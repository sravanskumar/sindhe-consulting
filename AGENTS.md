# Agent context — Sindhe Consulting website

**Project:** Personal / consulting marketing site for **Sindhe | Digital & Brand Consulting** (Sravan Kumar Sindhe, Munich).  
**Live URL:** https://sravanskumar.github.io/sindhe-consulting/  
**Repository:** https://github.com/sravanskumar/sindhe-consulting  
**Default branch:** `main` · **Hosting:** GitHub Pages (publish from repository root)

This is **not** the Royyal Exports client repo (`royyal-exports`). Royyal appears only as a **portfolio case study** linking to https://royyalexports.in/.

---

## Architecture (keep it simple)

| Item | Detail |
|------|--------|
| **Stack** | Single static file — `index.html` (HTML + embedded `<style>` + inline styles on some blocks) |
| **Build** | None — no npm, no bundler, no framework |
| **JS** | Minimal — contact form posts to Formspree and shows success or error on the page |
| **Assets** | `assets/` — profile photos (JPEG/PNG), referenced from About section |
| **Fonts** | Google Fonts: **DM Serif Display** (headings), **Inter** (body) |

**Do not** introduce React, Vite, or a build step unless the owner explicitly requests a migration.

---

## Design system

CSS variables in `:root` (edit consistently):

| Token | Value | Use |
|-------|-------|-----|
| `--teal` | `#0F6E56` | Primary brand, Sravan accent, CTAs |
| `--gold` | `#B8860B` | Secondary accent, Markus accent |
| `--dark` | `#1A1A1A` | Body text |
| `--stone` | `#5F5E5A` | Muted text |
| `--bg` | `#F7F5F0` | Page background |
| `--white` | `#FFFFFF` | Cards / contact panel text |
| `--border` | `#E2DDD6` | Dividers |
| `--teal-bg` | `#E4F0EE` | Light teal fills |

**Layout:** `.section-inner` max-width ~1100px; section padding ~80px desktop, reduced in `@media (max-width: 768px)`.

---

## Page map (`index.html`)

| Anchor | Section | Notes |
|--------|---------|--------|
| `#about` | About | Bio, TOGAF-scaled SME messaging, **Sravan + Prof. Dr. Markus Degen** photos (`assets/sravan-sindhe.jpg`, `assets/markus-degen.png`) |
| `#services` | Services | Capability pillars |
| `#approach` | Approach + “How I work” (nav duplicates two labels to same anchor) | TOGAF-informed delivery; red lines on product/legal claims |
| `#foundations` | Delivery model | T1 Core / T2 Growth / T3 Scale ladder |
| `#portfolio` | Portfolio | Maanvik, **Royvera/Royyal**, Jiya Handmade — external links |
| `#testimonials` | Clients | |
| `#thought` | Thinking | MACE, PACE, white paper teasers |
| `#contact` | Contact | Dark panel; form posts to Formspree (`https://formspree.io/f/mpppdkvp`) and emails the published Gmail address |

**Footer:** German Kleinunternehmer § 19 UStG, Munich address, Steuernummer (legal — do not remove without owner approval).

---

## Content voice

- **Positioning:** Delivery owner for businesses from first digital foundation through full MarTech — enterprise-grade architecture discipline, SME-scale delivery.
- **Method:** TOGAF ADM **scaled down** — baseline vs target, change records, BDAT thinking; not enterprise binder theatre.
- **Partners:** EMEA senior engagements with **Prof. Dr. Markus Degen** (LinkedIn linked from About).
- **Open source:** **MACE** (AEM governance MCP), **PACE** (staging architecture) — GitHub / LinkedIn links in Thought section.

When editing copy, preserve factual claims (Capgemini, AJO first in Europe, licence savings) unless owner supplies corrections.

---

## Contact form (current behaviour)

- `#contact-form` posts to Formspree with `fetch`, then shows `#form-success` or `#form-error`. The visitor stays on the page.
- Required fields: name, email, company. Industry and any intent outside the checkboxes are free text (`industry`, `intent_other`).
- A hidden `_gotcha` field is the spam honeypot. Do not remove it.
- Do not replace this endpoint without owner approval.

---

## Making changes

1. Edit `index.html` and/or replace files under `assets/`.
2. Test locally: open `index.html` in browser or `python3 -m http.server`.
3. Commit to `main`; GitHub Pages updates within a few minutes.
4. Prefer **small diffs** — match existing inline-style patterns when touching contact or About cards.
5. Profile images: 80×80 circular in About (`border-radius:50%`, `object-fit:cover`); Sravan **teal** border, Markus **gold** border.

---

## Related repositories (out of scope here)

| Repo | Relationship |
|------|----------------|
| `sravanskumar/royyal-exports` | Client delivery — Horizons SPA, deliverables/, not this site |
| Portfolio previews (e.g. Maanvik) | Separate GitHub Pages repos linked from Portfolio |

Agents working **only** on this site should not modify Royyal production unless the user opens that workspace.

---

## Quick links for humans

- Sravan LinkedIn: https://www.linkedin.com/in/sindhe-sravan-kumar-63b16766/
- Markus LinkedIn: https://www.linkedin.com/in/markus-degen-0228737b/
- GitHub: https://github.com/sravanskumar
