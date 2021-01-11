#			css选择器



#### 1、什么是css选择器

​	就是改变样式的对象

#### 2、有哪些选择器

​	2.1 类选择器

```
.box1{
        width:200px;
        height: 200px;
        background-color: darkorchid;
    }
```

​	2.2 id选择器

```
#box1-id{
        background-color: darkred;
    }
```

​	2.3 标签选择器

```
 div{
        width:200px;
        height: 200px;
        background-color: darkturquoise;
    }
```

​	2.4 群组选择器

```
    .box1,.box2{
        width: 200px;
        height: 200px;
        background-color: darkorange;
        margin-top: 20px;
    }
```

​	2.5 包含选择器

```
.box1 .box1-child {
        width:100px;
        height: 100px;
        background-color: darkseagreen;
    }
```

```
  .box1 > .box1-child{
        width:100px;
        height: 150px;
        background-color: darkseagreen;
    }
```

​	 2.6 相邻兄弟选择器

​	

```
.box1-child + div{
        background-color: brown;
    }
```

