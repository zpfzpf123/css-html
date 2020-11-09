# html

## 1 换行标签的区别

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Document</title>
</head>
<body>
  <p>sdasdsa<br />dfdfff</p>
  <p>ggggggggggggg</p>
</body>
</html>
```

![image-20201104140046435](D:\images\image-20201104140046435.png)

p标签之间会有16px的margin br标签没有

## 2 链接分类

![image-20201104143531057](D:\images\image-20201104143531057.png)

## 3 特殊字符

![image-20201104144030293](D:\images\image-20201104144030293.png)

## 4 表格标签示范

```html
<!DOCTYPE html>
<html lang="en">

<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Document</title>
</head>
<style>
</style>

<body>
  <table border="1" cellspacing="0" cellpadding="20px" align="center">
    <thead>
      <tr>
        <th>name</th>
        <th>age</th>
        <th>height</th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <td>zpf</td>
        <td rowspan="2">21</td>
        <td>1.88</td>
      </tr>
      <tr>
        <td>zzz</td>
        <td rowspan="2">1.85</td>
      </tr>
      <tr>
        <td>xx</td>
        <td>18</td>
      </tr>
    </tbody>
  </table>
</body>

</html>
```

![image-20201104151711248](D:\images\image-20201104151711248.png)

## 5 自定义列表

```html
<!DOCTYPE html>
<html lang="en">

<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Document</title>
</head>
<style>
  dl>dd{
    margin-left: 0;
  }
</style>
<body>
<dl>
  <dt>河神</dt>
  <dd>第一集</dd>
  <dd>第二集</dd>
  <dd>第三集</dd>
</dl>
</body>

</html>
```

![image-20201104153155447](D:\images\image-20201104153155447.png)

## 6 表单标签

### 1 表单域

![image-20201104153854868](D:\images\image-20201104153854868.png)

### 2 表单元素input

![image-20201104162801525](D:\images\image-20201104162801525.png)

![image-20201104162817735](D:\images\image-20201104162817735.png)

### 3 label标签

用于绑定一个表单元素

```html
<!DOCTYPE html>
<html lang="en">

<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Document</title>
</head>
<style>

</style>
<body>
  <form action="">
    <label for="tel">电话号码</label>
    <input type="number" name="" id="tel">
  </form>
</body>

</html>
```

input添加id label for属性添加input id标签，当我们点击label时，也就相当于点击了input

### 4 select标签

```html
<!DOCTYPE html>
<html lang="en">

<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Document</title>
</head>
<style>

</style>
<body>
  <form action="">
    籍贯:<select name="" id="">
      <option value="">四川</option>
      <option value="">山东</option>
      <option value="" selected>广东</option>
    </select>
  </form>
</body>

</html>
```

selected:默认选中

### 5 textarea标签

```html
<!DOCTYPE html>
<html lang="en">

<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Document</title>
</head>
<style>

</style>
<body>
  <form action="">
    <textarea name="" id="" cols="30" rows="10"></textarea>
  </form>
</body>

</html>
```

input:text 只能显示一行，textarea爱可以显示多行且可以自定义行数和列数



# css

## 7 text

### 1 text-indent

我们一般使用  text-indent: 2em; 是这样用的，1em代表一个文字的像素大小

### 2 line-height

![image-20201105165803704](D:\images\image-20201105165803704.png)

## 8 css选择器

### 1 子类选择器

```html
<!DOCTYPE html>
<html lang="en">

<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Document</title>
</head>
<style>
  ul>li>a {
    color: red; //亲儿子选择器 只会选择ul里的li里的a元素
  }

  ul>a {
    font-size: 30px;
  }

  ul a {
    font-weight: 700; //后代选择器 只有是ul里面的a元素都会被选择
  }
</style>

<body>
  <ul>
    <a href="#">yes</a>
    <li>
      <a href="#">hello</a>
    </li>
  </ul>
</body>
<script>

</script>

</html>
```

### 2 伪类选择器

#### 1 a标签链接

![image-20201105175743140](D:\images\image-20201105175743140.png)

书写顺序遵守爱恨原则(love/hate)link visited hover active

#### 2 表单聚焦

```html
<!DOCTYPE html>
<html lang="en">

<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Document</title>
</head>
<style>
  input:focus {
    background-color: #e6e6e6;
  }
</style>

<body>
  <input type="text" name="" id="">
  <input type="text" name="" id="">
  <input type="text" name="" id="">
</body>
<script>

</script>

</html>
```

![image-20201105181653027](D:\images\image-20201105181653027.png)

## 9 css背景

#### 背景附着

background-attachment:scroll(默认滚动)/fixed(区域滚动时图片位置不变)

## 10 css三大特性

层叠性：后一个属性会把前一个相同的属性覆盖掉

继承性：有些css属性父元素可以传承给子元素(如文字相关的属性和颜色等)

优先级:!important 8>id 4>class 伪类(:hover :link :onfocus)  属性(input[value] input:[value='ss'])  结构(nth-child()  nth-of-type()) **2**>元素选择器(div p span)  伪元素选择器(::before ::after) **1**>继承 通配符* 0

谁的权重大谁就执行谁，权重可以叠加

## 11 border

border-collapse:collapse =>表示把相邻的border边框合并起来

## 12 padding

**注意一下，盒子本身如果没有指定width/height属性，则padding不会撑开盒子大小**

## 13 水平居中

**块级元素**

1.设置块级元素width，然后margin:0 auto即可水平居中

2 加了绝对定位的元素不能用margin:0 auto 实现水平居中，我们可以使用如下方法进行水平垂直居中

```html
<!DOCTYPE html>
<html lang="en">

<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Document</title>
</head>
<style>
  * {
    margin: 0;
    padding: 0;
  }

  .c {
    position: absolute;
    left: 50%;
    top: 50%;
    width: 300px;
    height: 300px;
    background-color: gray;
    margin-left: -150px;// width/2
    margin-top: -150px;// height/2
  }
</style>

<body>
  <div class="a"></div>
  <div class="c"></div>

</body>
<script>

</script>

</html>
```

先left:50%和top:50%用来定位，然后我们会发现刚好多了宽度和高度的一半，所以只需要使用margin边距来控制盒子最后的位置，注意这里不能用margin-right和margin-buttom，因为浏览器是从左到右和从上到下进行渲染的，如果子元素的宽度还没有超过父元素的宽度，设置了也是无效的

**行内元素**

1.设置行内元素的父元素text-aligin:center

## 14 margin

### 1.盒子塌陷问题

嵌套块元素中如果父元素和子元素都有上外边距，这个时候师父元素会塌陷较大的边距值

解决办法：

1.给父元素盒子添加边框，如border:1px solid transport

2.给父元素添加内边距，如padding:1px

3.给父元素添加属性overflow:hidden

### 2.行内元素margin问题

行内元素我们只设置左右margin，上下margin是不起效果的

## 15 盒子box属性

box-shadow

![image-20201106132038987](D:\images\image-20201106132038987.png)

outset为默认属性 不用写 写了反而报错

盒子阴影不占用空间

16 文字阴影 

![image-20201106132651281](D:\images\image-20201106132651281.png)

## 16 浮动float

### **浮动可以改变标签的默认排列方式**

我们对于块级元素的纵向排列旺旺采用普通流，对于块级元素的横向排列我们就可以采用标准流或者flex布局

float属性用于创建浮动框，将其移到一边，知道左边缘或者右边缘触碰到包含块或者另一个浮动框的边缘

### 浮动特性

**1 脱离标准流**

浮动不在保留原先的位置，而是浮起来了

**2 上沿对齐**

多个浮动会按照属性值一行内显示并且顶端对齐排列

**3 行内块元素**

浮动元素具有行内块元素特点

块级元素如果没有设置宽度，默认和父级元素宽度大小一样，如果设置浮动了，width就是根据块级元素的内容来决定的

### 网页布局

先用标准流的父元素排列上下布局，再用浮动流排列子元素的左右布局

如下

```html
<!DOCTYPE html>
<html lang="en">

<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Document</title>
</head>
<style>
  * {
    margin: 0;
    padding: 0;
  }

  .box {
    width: 800px;
    height: 500px;
    margin: 100px auto;
    background-color: #e6e6e6;
  }

  .left {
    float: left;
    width: 300px;
    height: 300px;
    background-color: red;
  }

  .center {
    float: right;
    width: 400px;
    height: 400px;
    background-color: blue;
  }
</style>

<body>
  <div class="box">
    <div class="left"></div>
    <div class="center"></div>
    <div></div>
  </div>
</body>
<script>

</script>

</html>
```

![image-20201106145651008](D:\images\image-20201106145651008.png)

### 清除浮动

如果我们不给父元素高度，让子元素决定父元素有多高，标准流是没有问题的，子元素可以把父元素撑开，但是如果给子元素人添加浮动，脱离标准流之后，父元素高度就不会被撑开，这个时候为0，如果我们想在后面正常显示其它的元素，我们就需要清除浮动

#### 1.额外标签法

给最后一个浮动元素的后面添加一个块级元素(如div)并且添加style为clear:both方法就可以清除浮动对后面元素造成的影响

```html
<!DOCTYPE html>
<html lang="en">

<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Document</title>
</head>
<style>
  * {
    margin: 0;
    padding: 0;
  }

  .flexs {
    width: 800px;
    height: 300px;
    background-color: gainsboro;
  }

  div>div {
    width: 110px;
    height: 133px;
    float: left;
  }

  .left {
    background-color: blue;
  }

  .right {
    background-color: yellowgreen;
  }

  .a {
    background-color: red;
    height: 900px;
  }

  .flexs .last {
    width: 300px;
    height: 200px;
    background-color: black;
  }

  .flexs .clear {
    clear: both;
  }
</style>

<body>
  <div class="flexs">
    <div class="left"></div>
    <div class="right"></div>
    <div class="last"></div>
    <div class="clear"></div>
  </div>
  <div class="a">

  </div>

</body>
<script>

</script>

</html>
```

#### 2 父级元素添加属性

我们给需要清除浮动的子元素的父级元素添加样式 

```html
overflow:hidden
```

缺点：无法显示溢出的部分

#### 3 伪元素法

给父元素添加样式如下

```css
  .clearfix:after {
    content: "";
    height: 0;
    display: block;
    clear: both;
    visibility: hidden;
  }

  .clearfix {
    /* 兼容ie6 ie7 */
    *zoom: 1;
  }
```

#### 4 双伪元素法

给父元素添加如下样式

```css
 .clearfix:before,
  .clearfix::after {
    display: table;
    content: "";
  }

  .clearfix::after {
    clear: both;
  }

  .clearfix {
    *zoom: 1;
  }
```

## 17 定位position

**当我们想把盒子自由的在某个盒子中移动位置或者固定在某个位置，我们需要用到定位**

###  static

**标准定位 ，是默认定位，按照盒子标准流的位置展示，没有边偏移**

### relative

**元素在移动位置的时候，是相对原来的位置进行移动 ，而且相对定位的盒子会继续占有之前的标准流(不脱标)的位置，后面的盒子不受影响**

### absoulate

元素在移动位置时，是相对它的祖先元素来移动位置的

1.**如果没有祖先元素或者祖先元素没有定位，则以浏览器为准定位**

2 **如果祖先元素有定位(绝对，相对，固定，这里建议用相对，也就是子绝父相),子元素就会相对最近一级有定位的祖先元素移动位置**

3 **绝对定位不在占有原先的位置(脱标)**

### fixed

**元素固定在浏览器可视化位置**

1 **以浏览器的可视窗口来移动元素**

2 **和父元素没有任何关系，不随滚动条滚动**

3 **固定定位不占有原来的位置，也就是会脱标**

#### 技巧

如果我们想把盒子位置固定在某一个盒子的右测，我们可以这样做

1 设置该盒子

```css
position:fixd;
left:50%;
```

这样可以把位置固定在中心，然后在扩大这个盒子的左边距即可，左边距大小为另外一个盒子width/2

```css
width:width/2;
```

### sticky

粘性定位，通常被认为是相对定位和固定定位的结合

1 以浏览器的可视窗口为参照(固定定位特点)

2 会占有原先的位置(相对定位的特点)

3 必须添加top buttom left right 其中一个才起效果

```css
position:sticky;
top:10px;//当距离顶部还有10px时变为固定定位
```

### 定位特性

1 **行内元素添加绝对或固定定位，就可以设置宽度和高度**

2 **块级元素添加绝对或固定定位，如果不给宽度或者高度，其宽度和高度就由内容决定**

3 **上面两点可以得知，只要元素设置了绝对或固定定位，我们可以把元素看作行内块元素对待**

4 **脱标的盒子不会触发外边距塌陷**

5 **绝对定位和固定定位会完全压住盒子，也就是说浮动元素不能完全压住盒子，它会把盒子的文字和图片露出来，但是定位不会露出来，如下**



### z-index

**z-index的值越大，显示越靠上，只有定位元素才能设置z-index**

## 18 元素的显示和隐藏

![image-20201107151637291](D:\images\image-20201107151637291.png)

overflow:溢出的部分显示属性

## 19 精灵图的使用

![image-20201107155235609](D:\images\image-20201107155235609.png)

## 20 iconfont字体图标

![image-20201107160659500](D:\images\image-20201107160659500.png)

下载推荐**阿里 iconfont字库**或者**icommon字库**

**icommon**

下载完图标后解压，把font文件夹放到要使用的文件的根目录下

在css样式全局声明字体，解压后的style.css代码复制一份到页面style中

最后要使用时，打开解压后的html，找到要使用的体表，ctrl+c图标后的小图标，黏贴到html中，再修改样式font-family即可

## 21 css三角

如图所示

```html
<!DOCTYPE html>
<html lang="en">

<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Document</title>
</head>
<style>
  * {
    margin: 0;
    padding: 0;
  }

  .box {
    width: 0;
    height: 0;
    border-top: 100px solid black;
    border-right: 100px solid green;
    border-bottom: 100px solid yellow;
    border-left: 100px solid red;
  }
</style>

<body>
  <div class="box">

  </div>
</body>
<script>

</script>

</html>
```

![image-20201107165512689](D:\images\image-20201107165512689.png)

```html
<!DOCTYPE html>
<html lang="en">

<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Document</title>
</head>
<style>
  * {
    margin: 0;
    padding: 0;
  }

  .box {
    top: 200px;
    position: relative;
    width: 200px;
    height: 200px;
    background-color: pink;
  }

  .box span {
    position: absolute;
    left: 80px;
    top: -20px;
    width: 0;
    height: 0;
    border: 10px solid transparent;
    border-bottom-color: pink;
  }
</style>

<body>
  <div class="box">
    <span></span>
  </div>
</body>
<script>

</script>

</html>
```

![image-20201107170252675](D:\images\image-20201107170252675.png)



**添加中间三角**

```html
<!DOCTYPE html>
<html lang="en">

<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Document</title>
</head>
<style>
  * {
    margin: 0;
    padding: 0;
  }

  .box {
    position: relative;
    width: 100px;
    height: 40px;
    background-color: gray;
    margin: 100px auto;
    line-height: 40px;
    text-align: center;
  }

  .ms {
    width: 50px;
    height: 40px;
    background-color: red;
    float: left;
  }

  i {
    width: 0;
    height: 0;
    position: absolute;
    left: 40px;
    border-color: transparent gray transparent transparent;
    border-width: 40px 10px 0px 0px;
    border-style: solid;
  }
</style>

<body>
  <div class="box">
    <span class="ms">5000</span>
    <i></i>
    <span class="yb">4000</span>
  </div>
</body>

</html>
```

![image-20201107185728336](D:\images\image-20201107185728336.png)





##22 表单操作

### 1 去除表单轮廓线

```html
  <input type="text" name="" id="" style="outline: 0;">
```

### 2 去除文本域拖拽大小

## 23 vertical-align的使用

![image-20201107171411262](D:\images\image-20201107171411262.png)

语法： 

**vertical-align :** **baseline**  |**sub** | **super** |**top** |**text-top** |**middle**  |**bottom** |**text-bottom** |*length* 

**适用于行内元素和行内块元素**

参数： 

**baseline :** 　将支持valign特性的对象的内容与基线对齐  
**sub :** 　垂直对齐文本的下标 
**super :** 　垂直对齐文本的上标 
**top :**  将支持valign特性的对象的内容与对象顶端对齐 
**text-top :** 　将支持valign特性的对象的文本与对象顶端对齐  
**middle :** 　将支持valign特性的对象的内容与对象中部对齐 
**bottom :**  将支持valign特性的对象的文本与对象底端对齐 
**text-bottom :** 　将支持valign特性的对象的文本与对象顶端对齐  
*length :* 　CSS2　由浮点数字和单位标识符组成的长度值 |  或者百分数。可为负数。定义由基线算起的偏移量。基线对于数值来说为0，对于百分数来说就是0%。目前IE5尚不支持。

## 24 图片底部默认空白缝隙问题

![image-20201107173021446](D:\images\image-20201107173021446.png)

## 25 文字显示省略号

```html
<!DOCTYPE html>
<html lang="en">

<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Document</title>
</head>
<style>
  div {
    width: 100px;
    height: 65px;
    background-color: gray;
    /* 单行显示省略号 */
    /*     white-space: nowrap;
    overflow: hidden;
    text-overflow: ellipsis; */
    /* 多行显示省略号 */
    overflow: hidden;
    text-overflow: ellipsis;
    display: -webkit-box;
    -webkit-line-clamp: 3;
    -webkit-box-orient: vertical;
  }
</style>

<body>
  <div>
    衣带渐宽终不悔，为伊消得人憔悴
    衣sdfasfsaf
  </div>
</body>

</html>
```

![image-20201107174318668](D:\images\image-20201107174318668.png)

## 26 伪元素选择器

![image-20201107195959486](D:\images\image-20201107195959486.png)

## 27 盒子模型(box-sizing)

**box-sizing:content-box(默认，盒子宽度为width+border+padding)/border-box(盒子宽度为width，前提是padding和border不会超过width)**

## 28 过渡(transition)

![image-20201108224044963](D:\images\image-20201108224044963.png)



## 29 tranform(2d转换)

### translate(位置转换)

![image-20201109001230434](D:\images\image-20201109001230434.png)

### rotate(角度转换)

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<style>
    * {
        margin: 0;
        padding: 0;
    }

    .a {
        position: relative;
        width: 200px;
        height: 30px;
        border: 1px solid black;
        margin-left: 10px;
    }

    .a::after {
        position: absolute;
        top: 6px;
        right: 14px;
        content: '';
        width: 10px;
        height: 10px;
        border-right: 1px solid black;
        border-bottom: 1px solid black;
        transform: rotate(45deg);
        transition: all 0.45s;
    }

    .a:hover::after {
        transform: rotate(225deg);
        top: 10px;
    }
</style>

<body>
    <div class="a"></div>
</body>
<script>
</script>

</html>
```

可以修改转换的中心点

transform-origin:x y

x和y可以是百分比，也可以是方位名词，也可以是像素

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<style>
    * {
        margin: 0;
        padding: 0;
    }

    .a {
        width: 200px;
        height: 200px;
        border: 1px solid pink;
        margin: 100px auto;
        overflow: hidden;
    }

    .a::after {
        content: 'hello zpf';
        display: inline-block;
        background-color: yellowgreen;
        width: 200px;
        height: 200px;
        transform: rotate(180deg);
        transform-origin: left bottom;
        transition: all .5s;
        text-align: center;
        line-height: 200px;
    }

    .a:hover::after {
        transform: rotate(0deg);
    }
</style>

<body>
    <div class="a"></div>
</body>
<script>
</script>

</html>
```

### scale(缩放)

![image-20201109011733524](D:\images\image-20201109011733524.png)

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<style>
    * {
        margin: 0;
        padding: 0;
    }

    div {
        overflow: hidden;
        width: 100px;
        height: 100px;
        margin: 100px auto;
    }

    img {
        width: 100px;
        height: 100px;
        transition: all .5s;

    }

    img:hover {
        transform: scale(1.2);
    }
</style>

<body>
    <div>
        <img src="../supermall//src//assets//img//detail//cart.png" alt="">
    </div>
</body>
<script>
</script>

</html>
```

## 30 动画(animation)

- <' [animation-name](animation-name.htm) '>： 

  检索或设置对象所应用的动画名称 

- <' [animation-duration](animation-duration.htm)  '>： 

  检索或设置对象动画的持续时间 

- <' [animation-timing-function](animation-timing-function.htm) '>： 

  检索或设置对象动画的过渡类型 

- <' [animation-delay](animation-delay.htm) '>： 

  检索或设置对象动画延迟的时间 

- <' [animation-iteration-count](animation-iteration-count.htm) '>： 

  检索或设置对象动画的循环次数 

- <' [animation-direction](animation-direction.htm)  '>： 

  检索或设置对象动画在循环中是否反向运动 

- <' [animation-fill-mode](animation-fill-mode.htm)  '>： 

  检索或设置对象动画时间之外的状态 

- <' [animation-play-state](animation-play-state.htm)  '>： 

  检索或设置对象动画的状态。*w3c正考虑是否将该属性移除，因为动画的状态可以通过其它的方式实现，比如重设样式* 

**热点模式图**

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<style>
    * {
        margin: 0;
        padding: 0;
    }

    .a {
        position: relative;
        width: 8px;
        height: 8px;
        margin: 100px auto;
    }

    .dotted {
        width: 8px;
        height: 8px;
        background-color: greenyellow;
        border: 1px solid greenyellow;
        border-radius: 50%;
    }

    div[class^=shadow] {
        width: 8px;
        height: 8px;
        box-shadow: 0 0 12px greenyellow;
        position: absolute;
        top: 50%;
        left: 50%;
        transform: translate(-50%, -50%);
        border-radius: 50%;
        animation: move 1s linear infinite;
    }

    .shadow2 {
        animation-delay: 0.4s !important;
    }

    @keyframes move {
        70% {
            width: 40px;
            height: 40px;
        }

        100% {
            width: 70px;
            height: 70px;
            opacity: .2;
        }
    }
</style>

<body>
    <div class="a">
        <div class="dotted"></div>
        <div class="shadow1"></div>
        <div class="shadow2"></div>
    </div>
</body>
<script>
</script>

</html> 
```

## 31 3d效果

### translatez

tranlatez(一般用px)就是盒子z轴的位置，值越大，越像我们的眼睛靠近，所以投影到屏幕上的成像越大

前提：如果想让tranlatez其效果，我们可以给该盒子的父元素或者层级更高的元素添加透视(perspective),perspective就是模拟人眼到屏幕的距离，距离越大，自然投影到屏幕上的成像越小

### rotate

- [rotate3d()](#rotate3d)： 

  指定对象的3D旋转角度，其中前3个参数分别表示旋转的方向x,y,z，第4个参数表示旋转的角度，参数不允许省略 

- [rotatex()](#rotatex)： 

  指定对象在x轴上的旋转角度 

- [rotatey()](#rotatey)： 

  指定对象在y轴上的旋转角度 

- [rotatez()](#rotatey)： 

  指定对象在z轴上的旋转角度 

#### 左手准则

![image-20201109142939283](D:\images\image-20201109142939283.png)

### transform-style

![image-20201109144215089](D:\images\image-20201109144215089.png)

#### 两面翻转的盒子

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<style>
    * {
        margin: 0;
        padding: 0;
    }

    body {
        perspective: 800px;
    }

    .box {
        width: 200px;
        height: 200px;
        margin: 100px auto;
        transition: all 1s;
        position: relative;
        transform-style: preserve-3d;
    }

    div>div {
        position: absolute;
        left: 0;
        top: 0;
        width: 100%;
        height: 100%;
        background-color: orange;
        color: whitesmoke;
        text-align: center;
        font-size: 30px;
        line-height: 200px;
        border-radius: 50%;
    }

    .b {
        background-color: green;
        transform: rotateY(180deg);
    }

    .box:hover {
        transform: rotateY(180deg);
    }
</style>

<body>
    <div class="box">
        <div class="a">你好</div>
        <div class="b">周鹏飞</div>
    </div>
</body>
<script>
</script>

</html>
```

#### 从下到上的翻转

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<style>
    * {
        margin: 0;
        padding: 0;
    }

    ul,
    li {
        display: block;
        margin: 100px auto;
        position: relative;
        width: 60px;
        height: 20px;
        transition: all 1.5s;
        transform-style: preserve-3d;
    }

    li:hover {
        transform: rotateX(90deg);
    }

    div {
        position: absolute;
        left: 50%;
        top: 50%;
        width: 100%;
        height: 100%;
        text-align: center;
    }

    div:first-child {
        transform: translate3d(0, 0, 10px);
        background-color: pink;
        z-index: 1;
    }

    div:last-child {
        background-color: green;
        transform: translate(0, 10px) rotateX(-90deg);
    }
</style>

<body>
    <ul>
        <li>
            <div>你好</div>
            <div>周鹏飞</div>
        </li>
    </ul>
</body>
<script>
</script>

</html>
```

#### 旋转木马

```html
<!DOCTYPE html>
<html lang="en">

<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Document</title>
</head>
<style>
  .box {
    width: 150px;
    height: 150px;
    margin: 100px auto;
    position: relative;
    transform-style: preserve-3d;
    animation: move 10s linear infinite;
    background: url(./0.png) no-repeat;
    background-size: contain;
  }

  body {
    perspective: 600px;
  }

  .box div {
    width: 100%;
    height: 100%;
    background: url(./apic7990.jpg) no-repeat;
    background-position: right center;
    background-size: contain;
    position: absolute;
    right: 0;
    top: 0;
  }

  @keyframes move {
    0% {
      transform: rotateY(0deg);
    }

    100% {
      transform: rotateY(360deg);
    }
  }

  .box div:nth-child(1) {
    transform: rotateY(0deg) translateZ(300px);
  }

  .box div:nth-child(2) {
    transform: rotateY(60deg) translateZ(300px);
  }

  .box div:nth-child(3) {
    transform: rotateY(120deg) translateZ(300px);
  }

  .box div:nth-child(4) {
    transform: rotateY(180deg) translateZ(300px);
  }

  .box div:nth-child(5) {
    transform: rotateY(240deg) translateZ(300px);
  }

  .box div:nth-child(6) {
    transform: rotateY(300deg) translateZ(300px);
  }
</style>

<body>
  <div class="box">
    <div></div>
    <div></div>
    <div></div>
    <div></div>
    <div></div>
    <div></div>
  </div>
</body>

</html>
```

# css3 个人总结

![CSS3](D:\images\CSS3.png)