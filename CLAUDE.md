# Claude Rules and Commands

This file defines the build commands, runtime scripts, and code style conventions for the Frontend AI Engineering capstone project.

## Development & Build Commands

- **Install Dependencies:** `npm install`
- **Start Development Server:** `npm run dev`
- **Production Build:** `npm run build`
- **Linting & Code Quality:** `npm run lint`

## Code Style & Architecture

- **Tech Stack:** React, Next.js (App Router), Tailwind CSS, and TypeScript.
- **Component Structure:** Functional components only, with explicit TypeScript interfaces/types for all props. Use hooks for state management — no class components.
- **Styling:** Strict adherence to Tailwind CSS utility classes. Avoid inline styles or custom CSS files, with one exception: `app/globals.css` for Tailwind's base directives.
- **File Naming:** kebab-case for directories and source files (e.g., `components/custom-button.tsx`), PascalCase for component names within files (e.g., `export function CustomButton()`).
- **Error Handling:** Use error boundaries (`error.tsx` per route segment) and explicit type checks to prevent application crashes.

## Folder Structure

- **`app/`** — Routes, layouts, and route-local (`_components/`) UI, following Next.js App Router conventions.
- **`components/`** — Shared, cross-feature UI primitives.
- **`lib/types/`** — Shared TypeScript interfaces and types.
- **`lib/utils/`** — Pure utility/helper functions.
- **`lib/hooks/`** — Reusable client-side hooks.

## Route Segment Conventions

Each route folder under `app/` should include, where applicable:
- `page.tsx` — the route's main Server Component
- `layout.tsx` — persistent layout for that segment
- `loading.tsx` — Suspense fallback / skeleton state
- `error.tsx` — client-side error boundary with typed props (`{ error: Error; reset: () => void }`)

## Client vs. Server Components

Default to Server Components. Add `'use client'` only when a component needs interactivity, browser APIs, or local state (e.g., charts, dropdowns, toggles).

