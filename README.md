# React-Native 样式指南

`React-Native` 的样式基本上是实现了 `CSS` 的一个子集，并且属性名不完全一致，所以当你开始在编写 `React-Native` 之前，可以先简要了解一下。

## 当前对应 RN 版本

0.44

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
* [PixelRatio 像素密度](#user-content-pixelratio)


<a name="properties"></a>
## Properties 属性

<a name="text"></a>
### Text 文本（18）
属性名 | 取值 | 描述
---|---|---
color | [&lt;color&gt;](#user-content-color) | 对应 `CSS` [color](http://css.doyoe.com/properties/color/color.htm) 属性
fontFamily | string | 对应 `CSS` [font-family](http://css.doyoe.com/properties/font/font-family.htm) 属性
fontSize | [&lt;number&gt;](#user-content-number) | 对应 `CSS` [font-size](http://css.doyoe.com/properties/font/font-size.htm) 属性
fontStyle | `normal`, `italic` | 对应 `CSS` [font-style](http://css.doyoe.com/properties/font/font-style.htm) 属性，但阉割了 `oblique` 取值
fontWeight | `normal`, `bold` `100~900` | 对应 `CSS` [font-weight](http://css.doyoe.com/properties/font/font-weight.htm) 属性，但阉割了 `bolder, lighter` 取值
lineHeight | [&lt;number&gt;](#user-content-number) | 对应 `CSS` [line-height](http://css.doyoe.com/properties/text/line-height.htm) 属性
textAlign | `auto`, `left`, `right`, `center`, `justify`<sup>`iOS`</sup> | 对应 `CSS` [text-align](http://css.doyoe.com/properties/text/text-align.htm) 属性，但增加了 `auto` 取值。当取值为 `justify` 时，在 `Android` 上会变为 `left`
textDecorationLine | `none`, `underline`, `line-through`, `underline line-through` | 对应 `CSS` [text-decoration-line](http://css.doyoe.com/properties/text-decoration/text-decoration-line.htm) 属性，但阉割了 `overline`, `blink` 取值
textShadowColor | [&lt;color&gt;](#user-content-color) | 对应 `CSS` [text-shadow](http://css.doyoe.com/properties/text-decoration/text-shadow.htm) 属性中的颜色定义
textShadowOffset | {<br>width:[&lt;number&gt;](#user-content-number),<br>height:[&lt;number&gt;](#user-content-number)<br>} | 对应 `CSS` [text-shadow](http://css.doyoe.com/properties/text-decoration/text-shadow.htm) 属性中的阴影偏移定义
textShadowRadius | [&lt;number&gt;](#user-content-number) | 在 `CSS` 中，阴影的圆角大小取决于元素的圆角定义，不需要额外定义
includeFontPadding<br /><sup>`Android`</sup> | [&lt;bool&gt;](#user-content-bool) | Android在默认情况下会为文字额外保留一些padding，以便留出空间摆放上标或是下标的文字。对于某些字体来说，这些额外的padding可能会导致文字难以垂直居中。如果你把textAlignVertical设置为center之后，文字看起来依然不在正中间，那么可以尝试将本属性设置为false
textAlignVertical<br /><sup>`Android`</sup> | `auto`, `top`, `bottom`, `center` | 对应 `CSS` [vertical-align](http://css.doyoe.com/properties/text/vertical-align.htm) 属性，增加了 `auto` 取值，`center` 取代了 `middle`，并阉割了 `baseline, sub` 等值
fontVariant<br /><sup>`iOS`</sup> | `small-caps`, `oldstyle-nums`, `lining-nums`, `tabular-nums`, `proportional-nums` | 对应 `CSS` [font-variant](http://css.doyoe.com/properties/font/font-variant.htm) 属性，但取值更丰富
letterSpacing<br /><sup>`iOS`</sup> | [&lt;number&gt;](#user-content-number) | 对应 `CSS` [letter-spacing](http://css.doyoe.com/properties/text/letter-spacing.htm) 属性
textDecorationColor<br /><sup>`iOS`</sup> | [&lt;color&gt;](#user-content-color) | 对应 `CSS` [text-decoration-color](http://css.doyoe.com/properties/text-decoration/text-decoration-color.htm) 属性
textDecorationStyle<br /><sup>`iOS`</sup> | `solid`, `double`, `dotted`, `dashed` | 对应 `CSS` [text-decoration-style](http://css.doyoe.com/properties/text-decoration/text-decoration-style.htm) 属性，但阉割了 `wavy` 取值
writingDirection<br /><sup>`iOS`</sup> | `auto`, `ltr`, `rtl` | 对应 `CSS` [direction](http://css.doyoe.com/properties/writing-modes/direction.htm) 属性，增加了 `auto` 取值

<a name="dimension"></a>
### Dimension 尺寸（6）
属性名 | 取值 | 描述
---|---|---
width | [&lt;number&gt;](#user-content-number) | 对应 `CSS` [width](http://css.doyoe.com/properties/dimension/width.htm) 属性
minWidth | [&lt;number&gt;](#user-content-number) | 对应 `CSS` [min-width](http://css.doyoe.com/properties/dimension/min-width.htm) 属性
maxWidth | [&lt;number&gt;](#user-content-number) | 对应 `CSS` [max-width](http://css.doyoe.com/properties/dimension/max-width.htm) 属性
height | [&lt;number&gt;](#user-content-number) | 对应 `CSS` [height](http://css.doyoe.com/properties/dimension/height.htm) 属性
minHeight | [&lt;number&gt;](#user-content-number) | 对应 `CSS` [min-height](http://css.doyoe.com/properties/dimension/min-height.htm) 属性
maxHeight | [&lt;number&gt;](#user-content-number) | 对应 `CSS` [max-height](http://css.doyoe.com/properties/dimension/max-height.htm) 属性

<a name="positioning"></a>
### Positioning 定位（6）
属性名 | 取值 | 描述
---|---|---
position | `absolute`, `relative` | 对应 `CSS` [position](http://css.doyoe.com/properties/positioning/position.htm) 属性，但阉割了 `static, fixed` 取值
top | [&lt;number&gt;](#user-content-number) | 对应 `CSS` [top](http://css.doyoe.com/properties/positioning/top.htm) 属性
right | [&lt;number&gt;](#user-content-number) | 对应 `CSS` [right](http://css.doyoe.com/properties/positioning/right.htm) 属性
bottom | [&lt;number&gt;](#user-content-number) | 对应 `CSS` [bottom](http://css.doyoe.com/properties/positioning/bottom.htm) 属性
left | [&lt;number&gt;](#user-content-number) | 对应 `CSS` [left](http://css.doyoe.com/properties/positioning/left.htm) 属性
zIndex | [&lt;number&gt;](#user-content-number) | 对应 `CSS` [z-index](http://css.doyoe.com/properties/positioning/z-index.htm) 属性

<a name="margin"></a>
### Margin 外部白（7）
属性名 | 取值 | 描述
---|---|---
margin | [&lt;number&gt;](#user-content-number) | 对应 `CSS` [margin](http://css.doyoe.com/properties/margin/margin.htm) 属性，不同的是，它只能定义一个参数，如需分别定义`上、右、下、左`4个方位的外补白，可以通过下面的单向外部白属性
marginHorizontal | [&lt;number&gt;](#user-content-number) | 无对应的 `CSS` 属性。其效果相当于同时设置 `marginRight` 和 `marginLeft`
marginVertical | [&lt;number&gt;](#user-content-number) | 无对应的 `CSS` 属性。其效果相当于同时设置 `marginTop` 和 `marginBottom`
marginTop | [&lt;number&gt;](#user-content-number) | 对应 `CSS` [margin-top](http://css.doyoe.com/properties/margin/margin-top.htm) 属性
marginRight | [&lt;number&gt;](#user-content-number) | 对应 `CSS` [margin-right](http://css.doyoe.com/properties/margin/margin-right.htm) 属性
marginBottom | [&lt;number&gt;](#user-content-number) | 对应 `CSS` [margin-bottom](http://css.doyoe.com/properties/margin/margin-bottom.htm) 属性
marginLeft | [&lt;number&gt;](#user-content-number) | 对应 `CSS` [margin-left](http://css.doyoe.com/properties/margin/margin-left.htm) 属性

<a name="padding"></a>
### Padding 内部白（7）
属性名 | 取值 | 描述
---|---|---
padding | [&lt;number&gt;](#user-content-number) | 对应 `CSS` [padding](http://css.doyoe.com/properties/padding/padding.htm) 属性，不同的是，它只能定义一个参数，如需分别定义`上、右、下、左`4个方位的内补白，可以通过下面的单向内部白属性
paddingHorizontal | [&lt;number&gt;](#user-content-number) | 无对应的 `CSS` 属性。其效果相当于同时设置 `paddingRight` 和 `paddingLeft`
paddingVertical | [&lt;number&gt;](#user-content-number) | 无对应的 `CSS` 属性。其效果相当于同时设置 `paddingTop` 和 `paddingBottom`
paddingTop | [&lt;number&gt;](#user-content-number) | 对应 `CSS` [padding-top](http://css.doyoe.com/properties/padding/padding-top.htm) 属性
paddingRight | [&lt;number&gt;](#user-content-number) | 对应 `CSS` [padding-right](http://css.doyoe.com/properties/padding/padding-right.htm) 属性
paddingBottom | [&lt;number&gt;](#user-content-number) | 对应 `CSS` [padding-bottom](http://css.doyoe.com/properties/padding/padding-bottom.htm) 属性
paddingLeft | [&lt;number&gt;](#user-content-number) | 对应 `CSS` [padding-left](http://css.doyoe.com/properties/padding/padding-left.htm) 属性

<a name="border"></a>
### Border 边框（20）
属性名 | 取值 | 描述
---|---|---
borderStyle | `solid`, `dotted`, `dashed` | 对应 `CSS` `border-style` 属性，但阉割了 `none, hidden, double, groove, ridge, inset, outset` 取值，且无方向分拆属性
borderWidth | [&lt;number&gt;](#user-content-number) | 对应 `CSS` `border-width` 属性
borderTopWidth | [&lt;number&gt;](#user-content-number) | 对应 `CSS` `border-top-width` 属性
borderRightWidth | [&lt;number&gt;](#user-content-number) | 对应 `CSS` `border-right-width` 属性
borderBottomWidth | [&lt;number&gt;](#user-content-number) | 对应 `CSS` `border-bottom-width` 属性
borderLeftWidth | [&lt;number&gt;](#user-content-number) | 对应 `CSS` `border-left-width` 属性
borderColor | [&lt;color&gt;](#user-content-color) | 对应 `CSS` `border-color` 属性
borderTopColor | [&lt;color&gt;](#user-content-color) | 对应 `CSS` `border-top-color` 属性
borderRightColor | [&lt;color&gt;](#user-content-color) | 对应 `CSS` `border-right-color` 属性
borderBottomColor | [&lt;color&gt;](#user-content-color) | 对应 `CSS` `border-bottom-color` 属性
borderLeftColor | [&lt;color&gt;](#user-content-color) | 对应 `CSS` `border-left-color` 属性
borderRadius | [&lt;number&gt;](#user-content-number) | 对应 `CSS` `border-radius` 属性
borderTopLeftRadius | [&lt;number&gt;](#user-content-number) | 对应 `CSS` `border-top-left-radius` 属性
borderTopRightRadius | [&lt;number&gt;](#user-content-number) | 对应 `CSS` `border-top-right-radius` 属性
borderBottomLeftRadius | [&lt;number&gt;](#user-content-number) | 对应 `CSS` `border-bottom-left-radius` 属性
borderBottomRightRadius | [&lt;number&gt;](#user-content-number) | 对应 `CSS` `border-bottom-right-radius` 属性
shadowColor | [&lt;color&gt;](#user-content-color) | 对应 `CSS` [box-shadow](http://css.doyoe.com/properties/border/box-shadow.htm) 属性中的颜色定义
shadowOffset | {<br>width: [&lt;number&gt;](#user-content-number), <br>height: [&lt;number&gt;](#user-content-number)<br>} | 对应 `CSS` [box-shadow](http://css.doyoe.com/properties/border/box-shadow.htm) 属性中的阴影偏移定义
shadowRadius | [&lt;number&gt;](#user-content-number) | 在 `CSS` 中，阴影的圆角大小取决于元素的圆角定义，不需要额外定义
shadowOpacity | [&lt;number&gt;](#user-content-number) | 对应 `CSS` [box-shadow](http://css.doyoe.com/properties/border/box-shadow.htm) 属性中的阴影透明度定义

<a name="background"></a>
### Background 背景（1）
属性名 | 取值 | 描述
---|---|---
backgroundColor | [&lt;color&gt;](#user-content-color) | 对应 `CSS` `background-color` 属性

<a name="transform"></a>
### Transform 转换（3）
属性名 | 取值 | 描述
---|---|---
transform | `[{perspective: number}, {rotate: string}, {rotateX: string}, {rotateY: string}, {rotateZ: string}, {scale: number}, {scaleX: number}, {scaleY: number}, {translateX: number}, {translateY: number}, {skewX: string}, {skewY: string}]` | 对应 `CSS` `transform` 属性
transformMatrix | `TransformMatrixPropType` | 类似于 `CSS` 中 `transform` 属性的 `matrix()` 和 `matrix3d()` 函数
backfaceVisibility | `visible`, `hidden` | 对应 `CSS` `backface-visibility` 属性

<a name="flexbox"></a>
### Flexbox 弹性盒（9）
属性名 | 取值 | 描述
---|---|---
flex | [&lt;number&gt;](#user-content-number) | 对应 `CSS` `flex` 属性，但只能为整数值
flexGrow | [&lt;number&gt;](#user-content-number) | 对应 `CSS` `flex-grow` 属性
flexShrink | [&lt;number&gt;](#user-content-number) | 对应 `CSS` `flex-shrink` 属性
flexBasis | [&lt;number&gt;](#user-content-number) | 对应 `CSS` `flex-basis` 属性
flexDirection | `row`, `row-reverse`, `column`, `column-reverse` | 对应 `CSS` `flex-direction` 属性
flexWrap | `wrap`, `nowrap` | 对应 `CSS` `flex-wrap` 属性，但阉割了 `wrap-reverse` 取值
justifyContent | `flex-start`, `flex-end`, `center`, `space-between`, `space-around` | 对应 `CSS` `justify-content` 属性，但阉割了 `stretch` 取值。
alignItems | `flex-start`, `flex-end`, `center`, `stretch` | 对应 `CSS` `align-items` 属性，但阉割了 `baseline` 取值。
alignSelf | `auto`, `flex-start`, `flex-end`, `center`, `stretch` | 对应 `CSS` `align-self` 属性，但阉割了 `baseline` 取值

<a name="other"></a>
### Other 其他
属性名 | 取值 | 描述
---|---|---
opacity | [&lt;number&gt;](#user-content-number) | 对应 `CSS` `opacity` 属性
overflow | `visible`, `hidden`, `scroll` | 对应 `CSS` `overflow` 属性，但阉割了 `auto` 取值
elevation<br /><sup>`Android`</sup> | [&lt;number&gt;](#user-content-number) | `CSS`中没有对应的属性，只在 `Android5.0+` 上有效
resizeMode | `cover`, `contain`, `stretch` | `CSS`中没有对应的属性，可以参考 `background-size` 属性
overlayColor<br /><sup>`Android`</sup> | string | `CSS`中没有对应的属性，当图像有圆角时，将角落都充满一种颜色
tintColor<br /><sup>`iOS`</sup> | [&lt;color&gt;](#user-content-color) | `CSS`中没有对应的属性，`iOS` 图像上特殊的色彩，改变不透明像素的颜色


<a name="values"></a>
## Valuse 取值

<a name="color"></a>
### Color 颜色

`React Native` 支持了 `CSS` 中大部分的颜色类型：

* `#f00` (#rgb)
* `#f00c` (#rgba)：`CSS` 中无对应的值
* `#ff0000` (#rrggbb)
* `#ff0000cc` (#rrggbbaa)：`CSS` 中无对应的值
* `rgb(255, 0, 0)`
* `rgba(255, 0, 0, 0.9)`
* `hsl(360, 100%, 100%)`
* `hsla(360, 100%, 100%, 0.9)`
* `transparent`
* `0xff00ff00` (0xrrggbbaa)：`CSS` 中无对应的值
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

<a name="pixelratio"></a>
## PixelRatio 像素密度

在 `React-Native` 中，访问设备像素密度的方法由 `PixelRatio` 类提供。

我们的应用通常都会运行在不同的设备上，并且这些设备的像素密度很有可能各不相同。这会造成一个现象就是：

* 定义了元素的边框为 `1像素`，而实际上在不同像素密度的设备上结果不一样，比如：iPhone6 显示为 `2像素`，iPhone6 Plus 显示为 `3像素`；
* 对于一个图片来讲，因为设备的像素密度不同，它也需要对应不同尺寸的规则，以防止图片过小变得模糊；

### 根据像素密度指定边框厚度

出于对产品体验的一致性，我们会要求不论是在哪种设备上，其边框厚度都应该是相同的。一个取得物理上的相同边框厚度的好方法就是用逻辑尺寸除以像素密度比：

```
var styles = StyleSheet.create({
    box: {
        borderWidth: 1 / PixelRatio.get(),
        borderStyle: solid
    }
});
```

上述代码将保证你的应用在所有的设备上（像素密度），都获得 `1像素` 的边框厚度。`PixelRatio` 通过 `get()` 方法来返回设备的像素密度。

未完待续。。。