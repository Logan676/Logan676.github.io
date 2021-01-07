title: Hexo如何在线可视化写博客
author: 书虫
tags:
  - Demo
categories: []
date: 2021-01-06 21:08:00
---
可以试试这款插件`hexo-admin`
能够管理文章，添加分类和标签，也可以一键部署到pages现在图片可以实现粘贴上传，原插件为保存到`source/images`目录下,部署博客时同时上传。
我已修改上传图片到七牛,请参考[hexo-admin-qiniu](根据hexo-admin@2.1.0进行修改，添加粘贴图片上传至七牛)

草稿
刚刚提到了 Hexo 的一种特殊布局：draft，这种布局在建立时会被保存到 source/_drafts 文件夹，您可通过 publish 命令将草稿移动到 source/_posts 文件夹，该命令的使用方式与 new 十分类似，您也可在命令中指定 layout 来指定布局。


草稿默认不会显示在页面中，您可在执行时加上 --draft 参数，或是把 render_drafts 参数设为 true 来预览草稿。

模版（Scaffold）
在新建文章时，Hexo 会根据 scaffolds 文件夹内相对应的文件来建立文件，例如：

$ hexo new photo "My Gallery"
在执行这行指令时，Hexo 会尝试在 scaffolds 文件夹中寻找 photo.md，并根据其内容建立文章，以下是您可以在模版中使用的变量：

变量	描述
layout	布局
title	标题
date	文件建立日期
支持的格式
Hexo 支持以任何格式书写文章，只要安装了相应的渲染插件。

例如，Hexo 默认安装了 hexo-renderer-marked 和 hexo-renderer-ejs，因此你不仅可以用 Markdown 写作，你还可以用 EJS 写作。如果你安装了 hexo-renderer-pug，你甚至可以用 Pug 模板语言书写文章。

只需要将文章的扩展名从 md 改成 ejs，Hexo 就会使用 hexo-renderer-ejs 渲染这个文件，其他格式同理。