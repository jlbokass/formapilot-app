# AGENTS.md

## FormaPilot Design System Rules

- Figma is currently the source of truth for design tokens.
- Never invent a local token when an equivalent Figma token exists.
- Use CSS variables from `src/styles/tokens.css`.
- Never use a Figma primitive directly in a component; use public Semantic or Dimensions tokens.
- Do not edit `design-tokens/figma.snapshot.json` manually.
- Reuse existing UI components before creating a new one.
- Preserve the Figma variants and properties documented in `docs/figma-components.md`.
- Run lint, tests, and build when they become available.
- Never push directly to `main`.
