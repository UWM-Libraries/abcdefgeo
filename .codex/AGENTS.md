# Agent Reference Map

This file is a quick orientation guide for Codex agents working in this repo.
Do not treat it as a replacement for the project docs. Read the referenced
files when the task touches their area.

## Start Here

- `README.md`: project purpose, active SPA architecture, configuration model,
  environment variables, script commands, and static-site assumptions.
- `DESIGN.md`: visual contract. Read before meaningful UI or styling changes.
- `docs/README.md`: index for adopter-facing documentation.
- `docs/adopting-github-pages.md`: institutional adoption workflow, GitHub
  Pages deployment guidance, theme modeling, API key cautions, routing/base-path
  rules, and component customization constraints.
- `scripts/README.md`: script-specific notes, especially migration helpers that
  may modify files.

## Important Working Notes

- Prefer the active React/Vite SPA in `src/`; `app/` and `server/` are legacy or
  transitional unless a task explicitly targets them.
- Keep institution-specific branding, copy, assets, API scope, and deployment
  behavior in `theme.yaml`, `themes/*.yaml`, and `public/` where possible.
- Put shared UI copy in `src/i18n/messages.ts`; put institution-specific copy in
  localized theme fields.
- Preserve static hosting compatibility. Watch for GitHub Pages routing,
  `VITE_BASE_URL`, public asset paths, and browser-visible `VITE_*` values.
- Treat BTAA behavior as a first-class reference preset while keeping generic
  product behavior configurable.
- When adding or changing configuration fields, update `README.md` and keep
  backwards-compatible defaults where reasonable.
- If UI changes are intentional changes to the visual system, update
  `DESIGN.md` in the same task.
- Run the narrowest useful verification first, then broaden to `npm run lint`,
  `npm run test`, `npm run build`, or `npm run format:check` as the change
  warrants.
