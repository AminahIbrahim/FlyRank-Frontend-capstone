



# FlyRank Frontend Capstone

This is the core baseline repository for the FlyRank Frontend AI Engineering capstone project. The application is built using a modern software development toolchain focused on performance, type safety, and seamless AI assistance.

## Tech Stack & Core Tooling

- **Framework:** React / Next.js (App Router)
- **Styling:** Tailwind CSS (utility-first, responsive design)
- **Language:** TypeScript (strict type checking and safety)
- **AI Toolchain Integration:** Fully optimized for Claude Code and Cursor IDE integration

## Getting Started

1. **Install dependencies:**
```bash
   npm install
```
2. **Run the development server:**
```bash
   npm run dev
```
3. **Build for production:**
```bash
   npm run build
```
4. **Lint the codebase:**
```bash
   npm run lint
```

## Project Architecture

- **`app/`** — Next.js App Router structure for routes, layouts, and route-local components (e.g. `app/(dashboard)/dashboard/_components/`).
- **`components/`** — Shared, reusable UI elements used across multiple features (buttons, cards, inputs).
- **`lib/`** — Shared types, utilities, and hooks (`lib/types/`, `lib/utils/`, `lib/hooks/`).
- **`app/globals.css`** — The single global stylesheet, containing only Tailwind directives. This is the one sanctioned exception to the "no custom CSS" rule in `CLAUDE.md` — all other styling must use Tailwind utility classes inline.

## Conventions

See `CLAUDE.md` for detailed code style, naming, and architecture rules followed throughout this repo.

