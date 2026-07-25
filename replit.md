# Voltline Mobility Compass

An EV charging and trip management mobile web app built with TanStack Start + React.

## Stack

- **Framework**: TanStack Start (SSR) + TanStack Router (file-based routing)
- **UI**: React 19, Tailwind CSS v4, Radix UI, shadcn/c omponents
- **Bundler**: Vite 8 (via `@lovable.dev/vite-tanstack-config`)
- **Package manager**: Bun

## Running the app

```bash
bun run dev
```

Runs on port 5000. The `Start application` workflow is configured to start it automatically.

## Key structure

- `src/routes/` — file-based routes (TanStack Router). Each `.tsx` = one route.
- `src/components/` — shared UI components
- `src/hooks/` — custom React hooks
- `src/lib/` — utilities
- `src/start.ts` — TanStack Start entry (SSR middleware)
- `src/server.ts` — SSR error wrapper
- `vite.config.ts` — Vite config (extends Lovable's preset; server overridden to port 5000 / host 0.0.0.0)

## Routes overview

| Route | Purpose |
|---|---|
| `/` | Splash / landing |
| `/auth` | Authentication |
| `/onboarding` | Onboarding flow |
| `/home` | Main dashboard |
| `/charger/:id` | Charger detail |
| `/charger/:id/start` | Start charging session |
| `/charging/:id` | Active charging session |
| `/charging/:id/complete` | Session complete |
| `/trip` | Trip planner |
| `/saved-trips` | Saved trips |
| `/pay/:id` | Payment flow |
| `/receipt/:id` | Receipt |
| `/wallet` | Wallet |
| `/profile` | User profile |
| `/edit-profile` | Edit profile |
| `/notifications` | Notifications |
| `/settings` | Settings |
| `/help` | Help |
| `/states` | UI component states |

## User preferences

- Keep the existing project structure and stack.
