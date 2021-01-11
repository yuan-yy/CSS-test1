# css 之float样式

### 1、简介（作用的对象和参数)

float:html的标签

​		div span  a em 等等

### 2、float的用法

```
<style>
    div{
        width:60px;
        height: 60px;
        background-color: darkgray;
        margin: 20px;
        float:right
    }
</style>
<body>
    <div></div>
    <div style="background-color: red; float: left;" ></div>
    <div></div>
    <div style="background-color: black;"></div>
</body>
```



### 3、float样式应用

```
<style>

    .top{
        width:1129px;
        height: 50px;
        background-color: black;
        color: white;
        line-height: 50px;
    }
    .top span{
        float:left;
        margin-right: 20px;
    }
    .middle{
        width:1129px;
        height: 50px;
        background-color: darkgray;
    }
    .content{
        width: 1129px;
        height: 800px;
    }
    .content .content-left{
        width:70%;
        height: 100%;
        background-color: darkgreen;
        float: left;
        
    }
    .content .content-right{
        width:30%;
        height: 100%;
        background-color: darkgoldenrod;
        float: right;
        
    }
</style>
<body>
    <div class="box">
        <div class="top">
            <span>首页</span>
            <span>问答</span>
            <span>树洞</span>
            <span>动物园</span>
           
            <span style="float:right">鱼塘</span>
            <span style="float:right">走边</span>
        </div>
        <div class="middle"></div>
        <div class="content">
            <div class="content-left"></div>
            <div class="content-right"></div>   
        </div>
    </div>
</body>
</html>
```

