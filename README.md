:root {
    --side-bar-bg-color: #fafafa;
    --control-text-color: #777;
	/* background: url(https://www.toptal.com/designers/subtlepatterns/patterns/linedpaper.png) 这一行是背景图片，这个模式是无背景版本，需要背景请去掉注释 */
	/* background: #F5F5DC 或许有人喜欢纯色背景 */
}

@include-when-export url(https://fonts.loli.net/css?family=Open+Sans:400italic,700italic,700,400&subset=latin,latin-ext);

/* ******************** */
/* 导入字体 */
/* 这里是主要的西文字体 Times New Roman */

@font-face {
  font-family:'Times New Roman';/* 字体种类名 */
  font-style: normal;/* 常规或者斜体 */
  font-weight: normal;/* 常规或者粗体 */
  src: url("./my/times.ttf");/* 存入字体的文件，这里是相对路径 */
}

/* ******************** */
/* 这里是中文字体宋体 */ 

@font-face {
  font-family: simsun;/* 字体种类名 */
  src: url("./my/simsun.ttc");/* 存入字体的文件，这里是相对路径 */
}


html {
    font-size: 16px;
}

/* line-height是行高，改的小一点1.8→1.5 */
body {
    font-family: "Times New Roman", "Helvetica Neue", Helvetica, Arial, simsun , sans-serif;/* 主要字体 */
    color: rgb(0, 0, 0);/* 主体的字的色号，包括标题和正文，不含引用 */
    line-height: 1.5;/* 行高1.2到1.8合适 */
}

#write {
    max-width: 860px;
  	margin: 0 auto;
  	padding: 30px;
    padding-bottom: 100px;
}

@media only screen and (min-width: 1400px) {
	#write {
		max-width: 1024px;
	}
}

@media only screen and (min-width: 1800px) {
	#write {
		max-width: 1200px;
	}
}

#write > ul:first-child,
#write > ol:first-child{
    margin-top: 30px;
}

a {
    color: #4183C4;
}
h1,
h2,
h3,
h4,
h5,
h6 {
    position: relative;
    margin-top: 1rem;
    margin-bottom: 1rem;
    font-weight: bold;
    line-height: 1.4;
    cursor: text;
}
h1:hover a.anchor,
h2:hover a.anchor,
h3:hover a.anchor,
h4:hover a.anchor,
h5:hover a.anchor,
h6:hover a.anchor {
    text-decoration: none;
}
h1 tt,
h1 code {
    font-size: inherit;
}
h2 tt,
h2 code {
    font-size: inherit;
}
h3 tt,
h3 code {
    font-size: inherit;
}
h4 tt,
h4 code {
    font-size: inherit;
}
h5 tt,
h5 code {
    font-size: inherit;
}
h6 tt,
h6 code {
    font-size: inherit;
}
h1 {
    font-family:'Times New Roman', 黑体;/* 一级标题字体，各级标题同下 */
    font-size: 2.25em;/* 一级标题大小 */
    text-align:center;/* 一级标题居中 */
    line-height: 1.2;/* 一级标题行高 */
    /* border-bottom: 1px solid #eee; */    /* 这一行是下划线，建议取消，可以自己在typora中加 */
}
h2 {
    font-family:'Times New Roman', 黑体;/* 二级标题字体 */
    font-size: 1.75em;
    line-height: 1.225;
    /* border-bottom: 1px solid #eee; */    /* 这一行是下划线，建议取消，可以自己在typora中加 */
}

/*@media print {
    .typora-export h1,
    .typora-export h2 {
        border-bottom: none;
        padding-bottom: initial;
    }

    .typora-export h1::after,
    .typora-export h2::after {
        content: "";
        display: block;
        height: 100px;
        margin-top: -96px;
        border-top: 1px solid #eee;
    }
}*/

h3 {
    font-family:'Times New Roman', 黑体;/*小标题字体*/
    font-size: 1.5em;
    line-height: 1.43;
}
h4 {
    font-family:'Times New Roman', 黑体;/*小标题字体*/
    font-size: 1.25em;
}
h5 {
    font-family:'Times New Roman', 黑体;/*小标题字体*/
    font-size: 1em;
}
h6 {
   font-family:'Times New Roman', 黑体;/*小标题字体*/
   font-size: 1em;
    color: #777; /* 六级标题这里改了一个浅色 */
}

table{
    margin: 0.8em 0;
}

/*各种分割线以及下划线*/
li>ol,
li>ul {
    margin: 0 0;
}
hr {
    height: 1px;
    padding: 0;
    margin: 16px 0;
    background-color: #82318E;
    border: 0 none;
    overflow: hidden;
    box-sizing: content-box;
}

li p.first {
    display: inline-block;
}
ul,
ol {
    padding-left: 30px;
}
ul:first-child,
ol:first-child {
    margin-top: 0;
}
ul:last-child,
ol:last-child {
    margin-bottom: 0;
}
blockquote {
    border-left: 4px solid #82318E;/* 引用竖线在左侧，颜色为紫色 */
    padding: 0 15px;
    color: rgb(0,0,0);/* github模板一般把引用的字体颜色设为#777777灰色，我觉得这里统一和主体文本颜色一致挺好 */
}
blockquote blockquote {
    padding-right: 0;
}

/* 三线表 */

#write table{
border-top: 1.5pt solid;/* 表格顶线，实线，1.5粗 */
border-bottom: 1.5pt solid;/* 表格底线，实线，1.5粗 */
font-family:simsun,Times New Roman;/* 表格字体 */
font-size:9pt;/* 表格字号 */
text-align:center;/* 字居中 */
  page-break-inside:avoid;
}

#write table td{
padding:7px;
}
#write table tr{
padding:7px;
}

thead{
border-bottom: 0.75pt solid;/* 表头底线，实线，0.75粗 */
font-family:黑体,Times New Roman;/* 表头字体 */
font-size:9pt;
}



.CodeMirror-lines {
    padding-left: 4px;
}

.code-tooltip {
    box-shadow: 0 1px 1px 0 rgba(0,28,36,.3);
    border-top: 1px solid #eef2f2;
}

.md-fences,
code,
tt {
    border: 1px solid #e7eaed;
    background-color: #f8f8f8;
    border-radius: 3px;
    padding: 0;
    padding: 2px 4px 0px 4px;
    font-size: 0.9em;
}

code {
    background-color: #f3f4f4;
    padding: 0 2px 0 2px;
}

.md-fences {
    margin-bottom: 15px;
    margin-top: 15px;
    padding-top: 8px;
    padding-bottom: 6px;
}

/* 高亮，背景颜色：紫罗兰，字体颜色 */
mark {
    background: #EE82EE;
    color: #000;
}

.md-task-list-item > input {
  margin-left: -1.3em;
}

@media print {
    html {
        font-size: 13px;
    }
    table,
    pre {
        page-break-inside: avoid;
    }
    pre {
        word-wrap: break-word;
    }
}

.md-fences {
	background-color: #f8f8f8;
}
#write pre.md-meta-block {
	padding: 1rem;
    font-size: 85%;
    line-height: 1.45;
    background-color: #f7f7f7;
    border: 0;
    border-radius: 3px;
    color: #777777;
    margin-top: 0 !important;
}

.mathjax-block>.code-tooltip {
	bottom: .375rem;
}

.md-mathjax-midline {
    background: #fafafa;
}

#write>h3.md-focus:before{
	left: -1.5625rem;
	top: .375rem;
}
#write>h4.md-focus:before{
	left: -1.5625rem;
	top: .285714286rem;
}
#write>h5.md-focus:before{
	left: -1.5625rem;
	top: .285714286rem;
}
#write>h6.md-focus:before{
	left: -1.5625rem;
	top: .285714286rem;
}
.md-image>.md-meta {
    /*border: 1px solid #ddd;*/
    border-radius: 3px;
    padding: 2px 0px 0px 4px;
    font-size: 0.9em;
    color: inherit;
}

.md-tag {
    color: #a7a7a7;
    opacity: 1;
}

.md-toc { 
    margin-top:20px;
    padding-bottom:20px;
}

.sidebar-tabs {
    border-bottom: none;
}

#typora-quick-open {
    border: 1px solid #ddd;
    background-color: #f8f8f8;
}

#typora-quick-open-item {
    background-color: #FAFAFA;
    border-color: #FEFEFE #e5e5e5 #e5e5e5 #eee;
    border-style: solid;
    border-width: 1px;
}

/** focus mode */
.on-focus-mode blockquote {
    border-left-color: rgba(85, 85, 85, 0.12);
}

header, .context-menu, .megamenu-content, footer{
    font-family: "Segoe UI", "Arial", sans-serif;
}

.file-node-content:hover .file-node-icon,
.file-node-content:hover .file-node-open-state{
    visibility: visible;
}

.mac-seamless-mode #typora-sidebar {
    background-color: #fafafa;
    background-color: var(--side-bar-bg-color);
}

.md-lang {
    color: #b4654d;
}

.html-for-mac .context-menu {
    --item-hover-bg-color: #E6F0FE;
}

#md-notification .btn {
    border: 0;
}

.dropdown-menu .divider {
    border-color: #e5e5e5;
}

.ty-preferences .window-content {
    background-color: #fafafa;
}

.ty-preferences .nav-group-item.active {
    color: white;
    background: #999;
}
<h1 style="color:purple;text-align:center;">
    2020-2021秋季学期
</h1>

---

<body background="https://www.toptal.com/designers/subtlepatterns/patterns/blue-snow.png">
</body>

<p align=center>
<img src="http://m.qpic.cn/psc?/V12ccrmE2bUi2o/45NBuzDIW489QBoVep5mcREIyIOqS9Yczqz*mYMx2KE*ndO5REftk5nrd9HyNzkKwrpTK6GVeLBFKmT2qgeo9UchUXg2DPYBGQpXQfLq13s!/b&bo=oQNYAqEDWAIBGT4!&rf=viewer_4" width="250"/>
</p>

---

<p align="center">
<iframe frameborder="no" border="0" marginwidth="0" marginheight="0" width=330 height=86 src="//music.163.com/outchain/player?type=2&id=523863496&auto=1&height=66"></iframe>
</p>

---

## 一、选课情况
<table>
    <thead>
        <tr>
            <th>   </th>
            <th>周一</th>
            <th>周二</th>
            <th>周三</th>
            <th>周四</th>
            <th>周五</th>
            <th>周六</th>
            <th>周日</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <th>第一节<br/>(8:00-9:35)</th>
            <th style="color:purple;">生物统计学基础</th>
            <th> </th>
            <th> </th>
            <th> </th>
            <th> </th>
            <th> </th>
            <th> </th>
        </tr>
        <tr>
            <th>第二节<br/>(9:50-12:15)</th>
            <th> </th>
            <th style="color:red;">生物物理学</th>
            <th style="color:red;">生物信息学</th>
            <th style="color:red;">认知的<br/>神经生物学基础</th>
            <th> </th>
            <th> </th>
            <th> </th>
        </tr>
        <tr>
            <th>第三节<br/>(13:30-15:05)</th>
            <th style="color:purple;"></th>
            <th style="color:violet;">三年级<br/>男生游泳</th>
            <th> </th>
            <th> </th>
            <th style="color:red;">脑疾病的<br/>神经生物学研究</th>
            <th style="color:green;">运作管理<br/>（前八周）</th>
            <th> </th>
        </tr>
        <tr>
            <th>第四节<br/>(15:20-16:55)</th>
            <th style="color:purple;"></th>
            <th style="color:red;">系统生物学</th>
            <th style="color:red;">系统生物学</th>
            <th> </th>
            <th> </th>
            <th> </th>
            <th> </th>
        </tr>
        <tr>
            <th>第五节<br/>(17:05-18:40)</th>
            <th> </th>
            <th> </th>
            <th> </th>
            <th> </th>
            <th style="color:green;">运作管理<br/>（前八周）</th>
            <th> </th>
            <th> </th>
        </tr>
        <tr>
            <th>第六节<br/>(19:20-21:45)</th>
            <th> </th>
            <th style="color:orange;">统计学引论：<br/>数据分析的科学与艺术</th>
            <th > </th>
            <th style="color:orange;">公共卫生与健康</th>
            <th style="color:green;">数据库<br/>原理及应用</th>
            <th> </th>
            <th> </th>
        </tr>              
    </tbody>
</table>

<p style="color:grey;text-align:center;">
    注：紫色：外专业基础课（扩展视野）<br/>
    紫罗兰色：体育课<br/>
    红色：专业限选课<br/>
    橙色：文化素质课<br/>
    绿色：二学位课<br/>
</p>
---

## 二、学期目标
  - 掌握R语言基本知识→应用：统计学引论、生物信息学
  - 巩固与加强基本的python→应用：生物信息学
  - 学会游泳（注：本学期游泳测试名额已满，预计下个学期通过游泳测试，加油！）
  - 努力提高英语→应用：通过英语水平考试、准备冬奥会志愿者储备、为保研/科研做语言储备
  - 林枫计划答辩与结业
  - SRT结题
  - 探索兴趣点，为保研方向做准备
  - 成绩和上学期进步/保持
  - 志愿活动（校庆、冬奥、系庆、资助大使）
  
---

## 三、日常安排与规划（具体计划参考每日规划EXCEL表）
  - 周一
    - 生物统计学作业、课件回顾（预计1小时）
    - 生物物理学预习（预计1小时）
  - 周二
    - 生物物理学复习、作业（预计一小时）
    - 认真学习游泳（课上）
    - 统计学引论预习、复习、作业（课前；课后；课后）
  - 周三
    - 生物信息学预习、回顾、作业与自由探索
  - 周四
    - 认知的神经生物学基础预习、复习、作业
    - 公共卫生与健康课程讨论
  - 周五
    - 各科课件预习、复习
  - 周六/周日
    - 一周整理与总结

---

## 四、希望保持
 - 每日背单词100
 - 早睡早起
 - 每周跑步+游泳共5次
 - 每周学习R（3、每次约1-2小时）
 - 每周学习python（同上）

---

## 五、本学期常用网站
 >- [网络学堂](https://learn.tsinghua.edu.cn/)
 >- [Github](https://github.com/)
 >- [个人Github主页](https://sirjoeyu.github.io/)
 >- [清华大学信息门户](http://info.tsinghua.edu.cn/)
 >- [生物信息学导论教程](https://lulab2.gitbook.io/teaching/)
 >- [清华邮箱](https://mails.tsinghua.edu.cn/)
 >- [清华云盘](https://cloud.tsinghua.edu.cn/)

---

