# Mezbaur Are Rafi

**Software Engineer** · Dhaka, Bangladesh · [mezbaur.vercel.app](https://mezbaur.vercel.app) · [LinkedIn](https://www.linkedin.com/in/mezbaur2004) · [mezbaur2004@gmail.com](mailto:mezbaur2004@gmail.com)

Linux servers, backend services and the integrations between them: I connect Shopify, Moodle, WordPress and payment gateways, and make sure the data moving through them stays correct in production. Mostly Node.js and TypeScript, plus whatever Moodle and WordPress require.

## Experience

**Assistant Programmer · Pedago Academy** · Jan 2026 – present

- Primary in-house software engineer: administer the production Moodle LMS and maintain the WordPress/WooCommerce platform, from plugin evaluation and feature work to production debugging through logs and SQL.
- Build Node.js integrations for payments, authentication, and automation.
- Run the Linux VPS infrastructure: deployments, Nginx, PHP-FPM, SSL/TLS, backups, and monitoring.
- Authored 20+ technical documents, including SOPs, server architecture, deployment guides, and disaster recovery plans.

**Intern Software Engineer · Solution Spin Ltd** · Aug 2025 – Jan 2026

- Worked with senior engineers on frontend and backend features for production MERN applications: React routing, Redux Toolkit, form validation, REST APIs, and code reviews.

## Selected work

### [Shopify ↔ SSLCommerz payment middleware](https://github.com/mezbaur2004/shopify-sslcommerz-middleware)

Node.js/TypeScript service that takes a Shopify order through SSLCommerz and back, verifying every payment with the gateway before the order is completed. Deployed with the live store and tested end to end against the SSLCommerz sandbox; the payment option stays hidden until the organization buys a live merchant account.

<sub>Node.js · TypeScript · Express · MongoDB · Shopify Admin API · SSLCommerz · Vitest · GitHub Actions</sub>

<details>
<summary>How it works</summary>

- Full payment lifecycle: custom checkout, payment initiation, IPN verification, conversion of Draft Orders to paid orders, and customer email notifications.
- Every payment is verified with the gateway before an order is completed: status, amount within ±0.01 BDT, and transaction ID. A repeated IPN for an already-paid session is acknowledged without being processed again.
- Verified payments are recorded as manual-payment orders, so they don't incur Shopify's third-party transaction fee.
- A wake-up request sent when the customer opens checkout hides free-tier cold starts, keeping hosting cost at $0.
- Payment verification is covered by unit tests that run in CI.

</details>

### [Zoom attendance for Moodle](https://github.com/mezbaur2004/moodle-local_zoomattendance)

Turns the session data the Zoom activity plugin already stores into per-class attendance for students and teachers, with a [dashboard block](https://github.com/mezbaur2004/moodle-block_zoomattendance). Adds no Zoom API calls of its own.

<sub>Moodle · PostgreSQL · MariaDB · PHPUnit · Behat · GitHub Actions</sub><br>
<sub>*Designed, reviewed and tested by me; implemented with AI assistance (Claude).*</sub>

<details>
<summary>How it works</summary>

- Attendance is an interval union of join/leave segments clipped to each class window, so reconnects are never double-counted.
- Class rosters are frozen when a class ends, so later enrolment, role or group changes can't rewrite past attendance.
- Manual corrections (linking unmatched Zoom identities, setting class windows, excluding classes) are permission-checked and logged; teachers can't exclude classes they missed.
- PHPUnit and Behat tests, CI on Moodle 4.1–5.0 with PostgreSQL and MariaDB.

</details>

### [Moodle Patch Manager](https://github.com/mezbaur2004/moodle-local-patchmanager)

Applies, verifies and rolls back source patches to third-party Moodle plugins on a production site, with a [dashboard block](https://github.com/mezbaur2004/moodle-block_patchmanager) and a first [patch pack](https://github.com/mezbaur2004/moodle-local-zoomcustom) that fixes mod_zoom's duration-based grading.

<sub>Moodle · Linux · PHPUnit</sub><br>
<sub>*Designed, reviewed and tested by me; implemented with AI assistance (Claude).*</sub>

<details>
<summary>How it works</summary>

- Patching with pristine backups, dry runs, restore and reapply, and an audit history.
- A CLI-first workflow, so the web server never needs write access to code.
- Scheduled patch-state checks, reported through Moodle's Check API and the dashboard block.
- The Zoom pack pauses Zoom's report task until the fix is verified.

</details>

### [Upstream contribution to mod_zoom](https://github.com/jrchamp/moodle-mod_zoom/pull/730)

Reported that the Zoom activity plugin records attendance for recurring meetings but never writes grades for it ([issue #728](https://github.com/jrchamp/moodle-mod_zoom/issues/728)), and argued for fixing it rather than removing the feature. The maintainer agreed to a focused PR: it grades each occurrence separately and sums them, covers both grading methods, leaves existing activities unchanged, and passes the plugin's CI. In review.

<sub>Moodle · PHPUnit · open source</sub>

### Jolly Learning Bangladesh: Shopify store

Independently developed and launched the organization's production store: store setup, Liquid theme customization, product configuration, and SEO. Orders come in by cash on delivery, with SSLCommerz checkout built through the middleware above and ready for a live merchant account. Workshop registrations take manual bKash/Nagad payments; the first paid registrations came through organic search, before any marketing campaign.

<sub>Shopify · Liquid · JavaScript</sub>

## Personal projects

- **[Fulkopi](https://github.com/mezbaur2004/fulkopiBackend)**: full-stack store with Google OAuth and JWT authentication, role-based access control, an admin dashboard, and SSLCommerz checkout. [Live](https://fulkopi-frontend.vercel.app/) · [frontend](https://github.com/mezbaur2004/fulkopiFrontend)
- **[Inventory Management System](https://github.com/mezbaur2004/inventoryBackend)**: REST API and React/Redux dashboard for products, purchases, sales, returns, and expenses. A purchase, sale or return and its line items are written and deleted in one MongoDB transaction. [Live](https://inventory-frontend-mezbaur.vercel.app/) · [frontend](https://github.com/mezbaur2004/inventoryFrontend)

## Stack

| Area | Technologies |
|---|---|
| Languages | JavaScript (ES6+), TypeScript, SQL, Python, C, C++ |
| Backend | Node.js, Express.js, REST APIs, JWT, OAuth |
| Integrations | Shopify Admin API, SSLCommerz, webhooks, third-party APIs |
| LMS & CMS | Moodle, WordPress, WooCommerce, Shopify (Liquid) |
| Databases | MongoDB (Mongoose), MariaDB/MySQL, PostgreSQL |
| Infrastructure | Linux VPS, Nginx, PHP-FPM, SSL/TLS, backup & disaster recovery |
| Tooling & deployment | Git, GitHub, GitHub Actions, Postman, Vercel, Render |
| Frontend | React.js, Next.js, Redux Toolkit, HTML5, CSS3, Tailwind CSS, Bootstrap |
