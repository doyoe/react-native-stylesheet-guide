# React-Native 样式指南

`React-Native` 的样式基本上是实现了 `CSS` 的一个子集，并且属性名不完全一致，所以当你开始在编写 `React-Native` 之前，可以先简要了解一下。

## 目录

* [Properties 属性](#user-content-properties)
    * [Text 文本](#user-content-text)
    * [Dimension 尺寸](#user-content-dimension)
    * [Positioning 定位](#user-content-positioning)
    * [Margin 外部白](#user-content-margin)
    * [Padding 内补白](#user-content-padding)
    * [Border 边框](#user-content-border)
    * [Background 背景](#user-content-background)
    * [Transform 转换](#user-content-transform)
    * [Flexbox 弹性盒](#user-content-flexbox)
    * [Other 其他](#user-content-other)
* [Values 取值](#user-content-values)
    * [Color 颜色](#user-content-color)
    * [Number 数值](#user-content-number)
* [Units 单位](#user-content-units)
    * [Pt 点](#user-content-pt)


<a name="properties"></a>
## Properties 属性

<a name="text"></a>
### Text 文本
属性名 | 取值 | 描述
---|---|---
color | [&lt;color&gt;](#user-content-color) | 对应 `CSS` 中的 [color](http://css.doyoe.com/properties/color/color.htm) 属性
fontFamily | string | 对应 `CSS` 中的 [font-family](http://css.doyoe.com/properties/font/font-family.htm) 属性
fontSize | [&lt;number&gt;](#user-content-number) | 对应 `CSS` 中的 [font-size](http://css.doyoe.com/properties/font/font-size.htm) 属性
fontStyle | `normal`, `italic` | 对应 `CSS` 中的 [font-style](http://css.doyoe.com/properties/font/font-style.htm) 属性，但阉割了 `oblique` 取值
fontWeight | `normal`, `bold` `100~900` | 对应 `CSS` 中的 [font-weight](http://css.doyoe.com/properties/font/font-weight.htm) 属性，但阉割了 `bolder, lighter` 取值
lineHeight | [&lt;number&gt;](#user-content-number) | 对应 `CSS` 中的 [line-height](http://css.doyoe.com/properties/text/line-height.htm) 属性
textAlign | `auto`, `left`, `right`, `center`, `justify`<sup>`iOS`</sup> | 对应 `CSS` 中的 [text-align](http://css.doyoe.com/properties/text/text-align.htm) 属性，增加了 `auto` 取值
textAlignVertical<sup>`Android`</sup> | `auto`, `top`, `bottom`, `center` | 对应 `CSS` 中的 [vertical-align](http://css.doyoe.com/properties/text/vertical-align.htm) 属性，增加了 `auto` 取值，`center` 取代了 `middle`，并阉割了 `baseline, sub` 等值
textShadowColor | [&lt;color&gt;](#user-content-color) | 对应 `CSS` 中的 [text-shadow](http://css.doyoe.com/properties/text-decoration/text-shadow.htm) 属性中的颜色定义
textShadowOffset | {<br>width: [&lt;number&gt;](#user-content-number), <br>height: [&lt;number&gt;](#user-content-number)<br>} | 对应 `CSS` 中的 [text-shadow](http://css.doyoe.com/properties/text-decoration/text-shadow.htm) 属性中的阴影偏移定义
textShadowRadius | [&lt;number&gt;](#user-content-number) | 在 `CSS` 中，阴影的圆角大小取决于元素的圆角定义，不需要额外定义
letterSpacing<sup>`iOS`</sup> | [&lt;number&gt;](#user-content-number) | 对应 `CSS` 中的 [letter-spacing](http://css.doyoe.com/properties/text/letter-spacing.htm) 属性，但取值不同
textDecorationColor<sup>`iOS`</sup> | [&lt;color&gt;](#user-content-color) | 对应 `CSS` 中的 [text-decoration-color](http://css.doyoe.com/properties/text-decoration/text-decoration-color.htm) 属性
textDecorationLine<sup>`iOS`</sup> | `none`, `underline`, `line-through`, `underline line-through` | 对应 `CSS` 中的 [text-decoration-line](http://css.doyoe.com/properties/text-decoration/text-decoration-line.htm) 属性，但阉割了 `overline`, `blink` 取值
textDecorationStyle<sup>`iOS`</sup> | `solid`, `double`, `dotted`, `dashed` | 对应 `CSS` 中的 [text-decoration-style](http://css.doyoe.com/properties/text-decoration/text-decoration-style.htm) 属性，但阉割了 `wavy` 取值
writingDirection<sup>`iOS`</sup> | `auto`, `ltr`, `rtl` | 对应 `CSS` 中的 [direction](http://css.doyoe.com/properties/writing-modes/direction.htm) 属性，增加了 `auto` 取值

<a name="dimension"></a>
### Dimension 尺寸
属性名 | 取值 | 描述
---|---|---
width | [&lt;number&gt;](#user-content-number) | 对应 `CSS` 中的 `width` 属性
height | [&lt;number&gt;](#user-content-number) | 对应 `CSS` 中的 `height` 属性

<a name="positioning"></a>
### Positioning 定位
属性名 | 取值 | 描述
---|---|---
position | `absolute`, `relative` | 对应 `CSS` 中的 `position` 属性，但阉割了 `static, fixed` 取值
top | [&lt;number&gt;](#user-content-number) | 对应 `CSS` 中的 `top` 属性
right | [&lt;number&gt;](#user-content-number) | 对应 `CSS` 中的 `right` 属性
bottom | [&lt;number&gt;](#user-content-number) | 对应 `CSS` 中的 `bottom` 属性
left | [&lt;number&gt;](#user-content-number) | 对应 `CSS` 中的 `left` 属性

<a name="margin"></a>
### Margin 外部白
属性名 | 取值 | 描述
---|---|---
margin | [&lt;number&gt;](#user-content-number) | 对应 `CSS` 中的 `margin` 属性
marginHorizontal | [&lt;number&gt;](#user-content-number) | `CSS`中没有对应的属性，相当于同时设置marginRight和marginLeft
marginVertical | [&lt;number&gt;](#user-content-number) | `CSS`中没有对应的属性，相当于同时设置marginTop和marginBottom
marginTop | [&lt;number&gt;](#user-content-number) | 对应 `CSS` 中的 `margin-top` 属性
marginRight | [&lt;number&gt;](#user-content-number) | 对应 `CSS` 中的 `margin-right` 属性
marginBottom | [&lt;number&gt;](#user-content-number) | 对应 `CSS` 中的 `margin-bottom` 属性
marginLeft | [&lt;number&gt;](#user-content-number) | 对应 `CSS` 中的 `margin-left` 属性

<a name="padding"></a>
### Padding 内部白
属性名 | 取值 | 描述
---|---|---
padding | [&lt;number&gt;](#user-content-number) | 对应 `CSS` 中的 `padding` 属性
paddingHorizontal | [&lt;number&gt;](#user-content-number) | `CSS`中没有对应的属性，相当于同时设置paddingRight和paddingLeft
paddingVertical | [&lt;number&gt;](#user-content-number) | `CSS`中没有对应的属性，相当于同时设置paddingTop和paddingBottom
paddingTop | [&lt;number&gt;](#user-content-number) | 对应 `CSS` 中的 `padding-top` 属性
paddingRight | [&lt;number&gt;](#user-content-number) | 对应 `CSS` 中的 `padding-right` 属性
paddingBottom | [&lt;number&gt;](#user-content-number) | 对应 `CSS` 中的 `padding-bottom` 属性
paddingLeft | [&lt;number&gt;](#user-content-number) | 对应 `CSS` 中的 `padding-left` 属性

<a name="border"></a>
### Border 边框
属性名 | 取值 | 描述
---|---|---
borderStyle | `solid`, `dotted`, `dashed` | 对应 `CSS` 中的 `border-style` 属性，但阉割了 `none, hidden, double, groove, ridge, inset, outset` 取值，且无方向分拆属性
borderWidth | [&lt;number&gt;](#user-content-number) | 对应 `CSS` 中的 `border-width` 属性
borderTopWidth | [&lt;number&gt;](#user-content-number) | 对应 `CSS` 中的 `border-top-width` 属性
borderRightWidth | [&lt;number&gt;](#user-content-number) | 对应 `CSS` 中的 `border-right-width` 属性
borderBottomWidth | [&lt;number&gt;](#user-content-number) | 对应 `CSS` 中的 `border-bottom-width` 属性
borderLeftWidth | [&lt;number&gt;](#user-content-number) | 对应 `CSS` 中的 `border-left-width` 属性
borderColor | [&lt;color&gt;](#user-content-color) | 对应 `CSS` 中的 `border-color` 属性
borderTopColor | [&lt;color&gt;](#user-content-color) | 对应 `CSS` 中的 `border-top-color` 属性
borderRightColor | [&lt;color&gt;](#user-content-color) | 对应 `CSS` 中的 `border-right-color` 属性
borderBottomColor | [&lt;color&gt;](#user-content-color) | 对应 `CSS` 中的 `border-bottom-color` 属性
borderLeftColor | [&lt;color&gt;](#user-content-color) | 对应 `CSS` 中的 `border-left-color` 属性
borderRadius | [&lt;number&gt;](#user-content-number) | 对应 `CSS` 中的 `border-radius` 属性
borderTopLeftRadius | [&lt;number&gt;](#user-content-number) | 对应 `CSS` 中的 `border-top-left-radius` 属性
borderTopRightRadius | [&lt;number&gt;](#user-content-number) | 对应 `CSS` 中的 `border-top-right-radius` 属性
borderBottomLeftRadius | [&lt;number&gt;](#user-content-number) | 对应 `CSS` 中的 `border-bottom-left-radius` 属性
borderBottomRightRadius | [&lt;number&gt;](#user-content-number) | 对应 `CSS` 中的 `border-bottom-right-radius` 属性
shadowColor | [&lt;color&gt;](#user-content-color) | 对应 `CSS` 中的 [box-shadow](http://css.doyoe.com/properties/border/box-shadow.htm) 属性中的颜色定义
shadowOffset | {<br>width: [&lt;number&gt;](#user-content-number), <br>height: [&lt;number&gt;](#user-content-number)<br>} | 对应 `CSS` 中的 [box-shadow](http://css.doyoe.com/properties/border/box-shadow.htm) 属性中的阴影偏移定义
shadowRadius | [&lt;number&gt;](#user-content-number) | 在 `CSS` 中，阴影的圆角大小取决于元素的圆角定义，不需要额外定义
shadowOpacity | [&lt;number&gt;](#user-content-number) | 对应 `CSS` 中的 [box-shadow](http://css.doyoe.com/properties/border/box-shadow.htm) 属性中的阴影透明度定义

<a name="background"></a>
### Background 背景
属性名 | 取值 | 描述
---|---|---
backgroundColor | [&lt;color&gt;](#user-content-color) | 对应 `CSS` 中的 `background-color` 属性

<a name="transform"></a>
### Transform 转换
属性名 | 取值 | 描述
---|---|---
transform | `[{perspective: number}, {rotate: string}, {rotateX: string}, {rotateY: string}, {rotateZ: string}, {scale: number}, {scaleX: number}, {scaleY: number}, {translateX: number}, {translateY: number}, {skewX: string}, {skewY: string}]` | 对应 `CSS` 中的 `transform` 属性
transformMatrix | `TransformMatrixPropType` | 类似于 `CSS` 中 `transform` 属性的 `matrix()` 和 `matrix3d()` 函数
backfaceVisibility | `visible`, `hidden` | 对应 `CSS` 中的 `backface-visibility` 属性

<a name="flexbox"></a>
### Flexbox 弹性盒
属性名 | 取值 | 描述
---|---|---
flex | [&lt;number&gt;](#user-content-number) | 对应 `CSS` 中的 `flex` 属性
flexDirection | `row`, `column` | 对应 `CSS` 中的 `flex-direction` 属性，但阉割了 `row-reverse, column-reverse` 取值
flexWrap | `wrap`, `nowrap` | 对应 `CSS` 中的 `flex-wrap` 属性，但阉割了 `wrap-reverse` 取值
justifyContent | `flex-start`, `flex-end`, `center`, `space-between`, `space-around` | 对应 `CSS` 中的 `justify-content` 属性，但阉割了 `stretch` 取值。与CSS不同的是，这里控制的是纵轴
alignItems | `flex-start`, `flex-end`, `center`, `stretch` | 对应 `CSS` 中的 `align-items` 属性，但阉割了 `baseline` 取值。与CSS不同的是，这里控制的是横轴
alignSelf | `auto`, `flex-start`, `flex-end`, `center`, `stretch` | 对应 `CSS` 中的 `align-self` 属性，但阉割了 `baseline` 取值

<a name="other"></a>
### Other 其他
属性名 | 取值 | 描述
---|---|---
opacity | [&lt;number&gt;](#user-content-number) | 对应 `CSS` 中的 `opacity` 属性
overflow | `visible`, `hidden` | 对应 `CSS` 中的 `overflow` 属性，但阉割了 `scroll, auto` 取值
elevation<sup>`Android`</sup> | [&lt;number&gt;](#user-content-number) | `CSS`中没有对应的属性，只在 `Android5.0+` 上有效
resizeMode | `cover`, `contain`, `stretch` | `CSS`中没有对应的属性，可以参考 `background-size` 属性
overlayColor<sup>`Android`</sup> | string | `CSS`中没有对应的属性，当图像有圆角时，将角落都充满一种颜色
tintColor<sup>`iOS`</sup> | [&lt;color&gt;](#user-content-color) | `CSS`中没有对应的属性，`iOS` 图像上特殊的色彩，改变不透明像素的颜色


<a name="values"></a>
## Valuse 取值

<a name="color"></a>
### Color 颜色

`React-Native` 支持了 `CSS` 中大部分的颜色类型：

* `#f00` (#rgb)
* `#f00c` (#rgba)：`CSS` 中无对应的值
* `#ff0000` (#rrggbb)
* `#ff0000cc` (#rrggbbaa)：`CSS` 中无对应的值
* `rgb(255, 0, 0)`
* `rgba(255, 0, 0, 0.9)`
* `hsl(360, 100%, 100%)`
* `hsla(360, 100%, 100%, 0.9)`
* `transparent`
* `Color Name`：支持了 [基本颜色关键字](http://css.doyoe.com/appendix/color-keywords.htm#basic) 和 [拓展颜色关键字](http://css.doyoe.com/appendix/color-keywords.htm#extended)，但不支持 [28个系统颜色](http://css.doyoe.com/appendix/color-keywords.htm#system)；

<a name="number"></a>
### Number 数值

在 `React-Native` 中，目前仅支持 `Number` 这一种长度取值。默认缺省了 `pt` 单位，详细请看 [Units 单位](#user-content-units) 部分。

<a name="units"></a>
## Units 单位

<a name="pt"></a>
### Pt 点

在 `React-Native` 中，并不支持百分比单位，目前只支持一种单位，即 `pt` 绝对长度单位，同时，你在定义时不需要加单位，例如：

```
<View style={{width: 100, height: 50}}></View>
```

```
var styles = StyleSheet.create({
    box: {
        width: 100,
        height: 50
    }
});
```

未完待续。。。