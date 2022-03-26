**笔记参考书籍**

 > 《了不起的markdown》，《The Markdown Guide》

> 在使用过程中，有任何需要新掌握的地方，去《了不起的markdown》中找

 



[TOC]



#  0x00 **Basic Syntax**



* 我们要知道 在不同的markdown处理器（不同的软件，不同的环境，不同的网页中），会有细微的变化和差异。不过这不重要，我们只要掌握最主流的基本语法即可。


> Using Markdown doesn't mean that you can't also use HTML. You can add HTML tags to Markdown syntax. For example, some people find that it's easier to use HTML tags for images.




## Headings

```markdown
# Heading level 1
## Heading level 2
### Heading level 3
#### Heading level 4
##### Heading level 5
###### Heading level 6
```



```html
<h1>Heading level 1</h1>
<h2>Heading level 2</h2>
<h3>Heading level 3</h3>
<h4>Heading level 4</h4>
<h5>Heading level 5</h5>
<h6>Heading level 6</h6>
```



## **Bold**

`  use * like this:   **Bold**  `

`  <strong>Bold text</strong>              `



## *Italic*

`like this:     *Italic*             `        

`<em>Italic</em>`



## ***Bold and Italic***

`like this:     ***Bold and Italic***`

`<strong><em> Bold and Italic </em></strong>`



## Blockquotes



`> I want to use Markdown to write`

`<blockquote>I want to use Markdown to write</blockquote>`



> I want to use Markdown to write



当然这个引用可以连续很多行，直到你按回车去终止它

> emmmmmmmmmmmmmmmm
>
> emmmmmmmmmmmmmmmmmmmmmm
>
> emm
>
> emmmmmmmmmmmmmmmm



## Nested Blockquotes



```markdown
> I want to use Markdown
>> I want to use Markdown,too
```

```html
<blockquote>
    I want to use Markdown
    <blockquote>
        I want to use Markdown,too
    </blockquote>
</blockquote>
```

> I want to use Markdown
>
> > I want to use Markdown,too



* blockquotes中也可以存在其他的标记符号，例如headings，bold，italic都可以显示，具体哪种标记在blockquotes中可以显示可以自己去尝试



## Ordered Lists



```markdown
1. first item
2. second item
3. third item
4. fourth item
....
```

```html
<ol>
    <li>first item</li>
    <li>second item</li>
    <li>third item</li>
    <li>fourth item</li>
    ....
</ol>
```



1. first item
2. second item
3. third item
4. fourth item



### **Nesting List Items**



```markdown
1. first item
2. second item
	1. Indented item
	2. Indented item
3. third item
```

```html
<ol>
    <li>first item</li>
    <li>second item
        <ol>
            <li>Indented item</li>
            <li>Indented item</li>
        </ol>
	
    </li>
    <li>third item</li>
</ol>
    
```



1. first item
2. second item
   1. indented item
   2. indented item
3. third item



## Unordered Lists



```markdown
* first item
* second item
* third item

```

```html
<ul>
    <li>first item</li>
    <li>second item</li>
    <li>third item</li>
    
</ul>
```



* first item
* second item
* third item



### **Nesting List Items**



```markdown
* first
* second
	* indented
	* indented
* third
```

* first
* second
  * indented
  * indented
* third





> Ordered lists and Unordered lists，可以一起嵌套、任意嵌套，Ordered中可以嵌套Unordered，Unordered中也可以嵌套Ordered，全由书写人的喜好决定哦~，你想即所得





## Code



* use ``
* <code></code>

`code`

*注意：只能作用于一行，即单行代码，一旦换行这个符号的作用就失效了。多行代码就要用code blocks了*



## Code Blocks



```
use ```  and language's name

like this:     ```python          ```c         ```html
```

* typora中用```就自动显示围栏代码了，但是其实完整的围栏代码形式是

```
```python            ```c             ```java
```                  ```              ```
```





## Images



`![picture's name](https://www.pexels.com/zh-cn/photo/5673835/)`

![pexels-christian-heitz-842711](C:\Users\NightRaid\Desktop\pexels-christian-heitz-842711.jpg)



* 直接把图片拖到typora中就会自动上传到图床了，这也是typora非常方便的一点





## Horizontal Rules



* 分割线用***表示，起到分割上下部分的效果



***



***





## Links





* `use [Waitbutwhy](https://waitbutwhy.com/)   `



[Waitbutwhy](https://waitbutwhy.com/)



* 简单不可命名的link方式，`use <https://waitbutwhy.com/>`



 <https://waitbutwhy.com/>



* 直接输入网址也可以哦，markdown会为你自动跳转的，https://zh.z-lib.org/
  * 这种方法还是不要常用，有的平台或者软件不支持这样




  * 如果不想使用自动链接，也可以使用`包裹URL地址如下

    * ​      `www.baidu.com`(我刚刚看到这一点觉得很蠢，这样不就标亮了一下又没有生成超链接，人家告诉你这点就是想让你在记录一个网址但并不想生成超链接的情况下使用的！)    



* 强调link的方式，`use      ***[Waitbutwhy](https://waitbutwhy.com/)*** , **[Waitbutwhy](https://waitbutwhy.com/)**,    *[Waitbutwhy](https://waitbutwhy.com/)*`



***[Waitbutwhy](https://waitbutwhy.com/)***



**[Waitbutwhy](https://waitbutwhy.com/)**



*[Waitbutwhy](https://waitbutwhy.com/)*





## Escaping Characters



* 可以使我们平常用的有意义的字符都显示出来，不再作为markdown中的用法显示，use `\+everything  `



\* emmm 

\## emmm

\*emmm*





# 0x01 **Extended Syntax**





## Strikethrough



`use  The world is ~~flat~~  round.      `      

The world is ~~flat~~  round.





## Task Lists



```markdown
- [x] task 1
- [ ] task 2
- [ ] task 3
```

- [x] task 1
- [ ] task 2
- [ ] task 3

* typora里有个优点哦，生成的task lists是动态的，对钩的完成和未完成直接用鼠标点就可以了



## Table



| 标题 | 标题 | 标题 |
| :--: | :--: | :--: |
|  1   |  1   |  1   |
|  1   |  1   |  1   |
|  1   |  1   |  1   |



* 原来我也会在学习新知识时候尽量把每个东西都学到精细，但后来我发现这样不但没用而且一点都不便捷。
* 就像在这里表格这种东西自己去一点点打太蠢了吧，直接在typora中右键插入就好了啊！！



## Footnotes



```
Here's a simple footnote,[^1] and here's a longer one.[^bignote]

[^1]: This is the first footnote.
[^bignote]: emmmmmmmm
[^bignote]: Here's one with multiple paragraphs and code. 
这里bignote有两条脚注，鼠标每放上去一次显示其中一个，移开再放上去显示另一个。

```



Here's a simple footnote,[^1] and here's a longer one.[^bignote]

[^1]: This is the first footnote.
[^bignote]: emmmmmmmm
[^bignote]: Here's one with multiple paragraphs and code. 





## Emoji



```markdown
:smile:
:laughing:
:angry:
:+1:
:-1:
:clap:
```

:smile:
:laughing:
:angry:
:+1:
:-1:
:clap:

* 更多表情符号使用请参考[emoji网站](https://www.webfx.com/tools/emoji-cheat-sheet/)
* 当然，typora中已经给你放置了很多符号，直接拿来用就好~





## Punctuation



     对于包括我在内的很多人来说，全角符号和半角符号可能是最熟悉的陌生人，虽然它们随处可见，但大部分人都没用    
 * 全角 ：`中文标点符号`是全角，占两个字节
 * 半角 ： `英文标点符号和数字`是半角，占一个字节
 * 全角 ： ，。；：！#
 * 半角 ： ,.;:!#
      * 在中文排版中，也就是中文句子中，要使用全角标点符号
      * 在英文排版中，要使用半角标点符号
      * 我觉得其实都是废话，打什么语言就直接打对应的符号了啊……



## typora中特殊的拓展语法



1. 下标：`H~2~O`

​                             H~2~O



2. 上标：`X^2^`

​                             X^2^



3. 高亮：`==Highlight==`

​                            ==Highlight==

4. 下划线：在Typora中，下划线是通过HTML实现的      `<u>underline</u>`

​                           <u>underline</u>



5. 注释：在编辑和预览时，注释的内容会显示；但在导出成pdf和word时候，注释会消失。至于应用注释的场景，自行思考。`<!--我是注释-->`

​                            <!--我是注释-->

6. 目录：`[TOC]可以生成目录`     （Table of Contents）

​                             演示效果在笔记的开头



# 00x2 **Typora的学习**



* ## typora中能恢复你更改过的版本文件，而且可以设置自动保存，这样如果误删了什么文档也不怕了

  
  
* ## 基本设置都可以从偏好习惯里更改



  















