---
title: 主题 TKL 采坑及进阶
date: 2020-10-25 16:15
tags: 
- HEXO
- TKL
categories: 博客搭建
---

### 1.初始化

TKL主题的初始化到本地启动，根据 [TKL 的 README.md](https://github.com/SuperKieran/TKL) 操作即可

### 2.更换背景图

1. 图片放在 `themes\TKL\source\img` 下
2. 更新背景图指向：`themes\TKL\_config.yml` -> `cover: /img/bg_img.jpg` 改成你的图片

### 3.更换logo

同背景图

### 4.更换网页小图标

1. 将自己的图标文件放在 `themes\TKL\source\img` 下，不一定非得 `.ico` 格式才可以
2. 全局查找 `favicon.ico` 的使用处，替换为你想要的图标

### 5.右侧导航栏显示 TAGS

你会发现按照 [TKL 的 README.md](https://github.com/SuperKieran/TKL) 所提示的开启 `TAG`和`CATEGORY` 后，只有 `CATEGORY` 出来了。

- 原因：
    TKL 原代码有误
- 解决：
    `/themes/TKL\layout/_partial/header.ejs` 中 `<!-- Dropdown Menu -->` 的下方合适位置添加代码：
    > 其实就是修改了 该文件下 Categories 相关代码

        <!-- tags -->
        <% if (site.tags.length){ %>
        <li>
            <a class="sb-toggle-submenu">Tags<span class="sb-caret"></span></a>
            <ul class="sb-submenu">
                <% site.tags.sort('name').each(function(item){ %>
                <li><a href="<%- config.root %><%- item.path %>" class="animsition-link"><%= item.name %><small>(<%= item.posts.length %>)</small></a></li>
                <% }); %>
            </ul>
        </li>
        <% } %>

### 6.查找功能

按照 TKL 所提示的 [hexo-generator-search-zip](https://github.com/SuperKieran/hexo-generator-search-zip) 搞完后，public中的 search 相关文件是有了，但是功能怎么出来呢？

很简单，那是因为你没注意看他这个 README.MD 中的  [Guide](https://go.kieran.top/post/45/), 这里边也没什么，就是刚刚做的那些完成后，还有一个 TKL 主题的配置文件要改的，在主题下的 `_config.yml` 修改 `local_search.enable` 为 `true` 就好了

### 7.LINKS

待探索 ···

### 8.About

待探索 ···

### 9.RSS

待探索 ···

### 10.评论功能

待探索 ···

[TKL作者的blog](https://go.kieran.top/)，以示瞻仰

>祝你生活愉快
