# Web-tags notes

## body-elements

|tag|meaning
|:--|:--|
header|定义文档、或文档一部份区域的页眉；通常作为介绍内容，或者导航链接栏容器。`不能嵌套`、`h5新标签`
div|定义文档中的区域块。浏览器默认会在前后放置一个换行符。搭配 CSS 使用。`h5不支持align属性`
|ul|无序列表，通常和 li 一起使用；相对应的 ol 为有序列表|
|li|在列表(ol, ul)和菜单列表(menu)使用，定义列表项。
|form|表单，块级元素，前后产生折行。可添加属性：<hr>`accept`( `MIME_type` )：HTML 5不支持；<br>`accept-charset`( `charset_list` )：规定服务器可处理的表单数据字符集。
|input|可作为 `按钮` 、 `复选框` 、 `输入字段` 等交互控件。形式为 `<input type="value">`<hr>`type`可选：<br>`button`：定义可点击按钮（通常绑定 JS 脚本）；<br>`checkbox`：复选框；<br>`file`：输入字段和 `浏览` 按钮，供文件上传。<br>`hidden`：隐藏的输入字段；<br>`image`：图像形式的提交按钮；<br>`password`：密码字段，字符会被掩码；<br>`radio`：单选按钮；<br>`reset`：定义重置按钮。清楚表单中所有数据；<br>`submit`：提交按钮，将表单数据发送到服务器；<br>`text`：单行输入字段，默认宽度 20 字符。|
!important|提升指定样式规则的应用优先权；IE6 以下需要显式声明。
onerror|事件。在文档或图像加载发生错误时触发，调用该事件句柄。<br>语法：`onerror="SomeJavaScriptCode"`，参数为必须，规定该事件发生时执行的JavaSript。<br>`支持<img>,<object>,<style>`

## Meta-elements

> meta 元素用于指定网页描述、关键词、作者等，不显示，但会被浏览器解析

| elm        | effect                                      |
| :--------- | :------------------------------------------ |
| charset    | 定义文档字符编码                            |
| content    | 定义 htttp-equiv 或 name 属性相关的信息。   |
| http-equiv | 把 content 属性关联到 http 头部。           |
| name       | 把 content 属性关联到一个名称。             |
| scheme     | 定义用于翻译 content 属性的格式。`h5不支持` |

## 属性

|属性名|含义作用|
|:--|:---|
min-width|定义元素的最小宽度，即窗口宽度小于此值会自动出现横向滚动条
position|提供` static``relative``absolute``fixed `四个标签；<br>`static`：默认值，无定位效果，会忽略`top`,`left`,`z-index`等声明；<br>`relative`：相对与原来位置偏移一个值，无其它效果；<br>`absolute`：相对于父级包含块定位；<br>`fixed`：相对于整个窗口定位。
overflow|内容溢出时的选项；<br>`visible`：不裁剪内容，可能会显示在内容框之外。<br>`hidden`：只裁剪内容；<br>`scroll`：裁剪并提供滚动条；<br>`auto`：若溢出则滚动；<br>`no-display`：内容不合适内容框则删除整个框；<br>`no-content`：内容不合适内容框则隐藏内容。
Z-index|堆叠优先级，可为负值，默认为`auto`，与父元素相等；无父元素则为 0。`inherit`：从父元素继承值。<br>**_也可设定具体数值规定优先级，数值越高则离用户越近。_**
|zoom|根据 @viewport 来初始化一个缩放因数。可设置小数`(大于0)`或百分比`(非负百分比)`，`1.0`和`100%`表示不缩放
|margin|可设置`1-4`个值。总是从`上`开始顺时针指明，若某一方向缺省，则合并到相对方向的数值。
|text-decoration|文本修饰。<br>`none`无任何修饰；<br>`overline` ,`line-through` ,`underline`分别为上划线、删除线、下划线；<br>`blink`闪烁文本；<br>`inherit`继承父元素属性
usemap|属于标签 `<img>` 的属性，将图像定义为客户端图像映射（带有可点击区域的图像），与` <map> `的 name 或 id 属性关联，建立二者之间的关系
autocomplete|自动完成表单，即表单记忆功能，可设置` off `或` on `
cursor|鼠标移动到元素上时显示的样式。常用：<br>`Pointer`：可点击；<br>`wait`：加载图标；<br>`Defalut`：默认光标；<br>`Move`：移动图标；<br>`help`：帮助图标；
padding|内边距。数值设定同 `margin` ；默认值为0。可以设定 `auto`,`*length*`,`%`,`inherit`；

## 选择器重点

|样式|注意项|
|:---|:---|
:first-child|指定首个元素的属性。<br>`p:first-child i{}`指定`<p>`中的 **_每个_** `<i>`元素赋予属性；<br>`li:first-child{}`指定 **_每一个_**包含`<li>`的元素块中的 **_第一个_** `<li>`都被赋予属性；<br>`ul>:first-child{}`指定 **_每一个_** `<ul>`包含的 **_第一个_** 元素赋予属性。
