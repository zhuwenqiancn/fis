![fis logo](http://fis.baidu.com/static/docs/img/logo_3b5cdda.png)

[![NPM version](https://badge.fury.io/js/fis.png)](http://badge.fury.io/js/fis) [![Dependencies Status](https://david-dm.org/fis-dev/fis.png)](https://david-dm.org/fis-dev/fis)

## Front-end Integrated Solution（前端集成解决方案）

> 解决前端工程的根本问题！

## F.I.S简介

* [什么是F.I.S](https://github.com/fis-dev/fis/wiki/什么是F.I.S)

## 功能概述

* 跨平台支持win、mac、linux等系统
* 无内置规范，可配置开发和部署规范，用于连接给定的系统环境
* 对html、js、css实现 [三种语言能力](https://github.com/fis-dev/fis/wiki/三种语言能力) 扩展，解决绝大多数前端构建问题
* 支持二次包装，比如 [spmx](github.com/fouber/spmx)，对fis进行包装后可内置新的插件、配置，从而打造属于你们团队的自己的开发工具
* 自动生成静态资源表（map.json），可用于 [连接前后端开发框架](https://github.com/fis-dev/fis/wiki/基于map.json的前后端架构设计指导)
* 所有静态资源自动加 ``md5版本戳``
* 支持给所有静态资源添加域名前缀
* 灵活可扩展的插件系统，可对构建过程和命令功能进行扩展，现已发布N多 [插件](https://npmjs.org/search?q=fis)
* 轻松配置插件可以使用 [less](https://github.com/fouber/fis-parser-less)、[coffee](https://github.com/fouber/fis-parser-coffee-script)、[markdown](https://github.com/fouber/fis-parser-marked)、[jade](https://npmjs.org/package/fis-parser-jade)等语言开发
* 内置 [css sprites插件](https://github.com/xiangshouding/fis-spriter-csssprites)
* 内置 [png图片压缩插件](https://github.com/fis-dev/fis-optimizer-png-compressor)，采用c++编写的node扩展，具有极高的性能，支持 [将png24压缩为png8](https://github.com/fis-dev/fis-optimizer-png-compressor)
* 内置本地开发调试服务器，支持运行 ``jsp``、``php``
* 支持文件监听，保存即发布
* 支持浏览器自动刷新，保存即刷新
* 可以上传到远端服务器，保存即增量编译上传
* 超低学习成本，只须记忆 ``3`` 条命令即可完成开发
* 抹平编码差异，开发中无论是gbk、gb2312、utf8、utf8-bom等编码的文件，输出时都能统一指定为utf8无bom（默认）或者gbk文件

## 快速上手

* [安装](https://github.com/fis-dev/fis/wiki/快速上手)
    * npm install **-g** fis
* 三条命令，满足你的所有开发需求：
    * [fis install &lt;name&gt;](https://github.com/fis-dev/fis/wiki/快速上手#fis-install-name)
    * [fis release &#91;options&#93;](https://github.com/fis-dev/fis/wiki/快速上手#fis-release-options)
    * [fis server &lt;command&gt; &#91;options&#93;](https://github.com/fis-dev/fis/wiki/快速上手#fis-server-command-options)
* 试手样例
    * [纯前端组件化方案](https://github.com/fouber/modjs-todo-demo/)
    * [fis官网](http://fis.baidu.com/#section-6)

## 三种语言能力扩展

* [关于三种语言能力](https://github.com/fis-dev/fis/wiki/三种语言能力)
* 在html中：[定位资源](https://github.com/fis-dev/fis/wiki/在html中定位资源)、[嵌入资源](https://github.com/fis-dev/fis/wiki/在html中嵌入资源)、[声明依赖](https://github.com/fis-dev/fis/wiki/在html中声明依赖)
* 在js中：[定位资源](https://github.com/fis-dev/fis/wiki/在js中定位资源)、[嵌入资源](https://github.com/fis-dev/fis/wiki/在js中嵌入资源)、[声明依赖](https://github.com/fis-dev/fis/wiki/在js中声明依赖)
* 在css中：[定位资源](https://github.com/fis-dev/fis/wiki/在css中定位资源)、[嵌入资源](https://github.com/fis-dev/fis/wiki/在css中嵌入资源)、[声明依赖](https://github.com/fis-dev/fis/wiki/在css中声明依赖)

## 插件系统

* [编译过程运行原理](https://github.com/fis-dev/fis/wiki/运行原理)
* [插件调用机制](https://github.com/fis-dev/fis/wiki/插件调用机制)
* [插件扩展点列表](https://github.com/fis-dev/fis/wiki/插件扩展点列表)

## 配置文档

* [零配置](https://github.com/fis-dev/fis/wiki/配置API)
* [使用配置文件](https://github.com/fis-dev/fis/wiki/配置API)
* 系统配置
    * [project.charset](https://github.com/fis-dev/fis/wiki/配置API#projectcharset)
    * [project.md5Length](https://github.com/fis-dev/fis/wiki/配置API#projectmd5length)
    * [project.md5Connector](https://github.com/fis-dev/fis/wiki/配置API#projectmd5connector)
    * [project.include](https://github.com/fis-dev/fis/wiki/配置API#projectinclude)
    * [project.exclude](https://github.com/fis-dev/fis/wiki/配置API#projectexclude)
    * [project.fileType.text](https://github.com/fis-dev/fis/wiki/配置API#projectfiletypetext)
    * [project.fileType.image](https://github.com/fis-dev/fis/wiki/配置API#projectfiletypeimage)
* 插件配置
    * [modules.parser](https://github.com/fis-dev/fis/wiki/配置API#modulesparser)
    * [modules.preprocessor](https://github.com/fis-dev/fis/wiki/配置API#modulespreprocessor)
    * [modules.postprocessor](https://github.com/fis-dev/fis/wiki/配置API#modulespostprocessor)
    * [modules.lint](https://github.com/fis-dev/fis/wiki/配置API#moduleslint)
    * [modules.test](https://github.com/fis-dev/fis/wiki/配置API#modulestest)
    * [modules.optimizer](https://github.com/fis-dev/fis/wiki/配置API#modulesoptimizer)
    * [modules.prepackager](https://github.com/fis-dev/fis/wiki/配置API#modulesprepackager)
    * [modules.packager](https://github.com/fis-dev/fis/wiki/配置API#modulespackager)
    * [modules.spriter](https://github.com/fis-dev/fis/wiki/配置API#modulesspriter)
    * [modules.postpackager](https://github.com/fis-dev/fis/wiki/配置API#modulespostpackager)
    * [settings](https://github.com/fis-dev/fis/wiki/配置API#settings)
* 内置插件运行配置
    * [settings.postprocessor.jswrapper](https://github.com/fis-dev/fis/wiki/%E9%85%8D%E7%BD%AEAPI#settingspostprocessorjswrapper)
    * [settings.optimizer.uglify-js](https://github.com/fis-dev/fis/wiki/%E9%85%8D%E7%BD%AEAPI#settingsoptimizeruglify-js)
    * [settings.optimizer.clean-css](https://github.com/fis-dev/fis/wiki/%E9%85%8D%E7%BD%AEAPI#settingsoptimizerclean-css)
    * [settings.optimizer.png-compressor](https://github.com/fis-dev/fis/wiki/%E9%85%8D%E7%BD%AEAPI#settingsoptimizerpng-compressor)
    * [settings.spriter.csssprites](https://github.com/fis-dev/fis/wiki/%E9%85%8D%E7%BD%AEAPI#settingsspritercsssprites)
* 目录规范与域名配置
    * [roadmap.path](https://github.com/fis-dev/fis/wiki/配置API#roadmappath)
    * [roadmap.ext](https://github.com/fis-dev/fis/wiki/配置API#roadmapext)
    * [roadmap.domain](https://github.com/fis-dev/fis/wiki/配置API#roadmapdomain)
    * [roadmap.domain.image](https://github.com/fis-dev/fis/wiki/配置API#roadmapdomainimage)
* 部署配置
    * [deploy](https://github.com/fis-dev/fis/wiki/配置API#deploy)
* 打包配置
    * [pack](https://github.com/fis-dev/fis/wiki/配置API#pack)

## 高级使用

* [基于map.json的前后端架构设计指导](https://github.com/fis-dev/fis/wiki/基于map.json的前后端架构设计指导)

## 更多资料

* [phiz](https://github.com/fouber/phiz/) PHP组件化解决方案
* [spmx](https://github.com/fouber/spmx) 通过包装fis得到适应seajs架构的集成解决方案
* [sublime plugin](https://github.com/yuanfang829/fis-sublime-command) 支持FIS编译的sublime插件，可以替代watch功能