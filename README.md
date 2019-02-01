# hello

我是为了实现VSCode下开发vue项目的eslint规范化，不过目前最终还是放弃了。

尝试插件的方案，prettier和js-beautify，或配置[Vetur](https://github.com/vuejs/vetur/blob/master/docs/formatting.md)，其中的问题很多。[Vetur+js-beautify-html](https://github.com/vuejs/vetur/blob/master/server/src/modes/template/services/htmlFormat.ts)

去他参考的一些链接

* [vetur configurations](https://vuejs.github.io/vetur/)
* [eslint-plugin-vue](https://vuejs.github.io/eslint-plugin-vue/)
* [js-beautify](https://github.com/beautify-web/js-beautify)
* [cannot wrap with attrs limit]https://github.com/beautify-web/js-beautify/issues/1404#issuecomment-445357192
* [vue rules](https://vuejs.org/v2/style-guide/index.html)
* [Efficient Code Analyzing and Formatting (for Vue.js) with ESLint and Prettier](https://medium.com/@doppelmutzi/eslint-prettier-vue-workflow-46a3cf54332f)

## 我想要的

我希望配置好eslint就能通过`Alt+shift+f`达到规范的效果。或者：

通过保存文件达到规范效果。

`"editor.formatOnSave": true,`可以实现`Alt+shift+f`却无法实现按照规范格式化。

`"eslint.autoFixOnSave": true,`可以实现保存文件就eslint一下，但是无法一次性达成。我甚至希望能做到，保存的时候执行`npm run lintfix`来实现。这个钩子能实现吗。

用第三方插件，只能达到配置格式化代码能够尽量符合设置好的eslint，但是如果第三方没有对应的配置，永远没办法。

目前只能想，禁用保存格式化文档或者eslint。然后通过命令来fix，但是eslint又无法统一某些格式。例如：

```html
<img alt="Vue logo"
     src="./assets/logo.png">
<!-- 上面和下面这个 -->
<img alt="Vue logo" src="./assets/logo.png">
```

这就糟糕了。我暂时做个仓库，以后有空再研究。

## Project setup
```
npm install
```

### Compiles and hot-reloads for development
```
npm run serve
```

### Compiles and minifies for production
```
npm run build
```

### Run your tests
```
npm run test
```

### Lints and fixes files
```
npm run lint
```

### Customize configuration
See [Configuration Reference](https://cli.vuejs.org/config/).
