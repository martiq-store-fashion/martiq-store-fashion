# Deploying to GitHub and Vercel

## 1. Push to GitHub
1. Create an empty repository at github.com/new named `martiq-store-fashion` (no README, no .gitignore).
2. In this folder run:

       git remote add origin https://github.com/YOUR-USERNAME/martiq-store-fashion.git
       git branch -M main
       git push -u origin main

## 2. Deploy on Vercel
1. Sign in at vercel.com with GitHub.
2. Add New > Project > Import `martiq-store-fashion`.
3. Framework Preset: **Other**. Root Directory: `./`. Build Command: leave empty. Output Directory: `public` (already set in vercel.json).
4. No environment variables are needed. Click **Deploy**.
5. You get a `*.vercel.app` URL. Every push to `main` redeploys automatically.

## 3. Connect www.martiqstorefashion.com
1. Buy the domain from a registrar (it is not purchased yet).
2. Vercel project > Settings > Domains > add `www.martiqstorefashion.com`, then also `martiqstorefashion.com` (redirect to www).
3. At your registrar add the records Vercel shows. Typically: `CNAME www -> cname.vercel-dns.com` and `A @ -> 76.76.21.21`. Use the exact values Vercel displays.
4. HTTPS is issued automatically once DNS resolves.

## 4. Before real launch
- Remove `<meta name="robots" content="noindex">` in `public/index.html` and update `public/robots.txt`.
- Replace placeholder contact details, policies and sample products.
- Connect a commerce platform for accounts, checkout, payments, tax, shipping and admin (see README).
