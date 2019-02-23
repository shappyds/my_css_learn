颜色和背景
=========

## 前景色

前景是元素的文本，还包括元素周围的边框。因此，有两种方式可以影响一个元素的前景色：`color`和使用边框属性设置边框颜色。

`color`值可以影响元素周围的边框，假设`color`已经声明而`border-color`没有设置，那么边框颜色会与`color`的值一致。

`color`是可以继承的

## 背景色

`background-color`是不可继承的

## 背景颜色

默认是水平平铺，可以通过`background-repeat`来进行有方向的重复。

`background-repeat: no-repeat | repeat-x | repeat-y`