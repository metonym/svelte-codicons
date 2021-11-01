# svelte-codicons

[![NPM][npm]][npm-url]

> [VS Code Codicons](https://github.com/microsoft/vscode-codicons) as Svelte components.

This library uses [svelvg](https://github.com/metonym/svelvg) to convert SVG files from the `@vscode/codicons` NPM package into Svelte components.

<!-- REPO_URL -->

Try it in the [Svelte REPL](https://svelte.dev/repl/f47568d489c34e8892da08273368744e).

---

<!-- TOC -->

## Installation

**Yarn**

```bash
yarn add -D svelte-codicons
```

**NPM**

```bash
npm i -D svelte-codicons
```

**pnpm**

```bash
pnpm i -D svelte-codicons
```

## Usage

### Basic

```svelte
<script>
  import { Add, Calendar, Edit } from "svelte-codicons";
</script>

<Add />
<Calendar />
<Edit />
```

Refer to [ICON_INDEX.md](ICON_INDEX.md) for a list of supported icons.

### Direct import

Use the direct import for faster compiling during development.

**Note:** even if using base imports, unused imports are still tree shakeable by application bundlers like Rollup or webpack.

```html
<script>
  import Add from "svelte-codicons/lib/Add.svelte";
</script>
```

## Using `svelte:component`

```svelte
<script>
  import * as icons from "svelte-codicons";
</script>

{#each Object.entries(icons) as [icon, component]}
  <div>
    <svelte:component this={component} />
    {icon}
  </div>
{/each}
```

## TypeScript

Svelte version 3.31 or greater is required to use this library with TypeScript.

## [Changelog](CHANGELOG.md)

## License

[MIT](LICENSE)

`vscode-codicons` is licensed as [CC-BY-4.0](https://github.com/microsoft/vscode-codicons/blob/main/LICENSE).

[npm]: https://img.shields.io/npm/v/svelte-codicons.svg?color=%230066B8&style=for-the-badge
[npm-url]: https://npmjs.com/package/svelte-codicons
