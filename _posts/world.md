---
layout: hello
title: world
date: 2016-11-27 17:53:01
tags: 随笔

---

### md文件中预先定义的参数

`layout`布局参数描述

```
layout: hello
title: world 标题
date: 2016-11-27 17:53:01 建立日期
updated: 更新日期
tags: 与主题文件中的/tags中的名称相对于
author: 作者 
img: /medias/banner/7.jpg 
coverImg: /medias/banner/7.jpg 
top: true  // 置顶
cover: true  // 是否允许复制
toc: true 
password: 5f15b28ffe43f8be4f239bdd9b69af9d80dbafcb20a5f0df5d1677a120ae9110 
mathjax: true 
summary: 这是你自定义的文章摘要内容，如果这个属性有值，文章卡片摘要就显示这段文字，否则程序会自动截取文章的部分内容作为摘要 
categories: - 分类（不适用于分页）
```



#### `layout`布局md文件的创建

------

**1.2.4.1 post**

当你每一次使用代码

```
hexo new XXX
```

它其实默认使用的是`post`这个布局，也就是在`source`文件夹下的`_post`里面。

`Hexo`有三种默认布局：`post`、`page`和`draft`，它们分别对应不同的路径，而您自定义的其他布局和`post`相同，都将储存到`source/_posts`文件夹。

而new这个命令其实是：

```
hexo new [layout] <title>
```

只不过这个`layout`默认是`post`罢了。

**1.2.4.2 page**

如果你想另起一页，那么可以使用

``` 
hexo new page newpage
```

系统会自动给你在`source`文件夹下创建一个`newpage`文件夹，以及`newpage`文件夹中的`index.md`，这样你访问的`newpage`对应的链接就是http://xxx.xxx/newpage

**1.2.4.3 draft**

`draft`是草稿的意思，也就是你如果想写文章，又不希望被看到，那么可以

```
hexo new draft newdraft
```

这样会在`source/_draft`中新建一个`newdraft.md`文件，如果你的草稿文件写的过程中，想要预览一下，那么可以使用

```
hexo server --draft
```

如果你的草稿文件写完了，想要发表到`post`中，

```bash
hexo publish draft newdraft
```

就会自动把`newdraft.md`发送到`post`中。