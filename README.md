# Mezbaur Are Rafi

**Software Engineer** · Dhaka, Bangladesh

I connect the systems an organization already runs (payment gateways, Shopify, Moodle, WordPress) and keep the data moving between them correct in production. Mostly Node.js and TypeScript; inside Moodle and WordPress, whatever the platform requires. I also run the Linux servers those systems live on.

## Experience

**Assistant Programmer · Pedago Academy** · Jan 2026 – present<br>
Primary in-house software engineer. Administer the production Moodle LMS, maintain the WordPress/WooCommerce platform, build Node.js integrations for payments, authentication, and automation, and run the Linux VPS infrastructure: deployments, Nginx, PHP-FPM, SSL/TLS, backups, and monitoring. Authored 20+ technical documents, including SOPs, server architecture, deployment guides, and disaster recovery plans.

**Intern Software Engineer · Solution Spin Ltd** · Aug 2025 – Jan 2026<br>
Worked with senior engineers on frontend and backend features for production MERN applications, including React routing, Redux Toolkit, form validation, REST APIs, and code reviews.

## Selected work

### Shopify SSLCommerz Payment Middleware · [repo](https://github.com/mezbaur2004/shopify-sslcommerz-middleware)
Node.js/TypeScript service connecting a Shopify store to SSLCommerz through the Shopify Admin API. Deployed alongside the live store and tested end to end against the SSLCommerz sandbox; the online-payment option stays hidden until the organization buys a live merchant account.
- Full payment lifecycle: custom checkout, payment initiation, IPN verification, conversion of Draft Orders to paid orders, and customer email notifications.
- Every payment is verified with the gateway before an order is completed: status, amount within ±0.01 BDT, and transaction ID. A repeated IPN for an already-paid session is acknowledged without being processed again.
- Verified payments are recorded as manual-payment orders, so they don't incur Shopify's third-party transaction fee.
- A wake-up request sent when the customer opens checkout hides free-tier cold starts, keeping hosting cost at $0.

`Node.js` `TypeScript` `Express.js` `MongoDB` `Shopify Admin API` `SSLCommerz`

### Zoom attendance for Moodle · [local_zoomattendance](https://github.com/mezbaur2004/moodle-local_zoomattendance) · [block_zoomattendance](https://github.com/mezbaur2004/moodle-block_zoomattendance)
Turns the session data the Zoom activity plugin already stores into per-class attendance for students and teachers, without adding any Zoom API calls of its own.
- Attendance is an interval union of join/leave segments clipped to each class window, so reconnects are never double-counted.
- Class rosters are frozen when a class ends, so later enrolment, role or group changes can't rewrite past attendance.
- Manual corrections (linking unmatched Zoom identities, setting class windows, excluding classes) are permission-checked and logged; teachers can't exclude classes they missed.
- PHPUnit and Behat tests, CI on Moodle 4.1–5.0 with PostgreSQL and MariaDB.

Designed, reviewed and tested by me; the implementation was written with AI assistance (Claude).

`Moodle` `PostgreSQL` `MariaDB` `GitHub Actions`

### Moodle Patch Manager · [local_patchmanager](https://github.com/mezbaur2004/moodle-local-patchmanager) · [block_patchmanager](https://github.com/mezbaur2004/moodle-block_patchmanager) · [local_zoomcustom](https://github.com/mezbaur2004/moodle-local-zoomcustom)
Moodle plugins that apply and track source patches to third-party plugins on a production site.
- Patching with pristine backups, dry runs, restore and reapply, and an audit history. A CLI-first workflow, so the web server never needs write access to code.
- Scheduled patch-state checks, reported through Moodle's Check API and a dashboard block.
- A first pack that fixes mod_zoom's duration-based grading and pauses Zoom's report task until the fix is verified.

Designed, reviewed and tested by me; the implementation was written with AI assistance (Claude).

`Moodle` `Linux`

### Upstream contribution: cumulative grading for recurring Zoom meetings · [PR #730](https://github.com/jrchamp/moodle-mod_zoom/pull/730) · [issue #728](https://github.com/jrchamp/moodle-mod_zoom/issues/728)
Reported that mod_zoom records attendance for recurring meetings but never writes grades for it, and argued for fixing it rather than removing grading for recurring meetings. The maintainer agreed to a focused PR. The PR grades each occurrence separately and sums them, covers both grading methods, leaves existing activities unchanged, and passes the plugin's CI; it is in review.

`Moodle` `PHPUnit` `open source`

### Jolly Learning Bangladesh: Shopify store
Independently developed and launched the organization's production store, covering store setup, Liquid theme customization, product configuration, and SEO. Orders come in by cash on delivery, with SSLCommerz checkout built through the middleware above and ready for a live merchant account. Workshop registrations take manual bKash/Nagad payments; the first paid registrations came through organic search, before any marketing campaign.

`Shopify` `Liquid` `JavaScript`

### Pedago Academy: Moodle LMS & WordPress/WooCommerce
Maintain the production Moodle LMS and WordPress/WooCommerce platform: plugin evaluation and feature work, production debugging through logs and SQL, and SSL and backup management on the VPS.

`Moodle` `WordPress` `WooCommerce` `MariaDB` `Nginx` `Linux`

## Personal projects

### Fulkopi: MERN e-commerce platform · [live](https://fulkopi-frontend.vercel.app/) · [frontend](https://github.com/mezbaur2004/fulkopiFrontend) · [backend](https://github.com/mezbaur2004/fulkopiBackend)
Full-stack store with Google OAuth and JWT authentication, role-based access control, an admin dashboard, and SSLCommerz checkout.

`MongoDB` `Express.js` `React.js` `Node.js` `Redux Toolkit`

### Inventory Management System · [live](https://inventory-frontend-mezbaur.vercel.app/) · [frontend](https://github.com/mezbaur2004/inventoryFrontend) · [backend](https://github.com/mezbaur2004/inventoryBackend)
REST API and React/Redux dashboard to manage products, brands, categories, suppliers, customers, purchases, sales, returns, and expenses. A purchase, sale or return and its line items are written and deleted in one MongoDB transaction. Date-range reports and OTP password recovery.

`React.js` `Redux Toolkit` `Express.js` `MongoDB`

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

## Connect

[mezbaur2004@gmail.com](mailto:mezbaur2004@gmail.com) · [mezbaur.vercel.app](https://mezbaur.vercel.app) · [LinkedIn](https://www.linkedin.com/in/mezbaur2004)
