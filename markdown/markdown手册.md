
[toc]

# 基础知识点

1. 缩进 
   
- 使用全角空格(切换快捷键shift+空格)。即：在全角输入状态下直接使用空格键就ok了 


2. 添加空一行

- 使用 `<br>` 保持他的前面有两个空格然后回车，再添加，注意这里有很多问题，有时候要保持前后都要空一行。
- `&nbsp;` 这也可以空一行，保持前后都有空行就行，感觉稳定一些。

3. 高亮   
   
   `==带高亮文本== ` 
  用两个等于号包围  

4. 下划线   
   
   `<u>下划线</u>  `
  用两个`<u>`包围 

5. 插入图片
[教程](https://blog.csdn.net/xapxxf/article/details/105133999) 

   图片插入的统一格式是  
   `![Alternative text](link "optional title")` 


   Alternative text：图片的Alternative文本，用来描述图片的==关键词==，可以不写。最初的本意是当图片因为某种原因不能被显示时而出现的替代文字，后来又被用于SEO，可以方便搜索引擎根据Alt text里面的关键词搜索到图片。 

    link：可以是图片的本地地址、网址。

    "optional title"：鼠标悬置于图片上会出现的标题文字，可以不写。

   使用base64图片编码时格式：

    ![Alternative text][base64 label]  //都是中括号[]


 - 相对路径图片插入  
  
    如何返回父级目录`../`可以返回父级，通过累加使用可以一直返回上一级文件夹

    &nbsp;

    比如同一父级文件夹下从A文件夹获取B文件夹下的jap.jpg  
    相对路径为 `../B/jap.jpg`  

    <br>
  
    `./zha.jpg` 这是在同一目录下的图片路径

    <br>

    在这里我插入她的图片
    ![girl](photograph/girl.jpg)  

 <br>
 <br>

 - 如果对图片进行操作那么要进行下面的代码 [链接](https://zhuanlan.zhihu.com/p/80665637#:~:text=Markdown%E8%AF%AD%E8%A8%80%E5%9B%BE%E7%89%87%E5%B1%85%E4%B8%AD%E3%80%81%E5%B9%B6%E8%B0%83%E6%95%B4%E5%9B%BE%E7%89%87%E5%A4%A7%E5%B0%8F%201%20%E5%B1%85%E4%B8%AD%20%EF%BC%8C%E5%B9%B6%E6%8C%87%E5%AE%9A%E5%9B%BE%E7%89%87%20%E5%AE%BD%E5%BA%A6%E5%92%8C%E9%AB%98%E5%BA%A6%20%EF%BC%8C%E4%BB%A3%E7%A0%81%E5%A6%82%E4%B8%8B%EF%BC%9A%20html%20%3Cdiv,%3Cdiv%20align%3Dcenter%3E%20%3Cimg%20src%3D%22%E5%9B%BE%E7%89%87%E5%9C%B0%E5%9D%80%22%20width%20%3D%2080%25%2F%3E%20%3C%2Fdiv%3E)

    &nbsp;



    - Markdown语言图片居中、并调整图片大小

        1. 居中，并指定图片宽度和高度，代码如下：
  
         ```md
         <div align="center"> <img src="photograph/girl.jpg" alt="girl" width="200" height="200"> </div>
         ```

         <div align="center"> <img src="photograph/girl.jpg" alt="girl" width="200" height="200"> </div>

        2. 居中，仅指定宽度（高度按比例缩放），代码如下  
         ```md
         <div align="center"> <img src="photograph/girl.jpg" width = 400 /> </div>
         ``` 

         <div align="center"> <img src="photograph/girl.jpg" width = 400 /> </div>
        
        3. 居中，指定相对宽度（原图的百分比），代码如下：

         ```md
         <div align=center> <img src="图片地址" width = 80%/> </div>
         ```

         <div align=center> <img src="photograph/girl.jpg" width = 40%/> </div>






***

&nbsp;


# 笔记

## 1. 字体居中和改变字体大小

```md
<div align='center' ><font size='70'>实习总结报告</font></div>
```  


## 2. HTML一些知识点 
```md
<span style="display:block;text-align:center;color:red;"> 标题</span>
```
> 这段代码的作用是改变颜色并且将自己居中

- span  
```<span> ```是 HTML 中的内联元素，用于在文本中封装一小段内联内容，并且可以对这段内容应用样式或添加其他属性。```<span>``` 元素本身并没有特定的语义含义，它仅仅是一个用来包裹文本的容器。你可以在 ```<span>``` 元素上应用 CSS 样式
+ style  
style 是 HTML 中的属性，用于为元素指定样式。通过 style 属性，你可以直接在HTML 元素中定义内联样式，而不需要使用外部的 CSS 文件。style 属性接受一串 CSS 样式规则，多个样式规则之间使用分号进行分隔。每个样式规则由属性和值组成，用冒号将它们分开。
- display  
display 是 CSS 中的一个属性，用于控制元素的显示方式。通过设置 display 属性，你可以改变元素在页面中所占据的空间和布局方式。  
以下是一些常见的 display 属性取值及其作用：  
block：将元素显示为块级元素，使其独占一行，并且可以设置宽度、高度以及外边距和内边距。  
inline：将元素显示为内联元素，使其与相邻元素在同一行上，并且宽度、高度不可设置。  
inline-block：将元素显示为内联块级元素，使其与相邻元素在同一行上，但可以设置宽度、高度以及外边距和内边距。  
none：将元素隐藏，不占据页面空间。  
flex：使用弹性布局模型显示元素，可以轻松实现复杂的布局结构。  
grid：使用网格布局模型显示元素，用于实现复杂的网格布局。

## 3. 注脚

> 脚注是对文本的补充说明。  
> 要创建脚注参考，请在方括号`（[^1]）`内添加插入符号和标识符。 标识符可以是数字或单词，但不能包含空格或制表符。标识符仅将脚注参考与脚注本身相关联-在输出中，脚注按顺序编号。  
在括号内使用另一个插入符号和数字添加脚注，并用冒号和文本`（[^1])`: My footnote.）。您不必在文档末尾添加脚注。您可以将它们放在除列表，块引号和表之类的其他元素之外的任何位置。  

  
代码块如下
```md
中华人民伟大复兴[^1]
[^1]：指在中国新时代的伟大使命，是中国必将达到的总目标
```
 > 演示如下  

为什么总提及中华人民伟大复兴[^1]   
[^1]:指在中国新时代的伟大使命，是中国必将达到的总目标 <!-- 不必在文档末尾添加脚注。您可以将它们放在除列表，块引号和表之类的其他元素之外的任何位置。 -->

## 4. 改变文本位置、大小、颜色


```md
<div align=right> hello! P</div>  改变位置

left  center  right

<font face="宋体" color=red size=5> 文本 </font>
face 是字型
color 颜色
size 字体大小 数字越大，字体越大 3差不多是正常字体


```

示例如下

<div align=right> hello! P</div>

<font face="宋体" color=red size=6> 文本 </font>

<div align =center><font face="宋体" color=red size=14> 文本 </font> </div>









