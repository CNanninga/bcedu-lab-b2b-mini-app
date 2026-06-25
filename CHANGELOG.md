# Changelog

## 1.0.2

_Based on Vite (`create-vite`) 9.2.1_

### Summary

Framework and dependency upgrade. The progressive history was rebuilt on a clean `create-vite` 9.2.1 install, which moves the lab to Vite 8 and replaces the ESLint toolchain with oxlint. No lab code changes.

### Changes

- Rebuilt the progressive history on `npm create vite@9.2.1` (`react-ts` template), upgrading Vite from 7.1.7 to 8.3.0.
- Replaced the ESLint toolchain with oxlint, matching the new template: removed `eslint`, `@eslint/js`, `eslint-plugin-react-hooks`, `eslint-plugin-react-refresh`, `typescript-eslint`, and `globals` (and `eslint.config.js`); added `oxlint` and `.oxlintrc.json`. The `lint` script now runs `oxlint`.
- Upgraded `vite-plugin-css-injected-by-js` from 4.0.1 to 5.0.2 (major).
- Upgraded `zod` from 4.4.3 to 4.6.5.
- Upgraded template dependencies: `react`/`react-dom` to 19.2.8, `@vitejs/plugin-react` to 6.1.1, `typescript` to 6.0.2, and the `@types/*` packages.
- Dropped the new template's demo assets (`public/favicon.svg`, `public/icons.svg`, `src/assets/hero.png`, `src/assets/vite.svg`) in the "Strip to boilerplate" step, consistent with the prior history.

## 1.0.1

_Based on Vite (`create-vite`) 8.0.2_

### Summary

Refactored commit history to place TODO comments immediately before the commits that resolve them.

## 1.0.0

_Based on Vite (`create-vite`) 8.0.2_

### Summary

First project-versioned progressive history. Establishes the project's own version line (separate from the base-framework version) and the supporting structure: a dedicated tutorial document, a changelog, and the traditional-branch / progressive-history Git model.

### Changes

- Introduced project versioning in `package.json` (`version`), tagged on the progressive history tip.
- Moved the lab step listing and GitHub diff links out of `README.md` into `docs/TUTORIAL.md`, with a "Based on version" banner.
- Added this `CHANGELOG.md` and its entry format.
- Re-tagged legacy base-framework version tags to the `framework-<semver>` convention (e.g. `framework-8.0.2`), freeing plain semver for project versions.
- Documented the traditional-branch vs progressive-history model and the strict 1:1 TODO → code commit convention in `AGENTS.md` / `CLAUDE.md`.
- Fixed a mislabeled "Full Lab 2 diff" link under the Previously Ordered lab while relocating the lab content.
- No lab code changes — identical in code to the prior history.
