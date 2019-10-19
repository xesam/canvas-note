设置 canvas 的尺寸的时候，不应该使用 px 单位，这是不被canvas 规范所接受的。

canvas 实际上有两套尺寸：

1. canvas 元素本身的大小
2. 元素绘图表面（drawing surface）的大小

其他的操作系统里面有类似的问题吗？android 好像没有。


## canvas 

两个属性，三个方法：

1. width
2. height

getContext()
getDataURL(type, quality)
toBlob(callback, type, ...args)

## 2D Context 

全部属性：

## save() restore()

堆栈，绘图环境

这里的“绘图环境”包括哪些内容呢？

包括：

1. 坐标变换信息
2. 剪辑区域
3. Context 属性

不包括：

1. 路径。路径只能通过 beginPath 来重置路径
2. 位图。这是 canvas 的属性



## 矩形

clearRect
strokeRect
fillRect

## style
为什么 strokeStyle 和 fillStyle 不叫 strokeColor 和 fillColor？因为除了使用 Color ，还可以使用 CanvasGradient 以及 图案。


## CanvasGradient

线性渐变

放射渐变

## 阴影

context.shadowColor
context.shadowOffsetX
context.shadowOffsetY
context.shadowBlur

## 路径

context.arc
context.beginPath
context.closePath
context.fill
context.rect
context.stroke


## 子路径

    According to the Canvas specification, when you call the arc() method and an
    existing subpath is in the current path, the method must connect the last point
    in the existing subpath to the first point on the arc.
    
## 路径方向很重要 ！！

## 线段





























































