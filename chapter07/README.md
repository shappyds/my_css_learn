盒模型相关知识
============

## 元素框

每个元素都会生成一个或者多个矩形框，这成为元素框。各元素框中心有一个内容区(content area)，内容区周围还有可选的内边距、边框、外边距。

外边距通常是透明的，从中可以看到父元素的背景。

内边距不能是负值，而外边距可以。

## 块级元素-水平格式化

一个元素的width等于内容区的宽度，height等于内容区的高度。

width影响的是内容区的宽度，而不是整个可见的元素框。

可见的元素框 = 内容区 + 内边距 + 边框

整个元素框的宽度 = 可见的元素框 + 外边距

正常流中，**块级元素框的水平部分等于父元素的width**。

只有width、margin-left和margin-right可以设置为auto，这里面最大的原则是width最贪心，设置为auto时会越大越好。具体的情况有：

1. 当width和margin其中一个为auto，而另一个为定值时，这时候设置为auto的那个margin为0；    
2. 当三个都为auto时，则这时候margin都为0，width会尽可能宽。
3. 只设置width时，margin-left为0，margin-right为auto。
4. 三个都为定值时，而总大小小于父元素的width时，则margin-right强制设为auto.
5. width定值，margin-left和right为auto时，两个margin值相同，元素在父元素居中。

## 块级元素-垂直格式化

在正常流中，如果一个块元素的margin-top和margin-bottom设置为auto，那么它会**自动被计算为0**.


## 行内元素

外边距不会应用到行内非替换元素的顶端和底端