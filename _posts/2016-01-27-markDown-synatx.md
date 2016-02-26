---
layout: post
title: Markdown语法
category: 技术
comments: true
---
## markdown语法简介


###类ATX语法
### Headers(标题)

```
# H1 
## H2
### H3
#### H4
###### H6
```

# H1 
## H2
### H3
#### H4
###### H6

###类Setext语法
Alternatively, for H1 and H2, an underline-ish style:

```
Alt-H1
======
Alt-H2
------
```

Alt-H1
======
Alt-H2
------

###Emphasis(强调)

```
用两个 * 包含一段文本就是粗体的语法，用一个 * 包含一段文本就是斜体的语法

Emphasis, aka italics, with *asterisks* or _underscores_.

Strong emphasis, aka bold, with **asterisks** or __underscores__.

Combined emphasis with **asterisks and _underscores_**.

Strikethrough uses two tildes. ~~Scratch this.~~
```
Emphasis, aka italics, with *asterisks* or _underscores_.

Strong emphasis, aka bold, with **asterisks** or __underscores__.

Combined emphasis with **asterisks and _underscores_**.

Strikethrough uses two tildes. ~~Scratch this.~~

###Lists(列表)

```
#####无序列表
+ 文本1
+ 文本 2
+ Another item

#####有序列表
1.文本1

2.文本2

3.文本3

⋅⋅* Unordered sub-list. 
1. Actual numbers don't matter, just that it's a number
⋅⋅1. Ordered sub-list
4. And another item.

⋅⋅⋅You can have properly indented paragraphs within list items. Notice the blank line above, and the leading spaces (at least one, but we'll use three here to also align the raw Markdown).

⋅⋅⋅To have a line break without a paragraph, you will need to use two trailing spaces.⋅⋅
⋅⋅⋅Note that this line is separate, but within the same paragraph.⋅⋅
⋅⋅⋅(This is contrary to the typical GFM line break behaviour, where trailing spaces are not required.)

* Unordered list can use asterisks
- Or minuses
+ Or pluses
```
#####无序列表
无序列表使用星号、加号或者减号作为列表标记

+ 文本1
+ 文本 2
+ Another item

#####有序列表
1.文本1
2.文本2
3.文本3

```
如果列表项目间用空行分开，在输出 HTML 时 Markdown 就会将项目内容用 <p> 标签包起来，举例来说：

*   Bird
*   Magic
会被转换为：

<ul>
<li>Bird</li>
<li>Magic</li>
</ul>
但是这个：

*   Bird

*   Magic
会被转换为：

<ul>
<li><p>Bird</p></li>
<li><p>Magic</p></li>
</ul>
```
列表项目可以包含多个段落，每个项目下的段落都必须缩进 4 个空格或是 1 个制表符：

1.  This is a list item with two paragraphs. Lorem ipsum dolor sit amet, consectetuer adipiscing elit. Aliquam hendrerit mi posuere lectus.

    Vestibulum enim wisi, viverra nec, fringilla in,laoreet vitae, risus. Donec sit amet nisl. Aliquam semper ipsum sit amet velit.

2.  Suspendisse id sem consectetuer libero luctus adipiscing.

如果要在列表项目内放进引用，那 > 就需要缩进：
```
*   A list item with a blockquote:

    > This is a blockquote
    > inside a list item.
```
*   A list item with a blockquote:

    > This is a blockquote
    > inside a list item.

如果要放代码区块的话，该区块就需要缩进两次，也就是 8 个空格或是 2 个制表符：
```
*   一列表项包含一个列表区块：

        <代码写在这>
```
*   一列表项包含一个列表区块：

        <代码写在这>
要在 Markdown 中建立代码区块很简单，只要简单地缩进 4 个空格或是 1 个制表符就可以，例如，下面的输入：
```
这是一个普通段落：

    这是一个代码区块。
```
这是一个普通段落：

    这是一个代码区块。

* Unordered list can use asterisks
- Or minuses
+ Or pluses

###分割线

你可以在一行中用三个以上的星号、减号、底线来建立一个分隔线，行内不能有其他东西。你也可以在星号或是减号中间插入空格。下面每种写法都可以建立分隔线

```
* * *

***

*****

- - -

---------------------------------------
```

* * *

***

*****

- - -

---------------------------------------


###Links(链接)分为行内式和参考式


```
[I'm an inline-style link](https://www.baidu.com)

[I'm a relative reference to a repository file](../blob/master/LICENSE)
```
####参考式
参考式的链接是在链接文字的括号后面再接上另一个方括号，而在第二个方括号里面要填入用以辨识链接的标记：

```
This is [an example] [id] reference-style link.
[You can use numbers for reference-style link definitions][1]
[id]: http://example.com/  "Optional Title Here"
[arbitrary case-insensitive reference text]: https://www.mozilla.org
[1]: http://slashdot.org
[link text itself]: http://www.reddit.com

```
[I'm an inline-style link](https://www.baidu.com)

[I'm a reference-style link][Arbitrary case-insensitive reference text]
This is [an example] [id] reference-style link.
[id]: http://example.com/  "Optional Title Here"
[I'm a relative reference to a repository file](../blob/master/LICENSE)
[You can use numbers for reference-style link definitions][1]

Or leave it empty and use the [link text itself].

URLs and URLs in angle brackets will automatically get turned into links. 
Some text to show that the reference links can follow later.

[arbitrary case-insensitive reference text]: https://www.mozilla.org
[1]: http://slashdot.org

下面是参考式链接的范例
```
I get 10 times more traffic from [Google] [1] than from
[Yahoo] [2] or [MSN] [3].

  [1]: http://google.com/        "Google"
  [2]: http://search.yahoo.com/  "Yahoo Search"
  [3]: http://search.msn.com/    "MSN Search"
  
```
I get 10 times more traffic from [Google] [1] than from
[Yahoo] [2] or [MSN] [3].

  [1]: http://google.com/        "Google"
  [2]: http://search.yahoo.com/  "Yahoo Search"
  [3]: http://search.msn.com/    "MSN Search"
  
  
###Images(图片)

####行内式
Inline-style:
```
![alt text](https://github.com/adam-p/markdown-here/raw/master/src/common/images/icon48.png "Logo Title Text 1")

####参考式
Reference-style: 
![alt text][logo]

[logo]: https://github.com/adam-p/markdown-here/raw/master/src/common/images/icon48.png "Logo Title Text 2"
``` 

![alt text](https://github.com/adam-p/markdown-here/raw/master/src/common/images/icon48.png "Logo Title Text 1")

Reference-style: 
![alt text][logo]

[logo]: https://github.com/adam-p/markdown-here/raw/master/src/common/images/icon48.png "Logo Title Text 2"

###Code and Syntax Highlighting

Code blocks are part of the Markdown spec, but syntax highlighting isn't. However, many renderers -- like Github's and Markdown Here -- support syntax highlighting. Which languages are supported and how those language names should be written will vary from renderer to renderer. Markdown Here supports highlighting for dozens of languages (and not-really-languages, like diffs and HTTP headers); to see the complete list, and how to write the language names, see the highlight.js demo page.

Inline `code` has `back-ticks around` it.

Inline code has back-ticks around it.

Blocks of code are either fenced by lines with three back-ticks ```, or are indented with four spaces. I recommend only using the fenced code blocks -- they're easier and only they support syntax highlighting.


```javascript
var s = "JavaScript syntax highlighting";
alert(s);
```
 
```python
s = "Python syntax highlighting"
print s
```
 
```
No language indicated, so no syntax highlighting. 
But let's throw in a <b>tag</b>.
```

###Tables

Tables aren't part of the core Markdown spec, but they are part of GFM and Markdown Here supports them. They are an easy way of adding tables to your email -- a task that would otherwise require copy-pasting from another application.

Colons can be used to align columns.

| Tables        | Are           | Cool  |
| ------------- |:-------------:| -----:|
| col 3 is      | right-aligned | $1600 |
| col 2 is      | centered      |   $12 |
| zebra stripes | are neat      |    $1 |

There must be at least 3 dashes separating each header cell.
The outer pipes (|) are optional, and you don't need to make the 
raw Markdown line up prettily. You can also use inline Markdown.

Markdown | Less | Pretty
--- | --- | ---
*Still* | `renders` | **nicely**
1 | 2 | 3

###Blockquotes(引用)
####Markdown 标记区块引用是使用类似 email 中用 > 的引用方式。如果你还熟悉在 email 信件中的引言部分，你就知道怎么在 Markdown 文件中建立一个区块引用，那会看起来像是你自己先断好行，然后在每行的最前面加上 > 

> Blockquotes are very handy in email to emulate reply text.
> This line is part of the same quote.

也可以再段首加上>Quote break.

> This is a very long line that will still be quoted properly when it wraps. Oh boy let's keep writing to make sure this is long enough to actually wrap for everyone. Oh, you can *put* **Markdown** into a blockquote. 

区块引用也可以嵌套
> This is the first level of quoting
> 
> > This is nested blockquote
> 
> > Back to the first level

引用的区块内也可以使用其它的Markdown语法，包括标题、列表、代码区块等
> ## 这是一个标题。
> 
> 1.   这是第一行列表项。
> 2.   这是第二行列表项。
> 
> 给出一些例子代码：
> 
>     return shell_exec("echo $input |$markdown_script");

###Inline HTML

You can also use raw HTML in your Markdown, and it'll mostly work pretty well.

<dl>
  <dt>Definition list</dt>
  <dd>Is something people use sometimes.</dd>

  <dt>Markdown in HTML</dt>
  <dd>Does *not* work **very** well. Use HTML <em>tags</em>.</dd>
</dl> 

Definition list
Is something people use sometimes.
Markdown in HTML
Does *not* work **very** well. Use HTML tags.

###Horizontal Rule

Three or more...

---

Hyphens

***

Asterisks

___

Underscores

###Line Breaks

My basic recommendation for learning how line breaks work is to experiment and discover -- hit <Enter> once (i.e., insert one newline), then hit it twice (i.e., insert two newlines), see what happens. You'll soon learn to get what you want. "Markdown Toggle" is your friend.

Here are some things to try out:

Here's a line for us to start with.

This line is separated from the one above by two newlines, so it will be a *separate paragraph*.

This line is also a separate paragraph, but...
This line is only separated by a single newline, so it's a separate line in the *same paragraph*.

###Youtube videos

They can't be added directly but you can add an image with a link to the video like this:

<a href="http://www.youtube.com/watch?feature=player_embedded&v=YOUTUBE_VIDEO_ID_HERE
" target="_blank"><img src="http://img.youtube.com/vi/YOUTUBE_VIDEO_ID_HERE/0.jpg" 
alt="IMAGE ALT TEXT HERE" width="240" height="180" border="10" /></a>

Or, in pure Markdown, but losing the image sizing and border:

[![IMAGE ALT TEXT HERE](http://img.youtube.com/vi/YOUTUBE_VIDEO_ID_HERE/0.jpg)](http://www.youtube.com/watch?v=YOUTUBE_VIDEO_ID_HERE)


###参考文章：
[Markdown 语法说明](http://wowubuntu.com/markdown/)
[Markdown Cheatsheet](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet)	


