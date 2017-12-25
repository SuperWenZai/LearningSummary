# LearningSummary
对一些常用的知识做个小小的总结。

## CSS通用初始化样式（PC端）

``` bash

* {
	word-break: break-all;
	font-family: "微软雅黑",tahoma,'宋体',Arial,Lucida,Verdana,Helvetica,sans-serif;
}

body, div, dl, dt, dd, ul, ol, li,h1, h2, h3, h4, h5, h6, pre, code,form, fieldset, legend, input, button,textarea, p, blockquote, th, td {
	margin: 0;
	padding: 0;
}

fieldset, img {
	border: 0;
}

:focus {
	outline: 0;
}

address, caption, cite, code, dfn,em, strong, th, var, optgroup,i {
	font-style: normal;
	font-weight: normal;
}

h1, h2, h3, h4, h5, h6 {
	font-size: 100%;
	font-weight: normal;
}

abbr, acronym {
	border: 0;
	font-variant: normal;
}

input, button, textarea,select, optgroup, option {
	font-family: inherit;
	font-size: inherit;
	font-style: inherit;
	font-weight: inherit;
}

code, kbd, samp, tt {
	font-size: 100%;
}

input, button, textarea, select {
	*font-size: 100%;
}

body {
	line-height: 1.5;
	font-size: 12px;
	color: #333;
	background: #FFF;
	width: 100%;
	width: expression(document.body.clientWidth <= 1200? "1200px": "auto");
	min-width: 1200px;
}

ol, ul {
	list-style: none;
}

caption, th {
	text-align: left;
}

sup, sub {
	font-size: 100%;
	vertical-align: baseline;
}

:link, :visited , ins {
	text-decoration: none;
}

blockquote, q {
	quotes: none;
}

blockquote:before, blockquote:after,q:before, q:after {
	content: '';
	content: none;
}

a:link,a:visited,a:active {
	color: #333;
	text-decoration: none;
}

a:hover {
	color: #F60;
	text-decoration: underline;
}

img {
	vertical-align: middle;
}

.clearfix:before, .clearfix:after {
	content: "\0020";
	display: block;
	height: 0;
	overflow: hidden;
}

.clearfix:after {
	clear: both;
}

.clearfix {
	zoom: 1;
}

.wrapper {
	height: auto;
	margin: 0 auto;
	width: 1200px;
}

.fontArial {
	font-family: Arial,Helvetica,sans-serif;
}

*html {
	background-image: url(about:blank);
	background-attachment: fixed;
/*修正IE6振动bug*/
}

input:focus,textarea:focus,selects:focus {
	border-color: #feebd9 !important;
	outline: 0;
	box-shadow: inset 0 1px 1px rgba(0,0,0,.075),0 0 6px #fecb98;
}

```

# wap端的一些小适配（非绝对）

``` bash

<html>
 <head>
  <meta name="viewport" content="width=device-width,initial-scale=1.0, minimum-scale=1.0, maximum-scale=1.0, user-scalable=no" /> 
  <meta name="apple-mobile-web-app-capable" content="yes" /> 
  <!-- 是否启用 WebApp 全屏模式，删除苹果默认的工具栏和菜单栏 --> 
  <meta name="apple-mobile-web-app-status-bar-style" content="black" /> 
  <!-- 设置苹果工具栏颜色 --> 
  <meta name="HandheldFriendly" content="true" /> 
  <!-- 针对手持设备优化 --> 
  <meta name="full-screen" content="yes" /> 
  <!-- UC强制全屏 --> 
  <meta name="x5-fullscreen" content="true" /> 
  <!-- QQ强制全屏 --> 
  <meta name="msapplication-tap-highlight" content="no" /> 
  <!-- windows phone 点击无高光 -->
 </head>
 <body></body>
</html>

```
