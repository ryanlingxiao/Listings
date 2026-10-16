# Listings — Ryan Xu / Xceed Realty

Standalone listing pages for Ryan's listings. Each home gets its own folder (`/24528/`, `/12345/` …) in this one repo. Published with GitHub Pages from `main` / root:
`https://ryanlingxiao.github.io/Listings/<folder>/`

## What Ryan wants (non-negotiable)

- **Door/sign QR → this page, not xceedwa.com.** The xceedwa.com (Luxury Presence) listing page forces account registration; nobody signs up. Never point a QR there.
- **Flow on the page:** short contact form first (name, mobile, email; name + phone-or-email required) → on submit, the full listing shows immediately. Same phone doesn't have to fill it again (localStorage).
- **Leads go to email only**: `ryan@xceedwa.com` via FormSubmit AJAX (`https://formsubmit.co/ajax/ryan@xceedwa.com`). First-ever submission triggers a one-time activation email Ryan must click. No FUB API, no backend.
- **Never use Zapier** for anything (Ryan banned it and is cancelling the subscription).
- **Keep it simple.** Don't propose multi-service setups when a static page works.
- **Don't deliver until it's done and tested.** Test the form gate in a mobile-size browser (Playwright, 390×844) with the FormSubmit request intercepted, decode every QR code, then hand over. Say plainly what could not be tested from the sandbox (github.io and formsubmit.co are not reachable from the cloud container) and ask Ryan to do one live scan.
- **Use published facts only**: price, open house dates/times and MLS# come from what's live (NWMLS / syndication sites / Ryan's emails), never guessed. Leave nothing as a placeholder on anything printed.
- Ryan writes in Chinese; reply in Chinese, short.

## Adding a new listing

1. Copy `24528/` to `<new>/`, replace `p/` photos (resize to ≤1600px JPG q80) and all copy/facts.
2. Commit as `Claude <noreply@anthropic.com>` and push to `main`; Pages rebuilds in ~1 min (check `gh api repos/ryanlingxiao/listings/actions/runs`).
3. Add the home to the root `index.html` list.
4. QR: `qrcode` (ECC M) → the folder URL with trailing slash; decode it with OpenCV to verify; print cards at 300 DPI (6×6 in + 1/8 in bleed for the door card).

## Brand

Cream `#FBF8F2`, ink `#141414`, gold `#A9874F` / dark gold `#8A6A32`; Barlow Condensed (display) + Libre Franklin (body). Contact: Ryan Xu · 425-448-4960 · ryan@xceedwa.com · WA Real Estate Broker License #20108301. Mark AI-enhanced photos as such. Include Equal Housing Opportunity.
