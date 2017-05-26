# Webpack、Browserify和Gulp三者之间到底是怎样的关系？

(总结自知乎大神)

没有用过Browserify.Gulp是前端自动化工具，为了简化前端工作流程。

Gulp通过配置所需的插件，将以前需要手动做的事情帮你做了。

比如：自动刷新页面，压缩css、js文件、图片等，语法检查等

webpack和browserify是前端预编译模块的方案，

相比require.js，require.js是一种在线编译模块的方案，相当于在页面上加载一个 CMD/AMD 解释器。

而webpack是预编译的，不需要在浏览器中加载解释器。

另外，webpack可以兼容 AMD / CMD / ES6 风格的模块化。

- gulp的核心功能：
1. 任务定义和组织
2. 基于文件 stream 的构建
3. 插件体系

gulp 适合于任何基于 JavaScript 构建的场合，无论是前端还是后端（Node.js）；甚至可以在 gulp 里直接调用 Webpack

- webpack 最核心的功能：
1. 按照模块的依赖构建目标文件；
2. loader 体系支持不同的模块；
3. 插件体系提供更多额外的功能；

Webpack 的核心就是模块化地组织，模块化地依赖，然后模块化地打包。相对来上，场景局限在前端模块化打包上

目前大点的项目，Webpack 和 gulp 都是同时存在的，只是各自负责擅长的那部分

比如 Webpack 将模块的、互相依赖的分散的代码打包成数个文件，然后再使用 gulp 任务去做压缩，加版本号，替换等等其他工作。

[三大主流模块打包工具对比](http://www.techug.com/post/webpack-requirejs-browserify.html)

# webpack打包速度慢，你觉得可能的原因是什么，该如何解决?
[webpack打包分析与性能优化](https://github.com/hawx1993/tech-blog/issues/3)

[彻底解决Webpack打包性能问题](https://zhuanlan.zhihu.com/p/21748318)

[webpack使用优化](http://www.alloyteam.com/2016/01/webpack-use-optimization/)
