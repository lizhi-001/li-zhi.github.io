---
comments: true
---

# Material for mkdocs + github + giscus 博客搭建

整个博客的搭建可以分为四个部分：框架构建，主题修改，添加评论区和添加插件。

下面罗列每个部分参考的主要资料。

## 框架构建
B站up主我不是小杰的博客搭建教程[博客搭建教程](https://www.bilibili.com/video/BV1hL4y1w72r/?vd_source=df948814c39b99d73ca9c51827e7d8c9)及[相关文档](https://yang-xijie.github.io/BLOG/Markdown/mkdocs-site/)

搭建前需要一些git和linux的知识基础，这个up主也都有相关的教学视频，可以一一学习

## 主题修改
这部分主要参考一个博客的[主题修改记录](https://derrors.github.io/%E9%85%8D%E7%BD%AE%20YAML%20%E6%96%87%E4%BB%B6/)和material for mkdocs的[官方设置文档](https://squidfunk.github.io/mkdocs-material/setup/)

## 添加评论区
使用Giscus应用来配置网页的评论区，主要参考另一个博客的[评论区添加教程](https://yliu-fe.github.io/Techs/Notes%20for%20Mkdocs/Comment%20with%20Giscus/)

## 添加插件
关联文档的github最后更新日期，步骤参考[官网设置](https://squidfunk.github.io/mkdocs-material/setup/adding-a-git-repository/#document-dates)

需要注意的是，PublishMySite.yml文件中需要添加以下代码
```yaml
jobs: # 工作流的具体内容
  deploy:
      - run: pip install mkdocs-git-revision-date-localized-plugin # 使用pip包管理工具安装显示更新日期的支持
```
同时，在mkdocs.yml中设置是否显示生成日期，显示格式等
```yaml
plugins:
  - git-revision-date-localized:   # 显示更新时间
      enable_creation_date: false  # 显示创建时间
      type: date                   # 显示格式
```

---

每个流程按照对应的资料一步一步执行，基本不会出错，每份资料对于细节的把握都做的非常到位，感谢互联网和这些分享者。

得益于不同个体的分享精神和对细节的梳理，这个博客的构建可以说是在很短的时间内完成的。希望这个博客也能传承这种精神，不断输出足够细致、便于理解的内容。
