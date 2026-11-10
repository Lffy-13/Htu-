# HTML学习笔记

## 一、HTML后缀

文档后缀为`.html`
（最推荐），也可以使用`.htm`

## 二、HTML标签

### 1、标签

又称 **元素**，是html的基本组成单位。

### 2、标签分为

**双标签** 和 **单标签**（绝大多数是双标签。

### 3、大小写

标签名不区分大小写，但小写更规范，更推荐。

### 4、双标签

><标签名>+标签体+</标签名>

前面的<标签名>是起始标签，后面的</标签名>是结束标签

示范

```html
<marquee> 我爱学习 </marquee>
```

### 5、单标签

><单标签/>

“/”可省略

示例：

```html
<input>
```

### 6、标签之间的关系

并列关系、嵌套关系，可以用```tab```进行缩进：

```html
<marquee>
    我爱学习
    <input>
</marquee>
<input>
```

## 三、HTML标签属性

### 1、作用

用于给标签提供 **附加信息**。

### 2、可以写在

**起始标签**或**单标签**中，形式如下：
><**标签名** 属性名="属性值" 属性名="属性值">

### 3、特殊属性

只有属性名，没有属性值。

```html
<input disabled>
```

### 4、tips

- 不同的标签，有不同的属性；也有一些通用属性。
- 属性名、属性值都是规定好的，不能乱写。
- 标签中不要出现同名属性，否则后写的会失效。例如：

```html
<input type="text" type="password">
```

## 四、HTML基本结构

### 1、查看某段结构的具体代码

鼠标右键，选择“检查”。

### 2、【检查】和【查看网页源代码】的区别

- 【查看网页源代码】看到的是程序员编写的源代码。
- 【检查】看到的是：经过浏览器处理后的源代码。
- 日常开发中【检查】用的多。

### 3、网页的 **基本结构**

- 想要呈现在网页中的内容写在```body```标签中。
- ```head``` 标签中的内容不会出现在网页中。
- ```head```标签中的```title```标签可以指定网页的标题。

## 五、HTML注释

### 1、特点

注释的内容会被浏览器所忽略，不会呈现到页面中，源代码中可以看见。

### 2、作用

对代码进行解释和说明。

### 3、注释不可以嵌套

- 写法：

```html
<!--下面的文字只能滚动一次-->
<marquee loop="1">我爱学习</marquee>
```

- 错误示例：

```html
<!--
我是一段注释
<!-- 我是一段注释 -->
-->
```

## 六、HTML文档声明

### 1、文档声明作用

告诉浏览器当前网页的版本。

### 3、写法

新写法：HTML5的写法

```html
<!DOCTYPE html>
```

### 4、注意

文档声明，必须在第一行，且在```html```标签的外侧。

## 七、HTML字符编码

### 1、计算机对数据的操作

- 存储时，对数据进行：**编码**
- 读取时，对数据进行：**解码**

### 2、规范

编码、解码，会遵循一定的规范——**字符集**。

### 3、常见的字符集（了解即可）

>- **ASCII** ：大写字母、小写字母、数字、一些符号，共计128个。
>- **ISO 8859-1**：在 ASCII 基础上，扩充了一些希腊字符等，共计是256个。
>- **GB2312** ：继续扩充，收录了 6763 个常用汉字、682个字符。
>- **GBK** ：收录了的汉字和符号达到 20000+ ，支持繁体中文。
>- **UTF-8** ：万国码，包含世界上所有语言的：所有文字与符号。—— 很常用。

### 4、使用原则

（1）存储时，务必采用合适的字符编码。

否则：无法储存，数据会丢失

推荐：UTF-8

（2）存储时采用哪种方式编码，读取时就必须采用相同方式解码。

否则：数据能呈现，但会乱码。

### 5、总结

- 平时编写代码时，统一采用```UFT-8```编码（最稳妥）。
- 为了让浏览器在渲染
  ```html```时不犯错误，可以通过```meta```配合标签```charset```属性指定字符编码。

```html
<head>
    <meta charset="UFT-8"/>
</head>
```

## 八、HTML设置语言

### 1、主要作用

- 让浏览器显示对应的翻译提示。
- 有利于搜索引擎优化。

### 2、具体写法

```html
<html lang="zh-CN">
```

### 3、扩展（了解即可）

```lang```属性的编写原则

>1. 第一种写法（ 语言-国家/地区 ），例如：
>
>- zh-CN ：中文-中国大陆（简体中文）
>- zh-TW ：中文-中国台湾（繁体中文）
>- zh ：中文
>- en-US ：英语-美国
>- en-GB ：英语-英国
>
>2.第二种写法（ 语言—具体种类）已不推荐使用，例如：
>
>- zh-Hans ：中文—简体
>- zh-Hant ：中文—繁体
>
>3.W3School 上的说明：[《语言代码参考手册》](https://www.w3school.com.cn/tags/html_ref_language_codes.asp)、[《国家/地区代码参考手册》](https://www.w3school.com.cn/tags/html_ref_country_codes.asp)
>4. W3C官网上的说明:[《Language tags in HTML》](https://www.w3.org/International/articles/language-tags/)

## 九、HTML标准结构

### 1、HTML标准结构如下

```html
<!DOCTYPE html>
<html lang="zh-CN">
    <head>
        <meta charset="UFT-8">
        <title>我是一个标题</title>
    </head>
    <body>
        主体
    </body>
</html>
```

### 2、快速生成标准结构

输入`!`

>- 生成的结构中，有meta标签，此时暂时用不到，可以先删掉。
>- VScode的内置插件emmet可以对生成结构的属性进行定制。

### 3、图标

在存放代码的文件夹中，存放一个`favicon.ico`图片，可配置网站图标。

## 十、HTML基础

### 1、开发者文档

- [W3C官网](www.w3c.org)
- [W3School](www.w3school.com.cn)
- [MDN](developer.mozilla.org)——平时用的最多。

### 2、排版标签

|标签名|标签含义|单/双标签|
|:--:|:--|:--:|
|h1~h6|标题|双|
|p|段落|双|
|div|没有任何含义，用于整体管理|双|

- h1~h6不能互相嵌套

### 3、语义化标签

#### 概念

用特定的标签，去表达特定的含义。

#### 原则

标签的默认效果不重要，语义最重要。

#### 优势

- 代码的可读性强，结构清晰
- 有利于有利于SEO（搜索引擎优化）
- 方便设备解析（屏幕阅读器、盲人阅读器等）

### 4、块级元素 与 行内元素

#### 块级元素

独占一行（排版标签都是块级元素）

#### 行内元素

不单独占一行

#### 使用原则

> - 块级元素中<font  color="red">能</font>写 **块级元素** 和 **行内元素**
>-行内元素<font color="red">能</font>写 **行内元素**，但<font color="red">不能</font>写 **块级元素**
>-p中不要写块级元素

### 5、常用的文本标签

#### 用途

用于包裹词汇、短语等

#### 位置

通常写在排版标签里面

>排版标签更宏观，通常处理大段文字；文本标签更微观，一般都是行内元素

4、以下都是双标签

|标签名|标签语义|
|:--:|:--|
|span|没有语义，包裹短语的常用容器|
|em|要着重阅读的内容|
|strong|十分重要的内容，语气比`em`要强|

>类比：`div`是大包装袋，`span`是小包装袋

### 5、不常用的文本标签

|标签名|标签语义|
|:--:|:--|
|cite|作品标题|
|dfn|特殊术语或专属名词|
|del,ins|删除的文本，插入的文本|
|sub,sup|下标文字，上标文字|
|code|一段代码|
|samp|从正常的上下文中将某些内容提取出来|
|kbd|键盘文本，表示文本是通过键盘输入的，经常用在计算机相关手册中|
|abbr|缩写，最好配合`title`属性|
|bdo|更换文本方向，要配合`dir`属性，可选值：`ltr`（默认值）、`rtl`|
|var|标记变量，可以与`code`标签一起使用|
|small|附属细则——很少使用|
|b|摘要中的关键字、评论中的产品名称——很少使用|
|i|现多用于呈现字体图标|
|u|与正常内容有反差文本例如：错的单词、不合适的描述等。——很少使用|
|q|短引用——很少使用|
|blockquote|长引用——很少使用|
|address|地址信息|

- 以上均为双标签
- `blockquote`和`address`是块级元素
注：
1）不常用的文本标签，编码时不用过于纠结
2）语义感不强的标签很少使用，例如：
`small`、`b`、`u`、`q`、`blockquote`
3）记住重要的、语义感强的标签即可，例如：
`h1~h6`、`p`、`div`、`em`、`strong`、`span`

### 6、图片标签

#### 1、基本使用

标签名：`img`
标签语义：图片
>常用属性：
>`src`:图片路径（图片地址）——图片的具体位置
>`alt`:图片描述
>`width`:图片宽度，单位是像素。
例如：`200px`或`200`
`height`：图片高度，单位是像素

注：

（1） 尽量不同时修改图片的宽和高，可能会导致比例失调
（2）`alt`属性的作用：

- 搜索引擎通过`alt`属性，得知图片的内容。——最主要的内容
- 当图片无法展示的时候，有些浏览器会呈现`alt`属性的值。
- 盲人阅读器会朗读`alt`属性的值

#### 2、路径的分类

##### 相对路径

以<font color="red">当前位置</font>作为参考点，去建立路径

|符号|含义|
|:--:|:--:|
|./|同级|
|/|下一级|
|../|上一级|

注意点：

- 相对路径的`./`可以省略不写
- 相对路径以来的是当前位置，后期若调整了文件位置，那么文件中的路径也要修改。
  
##### 绝对路径

以<font color="red">根位置</font>作为参考点，去建立路径。

- 本地绝对路径：从盘符出发（E:/demo1/demo2/xxx.jpd），更换设备后有很大局限性，很少使用并且不推荐。
- 网络绝对路径：新标签页中打开图片，复制链接即可（链接必须是图片），但若服务器开启了防盗链，会造成图片引入失败。

#### 3、常见图片格式

##### `jpg`格式

- 概述：扩展名为`.jpg`或`.jpeg`，是一种有损的压缩格式（把肉眼不容易观察出来的细节丢弃了）
- 主要特点：<font color="green">支持的颜色丰富、占用空间较小</font>、不支持透明背景、不支持动态图。
- 使用场景：对图片细节<font color="blue">没有极高要求</font>的场景，例如：
  网站的产品宣传图等。——该格式网页中很常见

##### `png`格式

- 概述：扩展名为`.png`，是一种无损的压缩格式，能够高质量地保存图片
- 主要特点：<font color="green">支持的颜色丰富、支持透明背景</font>、占用空间略大、不支持动态图。
- 使用场景：(1)想让图片有透明背景；(2)想更高质量地呈现图片

##### `bmp`格式

- 概述：扩展名为`.bmp`,不进行压缩的一种格式，在最大程度上保存图片更多的细节。
- 主要特点：<font color="green">支持的颜色丰富、保留的细节更多</font>、占用空间极大、不支持透明背景、不支持动态图
- 使用场景：对图片细节要求<font color="blue">极高</font>的场景。（网页中很少使用）

##### `gif`格式

- 概述：扩展名为`.gif`，金支持256种颜色，色彩呈现不是很完整
- 主要特点：支持的颜色较少、<font color="green">支持<font color="red">简单</font>透明背景、支持动态图</font>
- 使用场景：网页中的动态图片

##### `webp`格式

- 概述：扩展名为 `.webp`，谷歌推出的一种格式，专门用来在网页中呈现图片。
- 主要特点：具备上述几种格式的优点，但<font color="green">兼容性不太好，</font>一旦使用务必要解决兼容性问题。
- 使用场景：网页中的各种图片

##### `base64`格式

- 本质：一串特殊的文本，要通过浏览器打开，传统看图应用通常无法打开。
- 原理：把图片进行 `base64` 编码，形成一串文本。
- 如何生成：靠一些工具或网站。
- 如何使用：直接作为 `img` 标签的 `src` 属性的值即可，并且不受文件位置的影响。
- 使用场景：一些较小的图片，或者需要和网页一起加载的图片。

### 7、超链接

#### 主要作用

从当前页面进行跳转。

#### 可以实现

- 跳转到指定页面
- 跳转到指定文件（也可触发下载）
- 跳到锚点位置
- 唤起指定应用

**标签名**: a (双标签)

**标签语义**：超链接

**常用属性**：
> href ： 指定要跳转到的具体目标。
target ： 控制跳转时如何打开页面，常用值如下:
_self ：在本窗口打开。
_blank ：在新窗口打开。
id ： 元素的唯一 标识，可用于设置锚点。
name ： 元素的名字，写在 a 标签中，也能设置锚点。

#### 跳转到页面

```html
<!-- 跳转到其他页 -->
<a href="https://www.jd.com/" target="_blank">去京东</a>

<!-- 跳转本地网页 -->
<a href="../ddd.html" target="_self">去看作业</a>
```

注意：

- 代码中的**多个空格**、**多个回车**，都会被浏览器解析成一个空格
- 虽然`a`是行内元素，但`a`元素可以包裹除它自身外的任何元素
  
#### 跳转到文件

```html
<!-- 浏览器能直接打开的文件 -->
<a href="./resource/自拍.jpg">看自拍</a>
<a href="./resource/小电影.mp4">看小电影</a>
<a href="./resource/小姐姐.gif">看小姐姐</a>
<a href="./resource/如何一夜暴富.pdf">点我一夜暴富</a>

<!-- 浏览器不能打开的文件，会自动触发下载 -->
<a href="./rensource/内部资源.zip">内部资源</a>

 <!-- 强制触发下载 -->
<a href="./resource/小电影.mp4" download="电影片段.mp4">下载电影</a>

```

注：

- 若浏览器无法打开文件，则会引导用户下载
- 若想强制触发下载，用download属性，属性值即为下载文件的名称。

#### 跳转到锚点

锚点——网页中的一个标记点。

##### 具体使用方式

1、设置锚点

```html
<!-- 第一种方式:a标签配合name属性 -->
<a name="test1"></a>

 <!-- 第二种方式：其他标签配合id属性 -->
<h2 id="test2">我是一个位置</h2>

```

注意：

- 具有`href`属性的a标签是**超链接**，具有`name`属性的`a`标签是**锚点**。
- `name`和`id`都是区分大小写的，且`id`最好别是数字开头。

2、跳转锚点

```html
<!-- 跳转到test1锚点 -->
<a href="#test1">去test1锚点</a>
<!-- 跳到本页面顶部 -->
 <a href="#">回到顶部</a>
 <!-- 跳转到其他页面锚点 -->
  <a href="demo.html#test1">去demo.html页面的test1锚点</a>
<!-- 刷新本页面   -->
 <a href="">刷新本页面</a>
 <!-- 执行一段js，如果还不知道执行什么，可以留空，javascript:; -->
  <a href="javascript:alert(1);">点我弹窗</a>

```

#### 唤起指定应用

通过`a`标签，可以唤起设备应用程序。

```html
<!-- 唤起设备拨号 -->
 <a href="tel:10010">电话联系</a>
 <!-- 唤起设备发送邮件 -->
  <a href="mailto:10010@qq.com">邮件联系</a>
  <!-- 唤起设备发送短信 -->
 <a href="sms:10086">短信联系</a>
 ```

#### 超文本的真正含义

是一种组织信息的方式，通过超链接将不同空间的文字、图片、等各种信息组织在一起，能从当前阅读的内容，跳转到超链接所指的内容。

### 8、列表

#### 有序列表(Ordered list)

##### 概念

有顺序或侧重顺序的列表

```html
<h2>把大象放进冰箱要几步</h2>
<ol>
    <li>把冰箱打开</li>
    <li>把大象放进去</li>
    <li>把冰箱门关上</li>
</ol>
```

#### 无序列表(Unorderde list)

##### 概念

无顺序或不侧重顺序的列表

```html
<h2>我想去的几个城市</h2>
<ul>
    <li>成都</li>
    <li>上海</li>
</ul>
```

#### 自定义列表(Definition list)

包含 <font color="red">术语名称</font> (`dt`) 和 <font color="red">术语描述</font> (`dd`) 的列表。（术语名称和术语描述可以有多个）

```html
<h2>如何更好得学习</h2>
    <dl>
        <dt>做好笔记</dt>
        <dd>笔记是我们以后复习的一个抓手</dd>
        <dt>多加练习</dt>
        <dd>只有敲出来的代码才是自己的</dd>
        <dt>别怕出错</dt>
        <dd>错很正常的，改正后记住，就是经验</dd>
    </dl>
```

#### 嵌套列表

列表中的某项内容，又包含一个列表。（嵌套时，务必把解构写完整）

```html
<h2>我想去的几个城市</h2>
<ul>
    <li>成都</li>
    <li>
        <span>上海</span>
        <ul>
            <li>外滩</li>
            <li>杜莎夫人蜡像馆</li>
            <li>
                <a href="https://www.opg.cn/">东方明珠</a>
            </li>
            <li>迪士尼乐园</li>
        </ul>
    </li>
    <li>西安</li>
    <li>武汉</li>
</ul>

```

> `li`标签最好写在`ul`或`ol`中，不要单独使用。

### 9、表格

#### 基本结构

##### 组成

一个完整的表格由：**表格标题**、**表格头部**、**表格主体**、**表格脚注**，四部分组成。

##### 涉及标签

`table`:表格
`caption`:表格标题
`thrad`:表格头部
`tbody`:表格主题
`tfoot`:表格脚注
`tr`:每一行
`th`、`td`:每一个单元格（表格头部中用`th`，表格主体、表格脚注中用`td`）
![表格结构示意图](image.png)

#### 常用属性

| 标签名 | 标签语义 | 常用属性 | 单/双标签 |
| ---- | ---- | ---- | ---- |
| `table` | 表格 | `width`：设置表格宽度。<br>`height`：设置表格最小高度，表格最终高度可能比设置的值大。<br>`border`：设置表格边框宽度。<br>`cellspacing`：设置单元格之间的间距。 | 双 |
| `thead` | 表格头部 | `height`：设置表格头部高度。<br>`align`：设置单元格的水平对齐方式，可选值如下：<br>1. `left`：左对齐<br>2. `center`：中间对齐<br>3. `right`：右对齐<br>`valign`：设置单元格的垂直对齐方式，可选值如下：<br>1.`top`：顶部对齐<br>2. `middle`：中间对齐<br>3. `bottom`：底部对齐 | 双 |
| `tbody` | 表格主体 | 常用属性与 `thead` 相同。 | 双 |
| `tr` | 行 | 常用属性与 `thead` 相同。 | 双 |
| `tfoot` | 表格脚注 | 常用属性与 `thead` 相同。 | 双 |
| `td` | 普通单元格 | `width`：设置单元格的宽度，同列所有单元格全都受影响。<br>`height`：设置单元格的高度，同行所有单元格全都受影响。<br>`align`：设置单元格的水平对齐方式。<br>`valign`：设置单元格的垂直对齐方式。<br>`rowspan`：指定要跨的行数。<br>colspan：指定要跨的列数。 | 双 |
| `th` | 表头单元格 | 常用属性与 `td` 相同。 | 双 |

注意：

- <table>元素的border属性可以控制表格边框，但border值的大小，并不控制单元格边框的宽度，只能控制表格最外侧边框的宽度。
- 默认情况下，每列的宽度，得到这一列单元格最长的那个文字。
- 某个th或td设置了宽度/高度后，他们所在的那一列/行的宽度/高度就确定了。
  
#### 跨行与跨列

##### 跨行跨列

`rowspan`：指定要跨的行数。
`colspan`：指定要跨的列数。

### 10、常用标签补充

`br`：换行（单标签）
`hr`：分隔（单标签）
`pre`：按原文显示，一般用于在页面中嵌入大段代码（双标签）

注意：

- 不要用`<br>`来增加文本之间的行间隔，应用`<p>`元素，或后面即将学到的`CSS margin`属性
- <hr>的语义是分隔，如果不想要语义，只是想画一条水平线，那么应当用`CSS`完成

### 表单

一个包含交互的区域，用于收集用户提供的数据

#### 基本结构

|标签名|标签语义|常用属性|单/双标签|
|---|---|---|---|
|`form`|表单|`action`：用于指定表单的提交地址 （需要与后端人员沟通后确定）。 <br>`target`：用于控制表单提交后，如何打开页面，常用值如下：<br>&emsp;`_self`：在本窗口打开。<br>&emsp;`_blank`：在新窗口中打开。<br>`method`：用于控制表单的提交方式（暂了解）。|双|
|`input`|输入框|`type`：设置输入框的类型，目前用到的值是`text`，表示普通文本<br>`name`：用于指定提交数据的名字（需要与后端人员沟通后确认）|单|
|`botton`|按钮|暂不涉及|双|

#### 常用表单控件

##### 文本输入框

```html
<input type="text">
```

常用属性如下：

- `name` 属性：数据的名称。
- `value`属性：输入框的默认输入值
- `maxlength`属性：输入框最大可输入长度

##### 密码输入框

```html
<input type="password">
```

常用属性如下：

- `name`属性：数据的名称
- `vakue`属性：输入框的默认输入值（在密码输入框中一般不用，无意义）
- `maxkength`属性：输入框最大可输入长度

##### 单选框

```html
<input type="radio" name="sex" value="female">女
<input type="radio" name="sex" value="male">男
```

常用属性如下：

- `name`属性：数据的名称（想要单选效果，多个radio 的name属性值要保持一致
- `value`属性：提交的数据值（单选框必须写，不写就收集不了数据了）
- `checked`属性：让该单选按钮默认选中

##### 复选框

```html
<input type="checkbox" name="hobby" value="smoke">抽烟
<input type="checkbox" name="hobby" value="drink">喝酒
<input type="checkbox" name="hobby" value="perm">烫头
```

常用属性如下：

- `name`：数据的名称
- `value`：提交的数据值（复选框必须写，不写就收集不了数据了）
- `checked`：让该复选框默认选中

##### 隐藏域

```html
<input type="hidden" name="tag" value="100">
```

用户不可见的一个输入区域，作用是：
提交表单的时候，携带一些固定的数据

- `name` 属性：指定数据的名称。
- `value` 属性：指定的是真正提交的数据。

##### 提交按钮

```html
<input type="submit" value="点我提交表单">
<button>点我提交表单</button>
```

注意：

- `button` 标签 `type` 属性的默认值是 submit
- <font color="red">`button` 不要指定 `name` 属性</font>
- `input` 标签编写的按钮，使用 `value` 属性指定按钮文字

##### 重置按钮

```html
<input type="reset" value="点我重置">
<button type="reset">点我重置</button>
```

注意:

- `button` 不要指定 `name` 属性
- `input` 标签编写的按钮,使用 `value` 属性指定按钮文字

##### 普通按钮

```html
<input type="button" value="普通按钮">
<button type="button">普通按钮</button>
```

注意：

- 普通按钮的`type`值为`button`，若不写`type`值是`submit`会引起表单的提交

##### 文本域

```html
<textarea name="msg" rows="22" cols="3">我是文本域</textarea>
```

常用属性如下：

- `rows`属性：指定默认显示的行数，会影响文本域的高度
- `cols`属性：指定默认显示的列数，会影响文本域的宽度
- 不能编写`type`属性，其他属性，与普通文本输入框一致

##### 下拉框

```html
<select name="form">
    <option value="黑">黑龙江</option>
    <option value="辽">辽宁</option>
    <option value="吉">吉林</option>
    <option value="粤" selected>广东</option>
</select>
```

常用属性及注意事项:

- `name` 属性:指定数据名称
- `option` 标签设置 `value` 属性,如果没有 `value` 属性,提交的数据是 `option` 中间的文字;如果设置了 `value` 属性,提交的数据就是 `value` 的值(建议设置 `value` 属性)
- `option` 标签设置了 `selected` 属性,表示默认选中

#### 禁用表单控件

给表单控件的标签设置 `disabled` 即可禁用表单控件

- `input` 、`textarea` 、 `button` 、 `select` `、option` 都可以设置 `disabled` 属性

#### lable标签

`lable` 标签可与表单控件相关联，关联之后点击文字，与之对应的表单控件就会获取焦点
两种与 `lable` 关联方式如下：

&emsp;1.让 `lable` 标签的 `for` 属性的值等于表单控件的 `id`
&emsp;2.把表单控件套在 `lable` 标签的里面

#### fieldset和legend的使用（了解）

`fieldest` 可以为表单控制分组， `legend` 标签是分组的标题

```html
<fieldset>
<legend>主要信息</legend>
<label for="zhanghu">账户：</label>
<input id="zhanghu" type="text" name="account" maxlength="10"><br>
<label>
密码：
<input id="mima" type="password" name="pwd" maxlength="6">
</label>
<br>
性别：
<input type="radio" name="gender" value="male" id="nan">
<label for="nan">男</label>
<label>
<input type="radio" name="gender" value="female" id="nv">女
</label>
</fieldset>
```

#### 表单总结

| 标签名 | 标签语义 | 常用属性 |
| ---- | ---- | ---- |
| `form` | 表单 | `action` 属性：表单要提交的地址。<br>&emsp;`target` 属性：要跳转的新地址打开位置；值：`_self`、`_blank`<br>&emsp;`method` 属性：请求方式，值：`get`、`post` |
| `input` | 多种形式的表单控件 | `type` 属性：指定表单控件的类型。<br>&emsp;值：`text`、`password`、`radio`、`checkbox`、`hidden`、`submit`、`reset`、`button` 等。<br>&emsp;`name` 属性：指定数据名称<br>&emsp;`value` 属性：<br>&emsp;&ensp;对于输入框：指定默认输入的值；<br>&emsp;&ensp;对于单选和复选框：实际提交的数据；<br>&emsp;&ensp;对于按钮：显示按钮文字。<br>&emsp;`disabled` 属性：设置表单控件不可用。<br>&emsp;`maxlength` 属性：用于输入框，设置最大可输入长度。<br>&emsp;`checked` 属性：用于单选按钮和复选框，默认选中 |
| `textarea` | 文本域 | `name` 属性：指定数据名称<br>&emsp;`rows` 属性：指定默认显示的行数，影响文本域的高度。<br>&emsp;`cols` 属性：指定默认显示的列数，影响文本域的宽度。<br>&emsp;`disabled` 属性：设置表单控件不可用。 |
| `select` | 下拉框 | `name` 属性：指定数据名称<br>&emsp;`disabled` 属性：设置整个下拉框不可用。 |
| `option` | 下拉框的选项 | `disabled` 属性：设置下拉选项不可用。<br>&emsp;`value` 属性：该选项事件提交的数据<br>&emsp;（不指定`value`，会把标签中的内容作为提交数据）<br>&emsp;`selected` 属性：默认选中。 |
| `button` | 按钮 | `disabled` 属性：设置按钮不可用。<br>&emsp;`type` 属性：设置按钮的类型，值：`submit`（默认）、`reset`、`button` |
| `label` | 与表单控件做关联 | `for` 属性：值与要关联的表单控件的`id`值相同。 |
| `fieldset` | 表单边框 | |

### 框架标签

#### 标签名

iframe
双标签

#### 功能和语义

框架(在网页中嵌入其他文件)

#### 属性

`name` ：框架名字，可与 `target` 属性配合
`width` ：框架的宽
`height` ：框架的高度
`frameborder` ：是否显示边框，值：0或1

#### 实际应用

1、在网页中嵌入广告
2、与超链接或表单的 tardet 配合，展示不同的内容

### HTML实体

在HTML中我们可以用一种<font colot="blue">特殊的形式</font>的内容，来表示某个**符号**，这种特殊形式的内容，就是HTML实体。比如小于号`<`用于定义HTML标签的开始。如果我们希望浏览器正确地显示这些字符，我们必须在HTML源码中插入字符实体。

- **字符实体**由三部分组成：一个`&`和一个实体名称（或者一个`#`和一个实体编号），最后加上一个分号`；`。

#### 常见字符实体总结

| 符号 | 描述 | 实体名称 | 实体编号 |
| ---- | ---- | ---- | ---- |
| | 空格 | `&nbsp;` | `&#160;` |
| < | 小于号 | `&lt;` | `&#60;` |
| > | 大于号 | `&gt;` | `&#62;` |
| & | 和号 | `&amp;` | `&#38;` |
| " | 引号 | `&quot;` | `&#34;` |
| ´ | 反引号 | `&acute;` | `&#180;` |
| ¢ | 分（cent） | `&cent;` | `&#162;` |
| £ | 镑（pound） | `&pound;` | `&#163;` |
| ¥ | 元（yen） | `&yen;` | `&#165;` |
| € | 欧元（euro） | `&euro;` | `&#8364;` |
| © | 版权（copyright） | `&copy;` | `&#169;` |
| ® | 注册商标 | `&reg;` | `&#174;` |
| ™ | 商标 | `&trade;` | `&#8482;` |
| × | 乘号 | `&times;` | `&#215;` |
| ÷ | 除号 | `&divide;` | `&#247;` |

完整实体列表，请参考：[HTML Standard (whatwg.org)](https://html.spec.whatwg.org/multipage/named-characters.html#named-character-references)

### HTML全局属性

|属性名|含义|
|---|---|
|`id`|给标签指定唯一标识，注意：`id` 是不能重复的。<br>作用：可以让 `label` 标签与表单控件相关联；也可以与 `CSS` 、`JavaScript` 配合使用。|
|`class`|给标签指定类名，随后通过`CSS`就可以给标签设置样式|
|`style`|给标签设置`CSS`样式|
|`dir`|内容的方向，值：`ltr`、`rtl`|
|`title`|给标签设置一个文字提示，一般超链接和图片用得比较多|
|`lang`|给标签指定语言，具体规范和可选值参考【10. HTML 设置语言】|

完整的全局属性，请参考[全局属性 - HTML（超文本标记语言） | MDN (mozilla.org)](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Reference/Global_attributes)

### meta元信息

1.配置字符编码

```html
<meta charset="utf-8">
```

2.针对IE浏览器的兼容性配置。

```html
<meta http-equiv="X-UA-Compatible" content="IE=edge">
```

3.针对移动端的配置

```html
<meta name="viewport" content="width=device-width,initial-scale=1.0">
```

4.配置网页关键字

```html
<meta name="keywords" content="8-12个以英文逗号隔开的单词/词语">
```

5.配置网页描述信息

```html
<meta name="description" content="80字以内的一段话，与网站内容相关">
```

6.针对搜索引擎爬虫配置：

```html
<meta name="robots" content="此处可选值见下表">
```

|值|描述|
|---|---|
|`index`|允许搜索爬虫索引此页面|
|`noindex`|要求搜索爬虫不索引此页面|
|`follow`|允许搜索爬虫跟随此页面上的链接|
|`nofollow`|要求搜索爬虫不跟随此页面上的链接|
|`all`|与 `index` 、 `follow` 等价|
|`none`|与 `noindex` 、 `nofollow` 等价|
|`noarchive`|要求搜索引擎不缓存页面内容|
|`nocache`|`noachive` 的替代名称|

7.配置网页作者：

```html
<meta name="author" content="tony">
```

8.配置网页作者：

```html
<meta name="generator" content="Visual Stido Code">
```

9.配置定义网页版权信息：

```html
<meta name="copyright" content="2003-2027©版权所有">
```

10.配置网页自动刷新

```html
<meta http-equiv="refersh" content="10;url=http://www.baidu.com">
```

完整的网页元信息，请参考:[文档级元数据元素 | MDN](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Reference/Elements/meta)
