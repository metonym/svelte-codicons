# svelte-codicons

[![NPM][npm]][npm-url]

> [VS Code Codicons](https://github.com/microsoft/vscode-codicons) as Svelte components.

This zero-dependency library uses [svelvg](https://github.com/metonym/svelvg) to convert SVG files from the [@vscode/codicons](https://www.npmjs.com/package/@vscode/codicons) into Svelte components.

<!-- REPO_URL -->

Try it in the [Svelte REPL](https://svelte.dev/repl/f47568d489c34e8892da08273368744e).

---

<!-- TOC -->

## Installation

```bash
# Yarn
yarn add -D svelte-codicons

# npm
npm i -D svelte-codicons

# pnpm
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

```svelte no-eval
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

### Custom size

`$$restProps` are forwarded to the `svg` element.

Use the `width` and `height` attributes to customize the icon size. The default is 16px.

```svelte
<Add width={36} height={36} />
```

### Custom color

Use the `fill` attribute to specify a custom color.

```svelte
<Add fill="red" />
```

## [Changelog](CHANGELOG.md)

## License

[MIT](LICENSE)

`vscode-codicons` is licensed as [CC-BY-4.0](https://github.com/microsoft/vscode-codicons/blob/main/LICENSE).

[npm]: https://img.shields.io/npm/v/svelte-codicons.svg?color=%230066B8&style=for-the-badge
[npm-url]: https://npmjs.com/package/svelte-codicons
