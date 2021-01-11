# 详解transform+transition+animation（包看包会）

## 1、transform(变形)

对元素进行移动、缩放、转动、拉长或拉伸

```
参数：translate(100px) 向右移动移动
	 scale(1.5,0.5)   x轴扩大到1.5倍，y轴扩大到0.5倍
	 skew(20deg,20deg)  根据给定的水平线（X 轴）和垂直线（Y 轴）参数
```

如图所示，为scale对元素进行缩放

![image-20210108112539543](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\image-20210108112539543.png)

## 2、transition（过度)

```
参数： transition-property:指定CSS属性的name，transition效果
			none     没有属性
			all      所有属性
			property 定义应用过渡效果的 CSS 属性名称列表，列表以逗号分隔。
	  transition-delay:	定义transition效果开始的时候,也就是反应时间。
      		.4s     为0.4秒
	  transition-duration: 动画的持续时间
	  		5s       为5秒
	  transition-timing-function:动画的方式
	  		linear	规定以相同速度开始至结束的过渡效果
            ease	规定慢速开始，然后变快，然后慢速结束的过渡效果。
            ease-in	规定以慢速开始的过渡效果
            ease-out	规定以慢速结束的过渡效果
            ease-in-out	规定以慢速开始和结束的过渡效果
            cubic-bezier(n,n,n,n):在 cubic-bezier 函数中定义自己的值。可能的值是 0 至 1 之间的数值。		
            
       理解关键的网站:https://cubic-bezier.com/
       可以把参数都写在一起：
		transition{ transition-property  transition-duration  transition-timing-function  transition-delay}来用
```



附一：自己调试代码，可以根据自己想要的情况，删除或增加注释。（看不懂，直接去吃屎）

```
   .box2 {
        width: 100px;
        height: 100px;
        margin: 100px auto;
        background-color: darkgoldenrod;
        /* transform: skew(20deg,20deg); */
        /* transition-property: width; */
        transition-property: all;
        transition-delay: .4s ;
        transition-duration: 1s;
        transition-timing-function:cubic-bezier(.19,-0.97,.82,1.86);
    }
    .box2:hover{
        width:300px;
        height: 300px;
        border-radius: 50%;
        background-color: blue;
        transform: rotate(180deg);
    }
</style>
<body>
        <div class="box2"></div>
</body>
```



## 3、animation（动画)



```
参数：
	animation-name:name  定义动画的名字
	animation-duration:5s 动画整个过程需要的时间
	animation-delay:.9s   动画开始时的反应时间
	animation-direction:normal 动画的方向
	animation-timing-function:cubic-bezier(n,n,n,n); 动画执行的方式

```



