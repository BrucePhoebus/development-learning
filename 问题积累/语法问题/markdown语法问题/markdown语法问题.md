# markdown语法问题整理

## 简单语法问题

	这是不该错的语法问题，一般用过之后都不应该错

#### 1. 图片显示不了

	新的项目，想显示一下图片，却发现一直404，肯定

*404写法*
![](/项目笔记/images/project.png)

> 虽然工具中也可以显示，但实际上浏览器是找不到该图片的，404，主要是语法不支持

*正确写法*
![](../../../项目笔记/images/project.png)

> 应该使用相对路径，使用./或../

#### 2. 文件引用404

	跟上面图片访问道理一样，写文件链接地址也有固定的语法

*404写法*
* [markdown语法问题](./markdown语法问题/markdown语法问题.md)

> 这里使用了相对路径，图片这样写是对的，但是文件就不能这样引用了

*正确写法*
* [markdown语法问题](问题积累/语法问题/markdown语法问题/markdown语法问题.md)

> 应该从SUMMARY.md所在文件根目录开始写起，因为它是直接从#开始替换路径的，如果使用相对路径，当然是找不到啦！
