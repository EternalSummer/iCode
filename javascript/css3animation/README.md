#CSS3动画讲解
##介绍内容

###* transform形变
###* transition动画
###* animation动画

<br/><br/><br/><br/>



#transform部分
---
###   浏览器支持情况
safari 3.1 up、chrome 8 以上、FireFox 4、Opera 10
###   transform功能
transform 实现四种文字、图像的变形处理，分别是旋转、缩放、倾斜、移动。

demo1.html基本使用<br/>

1.rotate(45deg);<br/>
2.scale(水平放大缩小、垂直放大缩小）
3.skew（水平倾斜角度、垂直倾斜角度）<br/>
4.ranslate 用于移动图像或者文字:translate(水平方向移动、垂直方向移动)<br/>

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

<br/><br/><br/><br/>


#Transition部分
----
###浏览器支持
Firefox4 up、Opera 10 up、Safari 3.1 up 、chrome 8 up ,IE 11 up 。

###Transition功能
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
		
		
		
		
		
	
<br/><br/><br/><br/>
#Animation部分
--- 
###浏览器支持
同Transition
###Transtion和Animation不同
Transition功能通过指定属性的开始值与结束值，然后在两个属性值之间进行平滑过渡实现动画效果。

Animation功能通过定义多个关键帧及定义每个关键帧中元素的属性值来实现更为复杂的动画。

	animation-name:指定关键帧集合的名称
	animation-duration:指定完成整个动画需要的时间
	animation-timing-function:实现动画的方法（linear，ease-in,ease-out,ease,ease-in-out）
	animation-delay:延时
	animation-iteration-count:动画执行次数 ，可指定infinite（无限次）
	animation-direction:用于指定动画的执行方向
						normal:初始值（动画执行完毕返回初始值）
						alternate:交替改变动画执行方向
						reverse:反方向执行动画
						alterate-reverse:从反方开始交替改动动画执行方向
	 简写:
	 animation:keyframes名称 动画执行时长 动画实现方法 延时 执行次数 执行方向；