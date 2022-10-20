# eslint-config-airbnb-vue3-ts
[airbnb](https://github.com/airbnb/javascript) 风格规范的 eslint 配置，适用于 vue3 + ts 项目。

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
