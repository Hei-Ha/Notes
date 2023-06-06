### 如何提高 `webpack` 的构建速度

1、使用插件 `DllPlugin` 将经常不变的代码提前打包，避免重复打包（`vue`, `react` 库）。  
2、开发环境时，可以在`webpack config`中将 `catch` 设置为 `true` 。  
3、生产环境时，关闭不必要的功能，例如 `souce map`。