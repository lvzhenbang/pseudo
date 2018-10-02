## 用css做图形

在前端开发中，你或多或少都会接触到css图形。之前我整理过 `[伪元素&伪类](https://github.com/lvzhenbang/pseudo)` 的内容，为的就是更加熟悉了解它们，以便更好的使用它们。同时也也使用它一做了一些动画。 `[css3-animate](https://github.com/lvzhenbang/css3-animate)`。

这里说的用css做图形，其实是使用一个html元素，结合它的伪元素 `::before & ::after` （不需要其他额外的非伪元素的html元素），然后定义样式来生成所需的图形。

这里不是说不可以使用其它的html元素，只是这样的好处是在html方便引入，而不需要每次引入都需要添加大量的html片段（夸张说法）。

### 目录

<details>
<summary> 几何图形 </summary>

* [等腰直角三角形(直角位置左上)](#shape-triangle-top-left)
* [等腰直角三角形(直角位置右上)](#shape-triangle-top-right)
* [等腰直角三角形(直角位置左下)](#shape-triangle-bottom-left)
* [等腰直角三角形(直角位置右下)](#shape-triangle-bottom-right)
* [等边三角形（箭头朝上）](#shape-triangle-up)
* [等边三角形（箭头朝下）](#shape-triangle-down)
* [等边三角形（箭头朝左）](#shape-triangle-left)
* [等边三角形（箭头朝右）](#shape-triangle-right)
* [矩形形](#shpae-rectangle)
* [正方形](#shpae-square)
* [正五边形](#shape-pentaton)
* [正六边形](#shape-shexagon)
* [正七边形](#shape-square)
* [正八边形](#shape-octagon)
* [平行四边形](#shape-parallelogram)
* [圆形](#shape-circle)
* [椭圆形](#shape-oval)
* [梯形](#shape-trapzoid)
* [扇形](#shape-cone)

</details>

<details>
<summary> 星形 </summary>

* [五角星](#shape-start-5)
* [六角星](#shape-star-6)
* [八角星形](#shape-burst-8)
* [十二角星形](#shape-burst-12)

</details>

<details>
<summary> 卡通图形 </summary>

* [吃豆人](#shape-pacman)
* [外星入侵者](#shape-sapce-invader)
* [鸡蛋](#shape-egg)

</details>

<details>
<summary> 图标图形 </summary>

* [facebook](#shape-facebook)
* [锁](#shape-lock)
* [放大镜](#shape-magnifying-glass)
* [星形](#shape-star-5)
* [心形](#shape-heart)
* [月亮](#shape-moon)
* [徽章](#shape-badge-ribbon)
* [电视](#shape-tv)
* [标签](#shape-flag)
* [十字形](#shape-cross)
* [方向标](#shape-pointer)
* [返回箭头](#shape-curve-arrow)

</details>

<details>
<summary> 钻石图形 </summary>

* [四方形钻](#shape-diamond-square)
* [‘盾’形钻](#shape-diamond-shield)
* [‘菱形’钻](#shape-diamonds-arrow)
* [‘切割’钻](#shape-diamond-cut)

</details>

<details>
<summary> 其他 </summary>

* [太极图](#shape-yinyang)

</details>

### 图形列表

#### shape-square

```
#square {
    width: 100px;
    height: 100px;
    background: red;
}
```

[demo]()

[▲ 返回目录](#目录)

#### shape-rctangle

```
#rectangle {
    width: 200px;
    height: 100px;
    background: red;
}
```

[▲ 返回目录](#目录)

#### shape-circle

```
#circle {
    width: 100px;
    height: 100px;
    background: red;
    border-radius: 50%
}
```

[▲ 返回目录](#目录)

#### shape-oval

```
#oval {
    width: 200px;
    height: 100px;
    background: red;
    border-radius: 100px / 50px;
}
```

[▲ 返回目录](#目录)

#### shape-cone

```
#cone {
    width: 0;
    height: 0;
    border-left: 70px solid transparent;
    border-right: 70px solid transparent;
    border-top: 100px solid red;
    border-radius: 50%;
}
```

[▲ 返回目录](#目录)

#### shape-trapezoid

```
#trapezoid {
    border-bottom: 100px solid red;
    border-left: 50px solid transparent;
    border-right: 50px solid transparent;
    height: 0;
    width: 100px;
}
```

[▲ 返回目录](#目录)

#### shape-parallelogram

```
#parallelogram {
    width: 150px;
    height: 100px;
    transform: skew(20deg);
    background: red;
}
```

[▲ 返回目录](#目录)

#### shape-pentagon

```
#pentagon {
    position: relative;
    width: 54px;
    box-sizing: content-box;
    border-width: 50px 18px 0;
    border-style: solid;
    border-color: red transparent;
}

#pentagon:before {
    content: "";
    position: absolute;
    height: 0;
    width: 0;
    top: -85px;
    left: -18px;
    border-width: 0 45px 35px;
    border-style: solid;
    border-color: transparent transparent red;
}
```

[▲ 返回目录](#目录)

#### shape-hexagon

```
#hexagon {
    width: 100px;
    height: 55px;
    background: red;
    position: relative;
}
#hexagon:before {
    content: "";
    position: absolute;
    top: -25px;
    left: 0;
    width: 0;
    height: 0;
    border-left: 50px solid transparent;
    border-right: 50px solid transparent;
    border-bottom: 25px solid red;
}
#hexagon:after {
    content: "";
    position: absolute;
    bottom: -25px;
    left: 0;
    width: 0;
    height: 0;
    border-left: 50px solid transparent;
    border-right: 50px solid transparent;
    border-top: 25px solid red;
}
```

[▲ 返回目录](#目录)

#### shape-octagon

```
#octagon {
    width: 100px;
    height: 100px;
    background: red;
    position: relative;
}
#octagon:before {
    content: "";
    width: 100px;
    height: 0;
    position: absolute;
    top: 0;
    left: 0;
    border-bottom: 29px solid red;
    border-left: 29px solid #eee;
    border-right: 29px solid #eee;
}
#octagon:after {
    content: "";
    width: 100px;
    height: 0;
    position: absolute;
    bottom: 0;
    left: 0;
    border-top: 29px solid red;
    border-left: 29px solid #eee;
    border-right: 29px solid #eee;
}  
```

[▲ 返回目录](#目录)

#### shape-triangle-up

```
#triangle-up {
    width: 0;
    height: 0;
    border-left: 50px solid transparent;
    border-right: 50px solid transparent;
    border-bottom: 100px solid red;
}
```

[▲ 返回目录](#目录)

#### shape-triangle-down

```
#triangle-down {
    width: 0;
    height: 0;
    border-left: 50px solid transparent;
    border-right: 50px solid transparent;
    border-top: 100px solid red;
}
```

[▲ 返回目录](#目录)

#### shape-triangle-left

```
#triangle-left {
    width: 0;
    height: 0;
    border-left: 50px solid transparent;
    border-right: 50px solid transparent;
    border-top: 100px solid red;
}
```

[▲ 返回目录](#目录)

#### shape-triangle-right

```
#triangle-right {
    width: 0;
    height: 0;
    border-top: 50px solid transparent;
    border-left: 100px solid red;
    border-bottom: 50px solid transparent;
}
```

[▲ 返回目录](#目录)

#### shape-triangle-top-left

```
#triangle-topleft {
    width: 0;
    height: 0;
    border-top: 100px solid red;
    border-right: 100px solid transparent;
}
```

[▲ 返回目录](#目录)

#### shape-triangle-top-right

```
#triangle-topright {
    width: 0;
    height: 0;
    border-top: 100px solid red;
    border-left: 100px solid transparent;
}
```

[▲ 返回目录](#目录)

#### shape-triangle-bottom-left

```
#triangle-bottomleft {
    width: 0;
    height: 0;
    border-bottom: 100px solid red;
    border-right: 100px solid transparent;
}
```

[▲ 返回目录](#目录)

#### shape-triangle-bottom-right

```
#triangle-bottomright {
    width: 0;
    height: 0;
    border-bottom: 100px solid red;
    border-left: 100px solid transparent;
}
```

[▲ 返回目录](#目录)

#### shape-curve-arrow

```
#curvedarrow {
    position: relative;
    width: 0;
    height: 0;
    border-top: 9px solid transparent;
    border-right: 9px solid red;
    transform: rotate(10deg);
}

#curvedarrow:after {
    content: "";
    position: absolute;
    border: 0 solid transparent;
    border-top: 3px solid red;
    border-radius: 20px 0 0 0;
    top: -12px;
    left: -9px;
    width: 12px;
    height: 12px;
    transform: rotate(45deg);
}
```

[▲ 返回目录](#目录)

#### shape-star-5

```
margin: 50px 0;
    position: relative;
    display: block;
    color: red;
    width: 0px;
    height: 0px;
    border-right: 100px solid transparent;
    border-bottom: 70px solid red;
    border-left: 100px solid transparent;
    transform: rotate(35deg);
}
#star-five:before {
    border-bottom: 80px solid red;
    border-left: 30px solid transparent;
    border-right: 30px solid transparent;
    position: absolute;
    height: 0;
    width: 0;
    top: -45px;
    left: -65px;
    display: block;
    content: '';
    transform: rotate(-35deg);
}
#star-five:after {
    position: absolute;
    display: block;
    color: red;
    top: 3px;
    left: -105px;
    width: 0px;
    height: 0px;
    border-right: 100px solid transparent;
    border-bottom: 70px solid red;
    border-left: 100px solid transparent;
    transform: rotate(-70deg);
    content: '';
}  
```

[▲ 返回目录](#目录)

#### shape-star-6


```
#star-six {
    width: 0;
    height: 0;
    border-left: 50px solid transparent;
    border-right: 50px solid transparent;
    border-bottom: 100px solid red;
    position: relative;
}
#star-six:after {
    width: 0;
    height: 0;
    border-left: 50px solid transparent;
    border-right: 50px solid transparent;
    border-top: 100px solid red;
    position: absolute;
    content: "";
    top: 30px;
    left: -50px;
}  
```

[▲ 返回目录](#目录)

#### shape-burst-12

```
#burst-12 {
    background: red;
    width: 80px;
    height: 80px;
    position: relative;
    text-align: center;
}
#burst-12:before,
#burst-12:after {
    content: "";
    position: absolute;
    top: 0;
    left: 0;
    height: 80px;
    width: 80px;
    background: red;
}
#burst-12:before {
    transform: rotate(30deg);
}
#burst-12:after {
    transform: rotate(60deg);
}  
```

[▲ 返回目录](#目录)

#### shape-burst-8

```
#burst-8 {
    background: red;
    width: 80px;
    height: 80px;
    position: relative;
    text-align: center;
    transform: rotate(20deg);
}
#burst-8:before {
    content: "";
    position: absolute;
    top: 0;
    left: 0;
    height: 80px;
    width: 80px;
    background: red;
    transform: rotate(135deg);
}  
```

[▲ 返回目录](#目录)

#### shape-heart

```
#heart {
    position: relative;
    width: 100px;
    height: 90px;
}
#heart:before,
#heart:after {
    position: absolute;
    content: "";
    left: 50px;
    top: 0;
    width: 50px;
    height: 80px;
    background: red;
    border-radius: 50px 50px 0 0;
    transform: rotate(-45deg);
    transform-origin: 0 100%;
}
#heart:after {
    left: 0;
    transform: rotate(45deg);
    transform-origin: 100% 100%;
}

```

[▲ 返回目录](#目录)

#### shape-infinity

```
#infinity {
    position: relative;
    width: 212px;
    height: 100px;
    box-sizing: content-box;
}
#infinity:before,
#infinity:after {
    content: "";
    box-sizing: content-box;
    position: absolute;
    top: 0;
    left: 0;
    width: 60px;
    height: 60px;
    border: 20px solid red;
    border-radius: 50px 50px 0 50px;
    transform: rotate(-45deg);
}
#infinity:after {
    left: auto;
    right: 0;
    border-radius: 50px 50px 50px 0;
    transform: rotate(45deg);
}
```

[▲ 返回目录](#目录)

#### shape-diamond-square

```
#diamond-square {
    width: 0;
    height: 0;
    border: 50px solid transparent;
    border-bottom-color: red;
    position: relative;
    top: -50px;
}
#diamond-square:after {
    content: '';
    position: absolute;
    left: -50px;
    top: 50px;
    width: 0;
    height: 0;
    border: 50px solid transparent;
    border-top-color: red;
}
```

[▲ 返回目录](#目录)

#### shape-diamond-narrow

```
#diamond-narrow {
    width: 0;
    height: 0;
    border: 50px solid transparent;
    border-bottom: 70px solid red;
    position: relative;
    top: -50px;
}
#diamond-narrow:after {
    content: '';
    position: absolute;
    left: -50px;
    top: 70px;
    width: 0;
    height: 0;
    border: 50px solid transparent;
    border-top: 70px solid red;
}
```

[▲ 返回目录](#目录)

#### shape-diamond-shield


```
#diamond-shield {
    width: 0;
    height: 0;
    border: 50px solid transparent;
    border-bottom: 20px solid red;
    position: relative;
    top: -50px;
}
#diamond-shield:after {
    content: '';
    position: absolute;
    left: -50px;
    top: 20px;
    width: 0;
    height: 0;
    border: 50px solid transparent;
    border-top: 70px solid red;
}
```

[▲ 返回目录](#目录)

#### shape-diamond-cut

```
#cut-diamond {
    border-style: solid;
    border-color: transparent transparent red transparent;
    border-width: 0 25px 25px 25px;
    height: 0;
    width: 50px;
    box-sizing: content-box;
    position: relative;
    margin: 20px 0 50px 0;
}
#cut-diamond:after {
    content: "";
    position: absolute;
    top: 25px;
    left: -25px;
    width: 0;
    height: 0;
    border-style: solid;
    border-color: red transparent transparent transparent;
    border-width: 70px 50px 0 50px;
}
```

[▲ 返回目录](#目录)

#### shape-egg

```
#egg {
    display: block;
    width: 126px;
    height: 180px;
    background-color: red;
    border-radius: 50% 50% 50% 50% / 60% 60% 40% 40%;
}
```

[▲ 返回目录](#目录)

#### shape-pacman

```
#pacman {
    width: 0px;
    height: 0px;
    border-right: 60px solid transparent;
    border-top: 60px solid red;
    border-left: 60px solid red;
    border-bottom: 60px solid red;
    border-top-left-radius: 60px;
    border-top-right-radius: 60px;
    border-bottom-left-radius: 60px;
    border-bottom-right-radius: 60px;
}
```

[▲ 返回目录](#目录)

#### shape-tablk-bubble

```
#talkbubble {
    width: 120px;
    height: 80px;
    background: red;
    position: relative;
    -moz-border-radius: 10px;
    -webkit-border-radius: 10px;
    border-radius: 10px;
}
#talkbubble:before {
    content: "";
    position: absolute;
    right: 100%;
    top: 26px;
    width: 0;
    height: 0;
    border-top: 13px solid transparent;
    border-right: 26px solid red;
    border-bottom: 13px solid transparent;
}
```

[▲ 返回目录](#目录)

#### shape-yin-yang

```
#yin-yang {
    width: 96px;
    box-sizing: content-box;
    height: 48px;
    background: #eee;
    border-color: red;
    border-style: solid;
    border-width: 2px 2px 50px 2px;
    border-radius: 100%;
    position: relative;
}
#yin-yang:before {
    content: "";
    position: absolute;
    top: 50%;
    left: 0;
    background: #eee;
    border: 18px solid red;
    border-radius: 100%;
    width: 12px;
    height: 12px;
    box-sizing: content-box;
}
#yin-yang:after {
    content: "";
    position: absolute;
    top: 50%;
    left: 50%;
    background: red;
    border: 18px solid #eee;
    border-radius: 100%;
    width: 12px;
    height: 12px;
    box-sizing: content-box;
}
```

[▲ 返回目录](#目录)

#### shape-badge-ribbon

```
#badge-ribbon {
    position: relative;
    background: red;
    height: 100px;
    width: 100px;
    border-radius: 50px;
}
#badge-ribbon:before,
#badge-ribbon:after {
    content: '';
    position: absolute;
    border-bottom: 70px solid red;
    border-left: 40px solid transparent;
    border-right: 40px solid transparent;
    top: 70px;
    left: -10px;
    transform: rotate(-140deg);
}
#badge-ribbon:after {
    left: auto;
    right: -10px;
    transform: rotate(140deg);
}
```

[▲ 返回目录](#目录)

#### shape-space-invader

```
#space-invader {
    box-shadow: 0 0 0 1em red,
    0 1em 0 1em red,
    -2.5em 1.5em 0 .5em red,
    2.5em 1.5em 0 .5em red,
    -3em -3em 0 0 red,
    3em -3em 0 0 red,
    -2em -2em 0 0 red,
    2em -2em 0 0 red,
    -3em -1em 0 0 red,
    -2em -1em 0 0 red,
    2em -1em 0 0 red,
    3em -1em 0 0 red,
    -4em 0 0 0 red,
    -3em 0 0 0 red,
    3em 0 0 0 red,
    4em 0 0 0 red,
    -5em 1em 0 0 red,
    -4em 1em 0 0 red,
    4em 1em 0 0 red,
    5em 1em 0 0 red,
    -5em 2em 0 0 red,
    5em 2em 0 0 red,
    -5em 3em 0 0 red,
    -3em 3em 0 0 red,
    3em 3em 0 0 red,
    5em 3em 0 0 red,
    -2em 4em 0 0 red,
    -1em 4em 0 0 red,
    1em 4em 0 0 red,
    2em 4em 0 0 red;
    background: red;
    width: 1em;
    height: 1em;
    overflow: hidden;
    margin: 50px 0 70px 65px;
}
```

[▲ 返回目录](#目录)

#### shape-tv

```
#tv {
    position: relative;
    width: 200px;
    height: 150px;
    margin: 20px 0;
    background: red;
    border-radius: 50% / 10%;
    color: white;
    text-align: center;
    text-indent: .1em;
}
#tv:before {
    content: '';
    position: absolute;
    top: 10%;
    bottom: 10%;
    right: -5%;
    left: -5%;
    background: inherit;
    border-radius: 5% / 50%;
}
```

[▲ 返回目录](#目录)

#### shape-mangnifying-glass


```
#magnifying-glass {
    font-size: 10em;
    display: inline-block;
    width: 0.4em;
    box-sizing: content-box;
    height: 0.4em;
    border: 0.1em solid red;
    position: relative;
    border-radius: 0.35em;
}
#magnifying-glass:before {
    content: "";
    display: inline-block;
    position: absolute;
    right: -0.25em;
    bottom: -0.1em;
    border-width: 0;
    background: red;
    width: 0.35em;
    height: 0.08em;
    transform: rotate(45deg);
}
```


[▲ 返回目录](#目录)

#### shape-facebook

```
#facebook-icon {
    background: red;
    text-indent: -999em;
    width: 100px;
    height: 110px;
    box-sizing: content-box;
    border-radius: 5px;
    position: relative;
    overflow: hidden;
    border: 15px solid red;
    border-bottom: 0;
}
#facebook-icon:before {
    content: "/20";
    position: absolute;
    background: red;
    width: 40px;
    height: 90px;
    bottom: -30px;
    right: -37px;
    border: 20px solid #eee;
    border-radius: 25px;
    box-sizing: content-box;
}
#facebook-icon:after {
    content: "/20";
    position: absolute;
    width: 55px;
    top: 50px;
    height: 20px;
    background: #eee;
    right: 5px;
    box-sizing: content-box;
}
```

[▲ 返回目录](#目录)

#### shape-moon

```
#moon {
    width: 80px;
    height: 80px;
    border-radius: 50%;
    box-shadow: 15px 15px 0 0 red;
}
```

[▲ 返回目录](#目录)

#### shape-flag

```
#flag {
    width: 110px;
    height: 56px;
    box-sizing: content-box;
    padding-top: 15px;
    position: relative;
    background: red;
    color: white;
    font-size: 11px;
    letter-spacing: 0.2em;
    text-align: center;
    text-transform: uppercase;
}
#flag:after {
    content: "";
    position: absolute;
    left: 0;
    bottom: 0;
    width: 0;
    height: 0;
    border-bottom: 13px solid #eee;
    border-left: 55px solid transparent;
    border-right: 55px solid transparent;
}
```

[▲ 返回目录](#目录)

#### shape-cross

```
#cross {
    height: 100px;
    width: 100px;
    position: relative;
}

#cross:before,
#cross:after {
    content: "";
    position: absolute;
    background: red;
}

#cross:before {
    top: 0;
    left: 40px;
    width: 20px;
    height: 100px;
}

#cross:after {
    top: 40px;
    left: 0px;
    width: 100px;
    height: 20px;
}
```

[▲ 返回目录](#目录)

#### shape-base

```
#base {
    background: red;
    display: inline-block;
    height: 55px;
    margin-left: 20px;
    margin-top: 55px;
    position: relative;
    width: 100px;
}
#base:before {
    border-bottom: 35px solid red;
    border-left: 50px solid transparent;
    border-right: 50px solid transparent;
    content: "";
    height: 0;
    left: 0;
    position: absolute;
    top: -35px;
    width: 0;
}
```

[▲ 返回目录](#目录)

#### shape-pointer

```
#pointer {
    width: 200px;
    height: 40px;
    position: relative;
    background: red;
}
#pointer:after {
    content: "";
    position: absolute;
    left: 0;
    bottom: 0;
    width: 0;
    height: 0;
    border-left: 20px solid white;
    border-top: 20px solid transparent;
    border-bottom: 20px solid transparent;
}
#pointer:before {
    content: "";
    position: absolute;
    right: -20px;
    bottom: 0;
    width: 0;
    height: 0;
    border-left: 20px solid red;
    border-top: 20px solid transparent;
    border-bottom: 20px solid transparent;
}
```

[▲ 返回目录](#目录)

#### shape-lock

```
#lock {
    font-size: 8px;
    position: relative;
    width: 18em;
    height: 13em;
    border-radius: 2em;
    top: 10em;
    box-sizing: border-box;
    border: 3.5em solid red;
    border-right-width: 7.5em;
    border-left-width: 7.5em;
    margin: 0 0 6rem 0;
}
#lock:before {
    content: "";
    box-sizing: border-box;
    position: absolute;
    border: 2.5em solid red;
    width: 14em;
    height: 12em;
    left: 50%;
    margin-left: -7em;
    top: -12em;
    border-top-left-radius: 7em;
    border-top-right-radius: 7em;
}
#lock:after {
    content: "";
    box-sizing: border-box;
    position: absolute;
    border: 1em solid ted;
    width: 5em;
    height: 8em;
    border-radius: 2.5em;
    left: 50%;
    top: -1em;
    margin-left: -2.5em;
}
```

[▲ 返回目录](#目录)
