# Mezbaur Are Rafi

**Software Engineer** · Dhaka, Bangladesh

I build and maintain production web applications, LMS, and e-commerce platforms. My work covers Node.js/TypeScript backends, payment and third-party integrations, Moodle and WordPress/WooCommerce customization, and the Linux servers they run on, from requirements through deployment, documentation, and production support.

## Experience

**Assistant Programmer · Pedago Academy** · Jan 2026 – present
The organization's primary in-house software engineer. I administer the production Moodle LMS, maintain the WordPress/WooCommerce platform, build Node.js integrations for payments, authentication, and automation, and run the Linux VPS infrastructure: deployments, Nginx, PHP-FPM, SSL/TLS, backups, and monitoring. I have also written 20+ technical documents, including SOPs, server architecture, deployment guides, and disaster recovery plans.

**Intern Software Engineer · Solution Spin Ltd** · Aug 2025 – Jan 2026
Worked with senior engineers on frontend and backend features for production MERN applications, including React routing, Redux Toolkit, form validation, REST APIs, and code reviews.

## Stack

| Area | Technologies |
|---|---|
| Languages | JavaScript (ES6+), TypeScript, SQL, Python, C, C++ |
| Backend | Node.js, Express.js, REST APIs, JWT, OAuth, WebSockets |
| Integrations | Shopify Admin API, SSLCommerz, webhooks, third-party APIs |
| LMS & CMS | Moodle, WordPress, WooCommerce, Shopify (Liquid) |
| Databases | MongoDB (Mongoose), MariaDB/MySQL, PostgreSQL |
| Infrastructure | Linux VPS, Nginx, PHP-FPM, SSL/TLS, backup & disaster recovery |
| Tooling & deployment | Git, GitHub, Postman, Vercel, Render |
| Frontend | React.js, Next.js, Redux Toolkit, HTML5, CSS3, Tailwind CSS, Bootstrap |

## Featured projects

### Shopify SSLCommerz Payment Middleware · [repo](https://github.com/mezbaur2004/shopify-sslcommerz-middleware)
This is a production Node.js/TypeScript service that connects Shopify to SSLCommerz through the Shopify Admin API.
- Handles the full payment lifecycle: custom checkout, payment initiation, IPN verification, conversion of Draft Orders to paid orders, and customer email notifications.
- Verifies each payment by checking its status, matching the amount within ±0.01 BDT, and confirming the transaction ID. It also uses Helmet, HPP, rate limiting, and input sanitization.
- Records payments as manual orders, so Shopify's 2% third-party transaction fee does not apply.
- Uses a wake-up request to hide free-tier cold starts, which keeps hosting cost at $0.

`Node.js` `TypeScript` `Express.js` `MongoDB` `Shopify Admin API` `SSLCommerz`

### Jolly Learning Bangladesh: Shopify store
I developed and launched the organization's production store on my own, covering store setup, Liquid theme customization, product configuration, and SEO. Local payments run through the middleware above. The store received customer inquiries and completed live payments before any marketing campaign ran.

`Shopify` `Liquid` `JavaScript`

### Moodle Patch Manager · [local_patchmanager](https://github.com/mezbaur2004/moodle-local-patchmanager) · [block_patchmanager](https://github.com/mezbaur2004/moodle-block_patchmanager) · [local_zoomcustom](https://github.com/mezbaur2004/moodle-local-zoomcustom)
These Moodle plugins apply and track source patches to third-party plugins on a production site.
- Applies patches with pristine backups, dry runs, restore and reapply, and an audit history. The workflow is CLI-first, so the web server never needs write access to code.
- Checks patch state on a schedule and reports it through Moodle's Check API and a dashboard block.
- The first pack fixes mod_zoom's duration-based grading and pauses Zoom's report task until the fix is verified.

`Moodle` `Linux`

## Platform maintenance

### Pedago Academy: Moodle LMS & WordPress/WooCommerce
I maintain the production Moodle LMS and WordPress/WooCommerce platform, which includes plugin evaluation and feature work, debugging production issues through logs and SQL, and managing SSL and backups on the VPS.

`Moodle` `WordPress` `WooCommerce` `MariaDB` `Nginx` `Linux`

## Personal projects

### Fulkopi: MERN e-commerce platform · [live](https://fulkopi-frontend.vercel.app/) · [frontend](https://github.com/mezbaur2004/fulkopiFrontend) · [backend](https://github.com/mezbaur2004/fulkopiBackend)
A full-stack store with Google OAuth and JWT authentication, role-based access control, an admin dashboard, SSLCommerz checkout, and a Docker-ready backend.

`MongoDB` `Express.js` `React.js` `Node.js` `Redux Toolkit`

### Inventory Management System · [live](https://inventory-frontend-mezbaur.vercel.app/) · [frontend](https://github.com/mezbaur2004/inventoryFrontend) · [backend](https://github.com/mezbaur2004/inventoryBackend)
A REST API with a React/Redux dashboard. It manages products, brands, and categories, along with suppliers, customers, purchases, sales, returns, and expenses. It also has date-range reports and OTP password recovery.

`React.js` `Redux Toolkit` `Express.js` `MongoDB`

## Connect

[mezbaur2004@gmail.com](mailto:mezbaur2004@gmail.com) · [mezbaur.vercel.app](https://mezbaur.vercel.app) · [LinkedIn](https://www.linkedin.com/in/mezbaur2004)