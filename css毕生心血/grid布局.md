# Css Grid layout

```html
display:grid #网格布局
display:inline-grid #生成一个内联网格
```

### grid-template-columns/rows

```
grid-template-columns:(1fr 1fr 1fr) 定义多少个列
grid-template-rows:(1fr 1fr)	定义多少个行
参数：
– <track-size>： 可以是长度值，百分比，或者等份网格容器中可用空间（使用 fr 单位）
– <line-name>：你可以选择的任意名称
```

### grid-template-areas

- `<grid-area-name>`：由网格项的 [`grid-area`](https://www.css88.com/archives/8510#prop-grid-area) 指定的网格区域名称
- `.`（点号） ：代表一个空的网格单元
- `none`：不定义网格区域

```php+HTML
.container {
  grid-template-areas: 
    "<grid-area-name> | . | none | ..."
    "...";
    
    比如" h h h h .
    	 e e e e ." 对应 5 *2 个网格
    
}
```

```html
.item-a {
  grid-area: header;  #这个是网格项
}
.container {
  grid-template-columns: 50px 50px 50px 50px;
  grid-template-rows: auto;
  grid-template-areas: 
    "header header header header"
    "main main . sidebar"
    "footer footer footer footer";
}
```

### grid-column-gap / grid-row-gap

指定网格线的大小。你可以把它想象为设置列/行之间间距的宽度。

```html
.container {
  grid-column-gap: <line-size>;
  grid-row-gap: <line-size>;
}
```

```
.container {
  grid-gap: <grid-row-gap> <grid-column-gap>;#grid-gap是前面整合版本
}
```

### justify-items

沿着 *inline*（行）轴线对齐网格项(grid items)（相反的属性是 [`align-items`](https://www.css88.com/archives/8510#prop-align-items) 沿着 *block*（列）轴线对齐）。此值适用于容器内的所有网格项。

- `start`：将网格项对齐到其单元格的左侧起始边缘（左侧对齐）
- `end`：将网格项对齐到其单元格的右侧结束边缘（右侧对齐）
- `center`：将网格项对齐到其单元格的水平中间位置（水平居中对齐）
- `stretch`：填满单元格的宽度（默认值）

```
.container {
  justify-items: start | end | center | stretch;
}
```

### align-items

沿着 *block*（列）轴线对齐网格项(grid items)（相反的属性是 [`justify-items`](https://www.css88.com/archives/8510#prop-justify-items) 沿着 *inline*（行）轴线对齐）。此值适用于容器内的所有网格项。

值：

- `start`：将网格项对齐到其单元格的顶部起始边缘（顶部对齐）
- `end`：将网格项对齐到其单元格的底部结束边缘（底部对齐）
- `center`：将网格项对齐到其单元格的垂直中间位置（垂直居中对齐）
- `stretch`：填满单元格的高度（默认值）

```
.container {
  align-items: start | end | center | stretch;
}
```

### place-items

前面两个的整合

### justify-content

有时，你的网格合计大小可能小于其 网格容器(grid container) 大小。 如果你的所有 网格项(grid items) 都使用像 `px` 这样的非灵活单位设置大小，就可能出现这种情况。在这种情况下，您可以设置网格容器内的网格的对齐方式。 此属性沿着 *inline*（行）轴线对齐网格（相反的属性是 [`align-content`](https://www.css88.com/archives/8510#prop-align-content) ，沿着 *block*（列）轴线对齐网格）。

值：

- `start`：将网格对齐到 网格容器(grid container) 的左侧起始边缘（左侧对齐）
- `end`：将网格对齐到 网格容器 的右侧结束边缘（右侧对齐）
- `center`：将网格对齐到 网格容器 的水平中间位置（水平居中对齐）
- `stretch`：调整 网格项(grid items) 的宽度，允许该网格填充满整个 网格容器 的宽度
- `space-around`：在每个网格项之间放置一个均匀的空间，左右两端放置一半的空间
- `space-between`：在每个网格项之间放置一个均匀的空间，左右两端没有空间
- `space-evenly`：在每个网格项目之间放置一个均匀的空间，左右两端放置一个均匀的空间

```
.container {
  justify-content: start | end | center | stretch | space-around | space-between | space-evenly;    
}
```

### align-items

有时，你的网格合计大小可能小于其 网格容器(grid container) 大小。 如果你的所有 网格项(grid items) 都使用像 `px` 这样的非灵活单位设置大小，就可能出现这种情况。在这种情况下，您可以设置网格容器内的网格的对齐方式。 此属性沿着 *block*（列）轴线对齐网格（相反的属性是 [`justify-content`](https://www.css88.com/archives/8510#prop-justify-content) ，沿着 *inline*（行）轴线对齐网格）。

- `start`：将网格对齐到 网格容器(grid container) 的顶部起始边缘（顶部对齐）
- `end`：将网格对齐到 网格容器 的底部结束边缘（底部对齐）
- `center`：将网格对齐到 网格容器 的垂直中间位置（垂直居中对齐）
- `stretch`：调整 网格项(grid items) 的高度，允许该网格填充满整个 网格容器 的高度
- `space-around`：在每个网格项之间放置一个均匀的空间，上下两端放置一半的空间
- `space-between`：在每个网格项之间放置一个均匀的空间，上下两端没有空间
- `space-evenly`：在每个网格项目之间放置一个均匀的空间，上下两端放置一个均匀的空间

```
.container {
  align-content: start | end | center | stretch | space-around | space-between | space-evenly;  
}
```

