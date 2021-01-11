# CSS之阴影

## box-shadow 常规用法

`box-shadow` 属性向框添加一个或多个阴影。

```
box-shadow: h-shadow v-shadow blur spread color inset;
```

像这样 `box-shadow: 10px 10px 5px #888888;` 除此之外，我们要知道，box-shadow 是分外 shadow 和内 shadow 的，内阴影即是在属性上添加 inset 。

```
   box-shadow:
            /* 右阴影 */
            10px 0 1px #eeeeee,
            /* 左阴影 */
            -10px 0 1px #eeeeee,
            /* 下阴影 */
            0px 10px 1px #eeeeee,
            /* 上阴影 */
            0px -10px 1px #eeeeee;

        ;
```

```
nth-child
按照个数来算。

nth-of-type
按照类型来计算，如果是class那么碰到不同类型的，单独一类，符合条件的选中。0
```

