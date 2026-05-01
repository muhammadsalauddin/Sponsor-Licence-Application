# Sponsor-Licence-Application

Static multi-page Sponsor Licence website built for a UK employer-focused consultancy brand.

Live site: https://spluk.netlify.app/

## Overview

This project is a static website for businesses that need help preparing for a UK Sponsor Licence application and ongoing sponsor compliance.

The site is written for employers rather than visa applicants and positions the service as:

- a compliance-led sponsor licence partner
- an application and audit-preparation specialist
- a practical adviser for overseas hiring readiness

The current implementation includes a main landing page plus four supporting pages for pricing, checklist, process, and compliance support.

## Pages

### Main page

- `sponsor-license.html`
	Main landing page for Sponsor Licence support, including hero, services, sectors, process, pricing, FAQ, and direct contact section.

### Supporting pages

- `sponsor-license-pricing.html`
	Package overview and pricing comparison page.
- `sponsor-license-checklist.html`
	Printable employer document and readiness checklist.
- `sponsor-license-process.html`
	Step-by-step Sponsor Licence roadmap from discovery to post-approval setup.
- `sponsor-license-compliance.html`
	Ongoing compliance support page focused on sponsor duties and audit readiness.

## Current contact setup

The site is configured for direct contact only.

- Email: `uddin@uplesk.com`
- WhatsApp: `+44 7481 866697`
- Telegram: `+44 7481 866697`

There is no form backend in this build.

## Design and UX features

- Static HTML site with Tailwind CSS loaded from CDN
- Shared custom styling in `styles.css`
- Shared JavaScript in `site.js`
- Mobile navigation toggle
- Scroll reveal animations via `IntersectionObserver`
- Sticky mobile CTA bar
- Print / Save PDF action available on all main pages
- Print-friendly layout for checklist, pricing, process, and other content sections

## Print / PDF system

Each real page includes a `Print / Save PDF` action. This calls `window.print()` from the shared script and uses dedicated print styles in `styles.css`.

Print behavior includes:

- A4 page sizing via `@page`
- removal of mobile CTA, background effects, and other screen-only UI
- simplified white backgrounds for printed output
- reduced section spacing for cleaner PDFs
- avoidance of card and timeline breaks where practical

## Tech stack

- HTML5
- Tailwind CSS via CDN
- Custom CSS
- Minimal vanilla JavaScript
- Netlify redirects for root routing

There is no build step, package manager, or framework dependency in this project.

## File structure

```text
README.md
_redirects
plan.md
site.js
styles.css
sponsor-license.html
sponsor-license-pricing.html
sponsor-license-checklist.html
sponsor-license-process.html
sponsor-license-compliance.html
```

## Local preview

Because there is no build process, you can preview the site in either of these ways:

### Option 1: open the main file directly

Open `sponsor-license.html` in a browser.

### Option 2: serve locally

If you want cleaner local navigation, run a simple local server from the project folder. Example:

```bash
python3 -m http.server 5500
```

Then open:

```text
http://127.0.0.1:5500/sponsor-license.html
```

## Deployment

The project is suitable for static hosting.

### Netlify

Netlify uses the `_redirects` file so the site root `/` serves:

- `sponsor-license.html`

Redirect rule:

```text
/ /sponsor-license.html 200
```

This allows the deployed root URL to work without an `index.html` file.

## Content and branding notes

The current build uses the following brand label throughout the UI:

- Northgate Sponsor Advisory

The site content is currently tuned around:

- UK Sponsor Licence preparation
- employer document readiness
- role and vacancy planning
- key personnel guidance
- post-licence compliance support

If branding, pricing, or contact details change, the main places to update are the individual page HTML files.

## Updating the site

Typical content updates can be made directly in the page files:

- update hero and service copy in `sponsor-license.html`
- update package details in `sponsor-license-pricing.html`
- update checklist items in `sponsor-license-checklist.html`
- update roadmap stages in `sponsor-license-process.html`
- update sponsor duty messaging in `sponsor-license-compliance.html`

Shared behavior and styling live here:

- `styles.css` for global layout, cards, buttons, hero panels, and print rules
- `site.js` for mobile menu behavior, reveal animations, footer year, and print button handling

## Repository purpose

This repository is intended to hold the static website source for the Sponsor Licence consultancy landing pages and supporting printable resources.