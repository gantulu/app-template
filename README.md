# Mobile UI Kit — React + Vite + TypeScript + PWA

A modular, mobile-first React component foundation and installable Progressive Web App starter.

## Stack
- React 19, Vite 7, TypeScript
- CSS design tokens and component-level styles
- `vite-plugin-pwa` + Workbox for manifest and app-shell caching
- ESLint and GitHub Actions CI

## Getting started
Requires Node.js 20.19+.

```bash
npm install
npm run dev
```

## Commands
| Command | Description |
| --- | --- |
| `npm run dev` | Start local development |
| `npm run typecheck` | Type-check the application |
| `npm run lint` | Run ESLint |
| `npm run build` | Type-check and create production PWA build |
| `npm run preview` | Preview production build |

## Structure
```text
public/pwa/icons/       PWA icons
src/components/ui/      Reusable primitives and mobile patterns
src/styles/             Design tokens and global styles
src/App.tsx             Component showcase
src/main.tsx            Application entry
vite.config.ts          Vite + PWA configuration
```

## UI library
Initial primitives: Button, Badge, Card, Input, Avatar, Skeleton, Tabs, BottomSheet, ToastProvider and useToast. Import from `src/components/ui`.

## PWA behavior
The manifest and Workbox service worker are generated during production builds. Static build assets and the app shell are precached; navigation falls back to `index.html`. API requests, authentication, payments and other server-dependent operations are not automatically offline-capable. The service worker is disabled in Vite development mode. Verify installability and offline behavior using a production build served over HTTPS or localhost. Platform support varies.

## Design foundations
Customize colors, spacing, radii and shadows in `src/styles/tokens.css`. Global layout and responsive showcase styles live in `src/styles/global.css`.

## CI
GitHub Actions installs dependencies, runs TypeScript checks, ESLint and a production build.

## Roadmap
- [x] React + Vite + TypeScript scaffold
- [x] PWA manifest, service worker and app-shell caching
- [x] Initial design tokens and modular UI primitives
- [x] Responsive component showcase
- [ ] Expand form, navigation, dialog, dropdown and list patterns
- [ ] Add unit and accessibility tests
- [ ] Add browser install/offline regression checks
