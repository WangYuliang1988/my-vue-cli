Vue CLI 学习工程，参考：<https://cli.vuejs.org/zh/guide/>

## Vue CLI 介绍及应用

## Vue CLI 简介
Vue CLI是一个基于Vue.js进行快速开发的完整系统，致力于将Vue生态中的工具基础标准化，使开发人员专注于编写应用，而不必纠结配置的问题。CLI即Command Line Interface，命令行交互界面，又称脚手架。

Vue CLI包含以下几个独立部分：
1. CLI
CLI (@vue/cli) 是一个全局安装的 npm 包，提供了终端里的 vue 命令。它可以通过 vue create 快速搭建一个新项目，或者直接通过 vue serve 构建新想法的原型。你也可以通过 vue ui 通过一套图形化界面管理你的所有项目。

2. CLI 服务
CLI 服务 (@vue/cli-service) 是一个开发环境依赖。它是一个 npm 包，局部安装在每个 @vue/cli 创建的项目中。CLI 服务构建于 webpack 和 webpack-dev-server 之上。
`vue-cli-service serve` 命令会启动一个开发服务器 (基于webpack-dev-server) 并附带开箱即用的模块热重载 (Hot-Module-Replacement)。
`vue-cli-service build` 会在 dist/ 目录产生一个可用于生产环境的包，带有 JS/CSS/HTML 的压缩，和为更好的缓存而做的自动的 vendor chunk splitting。

3. CLI 插件
CLI 插件是向你的 Vue 项目提供可选功能的 npm 包，例如 Babel/TypeScript 转译、ESLint 集成、单元测试等。Vue CLI 插件的名字以 @vue/cli-plugin- (内建插件) 或 vue-cli-plugin- (社区插件) 开头，非常容易使用。
每个CLI插件都包含一个用来创建文件的**生成器**和一个用来调整webpack核心配置和注入命令的**运行时插件**。

4. Preset
Vue CLI preset 是一个包含创建新项目所需预定义选项和插件的 JSON 对象，让用户无需在命令提示中重复选择。
在创建新项目过程中保存的 preset 会被放在 home 目录下的一个配置文件中 (~/.vuerc)。可以通过直接编辑这个文件来调整、添加、删除已保存的 preset。

## Vue CLI 安装
> Vue CLI 需要 Node.js 8.9 或更高版本 (推荐 8.11.0+)。

1. 通过以下命令安装Vue CLI：`npm install -g @vue/cli`；
2. 在命令行中运行`vue --version`，显示出vue的版本信息，安装成功！

## 创建工程
1. 方式一：命令行创建。打开命令行，切换到待创建工程的目录，然后执行`vue create my-vue-cli`，完成！
2. 方式二：图形化界面。打开命令行，执行`vue ui`，在打开的网页中进行工程创建，完成！

## 运行工程
1. 打开命令行，切换到工程目录，执行`cd my-vue-cli`；
2. 然后，执行`npm run serve`，启动服务；
3. 打开浏览器，输入<http://localhost:8080/>，出现欢迎页面，成功！