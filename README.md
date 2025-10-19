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



