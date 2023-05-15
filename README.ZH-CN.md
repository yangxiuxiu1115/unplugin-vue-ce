# unplugin-vue-ce
一个 `vue` 的插件能够让你扩展 `vue` 的 `custom element` 功能（提供 `v-model`、子组件 `style`）

[English](https://github.com/baiwusanyu-c/unplugin-vue-ce/blob/master/README.md) | 中文

## Feature

* 🧩 它是一个 vue 的功能扩展，让你能够在 css 文件中使用 v-bind
* 🌈 支持全平台打包工具构建（vite、webpack）
* ⛰ 支持 `v-model`
*  ⚡ 支持子组件 `style`


## Install

```bash
npm i unplugin-vue-ce -D
```
或
```bash
yarn add unplugin-vue-ce-D
```
或
```bash
pnpm add unplugin-vue-ce -D
```

## Usage
<details>
<summary>Vite</summary>

```ts
// vite.config.ts
import { defineConfig } from 'vite'
import { viteVueCE } from 'unplugin-vue-ce'
import vue from '@vitejs/plugin-vue'
import type { PluginOption } from 'vite'
export default defineConfig({
  plugins: [
    vue(),
    viteVueCE() as PluginOption,
  ],
})
```

</details>
<br>
<details>
<summary>Rollup</summary>

```ts
// rollup.config.js
import { rollupVueCE } from '@nplugin-vue-ce'
export default {
  plugins: [
    rollupVueCE(),
  ],
}
```

</details>
<br>
<details>
<summary>Webpack</summary>

```ts
// webpack.config.js
module.exports = {
  /* ... */
  plugins: [
    require('unplugin-vue-ce').webpackVueCE(),
  ],
}
```
</details>
<br>
<details>
<summary>Vue CLI</summary>

```ts
// vue.config.js
module.exports = {
  configureWebpack: {
    plugins: [
      require('unplugin-vue-ce').webpackVueCE({}),
    ],
  },
}
```

</details>
<br>
<details>
<summary>ESBuild</summary>

```ts
// esbuild.config.js
import { build } from 'esbuild'
import { esbuildVueCE } from 'unplugin-vue-ce'

build({
  plugins: [esbuildVueCE()],
})
```
</details>