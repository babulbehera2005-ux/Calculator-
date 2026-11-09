# Smart Kirana Calculator

A local-first, responsive grocery counter app built with vanilla HTML, CSS and JavaScript. It works offline after its first load and stores data in the browser's localStorage.

## Run it

**Recommended (for offline/PWA support):**
1. Install a local static server, for example Node.js and `npx serve`.
2. Open a terminal in this folder and run `npx serve .`
3. Open the local URL shown in the terminal (usually `http://localhost:3000`).
4. On a supported browser, use **Install app / Add to Home screen**.

You can also open `index.html` directly for basic use, but service-worker offline caching requires localhost or HTTPS.

## Features
- Calculator for kg, g, litre and piece; quick amounts; reverse price calculation.
- Product catalogue with categories, purchase/selling rates, stock and low-stock levels.
- Cart, discounts, configurable tax, payment method, stock validation and printable receipt (Print → Save as PDF).
- Stock purchase/add and manual adjustment; no negative stock from sales.
- Sales history, date filters, CSV export, customer summary and estimated gross profit.
- Currency display selection (does not convert saved values), theme toggle, JSON backup/restore.
- Local browser persistence and service-worker caching.

## Data and limitations
- Data stays in the current browser/device; this is not a cloud-synced multi-user POS.
- Browser storage can be erased by clearing site data. Export JSON backups regularly.
- Currency setting changes the display symbol only. It deliberately does not exchange stored amounts.
- Stock is tracked in the product's configured unit. Weight kg/gram conversion is supported. Litre and piece are not interchangeable.
- Tax is added to the subtotal; tax registration, invoices, GST compliance and jurisdiction-specific accounting are outside this starter app.
- Hindi/Odia language options are stored as preferences; full translation packs are not yet included.
- PDF is produced by the browser's print dialog, not by a bundled PDF library.
- Profit is an estimate from the current saved purchase cost; historical cost layers and returns are not implemented.

## Tests
Run the built-in logic tests with Node.js:
```bash
node tests.js
```
