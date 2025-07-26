+++
draft = false
date = 2025-07-26T17:01:04+08:00
title = "Hugo Archetypes 原型模板"
authors = ["RONGHUA LI"]
tags = ["hugo"]
categories = ["前端技术"]
series = ["Blog养成记"]

+++

#  原型是什么?

**原型**（Archetypes） 是项目的原型目录内的内容模板文件，这些模板包含预定义的**前言设定**， 同时也可以是**内容配置目录**。

在使用 `hugo new`命令创建新内容时，会寻找项目中最合适的原型模板。如果项目中不包含任何原型文件，命令也会查找theme主题目录中原型文件。

```powershell
hugo new posts/my-first-post.md
```

上面命令创建了一个新的内容文件在`content/posts/my-first-post.md`，创建中使用了下面原型模板中的第一个：

1. `archetypes/posts.md`
2. `archetypes/default.md`
3. `themes/my-theme/archetypes/posts.md`
4. `themes/my-theme/archetypes/default.md`

> 最后两个文件仅在使用了主题并且创建新内容的`hugo new`命令使用的路径包含`my-theme`这个主题名称。

# 基于目录的原型

从Hugo版本`0.49`开始，可以使用完整的目录作为原型模板。如下面这个原型目录:

```
archetypes
├── default.md
└── blogs
	└──Blog养成记
	    └── index.md
```

```markdown
draft = true
date = {{ .Date }}
title = "{{ replace .Name "-" " " | title }}"
authors = [""]
tags = [""]
categories = [""]
series = [""]
```

```powershell
hugo new --kind /blogs/Blog养成记 content/blogs/Blog养成记/"Hugo Archetypes 原型模板"
```

基于上面模板目录，这个命令 会在`/content/blogs/Blog养成记/"Hugo Archetypes 原型模板"`目录创建同`/blogs/Blog养成记` 原型目录相同结构的文件集合。



参考：[Hugo框架中文文档 Hugo Archetypes 原型模板 - Andbible](https://www.andbible.com/post/hugo-content-management-archetypes/)
