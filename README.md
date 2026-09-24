# Jacky's Service Portal

This repository provides the GitHub Pages entry point for Jacky's Service Portal.

## Public links

- **Portal home:** https://service-jackys.github.io/
- **Customer Complaint Registration:** https://service-jackys.github.io/complaints/
- **Internal Service Portal:** https://service-jackys.github.io/portal/

## What this repository does

The actual service applications are hosted in Google Apps Script. GitHub Pages provides clean, professional links that are easier to share with customers and the service team.

| GitHub Pages link | Destination | Intended users |
| --- | --- | --- |
| `/` | Branded service selection page | Customers and team members |
| `/complaints/` | Customer Complaint Registration Portal | Customers, sales team, and business clients |
| `/portal/` | Main Jacky's Service Portal | Authorized internal users |

The `complaints/index.html` and `portal/index.html` files redirect visitors to the corresponding Google Apps Script Web App routes. The GitHub Pages URL is the clean entry link; after redirection, the browser may display the Google Apps Script URL because the applications remain hosted there.

## Customer Complaint Registration Portal

The complaint portal allows customers or sales channels to submit service requests directly. It collects customer, contact, location, product, and complaint details and generates a complaint reference number.

Customer Care Executives review submitted complaints inside the authenticated Service Portal. They can complete internal information, assign appointment details, and link the complaint to a scheduled service appointment.

Customers do not receive access to the internal scheduler, technician records, appointment data, or CCE-only fields through the complaint link.

## Main Service Portal

The main portal is the authenticated internal application used by the service team for scheduling, complaint review, technician assignment, dashboards, service job cards, reports, and related service operations.

Team members should use the `/portal/` link rather than sharing the long Google Apps Script URL directly.

## Repository structure

```text
index.html                 Branded service selection page
complaints/index.html      Customer complaint redirect
portal/index.html          Internal service portal redirect
README.md                  This guide
```

## Updating the destination URLs

If the Google Apps Script deployment URL changes, update the destination URL in both redirect files:

- `complaints/index.html`
- `portal/index.html`

Update both the `meta` refresh URL and the `window.location.replace(...)` URL in the relevant file. Then commit and push the changes to the `main` branch.

```bash
git add index.html complaints/index.html portal/index.html README.md
git commit -m "Update service portal links"
git push origin main
```

## GitHub Pages configuration

GitHub Pages should be configured as follows:

- **Source:** Deploy from a branch
- **Branch:** `main`
- **Folder:** `/(root)`

After pushing changes, GitHub Pages may take a few minutes to publish the updated site.

## Important security note

Do not place passwords, API keys, GitHub tokens, or private credentials in this repository. The complaint page is intentionally public, while the internal Service Portal remains protected by its own login and session controls.