<<<<<<< HEAD
# artDialog
===========

######	优雅的web对话框控件

artDialog 是一个精心设计的对话框控件，它拥有精致的界面与易用的编程接口。

**演示与文档：**

<http://aui.github.com/artDialog/>

## 概述

artDialog 是一个精心设计的 web 对话框控件，它继承与延伸了桌面对话框的特性，拥有细致的用户体验与精致的界面。artDialog 基于 LGPL 协议开源，无论是个人还是商业项目都可免费使用。

## 特点

#### 1. 自适应内容尺寸

>	对话框采用特殊UI结构，无论使用AJAX异步填充内容还是类似tabs等控件导致内容变化，对话框均可自动自适应内容尺寸。

#### 2. 智能文本对齐

>	如果设置了对话框宽度（包括用户通过调节把柄改变了尺寸），对话框中的文本会自动居中或者居左对齐，这些都是使用用CSS实现的。

#### 3. 黄金比例垂直居中

>	对话框默认会采用黄金比例垂直居中弹出，正如网页中重要的内容会被安排在垂直黄金区域一样，这样更舒适。

#### 4. 可定位到元素附近

>	宽屏笔记本用户已经逐渐成为主流，很多时候大幅度的移动鼠标操作也是一个麻烦的事情（尤其是使用触控板），artDialog支持设置在onclick事件触发源弹出，以让用户操作更加便捷。

#### 5. 支持键盘操作

>	* ESC键可关闭对话框。

>	* 若有确定按钮，焦点默认停留在确定按钮上，否则停留在右上角关闭按钮上。

>	* 对话框关闭后焦点将恢复至原来的元素。

### 6. 支持信息无障碍(ARIA)

>	支持读屏器操作，让盲人能够平等的获取信息。


### 7. 友好的API

>	在保持小巧的程序体积之外，artDialog提供了丰富的可选配置与方法。它的API风格统一，简单易用，稍微阅读文档一个示例即可举一反三。

## 用户

* 腾讯
* 盛大
* 中国移动
* 中国电信
* ...

## 更新记录

### 5.0.4

1.	取消focus参数，对话框能自动处理
2.	取消鸡肋的esc参数

### 5.0.3

1.	**支持信息无障碍（ARIA）**
2.	锁屏可限制焦点元素保持在对话框内
3.	对话框关闭后焦点将恢复至原来的元素

### 5.0.2

1.	修复居中可能导致左边框显示不出的问题
2.	取消点击遮罩对话框恢复居中的特性

### 5.0.1

1. 修正重复调用 close 方法出现的错误
2. 修正设定了follow后再使用content()方法导致其居中的问题

### 5.0.0

[重新回到当初的理念：简单、优雅]

1.  follow 不再支持 String 类型
2.  button 参数只支持 Array 类型
3.  button name 成员改成 value
4.  button 增加 id 成员
5.  okVal 参数更名为 okValue, 默认值由 '确定' 改为 'ok'
6.  cancelVal 参数更名为 cancelValue, 默认值由 '取消' 改为 'cancel'
6.  close 参数更名为 beforeunload
7.  init 参数更名为 initialize
8.  title 参数默认值由 '消息' 改为 'message'
9.  time 参数与方法参数单位由秒改为毫秒
10. hide 参数方法更名为 hidden
11. 内部为皮肤增加动态样式 d-state-visible 类
12. 给遮罩增添样式 d-mask 类
13. background 参数被取消, 由 CSS 文件定义
14. opacity 参数被取消, 由 CSS 文件定义
15. **取消拖动特性，改由插件支持**
16. 取消 left 与 top 参数
17. 取消对 ie6 提供 fixed 支持，自动转换为 absolute
18. 取消对 ie6 提供 alpha png 支持
19. 取消对 ie6 提供 select 标签遮盖支持
20. 增加 focus 参数
21. 取消 position 方法
22. 取消对 ``<script type="text/dialog"></script>`` 的支持
23. **取消对 iframe 的支持**
24. title 方法不支持空参数
25. content 方法不支持空参数
26. button 方法的参数不支持数组类型
27. 判断 DOCTYPE, 对 xhtml1.0 以下的页面报告错误
28. 修复 IE8 动态等新内容时没有撑开对话框高度，特意为 ie8 取消 .d-content { display:inline-block }
29. show 参数与方法更名为 visible

### 4.0.0

[严谨的跨浏览器支持、对框架应用提供强大的api支持]

源码：<http://code.google.com/p/artdialog/>

1.	修复刷新框架后脚本报错的问题
2.	修复异步加载 artDialog.js 导致锁屏无法使用的问题
3.	双击遮罩不再直接关闭，而是等同于关闭按钮与取消按钮
4.	修复 IE6 在特殊情况下可能因为 fixed 定位出现 body 背景图片异常
5.	修复部分皮肤在 firefox7.0 版下，标题栏出现省略号的问题
6.	修复 v4.0.5 之后版本在浏览器窗口调节的时候可能出现对话框变形问题
7.	top 参数黄金比例不再采用单独的关键字，可使用 '38.2%' 表示
8.	**新增 content 扩展方法写入消息后，让对话框以自身为中心放大的特性**
9.	增加高亮按钮的样式：确定按钮默认高亮（自定义按钮可使用focus参数高亮）
10.	解决IE浏览器按钮字体模糊问题
11.	jQuery版本最低兼容jQuery 1.3.2
12.	新增artDialog 基本版本；它只拥有核心功能，文件只有常规版本的一半大小，可被客户端快速载入
13.	精简内嵌事件系统，进一步减少体积(压缩版比上一版本少近了3kb)
14.	iframeTools: open方法默认不再强制锁屏
15.	增强icon参数自由度，不再依赖对话框样式文件定义。可存入任意图标到“skins/icons/”并使用它们
16.	iframeTools: 拖拽操作增加透明遮罩，防止鼠标指针落入框架而导致监听失败，提高拖拽流畅性
17.	iframeTools: 对open方法增加一个私有的iframe扩展方法，用来引用其创建的iframe对象
18.	新增点击内容部分也可以如点击标题一样置顶对话框的特性
19.	iframeTools： 增加父页面刷新与关闭后子对话框也将关闭的特性。（由于iframe注销后其产生的对象会被大多数浏览器在内存中移除，增加此特性可以有效的解决对话框报错）
20.	**DOM底层api兼容jQuery api，同步发行jQuery版本**
21.	**消息内容支持传入DOM元素**
22.	增加title标题接口
23.	增加button自定义按钮接口
24.	增加lock与unlock接口
25.	新增data方法用来在iframe之间共享数据
26.	重定义zIndex配置参数
27.	重新支持调节对话框大小
28.	支持用第三方框架加载自身
29.	**配置参数全部为可选，如果没有content，它将出现loading动画**
30.	left与top关键字用百分比代替，同时增加width与height传递百分比参数
31.	更好的支持iframe
32.	修复若干BUG

### 3.0.0

[初次支持框架]

1.	修复iPad或iPhone下使用锁屏焦点自动弹出的问题
2.	修复移动设备使用手势缩放页面带来的漂移问题
3.	修复fixed在移动设备中支持不完整的问题
4.	修复window.top是框架集(frameset)页面可能会带来无限循环递归的问题
5.	增加art.dialog.get()方法获取指定ID对话框API
6.	修复框架集（frameset）页面不能植入artDialog而产生js报错的问题，并增加了其支持
7.	公开默认配置的读写
8.	重写IE6 fixed实现

### 2.0.0

[进一步封装]

1.	**支持多对话框共存**
2.	支持返回扩展方法关闭对话框
3.	解决v1已知的一些BUG

### 1.0.0

[诞生]

1.	**高度与宽度支持原生自适应内容，自适应文本对齐**
2.	支持拖动、Esc关闭对话框、坐标定位
3.	**支持自适应位置**
4.	**支持IE6无抖动静止定位**
=======
#	artDialog

artDialog——经典、优雅的网页对话框控件。
文档与示例：<http://aui.github.io/artDialog/doc/index.html>

##	成功案例

超过 40 万网站在使用 artDialog，其中不乏国内顶尖的产品：

*	[QQ空间 v8（腾讯）](http://qzone.qq.com)
*	[Phpcms（盛大）](http://www.phpcms.cn)
*	[极路由](http://www.hiwifi.com)
*	...

##	更新历史

6.0.4

1. ``content()``方法传入隐藏元素并显示，并且``remove()``的时候会将元素插入到``body``避免被销毁 [#103](https://github.com/aui/artDialog/issues/103) [#126](https://github.com/aui/artDialog/issues/126)
2. 修复``button``方法可能会多次绑定事件的问题
3. 模态对话框可以避免 shift + tab 将焦点移出对话框 [#67](https://github.com/aui/artDialog/issues/67)

6.0.3

1. 修复``button``方法直接传入 html 不显示的问题
2. 修复版本管理导致[#78](https://github.com/aui/artDialog/issues/78)重现问题

6.0.2

1. 提供无依赖 seajs 与 requirejs 的版本
2. 取消按钮增加``cancelDisplay``配置，保留``cancel``事件的同时也不会显示取消按钮

6.0.1

1. 进一步完善焦点管理，避免抢夺开发者自己设置的焦点[#67](https://github.com/aui/artDialog/issues/67)
2. 修复对话框内容使用 html5 data-id 属性冲突的问题[#78](https://github.com/aui/artDialog/issues/78)
3. 改善 Esc 快捷键与 cancel 的问题[#36](https://github.com/aui/artDialog/issues/36)

6.0.0

1. 功能增强：支持定义左下角的区域 HTML、支持 12 个方向的气泡对话框、支持无标题栏与按钮区的对话框
2. 更好的交互体验：更加先进的焦点管理，支持无障碍访问
3. 面向未来：基于 HTML5 Dialog 的 API
4. 模块化：支持 AMD、CMD 规范
5. 可选增强版：拖拽支持、简化框架页面调用

##	授权协议

免费，且开源，基于[LGPL](./LICENSE.md)协议。

------------------

*artDialog，因极致而骄傲！——作者，糖饼*
>>>>>>> 9fd667e0ced31a4757f10a1c49f3cb29eb951a95
