# PoemPort

A React SPA for browsing, reading, and commenting on poems. Talks to an Express backend at `localhost:3001`.

## Tech Stack

| Layer | Tool |
|---|---|
| UI | React 19 |
| Routing | React Router 7 (`createBrowserRouter`) |
| Styling | SASS (`.scss` per component) |
| Build | Vite 7 |
| Linting | ESLint 9 |

## Key Directories

| Path | Purpose |
|---|---|
| `src/api/` | Backend fetch functions (one file per resource) |
| `src/components/` | Reusable UI components (Card, Header, Navigation, Footer) |
| `src/Pages/` | Page-level components, each in its own folder with co-located `.scss` |
| `src/AppRoutes.jsx` | Single source of truth for all routes |
| `src/Layout.jsx` | Shell that wraps all pages (Header + Outlet + Footer) |

## Commands

```bash
npm run dev       # Start dev server (HMR, proxies /api → localhost:3001)
npm run build     # Production build → dist/
npm run preview   # Serve dist/ locally
npm run lint      # ESLint across all files
```

## Backend

Dev server proxies to `http://localhost:3001` (configured in `vite.config.js`). The backend must be running separately for data to load.

## Additional Documentation

Check these files when working on the relevant areas:

- `.claude/docs/architectural_patterns.md` — routing setup, data fetching conventions, component composition, state management approach
