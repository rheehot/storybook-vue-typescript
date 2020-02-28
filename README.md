# storybook-vue-typescript

This shows how to use Storybook alongside Vue with Typescript.

## Project setup
- clone my fork of `storybook/presets`: [graup/presets#typescript-vue](https://github.com/graup/presets/tree/typescript-vue/packages/preset-typescript), and `npm link` it into here

```
yarn
# or  npm i
```
### Storybook
```
yarn run storybook
# or  npm run storybook
```

## How I got here

1. [Install Vue CLI](https://cli.vuejs.org/guide/installation.html)
2. [Create a Vue Project](https://cli.vuejs.org/guide/creating-a-project.html) with Typescript and Babel
3. [Add Storybook.js](https://storybook.js.org/docs/guides/guide-vue/)
4. Add `@storybook/preset-typescript` and [configure it](./.storybook/main.js).
5. [Patch @storybook/preset-typescript](https://github.com/graup/presets/commit/01c06f95dea635d3b739931c420e5cba44a2139a)
6. Apply [a patch](./patches/@storybook+vue+5.3.14.patch) removing `babel-preset-vue` from the Storybook code. This patch is automatically run via a `postinstall` hook. Maybe [some day](https://github.com/storybookjs/storybook/issues/4475) this won't be needed anymore.
7. Profit!