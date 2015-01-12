[TOC]
# jquery 例子
http://www.w3school.com.cn/jquery/
下面的例子展示如何将文本点击隐藏。
jquery源码目录有很庞大的代码，使用grunt将他们合成一个文件。
```
<html>
<head>
<script type="text/javascript" src="jquery.js"></script>
<script type="text/javascript">
$(document).ready(function(){
  $("p").click(function(){
  $(this).hide();
  });
});
</script>
</head>

<body>
<p>If you click on me, I will disappear.</p>
</body>

</html> 
```
实际上，jquery代码如果要想分析其思路，就要做如下一些特殊的处理。直接分析代码，而不是分析编译好的代码。
```
<!DOCTYPE html>
<html>
<head>

    <title>jquery sample</title>
    <script src="./require.js"></script>
    
    <script type="text/javascript">
        require(['./bower_components/jquery/src/core.js'], function($) {
            console.log($);

        })
    </script>
</head>
<body>
<p>If you click on me, I will disappear.</p>
</body>
</html>
```

## code.js心得

升级webstrom版本，又可以快乐玩耍了。
jQuery之所以这么好用, 首先一点就是$()方法和它强大的选择器. 其中选择器使用的是sizzle引擎, sizzle是jQuery的子项目, 提供高效的选择器查询. 有个好消息告诉大家, 就是sizzle可以独立使用, 如果你觉得jQuery太大但又非常喜欢它的选择器, 那不妨可以用sizzle. 感兴趣的话可以到官方网站了解.

### jQuery的"栈"
比如查找某个列表下的链接可以用 $("#some-list").children("li").find("a")
实际上jquery构造了一个栈，能获取上一层的结果。

jquery关键的技术就在此处，后面是都是jquery实现的包

## requirejs的使用

requirejs是一个js模块加载的功能。

require(["xxx", "yyy"] function(xxx, yyy)
{
  xxx.fun1()
  yyy.fun2()
})

其实就是将xxx.js和yyy.js执行，将函数对象赋值给function中的xxx，和yyy

假定现在有一个math.js文件，它定义了一个math模块。那么，math.js就要这样写：
```js
　　// math.js
　　define(function (){
　　　　var add = function (x,y){
　　　　　　return x+y;
　　　　};
　　　　return {
　　　　　　add: add
　　　　};
　　});
```
加载方法如下：
```
　　// main.js
　　require(['math'], function (math){
　　　　alert(math.add(1,1));
　　});
```
[下一章:选择器](./jqueryselect.html)

