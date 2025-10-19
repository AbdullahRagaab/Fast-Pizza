# Fast Pizza (React + Vite + Tailwind)

A small example React app that demonstrates a pizza ordering UI with a minimal backend API, built with Vite, Tailwind CSS and Redux Toolkit.

## About

This project is a front-end for a mock pizza shop. It shows a menu, lets users add items to the cart, create and update orders, and search for orders. It uses a tiny public API for menu and orders and a public reverse-geocoding service to resolve locations.

Key features:
- Browse menu items
- Add/update/remove items in a cart (Redux Toolkit)
- Create and update orders
- Search orders by ID
- Uses browser geolocation to resolve an address (reverse geocoding)

## Tech stack
- React 18
- Vite (dev server + build)
- Tailwind CSS
- Redux Toolkit
- React Router

## Quick start

Prerequisites
- Node.js 16+ (or compatible)
- npm (or pnpm/yarn)

Install dependencies:

```bash
npm install
```

Run the dev server:

```bash
npm run dev
```

Build for production:

```bash
npm run build
```

Preview the production build locally:

```bash
npm run preview
```

## Project structure (important files)

- `index.html` - Vite entry HTML
- `src/main.jsx` - React entry file
- `src/App.jsx` - App component and routes
- `src/index.css` - Tailwind styles and global CSS
- `src/store.js` - Redux store
- `src/features` - Feature folders: `menu`, `cart`, `order`, `user`
- `src/services/apiRestaurant.js` - API helper for menu & orders
- `src/services/apiGeocoding.js` - Reverse geocoding helper
- `src/ui` - Shared UI components

## API / environment notes

This project uses a small public API and a public reverse-geocoding service. By default the endpoints used are:

- Restaurant API (menu & orders):
  `https://react-fast-pizza-api.jonas.io/api` (configured in `src/services/apiRestaurant.js` as `API_URL`).
- Reverse geocoding (get address from coordinates):
  `https://api.bigdatacloud.net/data/reverse-geocode-client` (used in `src/services/apiGeocoding.js`).

No environment variables are required out of the box. If you want to point the app at a different backend, edit `API_URL` in `src/services/apiRestaurant.js` or implement environment variable loading (e.g. using Vite's `import.meta.env`).

## Development notes

- The app uses Redux Toolkit slices located under `src/features`.
- Tailwind is configured via `tailwind.config.js` and PostCSS is already set up.
- Prettier + ESLint devDependencies are included; feel free to add lint scripts or apply formatting.

## Testing / quality gates

Quick manual checks to run locally:

1. `npm install`
2. `npm run dev` and open the app in the browser
3. Try creating an order from the cart, then search for the order ID using the order search UI

Automated tests are not included—adding a small test suite (Jest/React Testing Library or Vitest) is a good next step.

Enjoy building! 🍕



<img width="1355" height="636" alt="Image" src="https://github.com/user-attachments/assets/ac0e2c7d-a2a8-4393-a8c9-48e9972774a5" />
<img width="1355" height="639" alt="Image" src="https://github.com/user-attachments/assets/5a3b57bd-1b7a-4909-a4e8-c8642a672a50" />
<img width="1365" height="652" alt="Image" src="https://github.com/user-attachments/assets/6a607dbd-eb62-407c-960b-51dc77ed57c8" />
<img width="1363" height="649" alt="Image" src="https://github.com/user-attachments/assets/90229f93-287d-47b8-9eff-54a8e433c34c" />
<img width="1344" height="632" alt="Image" src="https://github.com/user-attachments/assets/bf0bbb02-e15b-4945-b3d4-c251286efe7d" />
<img width="1341" height="636" alt="Image" src="https://github.com/user-attachments/assets/28f363b3-24d1-48da-89b4-1ff6d0db7c93" />
<img width="1343" height="629" alt="Image" src="https://github.com/user-attachments/assets/2c1bd16a-6516-41f8-bc13-c346632a55c3" />
<img width="1344" height="633" alt="Image" src="https://github.com/user-attachments/assets/da68e8b7-7ca3-446e-9ca1-ec5469bfdb0a" />
<img width="1351" height="631" alt="Image" src="https://github.com/user-attachments/assets/ad1ac74c-2491-4046-80cc-dad1d1ecfce8" />
