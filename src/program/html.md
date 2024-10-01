**面试题：行内元素有哪些？块级元素有哪些？ 空(void)元素有那些？**

行内元素：a、b、span、img、input、strong、select、label、em、button、textarea

块级元素：div、ul、li、dl、dt、dd、p、h1-h6、blockquote

空元素：即系没有内容的HTML元素，例如：br、meta、hr、link、input、img

**面试题：页面导入样式时，使用link和@import有什么区别？**



示例：

　

```
　<link href="xxx.css" rel="stylesheet" type="text/css" />
```

 href 属性设置外部样式表文件的地址，可以是相对地址，也可以是绝对地址。

 rel 属性定义关联的文档，这里表示关联的是样式表。

 type 属性定义导入文件的类型，同 style 元素一样，text/css表明为 CSS 文本文件。

示例：

```
<style type="text/css">　　@import url("xxx.css")</style>
```

@import是 CSS 提供的语法规则，只有导入样式表的作用；

在 @import 关键字后面，利用 url() 函数包含具体的外部样式表文件的地址。

1.从属关系区别

[@import](https://github.com/import)是 CSS 提供的语法规则，只有导入样式表的作用；link是HTML提供的标签，不仅可以加载 CSS 文件，还可以定义 RSS、rel 连接属性等。



2.加载顺序区别

加载页面时，link标签引入的 CSS 被同时加载；[@import](https://github.com/import)引入的 CSS 将在页面加载完毕后被加载。



3.兼容性区别

[@import](https://github.com/import)是 CSS2.1 才有的语法，故只可在 IE5+ 才能识别；link标签作为 HTML 元素，不存在兼容性问题。



4.DOM可控性区别

可以通过 JS 操作 DOM ，插入link标签来改变样式；由于 DOM 方法是基于文档的，无法使用[@import](https://github.com/import)的方式插入样式。



5.权重区别(该项有争议，下文将详解)

link引入的样式权重大于[@import](https://github.com/import)引入的样式。

**面试题：title与h1的区别、b与strong的区别、i与em的区别？**

title与h1的区别

　　定义：

　　　　title是网站标题，

　　　　h1是文章主题

　　作用：

　　　　title概括网站信息，可以直接告诉搜索引擎和用户这 个网站是关于什么主题和内容的，是显示在网页Tab栏里的；

　　　　h1突出文章主题，面对用户，更突出其视觉效果，指向 页面主体信息，是显示在网页中的。

b与strong的区别

　　定义：

　　　　b(bold)是实体标签，用来给文字加粗，

　　　　strong是逻辑标签，作用是加强字符语气。

　　区别：

　　　　b标签只是加粗的样式，没有实际含义，常用来表达无强调或着重意味的粗体文字，比如文章摘要中的关键词、 评测文章中的产品名称、文章的导言；

　　　　strong表示标签内字符重要，用以强调，其默认格式是加粗，但是可以通 过CSS添加样式，使用别的样式强调。

　　建议：为了符合CSS3的规范，b应尽量少用而改用strong

i与em的区别

　　定义：

　　　　i(italic)是实体标签，用来使字符倾斜，

　　　　em(emphasis)是逻辑标签，作用是强调文本内容

　　区别：

　　　　i标签只是斜体的样式，没有实际含义，常用来表达无强调或着重意味的斜体，比如生物学名、术语、外来语；

　　　　em表示标签内字符重要，用以强调，其默认格式是斜体，但是可以通过CSS添加样式。

　　建议：为了符合CSS3的规 范，i应尽量少用而改用em

**面试题：img标签的title和alt有什么区别？**

title：当⿏标滑动到图片上的时候显示，相当于图片的注释

alt：当图片不能正常加载的时候，会代替图片显示alt定义的文字，相当于提示语

面试题：png、jpg、gif 这些图片格式解释一下，分别什么时候用？