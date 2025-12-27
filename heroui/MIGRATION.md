# Tailwind v4 migration notes

Changes applied during migration:

- Ran `npx @tailwindcss/upgrade --to 4` to apply automatic migrations ✅
- Fixed `styles/globals.css` plugin path (changed `@plugin './hero.ts'` -> `@plugin '../hero.ts'`) ✅
- Converted `tailwind.config.js` to CommonJS require (avoid module-type parsing warnings) ✅
- Ensured dependencies installed (`pnpm install`) and built successfully (`npm run build`) ✅

Notes / follow-ups:

- ESLint emitted a warning about `@eslint/compat` not being found in `eslint.config.mjs` — this is unrelated to Tailwind and can be addressed separately.
- Tests and further QA recommended across pages/components that use `@heroui/theme` plugin.
