# Iron Gate M&A (Marketing Site)

Marketing site for a boutique M&A advisory firm. Built as a static HTML + Tailwind CSS project to practice layout, typography, simple lead-capture flow, and connecting GTM/GA4 for marketing analytics.

Built with **HTML**, **Tailwind CSS**, and **vanilla JavaScript**, featuring a contact form designed to integrate with Google Apps Script + Google Sheets.

---

## Tech Stack

- HTML5 (semantic structure)
- Tailwind CSS (utility-first styling)
- Vanilla JavaScript (navigation + form handling)
- Contact form wired to Google Apps Script endpoint that writes leads into Google Sheets
- GA4 + Google Tag Manager (planned: conversion + attribution tracking)

---

## Features

**Implemented (Phase 1)**

- Responsive layout with sticky header and mobile nav
- Smooth scrolling navigation
- Services and “How We Work” sections to support a high-trust, advisory feel
- Contact form with basic client-side validation (HTML5 attributes)
- Accessible color contrast and typography (MVP level)

**Planned (Phase 2+)**

- Form success/error states and inline validation messaging
- More detailed deal-flow content (process steps, FAQs, team)
- Additional trust elements (case-study stubs, testimonials, logos)

---

## Marketing Analytics & Attribution Plan

These are not all live yet; tracked as Issues in this repo and will be implemented when the site goes into active use.

**Planned tracking stack**

- `sitemap.xml` and `robots.txt` for SEO crawl control
- Google Tag Manager (GTM) container on all production pages
- GA4 connected via GTM with:
  - Pageview and scroll-depth tracking
  - Two core conversions:
    - `lead_form_submit` (contact form)
    - `cta_click` with `cta_location` parameter (hero, footer, etc.)

**Planned form attribution fields**

Hidden fields on the contact form (populated by JS / GTM) for:

- `utm_source`, `utm_medium`, `utm_campaign`, `utm_content`, `utm_term`
- `landing_page` (request URI)
- `referrer_url`
- Optional `gclid` for Google Ads, if/when paid campaigns are running
- Honeypot field (ignored by backend if filled) to reduce bot spam

Detailed acceptance criteria for this work are documented in the
“Marketing analytics + Sitemaps + robots” issue.

---

## Project Structure

```text
assets/        # Images, logo, static assets
src/           # Tailwind input CSS (and any JS modules if added later)
index.html     # Main entry page (compiled HTML + Tailwind output)
package.json   # Tailwind/dev dependencies
README.md      # Project overview (this file)
```

## Roadmap (High-Level)

- Finalize branding & design polish (spacing, typography, minor layout tweaks)
- Add richer form validation + success/error states
- Implement SEO basics (title/meta review, sitemap, robots)
- Migrate Apps Script + Sheets + future GA4/GTM containers into a dedicated Iron Gate Google account
- Wire GA4 + GTM + form attribution fields (see analytics issue)
- Deploy to production hosting (Netlify / Vercel / Cloudflare Pages)

For detailed tasks, see [GitHub Issues](../../issues)_

## Status

🚧 Work in progress. Phase 1 complete: static marketing site with hero, services, process, and contact form sections.
Next steps (tracked in issues): refine layout, add more deal-flow content, and wire analytics + attribution.
