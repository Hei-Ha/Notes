## `webpack` 和 `vite` 的区别


###  区别
1、开发环境的区别：
- `vite` 是自己实现的 `server`，不对代码进行打包，是充分利用了浏览器的功能，（对 `<script type="module">` 的支持）
假设 `main.js` 里面引入了 `vue.js` ，`vite` 会改写引入 `vue.js` 的路径，浏览器会按照路径去找 `vue.js` 代码。 

- `webpack-dev-server` 是使用 `babel-loader` 对代码进行打包，然后拷贝到 `main.js` 里面，会比 `vite` 慢很多。 

2、生产环境的区别：  
- `vite` 使用的是 `rollup` + `esbuild` 打包 `JS` 的代码。
- `webpack` 使用的是 `babel` 打包的代码，比 `vite` 慢很多。（`babel` 比 `esbuild` 慢很多）

3、文件处理的时机不一样。
- vite 会在你需要某个文件的时候，才去处理该文件。
- webpack 会所有的文件打包好，一下子给出来。

## Vite 的缺点
- 热更新偶尔失败（刷新即可解决）。
- 生态不如 webpack 完善。
- 不支持老的浏览器。