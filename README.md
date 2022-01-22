# svelte-iconoir

[![NPM][npm]][npm-url]

> [Iconoir SVG icons](https://github.com/lucaburgio/iconoir) as Svelte components.

<!-- REPO_URL -->

<!-- Try it in the [Svelte REPL](). -->

---

<!-- TOC -->

## Installation

**Yarn**

```bash
yarn add -D svelte-iconoir
```

**NPM**

```bash
npm i -D svelte-iconoir
```

**pnpm**

```bash
pnpm i -D svelte-iconoir
```

## Usage

### Basic

```svelte
<script>
  import { Activity, BubbleStar, Camera } from "svelte-iconoir";
</script>

<Activity />
<BubbleStar />
<Camera />
```

Refer to [ICON_INDEX.md](ICON_INDEX.md) for a list of supported icons.

### Direct import

Use the direct import for faster compiling during development.

**Note:** even if using base imports, unused imports are still tree shakeable by application bundlers like Rollup or webpack.

```html
<script>
  import AddPage from "svelte-iconoir/lib/AddPage.svelte";
</script>
```

## Using `svelte:component`

```svelte
<script>
  import * as icons from "svelte-iconoir";
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

[npm]: https://img.shields.io/npm/v/svelte-iconoir.svg?color=%232b4cf9style=for-the-badge
[npm-url]: https://npmjs.com/package/svelte-iconoir
