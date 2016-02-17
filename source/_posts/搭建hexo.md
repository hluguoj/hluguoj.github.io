title: Markdown 语法学习
date: 2015-09-24 01:17:32
tags: markdown
---
## 什么是Markdown
Markdown是一种轻量级的标记语言，它的理念是：能让文档更容易读、写和随意改。语法简单，常用的标记也就8种，让我们在编写的时候从排版中脱离出来，可以更加关注书写的内容而不是格式。
<!-- more -->

## 标题
我们写每一篇文章，都少不了标题。表示标题，我们在前面添加`#`就好，标题经常会有多级，我们使用多个 `#` ，一个代表一级标题，两个代表二级，以此类推。最多6级

```
# 一级标题
## 二级标题
### 三级标题
#### 四级标题
##### 五级标题
###### 六级标题
```

## 列表
用 `*` 或 `-` 或 `+` 在前面代表无序，后面要有一个空格

用数字加一个英文点 `1.`，代表有序，前面的数字可以不按顺序，但是为了美观，还是希望大家按顺序写

```
* Python
* Java
* Ruby

- Python
- Java
- Ruby

+ Python
+ Java
+ Ruby

1. 1
2. 2
3. 3
```

效果如下：

* Python
* Java
* Ruby

1. 1
2. 2
3. 3

## 引用
在前面加一个  `>`，如果希望换行，就可以在一行后面加两个空格
> 我思故我在  
> I think,therefore I am

## 图片和链接
图片和链接的差别是前面有没有 `!`
markdown有两种链接方式，行内链接和引用链接

* 行内链接 格式为 `[name](url "Title")`

```
[百度一下](http://www.baidu.com "baidu")
```
效果如下：

[百度一下](http://www.baidu.com "baidu")

* 引用链接 格式为 `[name][id]`

```
[baidu][baidu]
\[baidu\]: www.baidu.com "百度一下"
```
上面第二行是一个引用，前面部分是id，用于对应第一行的id。如果第一行的id是空，默认使用中括号里面的name作为引用id

[baidu][]
[baidu]: www.baidu.com "百度一下"

## 粗体和斜体
用两个 `*` 或 `_` 括住是粗体，一个 `*` 或 `_` 括住是斜体，不能有空格

```
**加粗**
*斜体*
```
效果如下：

**加粗**

*斜体*

## 脚注
格式如下：

```
hello[^hello]
\[^hello\]: hi
```
这部分的引用跟链接中的引用只是多了一个`^`，用于表示是在右上角

a[^a]
[^a]: a

## 表格
```
|head1|head2|head3|head4|
|---|:---|:---:|---:|
|row1text1|row1text3|row1text3|row1text4|
|row2text1|row2text3|row2text3|row2text4|
```
效果如下：

|head1|head2|head3|head4|
|---|:---|:---:|---:|
|row1text1|row1text3|row1text3|row1text4|
|row2text1|row2text3|row2text3|row2text4|
`:` 所在地方是指表格那一列对齐的位置

## 代码框
用两个反撇号括住就引用代码框。

```
`print 1`
```
效果如下：

`print 1`

但这种支持单行代码，多行就不行了，为了支持多行，我们可以有以下两种方式

1. 统一在前面空4个空格
2. 前后用3个反撇号括住，添加代码语言

如下：

    ```python
    import time
    print time.time()
    ```
## 分割线
用三个或以上的 `*` 或 `-` 或 `_` 占一行即可

```
***
---
___
```
## 注意
markdown支持使用html代码，直接在markdown内容里面加入html代码就可以解析，但是在html代码里面就不能解析markdown代码

