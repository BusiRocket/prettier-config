# @vibracomet/prettier-config

Shared Prettier configuration presets for JavaScript, TypeScript, Markdown, and
optional Tailwind and Astro plugins.

## Requirements

- Node.js 20+
- Prettier 3+

Peer plugins are listed in `package.json` (`prettier-plugin-organize-imports`,
`prettier-plugin-css-order`, and optionally `prettier-plugin-astro`,
`prettier-plugin-tailwindcss`).

## Install

```bash
pnpm add -D @vibracomet/prettier-config@^0.1.0 prettier
```

Add optional peers for Astro or Tailwind when you use those stacks.

## Exports

| Subpath      | Use case                                      |
| ------------ | --------------------------------------------- |
| `.`          | Base config (organize-imports, css-order, MD) |
| `./frontend` | Tailwind class sorting                        |
| `./astro`    | Astro + Tailwind                              |

Example `prettier.config.mjs`:

```js
import base from '@vibracomet/prettier-config'

/** @type {import('prettier').Config} */
export default { ...base }
```

## Repository

Source and issues: [github.com/VibraComet/prettier-config](https://github.com/VibraComet/prettier-config).

Broader adoption docs: [engineering-baseline](https://github.com/VibraComet/engineering-baseline).
