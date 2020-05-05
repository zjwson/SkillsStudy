# Markdown For Typora中文版使用指南

本标题主要讲述什么是Markdown

# 一.概述

**Markdown**诞生自 [Daring Fireball](https://link.zhihu.com/?target=http%3A//daringfireball.net/)之手，点击[这里](https://link.zhihu.com/?target=http%3A//daringfireball.net/projects/markdown/syntax)可以找到最早版本的语法标准。然而，它的语法标准因解析器和编辑器而异，**Typora**使用的是[GitHub Flavored Markdown](https://link.zhihu.com/?target=https%3A//help.github.com/articles/github-flavored-markdown/)标准。

需要注意的是在Markdown中的HTML代码块可以被识别但并不会被解析和编译。同样要注意的是，保存之后的文档格式可能会对最初的编写的文档格式有所微调。

## 

## 

# 

# 二.块元件

## 

# 

## 1.段落和行间距

段落，顾名思义就是由一行或多行文本组成的，以段为形式的结构。在Markdown语法中，段落间以一行以上的空行作分隔。在Typora中，你只需要按一下`Enter`就可以插入一个新的段落。

按`Shift`+`Enter`可以创建一个比段落间距更小的行间距。然而，大多数的Markdown解析器会忽略这个方式创建的行间距，但是你可以通过在这一行的最后插入两个空格`Space`或者插入` <br/>`令解析器强制识别。



## 2.标题

可以通过在一行的开头使用1-6个`#`符号来创建标题，对应1-6个级别的标题。例如：

```tex
# 这是一个一级标题

## 这是一个二级标题

###### 这是一个六级标题
```

在Typora中，在标题文本前输入`#`，然后按下`Enter`可以创建一个标题。



## 3.引用

Markdown使用邮件风格的`>`符号来创建引用块。例如：

```text
> 这是一个由两个段落组成的引用块，这是第一个段落。
>
> 这是第二个段落，爱饭打森，爱乖出台，请曾爱萨菲，撒㩐，经爱抚，百分赛法。



> 这是另一个只有一个段落的引用块。两个代码块间可以用一空行来分隔。
```



## 4.普通清单

输入`* 清单事项1`就会创建一个无序列表，这里的`*`符号可以用`-`和`+`代替。

输入`1. 清单事项1`就会创建一个有序列表，它们的语法如下所示：

```text
## 无序列表
* 红色
* 绿色
* 蓝色

## 有序列表
1. 红色
2. 绿色
3. 蓝色
```



## 5.任务清单

任务清单是一种特殊的列表，列表中的事项用`「 」`或者`「X」`分别标记`未完成`和`已完成`。例如：

```text
- 「 」一个任务列表事项
- 「 」可以有如下格式
- 「 」正常 **加粗** @提及 #1234 等
- 「 」未完成
- 「x」已完成
```

你可以通过鼠标点击事项前的任务框，从而切换任务清单事项中的状态。



## 6.代码块

Typora仅仅支持[GFM](https://link.zhihu.com/?target=https%3A//help.github.com/articles/github-flavored-markdown/)的代码块，源码块是不支持的。[^此处翻译不确定]使用代码块的语法非常简单，输入`````然后按下`Enter` 就可以。

另外还可以自定义代码块的语言，只需要在 ```后追加输入所需要的语法名称后，我们就会通过语法高亮来实现它，例如：

~~~text
这是一个例子：

```
function test() {
  console.log("notice the blank line before this function?");
}
```

syntax highlighting:
```ruby
require 'redcarpet'
markdown = Redcarpet.new("Hello World!")
puts markdown.to_html
```
~~~



## 7.数学公式

你可以通过使用**MathJax**来实现*LaTeX*的数学符号的表达。

输入`$$`，然后按下`Enter`键就会弹出一个支持TeX/LaTeX语法的输入框，下面是一个例子：

```tex
$$
\mathbf{V}_1 \times \mathbf{V}_2 = \begin{vmatrix}
\mathbf{i} & \mathbf{j} & \mathbf{k} \
\frac{\partial X}{\partial u} & \frac{\partial Y}{\partial u} & 0 \
\frac{\partial X}{\partial v} & \frac{\partial Y}{\partial v} & 0 \
\end{vmatrix}
$$
```

在Markdown源文件中，数学的公式块是通过利用`$$`标记借用*LaTeX*语言来实现的：

```tex
$$
\mathbf{V}_1 \times \mathbf{V}_2 =  \begin{vmatrix} 
\mathbf{i} & \mathbf{j} & \mathbf{k} \\
\frac{\partial X}{\partial u} &  \frac{\partial Y}{\partial u} & 0 \\
\frac{\partial X}{\partial v} &  \frac{\partial Y}{\partial v} & 0 \\
\end{vmatrix}
$$
```



## 8.表格

输入`|标题一|标题二|`然后按下`Enter`将会创建一个有两个列的表格。

表格创建之后，你会看到一个顶部工具栏也会随之出现，通过工具栏你可以实现调整大小，增添和删除表格的功能，你也可以使用

下面的描述可以跳过，因为表格的源码语法是Typora自动生成的。

在markdown语法中，它们如下所示：

```text
| First Header  | Second Header |
| ------------- | ------------- |
| Content Cell  | Content Cell  |
| Content Cell  | Content Cell  |
```

效果如下：

```
| First Header | Second Header |
| ------------ | ------------- |
| Content Cell | Content Cell |
| Content Cell | Content Cell |
```

你也可以修饰内部的文本格式，比如链接、粗体、斜体、删除线等。

最后，通过使用冒号`：`你可以实现标题栏文字的对齐功能，比如向左对齐、向右对齐和居中对齐：

```text
| Left-Aligned  | Center Aligned  | Right Aligned |
| :------------ |:---------------:| -----:|
| col 3 is      | some wordy text | $1600 |
| col 2 is      | centered        |   $12 |
| zebra stripes | are neat        |    $1 |
```

效果如下：

```
| Left-Aligned | Center Aligned | Right Aligned |
| :------------ | :-------------: | ------------: |
| col 3 is | some wordy text | $1600 |
| col 2 is | centered | $12 |
| zebra stripes | are neat | $1 |
```

最左侧的`：`是向左对齐；最右侧的`：`是向右对齐；两侧各一个`：`是居中对齐。



## 9.脚注

```text
你可以创建一个脚注，如下所示：

脚注示范[^这是一个脚注]
```

上面的语法会编译成：

脚注示范[^这是一个脚注]

鼠标移动到`这是一个脚注`超链接可以看到脚注的文本内容。



## 10.分割线

在一空行输入`***`或者`---` 然后按下`Enter`可以创建一条分隔线。



## 11.YAML Front Matter

Typora现在支持 [YAML Front Matter](https://link.zhihu.com/?target=http%3A//jekyllrb.com/docs/frontmatter/)了，在文章的顶部输入`---`然后按下`Enter`就会创建。或者从菜单插入一个元数据块。



## 12.目录

输入`［toc］`然后按下`Enter`就会产生一个自动根据标题和标题等级自动创建的目录框。



## 13.示意图

Typora支持 [sequence](https://link.zhihu.com/?target=https%3A//bramp.github.io/js-sequence-diagrams/), [flowchart](https://link.zhihu.com/?target=http%3A//flowchart.js.org/) 和 [mermaid](https://link.zhihu.com/?target=https%3A//knsv.github.io/mermaid/%23mermaid)，之后的版本将会在设置面板中实现设置。



# 三.实时元件

实时元件将会在你输入完成后立即解码和编译完成。通过鼠标移动到这些语法元件上会显示出这些元件的源码内容，下面就将逐一介绍这些实时元件。

## 1.链接

Markdown支持两种类型的链接：直连链接和间接链接。

在上面两种链接类型中，链接文本都用`[方框]`来定义。

通过在`[ ]`后追加带有链接地址的`( )`来创建一个直接链接。在括号中，插入你需转到的网址链接，还可以在链接后追加一个`"文本"`来自定义所通往链接的网站标题。例子如下：

```text
这是一个[例子](http://example.com/ "栗子网站")网站的链接实例。

这个[例子](http://example.com/)没有网站标题。
```

上面语法效果如下：

这是一个[栗子](https://link.zhihu.com/?target=http%3A//example.com/)网站的链接实例。

这个[栗子](https://link.zhihu.com/?target=http%3A//example.com/)没有网站标题。

### 1）内部链接

**你可以把`( )`中的链接换成所在文档的标题**，这样通过点击这个链接就能实现文档内部的跳转。
例如：

`Ctrl`（在Mac上是`Command`）+ `Click` [这个链接](https://zhuanlan.zhihu.com/write#二、块元素)就会跳转到标题`二、块元素`。如果你想看这是怎么做到的，你可以将鼠标移动到这个链接然后点击就可以看到此链接方式的markdown的语法结构。

### 2）引用链接

引用类型的链接会使用第二个`[ ]`用来放置一个对应相应链接地址的标签，例子如下：

```text
这是个引用链接的[栗子][id]呦。

然后，你需要在文档的任何位置对标签作出有效的定义。

[id]:http://example/com/ "可选标题"
```

效果如下：

这是个引用链接的[栗子](https://link.zhihu.com/?target=http%3A//example/com/)呦。

然后，你需要在文档的任何位置对标签作出有效的定义。

另一种简洁的语法可以使用文本本身作为链接的名称，因而允许忽略掉链接的名称也可以实现地址追踪，所以第二个`[ ]`只需要空着就好了，但是还是需要对文本本身作出定义以提供追踪地址。

```text
[baidu][]
然后输入对文本本身的定义：

[baidu]:http://baidu.com/
```

在Typora中，`Click`链接就会展开语法结构供你编辑，`Ctrl` + `Click`会在内置浏览器中此超链接。



## 2.URLs

Typora允许你插入urls作为链接内容，用`<括号>`修饰。

``就变成如下效果：i@typora.io。

Typora也支持链接标准的URLs，栗如：



## 3.图片

图片也类似链接，但是需要额外的符号`!`放置在这一行的最开头。图片的语法结构如下所示：

```text
![图片名称](/path/to/img.jpg)
![图片名称](/path/to/img.jpg "可选名字")
```

你也可以使用`drag&drop`动作从图片文件或者网页浏览器实现插入图片的操作。随后可以通过点击图片来编辑语法的源码达到进一步修饰图片的效果。如果图片文件和所编辑的markdown文档在相同目录或亚目录则`drop&drop`操作会自动生成对应的相对路径。

如果你想查看更多插入图片的技巧，请阅读 [http://support.typora.io//Images/](https://link.zhihu.com/?target=http%3A//support.typora.io//Images/)。



## 4.斜体

Markdown识别`*`和`_`作为斜体语法的标识。用一个`*`或`_`修饰的文本会有一个HTML的标签``，例如：

```text
*一个乘号*

_一个下划线_
```

效果如下：

*一个乘号*

*一个下划线*

GFM会忽视掉文本中的下划线，而下划线在编码和名字中使用普遍，例如：

>wow_great_stuff
>do_this_and_do_that_and_another_thing.

另一需要注意的问题是如果你需要`*`或`_`本身而不想让它编译成此处的强调标识，你可以使用`\`来免除编译，例如：

```text
\*这个文本是被乘号修饰的，但是但不会变成斜体\*
```

效果如下：

\*这个文本是被乘号修饰的，但是但不会变成斜体\*

附：Typora推荐使用`*`符号。



## 5.强调

两个`*`或者`_`连用就会产生一个HTML标签``实现强调加粗的效果。

```text
**两个乘号连用**
__两个下划线连用__
```

效果如下：

**两个乘号连用两个下划线连用**

附：Typora推荐使用`*`符号。



## 6.代码

想要创建一个实时显示的代码，用两个` ``符号修饰就可以了。不像预格式化的代码块，这里的实时代码使用正常的段落来表达代码形式。栗如：

```text
使用 `printf()`功能。
```

效果如下：

使用 `printf()`功能。



## 7.删除线

GFM增添了使用符号添加删除线的语法，而标准的Markdown无此功能。

`~~错误的文本~~` 显示为 ~~错误的文本~~。

## 8.下划线

下划线功能由来源HTML的标签代码实现。

`下划线` 显示为下划线。

## 9.表情

输出表情需要借助 `：`符号。

栗子：`:smile` 显示为 :smile:。

使用者可以通过使用`ESC`键触发表情建议补全功能，也可在功能面板启用后自动触发此功能。同时，直接从菜单栏`Edit` -> `Emoji & Symbols`插入UTF8表情符号也是可以的。

## 10.HTML

Typora不能使用HTML元素，但是Typora可以解析和编译非常有限的HTML元素，作为Markdown功能的补充，这些有限的功能包括：

- 下划线： `underline`
- 图片：``（HTML标签中的`width`, `height` 以及属于样式的`width`, `height`, `zoom`样式可以被识别和应用。）
- 评论：``
- 超链接： `[link](http://typora.io)` 。

大多数这些属性、样式或分类会被忽略。对其他的标签，Typora会将它们以HTML片段的形式表达。

## 11.行内嵌数学符号

想要使用这个功能，需要在设置面板的 `Markdown`栏启用它。然后使用`$`来启动TeX命令，栗如：`$\lim_{x \to \infty} \exp(-x) = 0$` 会以LaTeX的命令形式表达出来。

为了触发行内内嵌数学符号的实时编译你需要：输入`$`然后按下`ESC`键之后输入TeX命令，之后就会弹出一个如图所示的工具提示栏：

![write.gif](https://pic3.zhimg.com/v2-4033508b043cad96c59ec4edbca92f36_b.webp)



## 12.下标

想要使用这个功能，需要在设置面板的 `Markdown` 栏启动它，之后使用`~`来修饰下标文本。栗如：

`H~2~O` 和`X~long\ text~` 显示为 H~2~O 和X~long\ text~ 。

## 13.上标

想要使用这个功能，需要在设置面板的 `Markdown` 栏启动它，之后使用`^`来修饰下标文本。栗如：

`X^2^` 显示为 X^2^ 。

## 14.高亮

想要使用这个功能，需要在设置面板的`Markdown` 栏启动它，之后使用`==`来修饰高亮文本，栗如：

`==highlight==` 显示为 ==highlight== 。

