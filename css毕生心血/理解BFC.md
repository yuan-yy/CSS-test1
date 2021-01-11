### 如何去触发bfc

1.float不为none

2.position不为relative和static

3.overflow为auto scroll和hidden

4.display的值为table-cell或inline-block







### 通过触发bfc解次的问题

#### 1、浮动元素的父元素高度塌陷

```
<style>
    .box > div{
        width: 200px;
        height: 200px;
        background-color: darkcyan;
        margin: 20px;
        float: left;
        
    }
    .box{
        background-color: red;
        /* 利用postion来触发BFC */
        position: absolute;
    }
</style>
<body>
    <div class="box" >
    <div></div>
    <div></div>
    <div></div>
    <div></div>
    <div></div>
</div>
</body>
```

#### 2、两栏自适应布局

​	1、左边飘起来，右边使用定位 利用margin-left

```
<style>
    .left{
        width:300px;
        height: 600px;
        background-color: darkblue;
        float: left;
    }
    .right{
        position: relative;
        margin-left: 300px;
        height: 600px;
        background-color: darkkhaki;
    }
</style>
<body>
    <div class="left"></div>
    <div class="right"></div>
</body>
```

#### 	2、左边使用绝对定位 右边使用margin-left

```
<style>
    *{
        margin: 0;
        padding: 0;
    }
    .left{
        position:absolute;
         top:0;
         bottom:0;
        width: 200px;
        background-color: yellow;
    }
    .right{

        right: 0;
        margin-left: 200px;
    height: 600px;        
        background-color: darkmagenta;

    }
</style>
<body>
    <div class="left"></div>
    <div class="right"></div>
</body>
```

#### 3、左右两边都使用绝对定位positon:absolute

```
<style>
    *{
        margin: 0;
        padding: 0;
    }
    .left{
        position:absolute;
        left: 0;
         top:0;
         bottom:0;
        width: 200px;
        
        background-color: yellow;
    }
    .right{

     position: absolute;
     top:0;
     right: 0;
     height: 100%;
     left: 200px;
     background-color: blue;

    }
</style>
<body>
    <div class="left"></div>
    <div class="right"></div>
</body>
```

3、外边距垂直方向重合

```
<style>
    .box1,.box2 {
        width: 200px;
        height: 200px;
        background-color: darkgoldenrod;
        margin: 20px;
    }
    .box3 {
        overflow: hidden;
    }
    .box1{
        margin:40px;
    }
</style>
<body>

    <div class="box1"></div>
    <div class="box3">
        <div class="box2"></div>
    </div>
</body>
```

