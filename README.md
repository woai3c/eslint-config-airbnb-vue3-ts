# eslint-config-airbnb-vue3-ts

结合了 [airbnb](https://github.com/airbnb/javascript) 和 [prettier](https://prettier.io/) 风格规范的 eslint 配置，适用于 vue3、js、ts 项目。

非 vue 项目可以使用这个插件 [eslint-prettier-config-airbnb-ts](https://github.com/woai3c/eslint-config-airbnb-vue3-ts/tree/no-vue)

## 使用

```
npm i -D eslint-config-airbnb-vue3-ts
```

配置 `.eslintrc.js` 文件：

```js
module.exports = {
  root: true,
  env: {
    browser: true,
    node: true,
    es6: true,
  },
  extends: ['eslint-config-airbnb-vue3-ts'],
  rules: {},
}
```

配置 `.prettierrc.json` 文件：

```json
{
  "$schema": "https://json.schemastore.org/prettierrc",
  "singleQuote": true,
  "semi": false,
  "printWidth": 120,
  "tabWidth": 2,
  "useTabs": false,
  "jsxSingleQuote": false,
  "bracketSameLine": false,
  "jsxBracketSameLine": false,
  "trailingComma": "all"
}
```

配置 `.vscode/settings.json` 文件，当保存代码时使用 prettier 格式化代码：

```json
{
  "editor.codeActionsOnSave": {
    "source.fixAll": "explicit"
  },
  "editor.formatOnSave": true,
  "editor.defaultFormatter": "esbenp.prettier-vscode"
}
```

配置 `.vscode/extensions.json` 文件：

```json
{
  "recommendations": ["Vue.volar", "dbaeumer.vscode-eslint", "esbenp.prettier-vscode"]
}
```

这个 eslint 插件将代码格式化的规则都禁用掉了，因为项目代码特别多的时候，eslint 格式化会很慢，经常需要等待。

所以在 eslint 只保留了代码错误的检查，代码格式化的工作需要使用 vsocde + prettier 插件来完成。但是这只会在保存代码的时候格式化代码，不会在提交代码的时候格式化代码。

所以需要配置 ci/cd 工具来在提交代码的时候格式化代码，例如可以使用 `lint-staged` + `husky` 来实现。

**PS**：这里提供了一个 [DEMO](https://github.com/impact-camp/easy-lowcode) 以供参考，如果你觉得配置不生效或者出错了，可以参考这个示例。
