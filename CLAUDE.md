# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Commands

```bash
npm install       # install deps
npm run dev       # dev server at http://localhost:5173
npm run build     # production build
npm run lint      # eslint
npm run preview   # preview production build
```

## Architecture

Single-page React app. All logic lives in `src/App.jsx` — one component, no routing, no global state library.

**Data model:** `transactions` array in `useState`. Each transaction: `{ id, description, amount, type, category, date }`.

**Known intentional issues (course material):**
- `amount` stored as string — `reduce` on income/expenses concatenates instead of summing
- UI is unstyled/basic
- Entire app is one monolithic component

`src/App.css` holds all styles. No component subdirectory exists yet.
