# Jacky's Service Portal

This repository is the public GitHub Pages entry point for Jacky's Distribution customer care and after-sales service workflow.

The root page is the professional landing page for customers, sales channels, and authorized internal users. It explains the service journey, shows the supported service brands, and directs each visitor to the correct portal.

## Live links

| Link | Purpose | Intended users |
| --- | --- | --- |
| [Jacky's Service Portal](https://service-jackys.github.io/) | Professional landing page with service overview, workflow, brands, and access options | Customers, sales team, and service team |
| [Customer Complaint Registration](https://service-jackys.github.io/complaints/) | Submit a new customer or sales-channel service complaint | Customers, sales team, and B2B clients |
| [Internal Service Portal](https://service-jackys.github.io/portal/) | Review complaints, complete internal details, and create appointments | Authorized Customer Care and service users |
| [Customer Portal Guide](https://github.com/service-jackys/service-jackys.github.io/blob/main/Customer-Complaint-Portal-Guide.md) | Instructions for customers and sales channels | Customers and sales team |
| [Internal Service Team Guide](https://github.com/service-jackys/service-jackys.github.io/blob/main/Internal-Service-Team-Complaint-Workflow.md) | Complaint review and appointment workflow | Customer Care and service team |

## Landing page

The landing page at [https://service-jackys.github.io/](https://service-jackys.github.io/) includes:

- Service-support hero section.
- Customer complaint and internal portal actions.
- Three-step service journey:
  1. Submit a complaint.
  2. Customer Care reviews the request.
  3. The service team arranges the appointment.
- Supported brand presentation for Thomson, Venus, and Philips AC.
- Separate access panels for customers/sales channels and internal service users.
- Responsive mobile navigation and reduced-motion accessibility support.

## What this repository does

The actual service applications are hosted in Google Apps Script. GitHub Pages provides the branded landing page and clean links that are easier to share with customers and the service team.

The landing page does not access Google Sheets or call Apps Script functions directly. It links to the two redirect pages below:

- `complaints/index.html` redirects to the Apps Script complaint route using `?page=complaints`.
- `portal/index.html` redirects to the normal Apps Script internal portal route.

After redirection, the browser may display the Google Apps Script URL because the applications remain hosted by Google Apps Script.

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
README.md                  Repository overview and maintenance guide
Customer-Complaint-Portal-Guide.md
                           Guide for customers and sales channels
Internal-Service-Team-Complaint-Workflow.md
                           Guide for Customer Care and service team
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