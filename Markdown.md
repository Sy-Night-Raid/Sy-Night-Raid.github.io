# 前言
* 我们都知道markdown的特点就是简单易用，如果想要学习它，网上已经有很多文章，但为什么要阅读《了不起的markdown》这本书呢？因为网上介绍markdown的文章良莠不齐，而且内容比较碎片化，我们并不能通过这些碎片化的信息全面系统地掌握学习markdown
# 第1章 人人都应学会markdown
## 1.1 语法学习
### 1. 学习基础语法    
markdown的基础语法是指John Gruber最初发布的markdown版本，大多数扩展语法都是基于此版本开发的，因此基础语法是需要学会的
### 2. 学习扩展语法
在众多扩展语法中，GFM（Github Flavored Markdown的简称，Github是全球最大的程序员“交友”网站）无疑是目前最流行的。它扩展了包括表格、任务列表、删除线、围栏代码、emoji等在内的语法，功能非常全面，是笔者重点推荐学习的扩展语法。

# 第2章 人人都能学会markdown
## 2.1 基础语法
### 2.1.1 字体
   #### 1. 标题
 * 我们用#来标记标题，使用语法为：== #+空格+标题内容 ==    
 * #的个数表示了标题的等级，#是一级标题，##是二级标题……依此类推，那么不同级别的标题有什么区别呢？区别就是一级标题最大，然后依次递减大小
 * markdown中最多只支持前六级标题
 #### 2. 粗体和斜体
 粗体由两个*包裹，斜体使用一个*包裹
 * **加粗内容** *斜体内容*
 ### 2.1.2 段落与换行
 markdown中的段落由一行或多行文本组成，不同的段落之间使用空行来标记
 * 语法说明如下
    1. 如果行与行之间没有空行，则会被视为同一段落（也就是说在markdown中你如果不特意去标记有空行的话，不管你怎么在文本编辑中输入回车换行来继续书写，最后浏览的内容都是在同一行中的）
    2. 空行是指行内什么都没有，或者只有空格和制表符
 * 如果想在段内换行，则需要在上一行的结尾插入两个以上的空格然后按回车键   
    
 ### 2.1.3 列表
 分为有序列表和无序列表两种，有序列表用数字序号+英文句号+空格+列表内容来标记，无序列表由*+空格+列表内容来标记
 * 嵌套列表的语法示例如下：   
 第一层列表   
 tab+第二层列表   
 tab+tab+第三层列表
 * 有序列表和无序列表也可以相互嵌套   
     
 ### 2.1.4 分隔线
 分隔线由3个以上的*来标记
 * 使用分隔线的语法是：
 **** 
 * 分隔线需使用至少3个以上的*来标记   
 行内不能有其他字符   
 可以在标记符中间加上空格   
    
  ### 2.1.5 图片
  插入图片的语法如下：   
  ！【图片替代文字】（图片地址）
  * 图片替代文字在图片无法正常显示时会比较有用，因为它能让你回想起这个图片是什么   
  图片地址可以是本地图片的路径也可以是网络图片的地址   
  本地图片支持相对路径和绝对路径两种方式（绝对路径就相当于源文件，就是图片所在最根本的位置；而相对路径就是你图片表面所在的位置，这个位置一旦变了，通过相对路径上传的图片就显示不出了）    
      
   ### 2.1.6 链接    
      
   #### 1. 文字链接
   文字链接就是把链接地址直接写在文本中，语法如下   
   【链接文字】（链接地址）    
   * 我们还有第二种写法，如下   
   在日常生活中我们经常使用的网址有【google】，【github】，【stack overflow】      
   【google】：https://www.google.com/     
   【GitHub】：网址    
   【stack overflow】：网址        
   这种方法把链接地址在某个地方同一定义好，然后在正文中通过“变量”来引用，可读性变强了，这种方法叫作引用链接。
   * 引用链接的注意事项   
      1. 链接标记不区分大小写
      2. 定义的链接内容可以放在当前文件的任意位置，建议放在页尾
      3. 当链接地址为网络地址时要以http/https开头，否则会被识别为本地地址
         
  #### 2. 网址链接
  将网络地址或邮箱地址使用<>包裹起来会被自动转换为超链接（URL是网络地址的英文名）   
  ### 2.1.7 行内代码与代码块
       
  #### 1. 行内代码
  行内代码引用使用`包裹（我们可能不会经常使用这个键，不清楚这个键在哪里，在笔记本键盘的左上方，esc键的下面）    
 
 `我是你爹`
 #### 2. 代码块
 代码块以tab键或4个空格开头     
       
      代码块
 * 小提示：因为代码块使用tab键或4个空格开头的效果不够直观，很多扩展语法（如GFM）提供了围栏代码块，并且支持语法高亮
     
 * 不要把自己的思想局限了，我们说是用`包裹的是代码，但想标明什么其他东西也可以用啊！    
 #### 3. 围栏代码
 如果代码超过1行，应该使用围栏代码块（扩展语法），并声明语言，这样做便于阅读，并且可以显示语法高亮    
 例如：    
 ```python
 def print_name():
 print("markdown")
 ```
     
  ### 2.1.8 引用
  * 语法：由> + 引用内容来标记
  * 多行引用也可以在每一行的开头都插入>      
    在引用中可以嵌套引用             
    在引用中可以使用其他的markdown语法      
    段落与换行的格式在引用中也是适用的      
  * 实战演练    
  >我是最基础的引用     
  
  >我是换行引用    
  >换行咯     
  
  >我是多行隔行引用    
  >
  >哈哈哈    
      
  >我是嵌套引用
  >>芜湖
   
  
  
  
  
  
  
  
  











