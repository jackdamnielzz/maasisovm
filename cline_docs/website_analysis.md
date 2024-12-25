# Website Analysis

This document summarizes the analysis of the Maasiso website, which was used to create the new sitemap.xml and robots.txt files.

## Website Structure

The website appears to be a business website for "Maasiso" offering services related to ISO certifications. The main pages are:

- **Homepage (`index.html`):** The main landing page of the website.
- **Terms and Conditions (`algemene-voorwaarden.html`):** Legal page outlining the terms of use.
- **Cookie Policy (`cookiebeleid.html`):** Legal page explaining the use of cookies.
- **Privacy Policy (`privacyverklaring.html`):** Legal page outlining the privacy practices.
- **Contact (`contact.html`):** Page with a contact form.
- **Contact Success (`contact-success.html`):** Confirmation page after submitting the contact form.
- **Services (`diensten.html`):** Page detailing the services offered.
- **ISO 9001 (`iso-9001.html`):** Page about ISO 9001 certification.
- **ISO 27001 (`iso-27001.html`):** Page about ISO 27001 certification.
- **About Us (`over-ons.html`):** Page about the company.
- **Why Maasiso (`waarom-maasiso.html`):** Page explaining why to choose Maasiso.
- **AVG Compliance (`avg-compliance.html`):** Page about AVG compliance.

## Sitemap and Robots.txt

Based on this analysis, a new `sitemap.xml` file was created, listing all the main pages of the website. A new `robots.txt` file was also created, disallowing access to the `error_docs` and `cline_docs` directories, and including the sitemap location.

## HTML Structure and Schema

The `index.html` file was updated to include the following:

-   Added more specific schema.org properties to the existing `Organization` schema, such as `logo`, `address`, and `telephone`.
-   Improved semantic HTML structure by wrapping the main content in a `<main>` element and using `<article>` elements for the sections.
-   Added ARIA attributes to improve accessibility.
