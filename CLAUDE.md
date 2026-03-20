# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Commands

```bash
npm install        # Install dependencies
npm run dev        # Start dev server at http://localhost:3000 (opens browser automatically)
npm run build      # Build for production (output: build/)
```

No test runner is configured.

## Architecture

This is a single-page React + TypeScript app built with Vite. All game logic lives in `src/App.tsx` — there are no separate service layers or state management libraries.

**Game logic (`src/App.tsx`):** Three treasure chests are rendered, one randomly assigned a treasure. Clicking a chest opens it (+$100 for treasure, -$50 for skeleton). The game ends when treasure is found or all chests are opened.

**UI components (`src/components/ui/`):** A full shadcn/ui component library backed by Radix UI primitives. These are pre-built and rarely need modification.

**Assets (`src/assets/`):** Three chest images (`treasure_closed.png`, `treasure_opened.png`, `treasure_opened_skeleton.png`). In code, they are imported using the `figma:asset/` prefix (e.g., `import closedChest from 'figma:asset/treasure_closed.png'`). Vite aliases in `vite.config.ts` resolve these to the actual asset paths.

**Styling:** Tailwind CSS via `src/index.css` and `src/styles/globals.css`. The `@` alias resolves to `src/`.

**Animation:** `motion/react` (Framer Motion) is used for chest open/close transitions and reveal effects.
