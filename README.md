# Merchant Command Center (Zoho CRM widget)

A single-page, filterable dashboard for Zoho CRM. Reads live data from your CRM when opened inside it,
and shows demo data when opened on its own (add `?demo=1` to force demo mode, `?lang=ar` for Arabic).

## Files
- `index.html`  the whole dashboard (no build step)
- `logos/`      optional merchant logos, named after the account (lowercase, spaces to underscores,
                "(Demo)" removed), e.g. `najd_dates_sweets.png`. Missing logos fall back to initials.

## CRM modules it reads (API names)
Accounts, Deals, Cases, Finance_Tickets, KYC_Documents, POS_Terminals, Field_Activities
The user's profile needs read access to all of them.

## Host on GitHub Pages
1. Create a GitHub repository (public, e.g. `geidea-dashboard`).
2. Upload `index.html` and the `logos` folder to the repository root.
3. Settings > Pages > Source: "Deploy from a branch", Branch: `main`, folder: `/ (root)`. Save.
4. After a minute your page is live at `https://<your-username>.github.io/geidea-dashboard/`.
5. Open the link with `?demo=1` in a normal browser tab to confirm it renders.

## Register in Zoho CRM
1. Setup > Developer Space (Developer Hub) > Widgets > Create New Widget.
2. Name: Merchant Command Center. Type / placement: Web Tab. Hosting: External.
3. Base URL: your GitHub Pages URL. Index page: `/index.html`. Save.
4. Setup > Customization > Web Tab (or the Tabs setting): create a tab that uses this widget,
   then enable it for the profiles that should see it.
5. Open the new tab from the CRM navigation menu.
