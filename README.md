xiaomi
======

仿制xiaomi.com首页


重新开始GitHub之旅，在之前仿制的jd.com 、qq.com不成气候都删除掉了。

使用HTML5仿制小米首页，要求兼容IE浏览器

==========================================================================================================================

* 问题记录 *

2014年1月21日：
问题1 :  在IE下使用HTML5标签
解决：
1.将HTML5标签转为块级特性（display: block）; 注：IE会把不认识的标签当成内联元素
article, aside, details, figcaption, figure,
footer, header, hgroup, main, nav, section, summary {
    display: block;
}
2.IE对会拒绝给无法识别的元素应用样式，需要通过脚本JavaScript创建新元素           
<script>document.createElement("header");                                        
更快捷：http://html5shim.googlecode.com/svn/trunk/html5.js                       



问题2：margin: 0 auto无法居中问题；
解决：
父元素css - text-align: center;
子元素css - margin: 0 auto; width: 1190px;



问题3：IE下display: inline-block无效
解决：
1. ul li { display: inline-block; *display: inline; zoom: 1; }  //添加*display: inline IE6生效 ，zoom: 1 IE7生效
2. ul li { display: inline-block; } ul li { *display: inline } //分开写只需一条IE6 7生效
