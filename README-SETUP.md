# Kingston Academy website — setup instructions

## Hosting and clean URLs
Upload the contents of this folder to the site root. All internal links use extensionless paths such as `/courses` and home uses `/`. Each page has both a `.html` file and a `page/index.html` copy for static hosts supporting directory indexes. `.nojekyll` is included. For Netlify, the included `_redirects` supports clean URLs. On some hosts, set clean URLs or rewrites to avoid redirects to trailing slashes.

## Contact form
The contact form sends submissions directly from the website using FormSubmit AJAX to `info@kingstonacademy.co.uk`, without opening the visitor's email client. The FIRST submission requires an email confirmation sent by FormSubmit to that inbox. Confirm it to activate delivery. Check spam. This is a third-party service; review GDPR/data-processing requirements before launch. For a production-grade solution with stronger spam prevention, replace with your own backend or managed forms service.

## Stripe
Checkout is intentionally DISABLED until you provide verified prices and Stripe setup. Never put Stripe secret keys in HTML or JS. To enable a multi-item cart with Stripe Checkout, deploy a serverless function or backend to create sessions using Stripe secret keys stored in environment variables, and add a checkout button that POSTs only product IDs and quantities. Server MUST resolve prices from a trusted catalog, not from the browser. Set success/cancel URLs, webhook signature verification and order fulfilment. A static-only GitHub Pages site cannot securely create Stripe Checkout Sessions.

## Assets
All supplied course images are in `assets/images/`. Replace images or adjust the product catalog in `assets/js/catalog.js`. The provided combined UKRLP/ICO/CPD screenshot appears as a single image. Confirm registration numbers and permission to display each logo. Do not imply ICO registration or UKRLP registration means course accreditation.

## Before launch
Confirm qualification names, levels, awarding scope, logos, registration numbers, training venues, prices, booking terms, refund policy, privacy policy, and data-processing obligations. Placeholder policies must be replaced before selling courses.
