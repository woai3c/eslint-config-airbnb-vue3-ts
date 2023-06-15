# eslint-config-airbnb-vue3-ts
结合了 [airbnb](https://github.com/airbnb/javascript) 和 [prettier](https://prettier.io/) 风格规范的 eslint 配置，适用于 js、ts 项目，兼容 vue3。

## 使用
```
npm i -D eslint-config-airbnb-vue3-ts
```
```js
// .eslintrc.js
module.exports = {
    root: true,
    env: {
        browser: true,
        node: true,
        es6: true,
    },
    extends: ['eslint-config-airbnb-vue3-ts'],
}
```
