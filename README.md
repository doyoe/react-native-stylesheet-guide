# React-Native StyleSheet Guide

`React-Native` 支持的样式相当于是 `CSS` 的一个子集，并且属性名不完全一致，所以当你开始在编写 `React-Native` 之前，可以先简要了解一下。

## 目录

* [Properties 属性](#user-content-properties)
    * [view](#user-content-view)
    * [Image](#user-content-view)
    * [Text 文本](#user-content-text)
    * [Layout 布局](#user-content-layout)
        * [Dimension 尺寸](#user-content-dimension)
        * [Positioning 定位](#user-content-positioning)
        * [Margin 外部白](#user-content-margin)
        * [Padding 内补白](#user-content-padding)
        * [BorderWidth 边框厚度](#user-content-border-width)
        * [Flexbox 弹性盒](#user-content-flexbox)
* [Values 取值](#user-content-values)
    * [Color 颜色](#user-content-color)


<a name="properties"></a>
## Properties 属性

<a name="text"></a>
### Text 文本
属性名 | 取值 | 描述
---|---|---
color | color | 对应 `CSS` 中的 [color](http://css.doyoe.com/properties/color/color.htm) 属性
fontFamily | string | 对应 `CSS` 中的 [font-family](http://css.doyoe.com/properties/font/font-family.htm) 属性
fontSize | number | 对应 `CSS` 中的 [font-size](http://css.doyoe.com/properties/font/font-size.htm) 属性
fontStyle | normal/italic | 对应 `CSS` 中的 [font-style](http://css.doyoe.com/properties/font/font-style.htm) 属性，但阉割了 `oblique` 取值
fontWeight | normal/bold/100~900 | 对应 `CSS` 中的 [font-weight](http://css.doyoe.com/properties/font/font-weight.htm) 属性，但阉割了 `bolder/lighter` 取值
lineHeight | number | 对应 `CSS` 中的 [line-height](http://css.doyoe.com/properties/text/line-height.htm) 属性
textAlign | auto/left/right/center/justify<sup>`iOS`</sup> | 对应 `CSS` 中的 [text-align](http://css.doyoe.com/properties/text/text-align.htm) 属性，增加了 `auto` 取值
textAlignVertical<sup>`Android`</sup> | auto/top/bottom/center | 对应 `CSS` 中的 [vertical-align](http://css.doyoe.com/properties/text/vertical-align.htm) 属性，增加了 `auto` 取值，`center` 取代了 `middle`，并阉割了 `baseline/sub` 等值
textShadowColor | color | 对应 `CSS` 中的 [text-shadow](http://css.doyoe.com/properties/text-decoration/text-shadow.htm) 属性中的颜色定义
textShadowOffset | {width: number, height: number} | 对应 `CSS` 中的 [text-shadow](http://css.doyoe.com/properties/text-decoration/text-shadow.htm) 属性中的阴影偏移定义
textShadowRadius | number | 在 `CSS` 中，阴影的圆角大小取决于元素的圆角定义，不需要额外定义
letterSpacing<sup>`iOS`</sup> | number | 对应 `CSS` 中的 [letter-spacing](http://css.doyoe.com/properties/text/letter-spacing.htm) 属性，但取值不同
textDecorationColor<sup>`iOS`</sup> | color | 对应 `CSS` 中的 [text-decoration-color](http://css.doyoe.com/properties/text-decoration/text-decoration-color.htm) 属性
textDecorationLine<sup>`iOS`</sup> | `none`, `underline`, `line-through`, `underline line-through` | 对应 `CSS` 中的 [text-decoration-line](http://css.doyoe.com/properties/text-decoration/text-decoration-line.htm) 属性，取值略有不同
textDecorationStyle<sup>`iOS`</sup> | `solid`, `double`, `dotted`, `dashed` | 对应 `CSS` 中的 [text-decoration-style](http://css.doyoe.com/properties/text-decoration/text-decoration-style.htm) 属性，但阉割了 `wavy` 取值
writingDirection<sup>`iOS`</sup> | `auto`, `ltr`, `rtl` | 对应 `CSS` 中的 [direction](http://css.doyoe.com/properties/writing-modes/direction.htm) 属性，增加了 `auto` 取值

<a name="layout"></a>
### Layout 布局

<a name="dimension"></a>
#### Dimension 尺寸
属性名 | 取值 | 描述
---|---|---
width | number | 对应 `CSS` 中的 `width` 属性
height | number | 对应 `CSS` 中的 `height` 属性

<a name="positioning"></a>
#### Positioning 定位
属性名 | 取值 | 描述
---|---|---
position | absolute/relative | 对应 `CSS` 中的 `position` 属性，但阉割了 `static/fixed` 取值
top | number | 对应 `CSS` 中的 `top` 属性
right | number | 对应 `CSS` 中的 `right` 属性
bottom | number | 对应 `CSS` 中的 `bottom` 属性
left | number | 对应 `CSS` 中的 `left` 属性

<a name="margin"></a>
#### Margin 外部白
属性名 | 取值 | 描述
---|---|---
margin | number | 对应 `CSS` 中的 `margin` 属性
marginHorizontal | number | `CSS`中没有对应的属性，相当于同时设置marginRight和marginLeft
marginVertical | number | `CSS`中没有对应的属性，相当于同时设置marginTop和marginBottom
marginTop | number | 对应 `CSS` 中的 `margin-top` 属性
marginRight | number | 对应 `CSS` 中的 `margin-right` 属性
marginBottom | number | 对应 `CSS` 中的 `margin-bottom` 属性
marginLeft | number | 对应 `CSS` 中的 `margin-left` 属性

<a name="padding"></a>
#### Padding 内部白
属性名 | 取值 | 描述
---|---|---
padding | number | 对应 `CSS` 中的 `padding` 属性
paddingHorizontal | number | `CSS`中没有对应的属性，相当于同时设置paddingRight和paddingLeft
paddingVertical | number | `CSS`中没有对应的属性，相当于同时设置paddingTop和paddingBottom
paddingTop | number | 对应 `CSS` 中的 `padding-top` 属性
paddingRight | number | 对应 `CSS` 中的 `padding-right` 属性
paddingBottom | number | 对应 `CSS` 中的 `padding-bottom` 属性
paddingLeft | number | 对应 `CSS` 中的 `padding-left` 属性

<a name="border-width"></a>
#### BorderWidth 边框厚度
属性名 | 取值 | 描述
---|---|---
borderWidth | number | 对应 `CSS` 中的 `border-width` 属性
borderTopWidth | number | 对应 `CSS` 中的 `border-top-width` 属性
borderRightWidth | number | 对应 `CSS` 中的 `border-right-width` 属性
borderBottomWidth | number | 对应 `CSS` 中的 `border-bottom-width` 属性
borderLeftWidth | number | 对应 `CSS` 中的 `border-left-width` 属性

<a name="flexbox"></a>
#### Flexbox 弹性盒
属性名 | 取值 | 描述
---|---|---
flex | number | 对应 `CSS` 中的 `flex` 属性
flexDirection | row/column | 对应 `CSS` 中的 `flex-direction` 属性，但阉割了 `row-reverse/column-reverse` 取值
flexWrap | wrap/nowrap | 对应 `CSS` 中的 `flex-wrap` 属性，但阉割了 `wrap-reverse` 取值
justifyContent | flex-start/flex-end/center/space-between/space-around | 对应 `CSS` 中的 `justify-content` 属性，但阉割了 `stretch` 取值
alignItems | flex-start/flex-end/center/stretch | 对应 `CSS` 中的 `align-items` 属性，但阉割了 `baseline` 取值
alignSelf | auto/flex-start/flex-end/center/stretch | 对应 `CSS` 中的 `align-self` 属性，但阉割了 `baseline` 取值


<a name="values"></a>
## Valuse 取值

<a name="color"></a>
### Color 颜色

`React-Native` 支持了 `CSS` 中大部分的颜色类型：

* `#f00 (#rgb)`
* `#f00c (#rgba)`：`CSS` 中无对应的值
* `#ff0000 (#rrggbb)`
* `#ff0000cc (#rrggbbaa)`：`CSS` 中无对应的值
* `rgb(255, 0, 0)`
* `rgba(255, 0, 0, 0.9)`
* `hsl(360, 100%, 100%)`
* `hsla(360, 100%, 100%, 0.9)`
* `transparent`
* `Color Name`：支持了 [基本颜色关键字](http://css.doyoe.com/appendix/color-keywords.htm#basic) 和 [拓展颜色关键字](http://css.doyoe.com/appendix/color-keywords.htm#extended)，但不支持 [28个系统颜色](http://css.doyoe.com/appendix/color-keywords.htm#system)；