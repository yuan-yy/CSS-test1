# css 所有的居中方式（仅限参考)

```
<div>
	<div><div>
</div>
```

### 1、水平居中

##### 	方式一（推荐)

```
  div:nth-of-type(1){
        width: 100px;
        height: 100px;
        border: 1px solid black;
    }
    div:nth-of-type(1)>div{
        margin:  0 auto;
        width:50px;
        height: 40px;
        border: 1px solid black;
    }
```

##### 方式二：子元素设置为display:inline-block(不推荐)

```
    div:nth-of-type(1){
        width: 100px;
        height: 100px;
        border: 1px solid black;
        text-align: center;
    }
    div:nth-of-type(1)>div{
        display: inline-block;
        width:50px;
        height: 40px;
        border: 1px solid black;
    }
```

##### 	方式三 利用绝对定位，父亲设置相对定位，左右为设置为0

```
div:nth-of-type(1){
        position: relative;
        width: 100px;
        height: 100px;
        border: 1px solid black;
        text-align: center;
    }
    div:nth-of-type(1)>div{
        position: absolute;
        left:0;
        right: 0;
        margin: auto;
        width:50px;
        height: 40px;
        border: 1px solid black;
    }
```

##### 	方式四 利用flex布局来实现

```
    div:nth-of-type(1){
        display: flex;
        flex-direction: row;
        justify-content: center;
        width: 100px;
        height: 100px;
        border: 1px solid black;
        text-align: center;
    }
    div:nth-of-type(1)>div{
        width:50px;
        height: 40px;
        border: 1px solid black;
    }
```



### 2、垂直居中

##### 	方式一 利用绝对定位

```
    div:nth-of-type(1){
       position: relative;
        width: 100px;
        height: 100px;
        border: 1px solid black;
        text-align: center;
    }
    div:nth-of-type(1)>div{
        position: absolute;
        top:0;
        bottom:0;
        margin:auto;
        width:50px;
        height: 40px;
        border: 1px solid black;
    }
```

##### 方式二 利用flex布局来实现

```
  div:nth-of-type(1){
        display: flex;
        align-items: center;
        width: 100px;
        height: 100px;
        border: 1px solid black;
        text-align: center;
    }
    div:nth-of-type(1)>div{
      
        width:50px;
        height: 40px;
        border: 1px solid black;
    }
```

### 3 水平加垂直居中

#### 1、对内容进行居中

​		

```
text-align:center
```

​	利用CSS进行元素的水平居中，比较简单，行级元素设置其父元素的text-align center，

```
line-height:200px #这里的200px为行的高度。自然内容就可以居中
```



​	

#### 2、使用display：flex 布局

```
 div:nth-of-type(1){
        display: flex;
        flex-direction: row;
        justify-content: center;
      	align-items: center;
        }
```

#### 3、使用定位position 来居中

##### 	方式一（不推荐)

```
div:nth-of-type(1){
        position: relative;
        width: 100px;
        height: 100px;
        border: 1px solid black;
    }
    div:nth-of-type(1)>div{
        position: absolute;
        top:50%;
        left:50%;
        margin-top:-20px;
        margin-left: -25px;
        width:50px;
        height: 40px;
        border: 1px solid black;
    }
```

##### 	方式二（推荐)

```
    div:nth-of-type(1){


        position: relative;
        width: 100px;
        height: 100px;
        border: 1px solid black;
    }

    div:nth-of-type(1)>div{
        position: absolute;
        top:0;
        left: 0;
        right: 0;
        bottom:0;
        margin:auto;
        width:50px;
        height: 40px;
        border: 1px solid black;
    }
```

​	

