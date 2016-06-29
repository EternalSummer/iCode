#CSS3动画讲解
##介绍内容
###1.transform形变
###2.transition动画
###3.animation动画



##transform 形变

###   浏览器支持情况
safari 3.1 up、chrome 8 以上、FireFox 4、Opera 10
###   transform功能
transform 实现四种文字、图像的变形处理，分别是旋转、缩放、倾斜、移动。

demo1.html 基本使用
#####rotate(45deg);
#####scale(水平放大缩小、垂直放大缩小）
#####skew（水平倾斜角度、垂直倾斜角度）
#####translate 用于移动图像或者文字:translate(水平方向移动、垂直方向移动)

demo2.html 同一个元素使用多种变形

demo3.html 指定变形的基准点
默认以元素的中心点 为基准点可以通过transform－origin改变基准点。

transform-origin(水平方向的基准点位置left center right,垂直方向的基准点位置 top center bottom);


###Transform之3D变形功能

实现X轴 Y轴 Z轴方向上的旋转、缩放、倾斜、移动。

案例中需要使用JS定时调用讲解:

setInterval() 方法可按照指定的周期（以毫秒计）来调用函数或计算表达式。
setInterval() 方法会不停地调用函数，直到 clearInterval() 被调用或窗口被关闭。由 setInterval() 返回的 ID 值可用作 clearInterval() 方法的参数。

1.旋转
rotateX(),rotateY(),rotateZ().




#Transition部分
###浏览器支持
Firefox4 up、Opera 10 up、Safari 3.1 up 、chrome 8 up ,IE 11 up 。

##Transition功能
通过将元素的某个属性从一个属性值在指定时间内平滑过渡到另一个属性值来实现动画
	
	用法：
	transition:property duration timing-function transition-delay;
	其中：property表示对哪个属性进行平滑过渡。
		 duration表示在多久时间内完成属性值的平滑过渡。
		 timing-function表示通过什么方法进行平滑过渡。
		 transition-delay:指定延时多少时间才真正开始执行。
	分开写：
		transition-property:background-color;
		transition-duration:1s;
		transition-timing-function:linear;
		transition-delay:2s;
	
