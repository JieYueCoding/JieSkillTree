# Markdown

### 概述

------

**Markdown**是一种[轻量级标记语言](https://zh.wikipedia.org/wiki/%E8%BD%BB%E9%87%8F%E7%BA%A7%E6%A0%87%E8%AE%B0%E8%AF%AD%E8%A8%80)，创始人为[约翰·格鲁伯](https://zh.wikipedia.org/wiki/%E7%B4%84%E7%BF%B0%C2%B7%E6%A0%BC%E9%AD%AF%E4%BC%AF)（英语：John Gruber）。它允许人们“使用易读易写的纯文本格式编写文档，然后转换成有效的[XHTML](https://zh.wikipedia.org/wiki/XHTML)（或者[HTML](https://zh.wikipedia.org/wiki/HTML)）文档”。[[4\]](https://zh.wikipedia.org/wiki/Markdown#cite_note-md-4)这种语言吸收了很多在[电子邮件](https://zh.wikipedia.org/wiki/%E7%94%B5%E5%AD%90%E9%82%AE%E4%BB%B6)中已有的纯文本标记的特性。

由于<u>Markdown的轻量化、易读易写特性，并且对于图片，图表、数学式都有支持</u>，当前许多网站都广泛使用 Markdown 来撰写帮助文档或是用于[论坛](https://zh.wikipedia.org/wiki/%E7%BD%91%E7%BB%9C%E8%AE%BA%E5%9D%9B)上发表消息。例如：GitHub、reddit、Diaspora、Stack Exchange、OpenStreetMap 、SourceForge等。甚至Markdown能被使用来撰写[电子书](https://zh.wikipedia.org/wiki/%E9%9B%BB%E5%AD%90%E6%9B%B8)。



### 历史

------

John Gruber 在 2004 年创造了 Markdown 语言，在语法上有很大一部分是跟[亚伦·斯沃茨](https://zh.wikipedia.org/wiki/%E4%BA%9A%E4%BC%A6%C2%B7%E6%96%AF%E6%B2%83%E8%8C%A8)（Aaron Swartz）共同合作的。这个语言的目的是希望大家使用“**易于阅读、易于撰写的纯文字格式，并选择性的转换成有效的XHTML（或是HTML）**”。 其中最**重要的设计是可读性**，也就是说这个语言应该要能直接在字面上的被阅读，而不用被一些格式化指令标记（像是RTF与HTML）。 因此，它是现行电子邮件标记格式的惯例，虽然它也借鉴了很多早期的标记语言，如：Setext、Texile、[reStructuredText](https://zh.wikipedia.org/wiki/ReStructuredText)。Gruber也编写了的[Perl](https://zh.wikipedia.org/wiki/Perl)脚本：*Markdown.pl*，用于把markdown语法编写的内容转换成有效的、结构良好的XHTML或HTML内容，并将左尖括号`<`和`&`号替换成它们各自的[字符实体引用](https://zh.wikipedia.org/wiki/%E5%AD%97%E7%AC%A6%E5%AE%9E%E4%BD%93%E5%BC%95%E7%94%A8)。它可以用作单独的脚本，[Blosxom](https://zh.wikipedia.org/wiki/Blosxom)和[Movable Type](https://zh.wikipedia.org/wiki/Movable_Type)的插件又或者BBEdit的文本过滤器[[4\]](https://zh.wikipedia.org/wiki/Markdown#cite_note-md-4)。Markdown也已经被其他人用Perl和别的编程语言重新实现，其中一个Perl[模块](https://zh.wikipedia.org/wiki/%E6%A8%A1%E5%9D%97_(%E7%A8%8B%E5%BA%8F%E8%AE%BE%E8%AE%A1))放在了[CPAN](https://zh.wikipedia.org/wiki/CPAN)(Text::Markdown)上。它基于一个[BSD风格的许可证](https://zh.wikipedia.org/wiki/BSD%E8%AE%B8%E5%8F%AF%E8%AF%81#BSD%E9%A3%8E%E6%A0%BC%E7%9A%84%E8%AE%B8%E5%8F%AF%E8%AF%81)分发并可以作为几个[内容管理系统](https://zh.wikipedia.org/wiki/%E5%86%85%E5%AE%B9%E7%AE%A1%E7%90%86%E7%B3%BB%E7%BB%9F)的插件[[7\]](https://zh.wikipedia.org/wiki/Markdown#cite_note-7)[[8\]](https://zh.wikipedia.org/wiki/Markdown#cite_note-8)。



### Markdown 语法介绍

------

#### 标题

用 Markdown 书写时，只需要在文本前面加上『# 』即可创建一级标题。同理，创建二级标题、三级标题等只需要增加『# 』个数即可，Markdown 共支持六级标题。如下所示：

```
# 一级标题
## 二级标题
### 三级标题
#### 四级标题
##### 五级标题
###### 六级标题
```

效果图如下：

#### ![1553603108356](C:\Users\gao03\AppData\Roaming\Typora\typora-user-images\1553603108356.png)引用

Markdown 标记区块引用和 email 中用 『>』的引用方式类似，只需要在整个段落的第一行最前面加上 『>』 ：

```
> Coding.net 为软件开发者提供基于云计算技术的软件开发平台，包括项目管理，代码托管，运行空间和质量控制等等。
```

效果图如下：

![1553667750472](C:\Users\gao03\AppData\Roaming\Typora\typora-user-images\1553667750472.png)

**区块引用可以嵌套，只要根据层次加上不同数量的**『>』：

```
> 这是第一级引用。
>
> > 这是第二级引用。
>
> 现在回到第一级引用。
```

效果图如下：

![1553667964961](C:\Users\gao03\AppData\Roaming\Typora\typora-user-images\1553667964961.png)

**引用的区块内也可以使用其他的 Markdown 语法，包括标题、列表、代码区块等**：

```
> ## 这是一个标题。
> 1. 这是第一行列表项。
> 2. 这是第二行列表项。
>
> 给出一些例子代码：
>
> return shell_exec(`echo $input | $markdown_script`);
```

效果图如下：

![在这里输入图片描述](https://dn-coding-net-production-pp.codehub.cn/a3485b98-6e38-45f2-9c9c-fb0b5027174c.png)



#### 列表

列表项目标记通常放在最左边，项目标记后面要接一个字符的空格。

**无序列表**：使用星号、加号或是减号作为列表标记

```
+ Red
- Green
* Blue
```

效果如下：

+ Blue
- Red
* Green

    

**有序列表**：使用数字接着一个英文句点

```
1. Red
2. Green
3. Blue
```

效果如下：

1. Red
2. Green
3. Blue



**代办列表: 表示列表是否勾选状态（注意：[ ] 前后都要有空格）**

```
- [ ] 不勾选
- [x] 勾选
```

效果如下:

- [ ] 不勾选

- [x] 勾选



**如果要在列表项目内放进引用，那『>』就需要缩进：**

```
* Coding.net有以下主要功能:
    > 代码托管平台
    > 
    > > 在线运行环境  
    > 
    > > 代码质量监控   
    >  
    > > 项目管理平台
```

效果如下：

* Coding.net有以下主要功能:

    > 代码托管平台
    > 
    > > 在线运行环境  
    > 
    > > 代码质量监控   
    >  
    > > 项目管理平台



#### 代码块

只要把你的代码块包裹在 “` 之间，你就不需要通过无休止的缩进来标记代码块了。 在围栏式代码块中，你可以指定一个可选的语言标识符，然后我们就可以为它启用语法着色了。 举个例子，这样可以为一段 Ruby 代码着色：

```
​```ruby
require 'redcarpet'
markdown = Redcarpet.new("Hello World!")
puts markdown.to_html
​```
```

效果如下：

```ruby
require 'redcarpet'
markdown = Redcarpet.new("Hello World!")
puts markdown.to_html
```

#### 强调

在Markdown中，可以使用 * 和  _  来表示斜体和加粗。

**斜体**：

*两边单个*   *  *或单个 _ 都可以变成斜体*

```
*Coding，让开发更简单*
_Coding，让开发更简单_
```

效果如下：

*Coding, 让开发更简单*

_Coding, 让开发更简单_

**加粗**：

**两边双个**   *  **或双个 _ 都可以变成斜体**

```
**Coding，让开发更简单**
__Coding，让开发更简单__
```

*效果图如下：*

#### 链接

方括号显示说明，圆括号内显示网址， Markdown 会自动把它转成链接，例如：

```
[超强大的云开发平台Coding](http://coding.net)
```

效果如下：

[超强大的云开发平台Coding](http://coding.net)

#### 表格

在 Markdown 中，可以制作表格，例如：

```
First Header | Second Header | Third Header
------------ | ------------- | ------------
Content Cell | Content Cell  | Content Cell
Content Cell | Content Cell  | Content Cell
```

效果如下：

| First Header | Second Header | Third Header |
| ------------ | ------------- | ------------ |
| Content Cell | Content Cell  | Content Cell |
| Content Cell | Content Cell  | Content Cell |

或者也可以让表格两边内容对齐，中间内容居中，例如：

```
First Header | Second Header | Third Header
:----------- | :-----------: | -----------:
Left         | Center        | Right
Left         | Center        | Right
```

效果如下：

| First Header | Second Header | Third Header |
| :----------- | :-----------: | -----------: |
| Left         |    Center     |        Right |
| Left         |    Center     |        Right |

#### 分割线

在 Markdown 中，可以使用 3 个以上『-』符号制作分割线，例如：

```
这是分隔线上部分内容
---
这是分隔线上部分内容
```

效果如下:

这是分隔线上的部分内容

---

这是分割线上的部分内容

#### 图片

Markdown 使用了类似链接的语法来插入图片, 包含两种形式: **内联** 和 **引用**.

**内联图片语法如下**:

```
![Alt text](/path/to/img.jpg)
或
![Alt text](/path/to/img.jpg "Optional title")
```

也就是:

- 一个惊叹号『!』
- 接着一个方括号，里面是图片的替代文字
- 接着一个普通括号，里面是图片的网址，最后还可以用引号包住并加上 选择性的『title’』文字。

**引用图片语法如下**:

```
![Alt text][id]
```

『id』 是图片引用的名称. 图片引用使用链接定义的相同语法:

```
[id]: url/to/image "Optional title attribute"
```

#### 流程图

Markdown 编辑器已支持绘制流程图、时序图和甘特图。通过 mermaid 实现图形的插入，点击查看 [更多语法详情](https://mermaidjs.github.io/)。

```
​```graph
graph TD;
    A-->B;
    A-->C;
    B-->D;
    C-->E;
    E-->F;
    D-->F;
    F-->G;
​```

```

效果图如下：

![img](https://dn-coding-net-production-pp.codehub.cn/9a6a38b8-172e-47f7-8464-b31948728149.jpg)

#### 时序图

```
​```graph
sequenceDiagram
    participant Alice
    participant Bob
    Alice->John: Hello John, how are you?
    loop Healthcheck
        John->John: Fight against hypochondria
    end
    Note right of John: Rational thoughts 
prevail...
    John-->Alice: Great!
    John->Bob: How about you?
    Bob-->John: Jolly good!
​```
```

效果图如下：![img](https://dn-coding-net-production-pp.codehub.cn/65d713f4-4088-4988-8959-79ba16b1fa6e.jpg)

#### 甘特图

```
​```graph
gantt
        dateFormat  YYYY-MM-DD
        title Adding GANTT diagram functionality to mermaid
        section A section
        Completed task            :done,    des1, 2014-01-06,2014-01-08
        Active task               :active,  des2, 2014-01-09, 3d
        Future task               :         des3, after des2, 5d
        Future task2               :         des4, after des3, 5d
        section Critical tasks
        Completed task in the critical line :crit, done, 2014-01-06,24h
        Implement parser and jison          :crit, done, after des1, 2d
        Create tests for parser             :crit, active, 3d
        Future task in critical line        :crit, 5d
        Create tests for renderer           :2d
        Add to mermaid                      :1d
​```
```

效果图如下：![img](https://dn-coding-net-production-pp.codehub.cn/651d802e-6409-4cf0-a3dd-b260c8d2cc60.jpg)