## 使用伪类的demo

> 不需要向页面添加html元素，使用伪元素，通过样式实现loading

可实现跳转的元素（如：a, button）在请求服务器内容时，由于延时导致请求的内容无法到达客户端，往往需要添加一个 `loading` 的模块作为提示，这样往往需要向页面添加内元素，利用伪元素也可以实现这样的效果。

[demo](https://codepen.io/lvzhenbang/pen/ReNaBV)

> *child, *type

`*child, *type` 这两大类元素是常用的伪类，下面是一个可视化的工具，可以更好的认识这两类伪类。

[可视化工具](https://codepen.io/rachel_web/pen/RPOxxR)

> `::marker` 定制列表项标记块的效果

除了使用元素li，dt, dd这样的列表项，还可以通过 `display: list-item; counter-reset:*; counter-increament:*;`自定义列表项的标记。由于`::marker`的浏览器支持不好，可以使用 `::before` 来代替。

[demo](https://codepen.io/lvzhenbang/pen/ReNeoa)

> 开关状态（非默认的input(type为radio、checkbox)样式）(::before, ::after)

[demo](https://codepen.io/lvzhenbang/pen/vVEeoZ)

> 下拉菜单的指示按钮(::after)

[demo](https://codepen.io/lvzhenbang/pen/QZbEoe)

> dialog (::backdrop)

[demo](https://codepen.io/lvzhenbang/pen/PyjYzZ)

> 浮动的label (:focus/:not/::placeholder/:placeholder-shown)

[demo](https://codepen.io/lvzhenbang/pen/yRowVE)

> 多行文本的省略，使用伪元素 (::after) ，末尾的淡出效果

[demo](https://codepen.io/chriscoyier/pen/iBtep)

> 多行文本的省略，使用伪元素 (::after) ，末尾的淡出效果

[demo](https://codepen.io/lvzhenbang/pen/ROmzzj)
