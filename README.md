# ShopZone — React + Vite shopping demo

A responsive student shopping demo with separate User and Admin modules. It uses React and Vite, and stores demo accounts, the signed-in session, catalogue edits, cart, wishlist and orders in the browser's Local Storage.

## Features

- **User module:** browse and search products, filter by category, save favourites, manage a cart, and place a sample order.
- **Account access:** sign up and sign in with email and password; user accounts are saved locally. User-only pages and actions prompt for sign-in.
- **Admin module:** separate role-guarded dashboard with catalogue counts, registered-user/order counts, product creation/removal and order review.
- **Responsive storefront:** product cards, category navigation, cart and mobile layouts.
- **Vercel SPA routing:** `vercel.json` sends app routes to the Vite entry point.

## Run locally

Install [Node.js](https://nodejs.org/) (LTS), then from this folder run:

```bash
npm install
npm run dev
```

Open the local URL printed by Vite. To create and preview the production build:

```bash
npm run build
npm run preview
```

## Demo access

- Create a user account from **Sign in → New to ShopZone? Create an account**.
- Admin: `admin@shopzone.demo` / `admin123`.

The admin credentials are intentionally visible for classroom demonstration. This is a front-end-only educational demo, not a secure authentication system. Passwords and records live in Local Storage on that browser. Do not use real passwords or personal information. Checkout is simulated; it does not collect payments or connect to a fulfilment service. The catalogue starts with bundled sample products and can be edited in the admin module.

## Push to GitHub

1. Create a new empty repository on GitHub and copy its repository URL.
2. Open a terminal in this project folder and run:

```bash
git init
git add .
git commit -m "Build ShopZone React shopping demo"
git branch -M main
git remote add origin YOUR_GITHUB_REPOSITORY_URL
git push -u origin main
```

Replace `YOUR_GITHUB_REPOSITORY_URL` with the URL copied from your repository. GitHub sign-in/authorization is required to push.

## Deploy to Vercel

1. Sign in to [Vercel](https://vercel.com/) and choose **Add New → Project**.
2. Import the GitHub repository and authorize Vercel to access it.
3. Keep the detected Vite settings: build command `npm run build`, output directory `dist`, install command `npm install`.
4. Choose **Deploy**. Vercel will provide a public URL. Open it and check the shop, account flow, admin demo, and refresh behavior.

You need your own GitHub and Vercel accounts and must authorize those services. This package is configured for deployment but has not been pushed or deployed.

## Project structure

```text
src/
  main.jsx       React entry point
  ShopZone.jsx   Storefront, account flows, User and Admin modules
  style.css      Responsive visual styles
index.html       Vite page entry
vite.config.js   React plugin configuration
vercel.json      SPA route rewrite for Vercel
```
