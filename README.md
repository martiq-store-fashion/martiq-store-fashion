# MARTIQ STORE FASHION

Luxury fashion storefront (demonstration). Static HTML, CSS and JavaScript. No build step.

## Structure
- `public/index.html`: the full homepage (HTML, CSS and JS in one file)
- `public/favicon.svg`, `public/robots.txt`
- `vercel.json`: Vercel settings and security headers
- `.env.example`: placeholders for future services (none needed today)

## Run locally
    npm run dev        # serves ./public at http://localhost:3000

## Deploy
See DEPLOY.md.

## What is real and what is not
Working in the browser: product cards, quick-add, bag (persisted in localStorage), wishlist, search, responsive layout, light and dark themes.
Not connected: customer accounts, payments and checkout, discount codes, newsletter, inventory database, admin dashboard, order emails. Products are sample data inside `public/index.html` (`const P`).
