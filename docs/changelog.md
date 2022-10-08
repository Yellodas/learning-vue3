---
outline: 'deep'
---

# 更新记录

由于平时也比较忙，都是利用碎片时间整理的文档，习惯勤备份，因此 commit 记录比较多，而且有些提交记录跟内容也无关，比如文档程序的调整和优化等代码提交是和内容无关的。

考虑到后面还会不定期更新内容，所以翻了一下之前跟朋友的微信聊天记录整理了前期的更新记录，之后当文档有再次更新的时候也会继续整理更新记录，方便读者们查阅。

## 2022-10-08

在 “开发 npm 包” 的相关内容处增加了 [添加版权注释](plugin.md#添加版权注释) 的构建说明，它的作用除了声明版权归属之外，还会告知使用者关于项目的主页地址、版本号、发布日期、 BUG 反馈渠道等信息，例如 jQuery / Lodash / Swiper 等库都有这样的版权注释，因此补充了这部分的内容，供有需要的开发者了解和使用。

## 2022-10-07

1. 文档程序从 VuePress 2.x 迁移到 VitePress 1.x ，并做了简单的主题适配
2. 原来的 “脚手架的升级与配置” 一章的访问地址从 `update` 调整为 `upgrade` ，访问地址已配置重定向
3. 由于原来的 “起步准备” 一章内容有点太长，这一次续写拆分了一下内容，重新划分为单独的三章，分别是：
   - 独立出来了 [了解前端工程化](engineering.md) 一章，用于科普现代前端开发所要求的工程化概念，属于讲故事性质的一章内容
   - [工程化的前期准备](guide.md) 是原来 “起步准备” 的核心内容部分，主要是科普前端工程化的入门实践，属于动手实操章节
   - 另外考虑到本书是直接使用 TypeScript 来入门 Vue 3 ，语言部分也是内容的重点之一，所以把 TypeScript 部分也独立成了 [快速上手 TypeScript](typescript.md) 一章
4. 在 “了解前端工程化” 一章里，增加以下内容：
   - 新增 [Vue.js 与工程化](engineering.md#vue-js-与工程化) ，帮助新入门的开发者了解两者之间的关系
   - 新增 [现代化的开发概念](engineering.md#现代化的开发概念) ，科普在现代前端开发过程中会频繁接触到的名词
   - 新增 [工程化不止于前端](engineering.md#工程化不止于前端) ，科普在前端工程化的帮助下，前端工程师可以做到的很多事情
   - 完善 [工程化的构建工具](engineering.md#工程化的构建工具) ，避免后面开发过程中，使用了很久还不知道这些工具的作用
5. 在 “工程化的前期准备” 一章里，增加以下内容：
   - 新增 [控制编译代码的兼容性](guide.md#控制编译代码的兼容性) ，作为工程师，了解如何控制项目的兼容性是非常重要的技能
6. 在 “插件的开发和使用” 一章里，增加了以下内容：
   - 新增 [npm 包的开发与发布](plugin.md#npm-包的开发与发布) ，介绍了 npm 包从开发到发布的一些基础知识

## 2022-09-01

更新了引用到的官方文档链接，同时修复了部分官方文档未做好重定向的无效链接，感谢 [@alleluya-young](https://github.com/alleluya-young) 在 [#191](https://github.com/chengpeiquan/learning-vue3/issues/191) 的反馈！

## 2022-07-03

补充了关于 [Node.js 版本之间的区别](guide.md#版本之间的区别) 的一些说明。

## 2022-06-23

根据 [#163 (comment)](https://github.com/chengpeiquan/learning-vue3/issues/163#issuecomment-1163008926) 的反馈，对一些 ES6+ 可能容易混淆的新语法进行了一些 Tips 补充，减少学习过程中的理解成本。

## 2022-05-03

更新了 “升级与配置” 一章的部分内容：

1. 更新了使用 [Create Preset](upgrade.md#create-preset) 创建项目的说明，现在可以通过 `--template` 选项来指定模板创建，例如：

```bash
# 全局安装
npm install -g create-preset

# 将使用 `vue3-ts-vite` 模板创建一个名为 `hello-vue3` 的项目
preset init hello-vue3 --template vue3-ts-vite
```

2. 配合 1 的更新，相应的增加了 [Hello Vue3](upgrade.md#hello-vue3) 一节
3. 配合 @vue/cli 5.x 版本的命令行交互，更新了 [使用 @vue/cli 创建项目](upgrade.md#使用-vue-cli-创建项目) 的内容
4. 更新了 [调整 TS Config](upgrade.md#调整-ts-config) 部分的内容，由于现在通过各类脚手架创建的 TypeScript 项目都自带了该文件，所以这部分内容移除了之前的配置参考，仅保留 paths 的配置提醒

## 2022-04-30

最近有时间，所以对内容做了一大波更新，主要是补充了在开始开发 Vue 项目之前的一些基础知识点，当然 Vue 相关的内容也做了一些新增或者完善。

1. 增加了全新的一章 “起步准备” ，面向对前端工程化开发不太熟悉的开发者，包含了以下内容：

   - [了解前端工程化](guide.md#了解前端工程化)
   - [命令行工具](guide.md#命令行工具)
   - [了解 Node.js](guide.md#了解-node-js)
   - [了解 Node 项目](guide.md#了解-node-项目)
   - [了解模块化设计](guide.md#了解模块化设计)
   - [了解组件化设计](guide.md#了解组件化设计)
   - [了解包和插件](guide.md#了解包和插件)
   - [了解 TypeScript](guide.md#了解-typescript)
   - [了解构建工具](guide.md#了解构建工具)

2. 在 “升级与配置” 一章里，增加了以下内容：

   - Vite 项目如何 [管理项目配置](upgrade.md#管理项目配置)
   - 添加协作规范增加了 [Prettier](upgrade.md#prettier) 和 [ESLint](upgrade.md#eslint) 的使用
   - 增加了对 [Vue Devtools](upgrade.md#vue-devtools) 的简单介绍

3. 在 “单组件的编写” 一章里，增加了以下内容：

   - 响应式数据 [设计上的变化](component.md#设计上的变化)
   - 增加了 [指令](component.md#指令) 一节的内容，主要讲解如何在 Vue 3 开发自定义指令
   - 增加了 [插槽](component.md#插槽) 一节的内容

4. 在 “路由的使用” 一章里，增加了以下内容，整理了一些常见的部署问题原因以及解决方案：

   - [部署问题与服务端配置](router.md#部署问题与服务端配置)

5. 在 “插件的使用” 一章里，对 “本地插件” 作了进一步的细化讲解：

   - 重写了 [插件的安装和引入](plugin.md#插件的安装和引入) ，完善了包管理器的一些基础配置说明
   - 增加了 [开发本地通用 JS / TS 插件](plugin.md#开发本地通用-js-ts-插件)
   - 增加了 [开发本地 Vue 专属插件](plugin.md#开发本地-vue-专属插件)

## 2022-04-20

更正了 watch API 在 [监听选项之 deep](component.md#监听选项之-deep) 部分内容的错误，并增加了如何检测特例的用法，感谢 [@zcc0329](https://github.com/zcc0329) 的反馈！

## 2022-04-10

重写了单组件关于 [数据的监听](component.md#数据的监听-new) 这一节的内容，因为在写 Pinia 的订阅功能的时候，有很多跟 watch 相关联的知识点，发现之前这部分内容写的比较简单，所以完善了一下。

## 2022-04-07

补充了昨天新增的关于 Pinia [订阅 state](pinia.md#订阅-state) 部分的一些内容。

## 2022-04-06

1. 创建基于 Vite 的 Vue 3 项目增加了一些内容：

   - 增加了使用 [Create Vue](upgrade.md#create-vue) 创建 Vite 项目的说明
   - 使用 [Create Preset](upgrade.md#create-preset) 创建的 vue3-ts-vite 预设项目，使用 Pinia 代替 Vuex

2. 补充了 Pinia 的部分内容：

   - [批量更新 state](pinia.md#批量更新-state)
   - [全量更新 state](pinia.md#全量更新-state)
   - [重置 state](pinia.md#重置-state)
   - [订阅 state](pinia.md#订阅-state)

## 2022-04-04

> 先跟大家说声抱歉，在 [2022-02-09](#_2022-02-09) 的更新里说要写这部分内容，结果因为现实里的一些事情还有工作比较忙，现在借着假期才得以继续更新。

增加了 [全局状态的管理](pinia.md) 一章，主要是面向 Vue 3 全新的状态管理工具 Pinia 展开，里面的大部分内容也加入了和 Vuex 的对比。

虽然可以归入 [组件之间的通信](communication.md) 里，但 Pinia 作为被官方推荐在 Vue 3 项目里作为全局状态管理的新工具，写着写着我觉得还是单独开一章来写会更方便阅读和理解。

## 2022-03-04

把 Algolia 的搜素功能申请下来了，看看文档的搜索体验会不会比较好（搜索框在页面的右上角）。

## 2022-02-28

升级了文档的程序版本，加入了 Dark Mode 暗黑模式的支持，默认跟随系统模式进行适配，可以在右上角的 “主题切换” 按钮手动切换主题。

## 2022-02-09

1. 优化了 [升级与配置](upgrade.md) 一章，配合 2022-02-07 Vue 3 成为默认版本带来的调整变化，主要改动如下：

   - 新增：[全新的 Vue 版本](upgrade.md#全新的-vue-版本-new) 一节，用于记录 Vue 默认版本变更后的一些注意事项
   - 新增：[使用 Vite 创建项目](upgrade.md#使用-vite-创建项目-new) ，可以通过 `create-vite` 和 `create-preset` 创建 Vite 项目
   - 调整： CLI 相关内容归类到 [使用 @vue/cli 创建项目](upgrade.md#使用-vue-cli-创建项目) 小节下面
   - 调整：[添加 VSCode 插件](upgrade.md#添加-vscode-插件) 一节，新增了 Volar 、 Prettier 、 ESLint 的插件说明

2. 在 [高效开发](efficient.md) 一章开头的 `WARNING` 改成了 `TIP` ，里面提到的功能在最新版的 Vue 下发挥稳定，后续如果有实验性的 API 再单独标记。

3. 把原先演示命令里的 `@next` 版本都改成了 `@latest` ，现在不需要指定 next 就能使用 Vue 3 了。

4. 更新了 [官方文档](#官方文档) 里面的链接说明，因为各个官网在 2022-02-07 都上线了新版本，更换了新地址。

5. 在 [组件之间的通信](communication.md) 里加入了 [Pinia](communication.md#pinia-wip-new) 的介绍，不过暂时没有写实践记录（还没有时间哈哈哈），欢迎先自行体验，这是一个官方推荐的适合 Vue 3 的状态管理工具，因为它更加面向 Composition API 的编程方式（至少在 Vuex 5 推出之前，建议用来代替 Vuex 4）。

6. 改了一下文档名称：《Vue3.0 学习教程与实战案例》 --> 《Vue 3 入门指南与实战案例》，其他原先使用 Vue 3.0 叫法的地方，后面也会陆续改成 Vue 3 了。

## 2022-01-20

1. 更新了 [cnpm](plugin.md#通过-cnpm-安装) 的用法，原因是旧的 cnpm 源即将下线，需要使用新的域名啦！（感谢 [@alleluya-young](https://github.com/alleluya-young) 在 [#135](https://github.com/chengpeiquan/learning-vue3/issues/135) 的反馈！）

2. 添加了 [pnpm](plugin.md#通过-pnpm-安装) 的用法说明，目前开源社区越来越流行使用 pnpm ，对大型项目管理也有好处，值得了解和体验。

## 2021-12-05

由于离第一次执笔到现在有了差不多一年的时间，当时的前言信息有些陈旧，重新写了一下 [前言](index.md) 。

另外经过 2021 年的开发实践，很多地方我又有了新的认知，打算在接下来的时间里，我会再继续抽空把各部分的内容再精细化一下，把以前可能写的比较简单的部分，或者没有写进来的一些功能点，都再做一次完善。

## 2021-11-16

重写了 [数据的计算](component.md#数据的计算-new) 一节，之前对于计算数据的介绍，描述上确实有点难以理解，而且有点简单带过，所以重新写了这部分内容，感谢读者 [@superficial](https://www.zhihu.com/people/superficial-14-33) 的反馈！

## 2021-10-07

补充了 [全局编译器宏](efficient.md#全局编译器宏) 的配置说明，本来很久前就想写的，一直偷懒，国庆结束前补充进来啦！

## 2021-08-17

更新了 `3.2.0` 版本新增的一些知识点：

1. 增加了 [使用 v-bind 动态修改 style](component.md#使用-v-bind-动态修改-style-new) 功能说明，同时结合上下文知识点补充了 [动态绑定 CSS](component.md#动态绑定-css) 一节

2. 增加了 [CSS Modules](component.html#style-module-new) 一节的内容

3. 增加了 [useCssModule](component.md#usecssmodule-new) 一节的内容

## 2021-08-16

1. 更新了 [深度操作符](component.html#深度操作符-new) 的内容，原有的 API 已被废弃，请注意使用新写法

2. 补充了几个拓展阅读链接到 [教程工具](#教程工具) 里

## 2021-07-28

迎接 Vue `3.2.0` 的新版本内容，对 [script-setup](efficient.md#script-setup-new) 做了较多的调整。

目前 3.2 还处于 Beta 阶段，不过从这个版本开始，script-setup 脱离实验性阶段，正式进入 Vue 3.0 的队伍，本次的更新内容较多，很多测试阶段的 API 被移除或者修改，如果之前有用过 script-setup ，建议先简单看我之前的博客，了解本次的一些变更：

[Vue3.0 最新动态：script-setup 定稿 部分实验性 API 将弃用](https://chengpeiquan.com/article/vue3-script-setup-finalization.html)

## 2021-03-31

1. 调整了 [使用全局 API](plugin.md#使用全局-api-new) 一节的内容

原因是原来推荐的 `const { proxy } = getCurrentInstance()` 的方案，在 TS 新版本校验下，使用成本非常高，原来的代码不做多层判断的情况下已经无法正常运行，所以按照目前的 “最佳实践” 重新更新了这一节。

2. 新增了一节 [全局 API 的替代方案](plugin.md#全局-api-的替代方案)

由于 Vue 3.0 的有意为之，这个 “最佳实践” 实际上用起来也挺繁琐（在官网和 GitHub 对此都有说明，不推荐使用），所以补充了这一节内容。

## 2021-03-23

对 [DOM 元素与子组件](component.md#dom-元素与子组件) 一节增加了 TS 类型的定义说明，以及编译失败的原因说明及解决方案补充，非常感谢 [@aierong](https://github.com/aierong) 的反馈和支持。

## 2021-03-21

增加了 [高效开发](efficient.md) 一章，将记录一些提高 Vue 3.0 开发效率的内容，面像对 Vue 3.0 已上手，想提高开发效率的同学。

本次更新了 [script-setup](efficient.md#script-setup-new) 一节的内容。

## 2021-01-21

增加了 [组件之间的通信](communication.md) 一章的内容。

## 2020-12-18

本文档的第一个版本上线，完成了 [升级与配置](upgrade.md) 、 [单组件的编写](component.md) 、 [路由的使用](router.md) 、 [插件的使用](plugin.md) 等章节的编写。

## 2020-10-01

国庆期间开始开荒 Vue 3.0，陆陆续续打了不少笔记，业余时间着手整理成文档。

<!-- 谷歌广告 -->
<ClientOnly>
  <GoogleAdsense />
</ClientOnly>
<!-- 谷歌广告 -->