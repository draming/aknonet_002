# [《移动网页设计与开发》](http://product.dangdang.com/23440270.html) 书摘（20150620）

内容简介：   
多屏交互时代的网页设计，要求从业者必须掌握HTML5+CSS3的新标准。在本书中，我们将抛开设备差异，学习网页开发中*、最重要的工具——HTML5、CSS3和JavaScript。通过说明与实例，作者用轻松易懂的方式向我们重点介绍了针对不同浏览器的开发技巧和原则。《移动网页设计与开发 HTML5+CSS3+JavaScript》的主要内容包括：规划内容，使其可以在多个平台中流畅显示；针对使用*API的设备进行设计；插入跨平台音频和视频，而无需使用麻烦的插件；通过使用SVG，使高分辨率设备上的图像和图形具有扩展性；使用强大的HTML5元素设计出更好的表单，等等。      

     
**以下基本上是关键内容摘录，就不特地用引用格式了，2333**              
     
     
## 第2章 结构和语义    
- 微格式：通过使用现有属性的标准化标记模式，给内容添加了更多的属性    
既是一种设计原则，也是一组标准用法模式，例如hCard模式：
```<div class=”vCard”>    
<p><a href=”http://about.me/petergasston” class=”url fn”>PeterGasston</a>    
Write for<a href=”http://broken-links.com” class=”url org”>BrokenLinks</a>.</p>    
</div>   
”url fn”-联系人全名    
”url org”-联系人工作单位 ```   

- RDFa：资源描述格式属性（Resource Description Format in Attributes, RDFa）    
使用一套全新的定制属性为内容提供上下文，RDFa Core和RDFa Lite，都依赖预定义schema（数据说明）来描述内容，例如：    
```<p property=”http://purl.org/dc/elements/1.1/date”content=”2013-04-01”>April</p>    
”http://purl.org/dc/elements/1.1/date”-术语“date”相关描述的url，来自一个架构（Dublin Core）的标准化词汇表的一部分 ```   
”2013-04-01”机器读到的是该属性的值    
April人看到的是元素内容    

- 微数据：一系列提供富有意义的机读数据的名称值对，如：    
```<p itemscope> I live in <span itemprop=”city”> London </span></p>```
Itemscope被用于标记此特定项的界限或范围的包含元素    
Itemprop属性的值是名称，”City”    
Itemprop元素的内容是值，”London”    
和RDFa一样，通过itemtype属性链接到内容，可以用预定义架构来描述内容:    
```<p itemscope itemtype=”http://example.org/birthday”>My birthday this year is on    
<span itemprop=”birthday” datatime=”2013-12-14”>December 14</span>.</p>``` 
微数据API：DOM API=>提取页面中的数据，参见microdata-api.html    
说明：    
<p>标签定义段落    
<span>标签用来组合文档中的行内元素    
<href>属性规定链接的目标    
HTML DOM是HTML Document Object Model(文档对象模型)的缩写，HTML DOM则是专门适用于HTML/XHTML的文档对象模型。熟悉软件开发的人员可以将HTML DOM理解为网页的API。    
在未来，我们通常看到的是简单微格式与微数据的混合体，由于微数据语法灵活，它可以同时适应微格式和RDFa，当然，一些微格式，如Rel-Tag，本身就非常简洁易于使用，没必要试图用微数据去替换它们。    
Schema.org=>介绍了一组使用微数据标记常见模式的共享词汇    
富摘要（Rich snippets）    
无障碍的富因特网应用程序组件（WAI-ARIA，Accessible Rich Internet Applications）    



## 第3章 设置响应性CSS    
- 媒体查询=>逻辑正确则应用语句中的样式规则    
- 屏幕分辨率媒体查询=>图形显示相关（虚拟像素、物理像素）    
- 设备适配    
- 输入机制（鼠标、键盘、触摸、手写笔、声音）媒体功能    
- JavaScript中的媒体查询    
- CSS3消除自适应/响应式网页设计中的一些问题的方法    
- 功能点考虑：    
1. 媒体查询    
窗口&设备：长、宽、最大/最小长、最大/最小宽、纵横比    
纵向/横向模式    
屏幕分辨率    
设备适配（通过修改一个CSS规则判断并适配屏幕（字体、图片等））    
输入规则    
2. 页面弹性布局&网格布局    
3. 自适应&响应式网页设计    
4. 移动（设备）优先和内容断点（阅读内容的可读性）    
5. 图像、视频等的处理    



## 第4章 CSS布局的新方法    
- 多栏结构    
- 弹性布局盒    
- 网格布局    



## 第5章 现代JavaScript    
- 前端网页开发中的行为=>JavaScript呈现    
- 一些新功能    
- 功能点考虑：    
页面加载与脚本执行（async&defer）    
输入事件、触摸事件、指针事件    
JavaScript库（jQuery、YepNote、Modernizr、Mustache），可能给网页带来较重负担，影响性能，是否使用需要权衡    



## 第6章 Device（设备）API    
- 功能点考虑：    
地理定位    
方向（探测在三维空间的位置变化）    
全屏    
震动    
电池状态    
网络信息（网络连接能力，连接哪种网络是否付费等）    
摄像头和麦克风    
网络存储（在设备上存储数据，类似cookie实现）    
拖放    
文件交互    
PhoneGap和本地封装器：封装器相当于网络应用和设备之间的中间层，用于创建混合应用；PhoneGap可以适用于IOS、安卓、Windows Phone和黑莓    



## 第7章 图像和图形    
- SVG（可缩放矢量图形，Scalable Vector Graphics），将所有用户希望获得的图标依次叠加到一张SVG图像上，然后使用CSS隐藏除一个之外的所有图标    
- canvas（HTML5的一个元素，通过使用一个API，可作为绘制图像的画布），适用于图像操纵    


        
## 第8章 新表单        
- 表单相关    
输入类型：textarea、checkbox、radio、search、email、url、tel，其中email和url可格式校验    
属性：    
自动对焦（autofocus）-光标置于输入栏    
占位符（placeholder）-如（email：e.g. foo@bar.com）中“e.g. foo@bar.com”以浅色文本显示，说明是文本而非一个值，不应该用“input email address”这样的说明性字样    
自动完成（autocomplete）    
拼写检查（spellcheck）-利用字典    
多重输入（multiple）-输入/提交一个以上条目        
表单（form）-解决排列布局问题    
数据单（datalist）：键入一个字母（字母序列）时，在下方显示推荐表单内容    

- 屏幕控件与部件：        
数字（number）-输入数字    
范围（range）-范围（滚动条）            
日期（date）-日期选择器    
颜色（color）-自定义应用程序外观颜色    

- 显示信息给用户：    
进度（progress）-进度条    
测量表（meter）-类似进度条的样子，语义为测量，如投票结果    
输出（output）    

- 表单验证：即输入校验，Constraint Validation API    



## 第9章 多媒体        
音频、视频文件等    



## 第10章 网络应用程序    
- 网络应用程序    
托管网络应用程序：将所有文件托管于外部服务器    
打包网络应用程序：将运行所需资产压缩在一个单一文件中    
网络应用程序必备清单文件（XML/JSON），包含应用的关键信息（名称、描述等）    

- 混合应用程序    
与打包应用相似，同时还在文件周围添加了一个本地壳，或称为包装，最常见的是PhoneGap    

- 应用程序缓存    
即网络不可用时离线工作，或至少保存数据    
使用应用程序缓存，或称为AppCache        
使用AppCache API    
