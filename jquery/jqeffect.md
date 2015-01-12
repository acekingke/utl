[TOC]

# jquery特效

## hide and show


通过 jQuery，您可以使用 hide() 和 show() 方法来隐藏和显示 HTML 元素：

```
$("#hide").click(function(){
  $("p").hide();
});

$("#show").click(function(){
  $("p").show();
});
```

*语法：*
`$(selector).hide(speed,callback);`

`$(selector).show(speed,callback);`
可选的 speed 参数规定隐藏/显示的速度，可以取以下值："slow"、"fast" 或毫秒。
可选的 callback 参数是隐藏或显示完成后所执行的函数名称。
下面的例子演示了带有 speed 参数的 hide() 方法：
实例
```$("button").click(function(){
  $("p").hide(1000);
});```



## jQuery toggle()
通过 jQuery，您可以使用 toggle() 方法来切换 hide() 和 show() 方法。
显示被隐藏的元素，并隐藏已显示的元素：
实例```
$("button").click(function(){
  $("p").toggle();
});```
 
语法：
`$(selector).toggle(speed,callback);`
可选的 speed 参数规定隐藏/显示的速度，可以取以下值："slow"、"fast" 或毫秒。
可选的 callback 参数是 toggle() 方法完成后所执行的函数名称。


## jQuery 效果函数
|方法	|描述
---:--|---:------
animate()	|对被选元素应用“自定义”的动画
clearQueue()|	对被选元素移除所有排队的函数（仍未运行的）
delay()	|对被选元素的所有排队函数（仍未运行）设置延迟
dequeue()	|运行被选元素的下一个排队函数
fadeIn()	|逐渐改变被选元素的不透明度，从隐藏到可见
fadeOut()	|逐渐改变被选元素的不透明度，从可见到隐藏
fadeTo()	|把被选元素逐渐改变至给定的不透明度
hide()	|隐藏被选的元素
queue()	|显示被选元素的排队函数
show()	|显示被选的元素
slideDown()	|通过调整高度来滑动显示被选元素
slideToggle()|	对被选元素进行滑动隐藏和滑动显示的切换
slideUp()	|通过调整高度来滑动隐藏被选元素
stop()	|停止在被选元素上运行动画
toggle()	|对被选元素进行隐藏和显示的切换

## 回调函数
例子
```
$("p").hide(1000,function(){
alert("The paragraph is now hidden");
});
```
## jquery链

可以做一个连串动作
```$("#p1").css("color","red").slideUp(2000).slideDown(2000);```