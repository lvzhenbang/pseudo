# pseudo

what can a pseudo-class do?

## 伪类（pseudo-class）& 伪元素（pseudo-element）

伪类和伪元素在web开发中用的好的话，可以说犹如神助。

但一定要分清楚，什么是伪类，什么是伪元素。

如何区分伪元素与伪类？

答：伪元素在html文档渲染后，页面中有相应的内容显示，同时能够设置它的样式，而伪类只能设置样式

伪元素和元素的区别？

答：很明显，从字面意思上来说，伪元素就不是真正的元素，而只有形而没有神，在DOM结构中根本没有它，也就是说你不能用js来操作它。（伪类可以，因为伪类是css选择器）

常见伪元素如下：

::before, ::after, ::placeholder

## 常用

### 元素状态

<details>

<summary> 目录</summary>

* [:enabled/:disabled](#:enabled/:disabled)
* [:focus](#:focus)
* [:checked](#:checked)
* [:link/:hover/:visited/:active](#:link/:visited/:hover/:active)

</details>

### 文章排版

<details>
<summary> 目录 </summary>

* [:first-line](#:first-line)
* [:first-letter](#:first-letter)

</details>

### 表单样式

<details>
<summary> 目录 </summary>

* [:checked](#:checked)
* [:focus](#:focus)
* [:required](#:required)（兼容性不好）
* [:read-write/:read-only](#:read-write/:read-only)（兼容性不好）
* [:valid/:invalid](#:valid/:invalid)
* [:optional](#:optional)（兼容性不好）
* [:placeholder](#:placeholder)
* [:placeholder-shown](#:placeholder-shown)（兼容性不好）
* [:in-range/:out-of-range](#:in-range/:out-of-range)（兼容性不好）

</details>

### 其他

<details>

<summary> 目录 </summary>

* [:lang](#:lang)
* [:root](#:root)
* [:target](#:target)
* [:not](#:not)
* [:empty](#:empty)
* [:matches](#:matches)

*-child 系列
*-type 系列

</details>

未完待续...

### 目录列表

#### ::after/ ::before

描述：这一对伪元素，它们允许使用者通过css向html页面中添加内容。

浏览器支持：ie8+/chrome2+/safari1.3+/opera 6+/Android/ios

用途：在[清除浮动](https://github.com/twbs/bootstrap/blob/v3.4.0-dev/less/mixins/clearfix.less)中，用作一个占位元素；字体图标（[iconfont](http://www.iconfont.cn/)）

注意：ie8只支持这种形式 `:after/:before`

是否常用：是

#### :link/:visited/:hover/:active

* :link(直接设置连接的样式),
* :visited（区别与其他未访问过的样式）,
* :hover（鼠标移动上去后的样式）,
* :active（鼠标单击触发时的样式）

描述：这是一组伪类，除了`:link` 只能作用于a[href]外，其它的适用于任何元素。

浏览器支持：chrome, sarari 2.0.4+, firefox, opera, ie 4+; android/ios(未定义)

注意：常用的为hover 和 active

是否常用：是

</br> [▲ 返回目录](#元素状态)

#### :focus

描述：当元素获得焦点时，该伪类样式起效果。

用途：当按键盘的tab键时，页面出现变化的样式，不同的浏览器默认的focus样式不一样；默认的input, textarea, button, 以及设置了contentediable的元素focus工作，如果给其他的元素设置tabindex属性，它们的focus也将工作。

浏览器支持：chrome 2+, safari 1.3+, firefox, opera 9.2, ie 8+, android, ios

参考资料：

[CSS-TRICKS :focus](https://css-tricks.com/almanac/selectors/f/focus/)
[More about contenteditable](http://html5doctor.com/the-contenteditable-attribute/)
[More about TabIndex](http://snook.ca/archives/accessibility_and_usability/elements_focusable_with_tabindex)

是否常用：是

</br> [▲ 返回目录](#元素状态)

#### :focus-within

描述：匹配哪些它们自身没有 `:focus` 或者它们的子孙元素没有 `:focus` 的元素。

浏览器支持：chrome 60+, firefox 52+, edg/ie(不支持)， safari 10.1+, opera 47+, ios 10.3+, android(不支持)

#### :checked

用途：当元素处于选中状态的时候这个伪类起作用。常见的元素是input(type为radio或checkbox)。这种可以表示开关的状态的伪类可以减少对js的使用。

浏览器支持：chrome, safari, firefox, opera 9+, ie 9+，android, ios

注意：虽然其他浏览器的支持不错，但是ie支持9以上的版本。

是否常用：是

</br> [▲ 返回目录](#元素状态)

#### :enabled/:disabled

描述：该对伪类给元素提供了一个条件，用来设置元素的样式。

用途：该伪类对应元素(input/ button/ textarea/ optgroup / option /fieldset /seelect)内的属性 `disabled` ，这些元素时html用于与用户进行交互的。

浏览器支持：chrome, safari 3.1+, firefox, opera 9+, android, ios

参考资料：

[Pseudo-classes – The Basics](https://www.sitepoint.com/pseudo-classes-the-basics/)

[MDN](https://developer.mozilla.org/en-US/docs/Web/CSS/:disabled)

是否常用：是

</br> [▲ 返回目录](#元素状态)

#### :not

描述：它是一个取反的伪类，ie7/8只支持[element~element], [attr*=] 这种方式。

浏览器支持：chrome, safari 3.2+, firefox 3.5+, opera, ie 9+, ios, android

是否常用：是

</br> [▲ 返回目录](#文章排版)

#### :empty

描述：改为元素匹配不含任何内容的元素，或者只含有注释的元素。

浏览器支持：chrome 4+, safari 3.2+, firefox 3.5, opera 9+, ie 9+, android, ios 3.2

</br> [▲ 返回目录](#文章排版)

#### :matches

描述：这是个实验特性，跟以前的 `:any()` 类似，它的参数是一个选择器列表

浏览器支持：支持很差，ie根本不支持，andriod 和 ios 也只支持部分特性。

</br> [▲ 返回目录](#文章排版)

#### :nth-child(an+b)/:nth-last-child() // a,b是整数值，+/-为运算符

描述：根据传入的一个运算公式，选择第几个元素，或者说每个几个元素选择一个。`:nth-child` 是从第一个开始，`:nth-last-child` 是从最后一个开始。

用途：给子元素按照不同的分类设置样式，bootstrap/v2.2.0 [table tbody 中的斑马线效果](https://github.com/twbs/bootstrap/blob/v2.2.0/less/tables.less)

浏览器支持：chrome, safari 3.2+, firefox, opera, ie 9+, android, ios

是否常用：是

#### :first-child/:last-child

描述：匹配该伪类所指代的元素的父元素下的第一个子元素（或最后一个子元素）

用途：bootstrap中table 的{斑马线](https://github.com/twbs/bootstrap/blob/v2.2.0/less/tables.less#L39)

浏览器支持：chrome, safari 3.2+, firefox, opera 9.5+, ie 7, android, ios

是否常用：是

#### :nth-only-child

描述：匹配该伪类所指代元素的父元素下只有它这么一个元素，该伪类设置的样式起作用。

用途：它可以用来和 `:nth-child()` 一起使用，处理只有一个元素的情况。

浏览器支持：chrome, safari, firefox, opera, ie, android, ios

示例：

[demo](https://codepen.io/lvzhenbang/pen/GXPavj)

#### :first-of-type/:last-of-type

描述：它们与 `:first-child/:last-child` 的效果类似，但不同的是它们匹配的元素类型可以不一致，但是后者必须一致。

#### :nth-of-type(an+b)/:nth-last-of-type  // a,b是整数值，+/-为运算符

描述：根据传入的一个运算公式，选择某类元素的第n个，或者每隔n个选择一个。`:nth-of-type` 是从第一个开始，`:nth-last-of-type` 是从最后一个开始。

用途：给子元素按照不同的分类设置样式，bootstrap/v2.2.0 [table tbody 中的斑马线效果](https://github.com/twbs/bootstrap/blob/v3-dev/less/tables.less#L114), 也包括之后的版本

浏览器支持：chrome, safari 3.2+, firefox, opera 9.5+, ie 9+, android, ios

是否常用：是

#### :nth-only-child

描述：该伪类所指代元素的父元素下只有它这么一个元素，该伪类设置的样式起作用。

用途：它可以用来和 `:nth-of-type()` 一起使用，处理只有一个元素的情况。它与 `nth-only-child`，区别就是伪类所指代的元素的父元素的所有子元素是否是同一类。

浏览器支持：chrome, safari, firefox, opera, ie, android, ios

示例：

[demo](https://codepen.io/lvzhenbang/pen/KxbLqo)


#### ::first-line

描述：该伪类所指代元素的第一行文本。具体支持哪些样式，可参考[w3c 官方文档](https://www.w3.org/TR/CSS2/selector.html#first-line-pseudo)

用途：文章排版。

浏览器支持：chrome, safari, firefox, opera, ie, android, ios

注意：该伪类指代的元素必须是块级元素

参考资料：

[::first-line](https://css-tricks.com/almanac/selectors/f/first-line/)

示例：

[demo](https://codepen.io/lvzhenbang/pen/MqZMYR)

</br> [▲ 返回目录](#文章排版)

#### ::first-letter

描述：该伪类所指代元素的第一个字符的样式。具体支持哪些样式，可参考[w3c 官方文档](https://www.w3.org/TR/CSS2/selector.html#first-line-pseudo)

用途：文章排版

浏览器支持：chrome 1+, safari 1+, firefox 1+, opera 3.5+, ie 5.5+, android, ios

注意：该伪类指代的元素必须是块级元素

参考资料：

[::first-letter](https://css-tricks.com/almanac/selectors/f/first-letter/)

示例：

[demo](https://codepen.io/lvzhenbang/pen/MqZMYR)

</br> [▲ 返回目录](#文章排版)

#### :target

描述：该伪类匹配与地址导航栏中当前url中的hash值与html源代码中的id选择器值一致的元素。若匹配成功，则该样式起作用；反之，则不起作用。

注意：该伪类所指定的元素的子元素，无法设置动画效果，只能对目标元素自身设置动画效果。

浏览器支持：chrome, safari 1.3+, firefox 1.3+, opera 9.5+, ie 9+, android 2.1+, ios 2+

参考资料：

[A simple image gallery using only CSS and the :target selector](https://hacks.mozilla.org/2012/02/a-simple-image-gallery-using-only-css-and-the-target-selector/)

示例：

[demo](https://codepen.io/lvzhenbang/pen/eLbwxz)

[css-tricks demo](https://css-tricks.com/examples/Target/)

[http://jsfiddle.net/codepo8/wsD9L/1/]

</br> [▲ 返回目录](#文章排版)

#### :lang()

描述：该伪类匹配的元素是依据html文档中的lang属性值和该伪类内传入的参数是否一致来决定的。

浏览器支持：兼容所有浏览器。


</br> [▲ 返回目录](#其他)

#### :root

描述：该伪类就表示html文档中的根元素，它也可以用于其他标记性语言中，如：svg, xml。

注意：如果该伪类选择器和html元素选择器同时出现在页面中，伪类选择器的（权重大）优先级高。

浏览器支持：chrome, safari, firefox, opera 9.5+, ie 9+, android, ios

</br> [▲ 返回目录](#文章排版)

#### :dir()

描述：它可以控制document文档中的文本流向（ltr/rtl），实现效果和text-align (left/center/right/justify)

浏览器支持：最新版的edg/firfox/chrome/safari

#### :valid/:invalid

描述：匹配用户的输入是否合法，如果合法显示 `:valid` 的样式， 否则，显示 `:invalid` 的样式。

浏览器支持：chrome 10+, safari 5+, firefox 4+, opera, ie 10+, android 4.4.4, ios 10.3+

是否常用：不常用

</br> [▲ 返回目录](#表单样式)

#### :required

描述：该伪类指代元素中含有required属性的元素，常见的就是form表单中的元素。

用途：不把服务器当作验证用户输入的唯一途径，实现浏览器的自检测。

浏览器支持：chrome 10+, safari 5+, firefox 4+, opera, ie 10+, android 4.4.4, ios 10.3+

</br> [▲ 返回目录](#表单样式)

#### :optional

描述：该伪类针对form表单元素, 如：input或select，当它们未设置required属性，它们设置的样式起效果。

浏览器支持：chrome 15+, safari 5+, firefox 4+, opera 15+, ie 10+, android 2.3, ios 5.1+

</br> [▲ 返回目录](#表单样式)

#### ::placeholder

描述：设置显示的 `placeholder` 属性值的样式

浏览器支持：chrome 4+, firefox 19+, safari 5+, opera 15+, ie(no), edg(需要前缀), android, ios 4.3+

</br> [▲ 返回目录](#表单样式)

#### :placeholder-shown

描述：匹配表单元素，设置元素展示 `placeholder` 属性值时的 input 元素样式。

浏览器支持：chrome 4+, safari 5+, firefox 19+, opera 15+, ie(no), edg(no), ios 4.3+, android 6+

</br> [▲ 返回目录](#表单样式)

#### :read-write/:read-only

描述：匹配用户可选择的元素。

浏览器支持：chrome 36+, safari 9+, firefox 3+, opera 23+, edg 13+, ie(不支持)，android ios 6+, ios 9.2+

是否常用：不常用

#### :in-range/:out-of-range

描述：匹配属性值在这个范围内（或不再范围内），例如：input(type=range) 的 max 和最小。

浏览器支持：chrome 53+, safari 10.1+, firefox 50+, opera +40, ios 10.3+, android 6+,

是否常用：否

</br> [▲ 返回目录](#表单样式)

#### ::selection

描述：匹配被用户选中的元素的样式。

浏览器支持：chrome 4+, safari 3.1+, firefox 2+, opera 10.1+, ie 9+, ios (不支持), android 4.4+

#### :blank

描述：除了火狐支持外

浏览器支持：其他浏览器均不支持。(`can i use` 上根本查不到)

