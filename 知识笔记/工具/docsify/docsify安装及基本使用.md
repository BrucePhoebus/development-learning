# docsify安装及基本使用

## docsify概述

	无需构建快速生成文档网站

*特性*

1. 无需构建，写完 markdown 直接发布
2. 支持自定义主题
3. 容易使用并且轻量

[github](https://github.com/docsifyjs/docsify) | 
[中文文档](https://docsify.js.org/zh-cn) | 
[英文文档](https://docsify.js.org/#/?id=docsify)

## docsify安装

*安装依赖*

```bash
npm i docsify-cli -g
```

*创建个文件并初始化*

```bash
mkdir project_name && cd project_name
docsify init
```

*运行*

```bash
# 现在就可以直接运行了
docsify serve
```

> 不过现在一切空白，当然，有布局效果，最好是完成配置后运行看看效果

*完善package.json*

```js
# 不过最好完善下package.son，最简单的就是添加个script，即：快捷键
"scripts": {
	"start": "docsify serve --open --port 4000"
}
```
*可以参考*：[package.json](https://github.com/BrucePhoebus/developer-note/tree/big-file/package.json)


## docsify项目结构及配置

*.nojekyll*

	这个文件主要是用来阻止 GitHub Pages 会忽略掉下划线开头的文件

*README.md*

	作为首页的渲染内容，也是当前目录或项目的说明
	每个功能子目录也应该有README.md，作为首页内容渲染，也作为子目录的内容说明

*index.html*

	入口文件，可以写一些配置，也可以同个这里为每个页面添加些内容，例如：时间

> 现在其实已经可以运行了，但最好了解下index.html怎么配置，这会让页面更好看写

*参考配置*：[index.html](https://github.com/BrucePhoebus/developer-note/tree/big-file/index.html)

*SUMMARY.md*

	这个是配置左侧目录的文件
	这个每个功能子目录都要有

*_navbar.md*

	这个是配置顶部目录的文件，相当于功能子目录，每个子目录跟根文件结构处理类似

*package.json*

	项目管理必备工具，管理依赖包，当然当前项目主要依赖只有docsify了

*.gitignore*

	要进行git管理的项目最好有一个这个文件，让git忽略一些文件

###### docsify使用

	直接写文件就可以了，然后通过在现在目录的文件中添加文件引用

> [markdown语法](/知识笔记/工具/markdown/markdown语法说明.md)

*目录参考写法*

	也就是_navbar.md和_sidebar.md目录文件的写法

```
* 项目说明

	* [项目说明](项目笔记/项目说明.md)
	* [技术目录](项目笔记/技术目录.md)
	* [项目构建过程](项目笔记/项目构建过程.md)
```

*效果图*：
![](./images/project.png)
