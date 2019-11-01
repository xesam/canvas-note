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

lineWidth
lineCap
lineJoin
miterLimit

## 圆弧

arc


## 合成

定义和用法
globalCompositeOperation 属性设置或返回如何将一个源（新的）图像绘制到目标（已有）的图像上。

源图像 = 您打算放置到画布上的绘图。

目标图像 = 您已经放置在画布上的绘图。


默认值：	source-over
JavaScript 语法：	context.globalCompositeOperation="source-in";
属性值
值	描述
source-over	默认。在目标图像上显示源图像。
source-atop	在目标图像顶部显示源图像。源图像位于目标图像之外的部分是不可见的。
source-in	在目标图像中显示源图像。只有目标图像内的源图像部分会显示，目标图像是透明的。
source-out	在目标图像之外显示源图像。只会显示目标图像之外源图像部分，目标图像是透明的。
destination-over	在源图像上方显示目标图像。
destination-atop	在源图像顶部显示目标图像。源图像之外的目标图像部分不会被显示。
destination-in	在源图像中显示目标图像。只有源图像内的目标图像部分会被显示，源图像是透明的。
destination-out	在源图像外显示目标图像。只有源图像外的目标图像部分会被显示，源图像是透明的。
lighter	显示源图像 + 目标图像。
copy	显示源图像。忽略目标图像。
xor	使用异或操作对源图像与目标图像进行组合。

## 文字

文本
属性	描述
font	设置或返回文本内容的当前字体属性
textAlign	设置或返回文本内容的当前对齐方式
textBaseline	设置或返回在绘制文本时使用的当前文本基线

方法	描述
fillText()	在画布上绘制“被填充的”文本
strokeText()	在画布上绘制文本（无填充）
measureText()	返回包含指定文本宽度的对象



# ImageData

ImageData 的 width 属性是设备像素



JavaScript 语法：
context.putImageData(imgData,x,y,dirtyX,dirtyY,dirtyWidth,dirtyHeight);
参数值
参数	描述
imgData	规定要放回画布的 ImageData 对象。
x	ImageData 对象左上角的 x 坐标，以像素计。（CSS像素）
y	ImageData 对象左上角的 y 坐标，以像素计。（CSS像素）
dirtyX	可选。水平值（x），以像素计，在画布上放置图像的位置。（设备像素）
dirtyY	可选。水平值（y），以像素计，在画布上放置图像的位置。（设备像素）
dirtyWidth	可选。在画布上绘制图像所使用的宽度。（设备像素）
dirtyHeight	可选。在画布上绘制图像所使用的高度。（设备像素）















































