# Web-tags notes

## body-elements


tag|meaning
:--:|:---
header|定义文档、或文档一部份区域的页眉；通常作为介绍内容，或者导航链接栏容器。```不能嵌套```、```h5新标签```
div|定义文档中的区域块。浏览器默认会在前后放置一个换行符。搭配CSS使用。```h5不支持align属性```
ul|无序列表，通常和 li 一起使用；相对应的 ol 为有序列表。
li|在列表(ol, ul)和菜单列表(menu)使用，定义列表项。

## Meta-elements

> meta元素用于指定网页描述、关键词、作者等，不显示，但会被浏览器解析

elm|effect
:--:|:---
charset|定义文档字符编码
content|定义htttp-equiv或name属性相关的信息。
http-equiv|把content属性关联到http头部。
name|把content属性关联到一个名称。
scheme|定义用于翻译content属性的格式。```h5不支持```
