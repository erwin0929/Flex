## Flex学习总结

> 传统布局

 本文非教程,故只做文字总结,不使用图片说明。  
 本文以'阮一峰的flex布局教程'为蓝本,借鉴了教程中的部分内容,在自身完全理解的情况下才写下本文。  
 传统的布局方式基于盒模型,依赖`display` `position` `float`等属性来完成。  
 大多情况下能确实能制作日常需求,但对于个别案例来说显得力不从心,比如垂直居中就不容易实现。  
 附上我网上找的布局,几个小栗子来练手,纯手写绝无复制粘贴。  
 ### <a href="https://erwin0929.github.io/Flex/" target="_blank">[练习demo]</a>
 
> Flex

该布局方式可以响应式地实现各种页面布局,并且得到众多浏览器的支持。  
Flex 又称为'弹性布局',为盒模型提供了更多的灵活性和扩展性。

> display:flex

任何容器都可转变为`flex`。
```
.box{
  display: flex;
}
```
该属性使元素变为`flex`,设置该属性时子元素的`float` `clear` `vertical-align` 将失效。
`flex`容器的子元素称为'item:项目'。  
容器拥有2根轴线,水平的主轴以及垂直的交叉轴。  

> `flex-direction`

决定主轴的方向,默认为水平方向。  
该属性有4个可选值:  
* `row` 主轴为水平方向,项目排列以`左端`为起点。
* `row-reverse` 主轴为水平方向,项目排列以`右端`为起点。
* `column` 主轴为垂直方向,项目以上下排列,起点在上方。
* `column-reverse` 主轴为垂直方向,起点在下方。

> `flex-wrap`

默认情况下项目排列在同一行,又称为'轴线'。该属性定义换行方式,3个可选值:
* `nowrap` 不换行。
* `wrap` 换行,第一行在上方。
* `wrap-reverse` 换行,第一行在下方。

> `justify-content` 

该属性定义项目在水平轴上的对齐方式,5个可选值:
* `flex-start` 左对齐。
* `flex-end` 右对齐。
* `center` 居中对齐。
* `space-between` 两端对齐,项目之间间隔相等。
* `space-around` 项目两侧间隔相等。

> `align-items`

该属性定义项目在交叉轴上的对齐方式,5个可选值:  
* `flex-start`  交叉轴的起点对齐。
* `flex-end` 交叉轴的终点对齐。
* `center` 垂直居中对齐。
* `baseline` 以项目第一行文字的基线对齐。
* `stretch` 默认值,撑满整个容器。

> `align-content` 

该属性定义多根轴线的对齐方式,6个可选值:  

* `flex-start` 与交叉轴起点对齐。
* `flex-end` 与交叉轴终点对齐。
* `center` 居中对齐
* `space-between` 与交叉轴两端对齐
* `space-around` 每根轴线两侧的间隔都相等
* `stretch`

> 项目的属性: `order` 

* 定义项目的排列顺序,值越小越靠前。  

> `flex-grow`

* 项目的放大比例,默认为0,存在剩余空间也不放大。  
* 如果项目都为1,则等分空间。
* 如果一个为0,一个为1,0值自适应宽度,1占满剩余空间。

> `flex-shrink`

* 定义项目缩小比例,默认为1,空间不足,项目自动缩小。
* 如果一个项目为0,其他为1,空间不足时,0值不缩小。

> `flex-basis`

* 可设置项目占据的空间。默认为auto,项目本来的大小。

> `flex`

* 该属性是`flex-grow`, `flex-shrink` 和 `flex-basis`的简写，默认值为0 1 auto 。
* 有2个快捷值 `auto (1 1 auto)` 和 `none (0 0 auto)`。
* 建议优先使用这个属性，而不是单独写三个分离的属性，因为浏览器会推算相关值。

> `align-self`

* 定义单个项目与其他项目不同的对齐方式,覆盖父级的`align-item`。
* 该属性的取值方式与`align-item`一致,多加一个默认值`auto`。


















> 
