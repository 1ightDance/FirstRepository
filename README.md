##**开发报告**##

------
###目录

 - 策划思路
 - 页面结构与说明
 - 技术指标
 - 技术点说明
 - 开发时所遇到的困难
 - 开发心得

----------

### 策划思路

> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;由于希望今后从事游戏开发，因此事先想做一个工作室的首页，一则放置作品的下载链接，二则为其他致力于游戏开发工作的同志们提供一个可以参考的游戏配乐、插图资源平台，顺便带动与此相关的音乐、美术行业发展。目前的内容，作品方面来自现阶段的几个游戏IP，配乐来自一些我自己听过的和网上力荐的大师级配乐，插图方面接触较少，因此在开发中

###页面结构与说明
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;由主页+对应模块的列表页+对应的详细内容页+站长简介组成，这些页面之间可以自由跳转。

 - 主页：提供导航和几个最新的对应信息
 - 列表页：提供相应模块的所有资讯或作品
 - 详细内容页：包含每一则资讯或某个作品的详细介绍和资源连接
 - 站长简介：简单修改后的自我介绍作业

，，
### 技术指标

> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;基于html5和css3，用sublime编写代码，辅以bootstrap组件、jquery，主要使用搜狗浏览器进行预览，git和github存放html相关文件并建站，代码设置了兼容IE9以下版本的css和js文件
###技术点说明
    

 - 整体

> 基于bootstrap的栅栏布局与自适应
> Head：阐明自适应、描述、作者、渲染模式、兼容性（以ie9为界）、引用js和css，自己定义style（使用了透明度设置和线性渐变的背景色）

 - 主页

> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;导航栏：<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;跳转到本页id，用data-toggle和data-target取消默认功能，用自定义的功能，比如下拉按钮，浮动的使用，下拉按钮中设置了分割线，可点击和不可点击的按钮以及调用系统的email功能<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;欢迎banner:<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;在线banner制作网站的使用，.class将图片设置为自动缩放，但大小不超过原图大小 <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;页头：<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;线性渐变，加粗<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;轮播图:<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;js引用<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;资讯：<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;无序列表，字间距、行间距的设置 <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;作品列表：<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;运用panel样式，圆形图片 <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;背景音乐模块：表格的使用 <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;页脚：<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;footer标签<br>
>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; *注：所有没有内容页的按钮和超链都会弹出对话框，显示网络环境不好无法打开<br>

 - 列表页

>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 筛选：<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;单选按钮与提交按钮的使用<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;换页：<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;inline-block与无序列表配合使用<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;排行：<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;图标字体的使用<br>

 - 自我介绍

> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;背景音乐<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;自动播放 <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;自定义超链接样式 <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;手风琴列表<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;留言区的textarea表单<br>

 - 内容页

> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;切换面板的使用<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;下载地址：表格，字体图标 <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;广告：float<br>

###技术难点

1.图片自适应缩放之后大小不一致，轮播起来会很怪异

> 设置高度为固定的px值，然后通过css文件中height的auto属性进行自动缩放

2.容页和列表页通过导航栏跳转至主页相应的id对应元素处

> 仅仅通过html的a标签是无法实现的，需要通过js，将a标签的href设置为:
```html
href="javascript:location.href='./index.html#id';
```
> 从而进行跳转

3.栏设置为固定位置之后会遮挡页面内容

> 将nav的class设置为clearfix即可解决遮挡问题

4.自动播放的背景音乐进度条太丑

> 把它的层次z-index降到导航栏以下，并与固定位置的导航栏位置重叠，这样只要导航栏不透明，就看不到了那个丑丑的进度条了，也就是把它用导航栏“遮住”

###开发心得

> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;网页的开发过程其实也是对于美感的考验，基本知识的掌握熟练度、知识面的广度、网页构思都在这里得到考验，一个好的网站需要开发者了解并能使用各种各样的开发工具，并有机地结合在一起。<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;个人感觉，web前端这门课不仅使我学会了基本的网页开发知识，更重要的是了解了各种各样的相关知识，开阔了视野，增大了自己的知识面。课程中所讲的内容，比如服务器的使用，wordpress搭建自己博客，git和github实现代码的多人开发，各种网页开发工具和他们的优劣比较......这些东西以及其中所蕴含的思想不仅在前端开发，在今后各种程序语言的学习和程序开发的工作中说不定什么时候就会对我们有所帮助。虽然我并不打算致力于前端开发，但通过这门课程所收获的编程思想、工具使用的能力、事业的扩宽定会使我今后受益匪浅
