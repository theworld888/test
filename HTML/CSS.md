## **css**构成

```html
选择器
	{
	键：值；
	键：值；
}
```

## 选择器

- **标签选择器**

  > p {     }

- **类选择器**

  > .class {    }

  - **多类名**

    > \<div class="red fontsize">

- **id选择器**

  > #id {    }

- **通配符选择器(针对所有标签)**

  > \* {    }

- **后代选择器**

  > ol li {    }
  >
  > 可以是.class a或者#name a

- **子选择器**

  > div>p {}

- **并集选择器**

  > div,p {    } 
  >
  > 选择多种标签

- **伪类选择器**

  > | 属性      | 说明             |
  > | --------- | ---------------- |
  > | a:link    | 未访问           |
  > | a:visited | 已访问           |
  > | a:hover   | 鼠标放置         |
  > | a:active  | 鼠标按下(未弹起) |

- **focus伪类选择器**

  > 获取焦点的表单元素,主要用于input
  >
  > input：focus {     }

## Emmet语法

- div+Tab=\<div>\</div>

- div*3：生成多个标签

- ul>li：父子级标签

- div+p：同级标签

- .dome或者#two：取类名或名字

  > 默认div，可以p.dome或者p#two

- .demo$*5：生成类名为demo1到demo5

- div{xxx}：\<div>xxx\</div>

## 显示模式转换

| 属性                  | 说明           |
| --------------------- | -------------- |
| display:block;        | 转换块级元素   |
| display:inline;       | 转换行内元素   |
| display:inline-block; | 转换行内块元素 |

## 字体

| 属性        | 说明                          |
| ----------- | ----------------------------- |
| font-family | 字体                          |
| font-size   | 大小                          |
| font-weight | 粗细：normal，bold，100-900   |
| font-style  | 文字样式：normal，italic/斜体 |

> ### 复合属性
>
> ```html
> {
> font: font-style font-weight font-size/line-height font-family;
> font: italic 700 16px/5px yahei;
> }
> ```
>
> **除了size和family其他的可以省略**

## 文本

| 属性            | 说明                             |
| --------------- | -------------------------------- |
| color           | 颜色：red，#ff0000，rgb(200,0,0) |
| text-align      | 对齐                             |
| line-height     | 行间距=上间距+文字+下间距        |
| text-indent     | 文本首行缩进(px)                 |
| text-decoration | 装饰线                           |

> - underline 下划线
> - overline 上划线
> - line-through 删除线

## 背景

#### 颜色：

background-color：颜色；

#### 背景图片：

background-image：url(xxx);

#### 背景平铺：

background-repeat：repeat|no-repeat|repeat-x|repeat-y

#### 位置：

background-position：x y;

| 参数值   | 说明                             |
| -------- | -------------------------------- |
| length   | px                               |
| position | top\|center\|bottom\|left\|right |

#### 固定：

background-attachment：scroll | fixed

| 参数   | 作用       |
| ------ | ---------- |
| scroll | 随对象滚动 |
| fixed  | 图像固定   |

#### 背景复合写法:

 background：red url(xxx) repeat-x fixed top;

#### 背景透明：

> background：rgba(0,0,0,0.3);
>
> a表示透明度，范围是0-1

## 优先级

1. 继承和*
2. 元素选择器
3. 类选择器
4. ID选择器
5. 行内样式style
6. ！important

## 盒子模型

<img src="image\1.png"/>   

### border

border：border-width|border-style|border-color

| 属性         | 作用 |
| ------------ | ---- |
| border-width | 粗细 |
| border-style | 样式 |
| border-color | 颜色 |

![Snipaste_2021-01-25_14-44-47](image\2.png) 

> **复合写法没有顺序要求**
>
> **还可以border-top选择不同边**

#### 表格的边框

> **合并相邻单元格的边框border-collapse：collapse;**

### padding

| 值                           | 意思               |
| ---------------------------- | ------------------ |
| padding：5px;                | 上下左右5          |
| padding：5px 10px;           | 上下5 左右10       |
| padding：5px 10px 20px;      | 上5 左右10 下20    |
| padding：5px 10px 20px 30px; | 上5 右10 下20 左30 |

### margin

#### 盒子居中

| 居中对象             | 方式                      |
| -------------------- | ------------------------- |
| 块级盒子             | margin：0 auto;           |
| 行内元素和行内块元素 | 为其父元素添加text-center |

## 嵌套块元素塌陷（p154）

- 为父元素定义上边框
- 为父元素定义上内边距
- 为父元素添加overflow：hidden

## 圆角边框

> border-radius：数值px |百分比%；
>
> 可以分别设置每个角

## 盒子阴影

> box-shadow:h-shadow v-shadow blur spread color insert;

| 属性     | 描述                           |
| -------- | ------------------------------ |
| h-shadow | 必须\|水平阴影位置（允许负值） |
| v-shadow | 必须\|垂直阴影位置（允许负值） |
| blur     | 模糊强度                       |
| spread   | 阴影尺寸                       |
| color    | 阴影颜色                       |
| insert   | 将外部阴影改为内部阴影         |

## 文字阴影

> text-shadow：h-shadow v-shadow blur color;
| 属性     | 描述                           |
| -------- | ------------------------------ |
| h-shadow | 必须\|水平阴影位置（允许负值） |
| v-shadow | 必须\|垂直阴影位置（允许负值） |
| blur     | 模糊强度                       |
| color    | 阴影颜色                       |

## 浮动

> float：xxx;

| 属性值 | 描述   |
| ------ | ------ |
| none   | 无     |
| left   | 左浮动 |
| right  | 右浮动 |

## 清除浮动（183-188）

## 定位

### 四种定位

| 值       | 语义     |
| -------- | -------- |
| static   | 静态定位 |
| relative | 相对定位 |
| absolute | 绝对定位 |
| fixed    | 固定定位 |
| sticky   | 粘性定位 |

> #### 相对定位
>
> 相对于自身移动
>
> 保留原位置

> #### 绝对定位
>
> 相对于父级元素移动，但如果父元素没有定位，则以浏览器为准
>
> 不保留原位置

> 粘性定位
>
> {position：sticky；top：10px}
>
> 当距离top有10px时，将相对定位变为固定定位

### 叠放次序

> {z-index：1；}
>
> 取值：负数 ，正数，0
>
> (只针对定位盒子)

### 扩展

- 使用绝对定位的盒子不可以使用margin：0 auto来水平居中

  > 居中
  >
  > 1. left:50%
  > 2. margin-left:-100px

- **行内元素设置绝对定位和固定定位后，可直接设置高度宽度**

- **块级元素添加绝对或者固定定位后，默认为内容大小**

- **层级显示**

  > | 元素类型             | 盒子     | 内容           |
  > | -------------------- | -------- | :------------- |
  > | 浮动元素             | 只压盒子 | 文字不会被压住 |
  > | 绝对定位（固定定位） | 压住     | 压住           |

## 隐藏元素

| 属性                                    | 描述             |
| --------------------------------------- | ---------------- |
| display：none；                         | 隐藏（不占位置） |
| visibility：visible可见\|hidden隐藏     | 隐藏（占位置）   |
| overflow：visible\|hidden\|scroll\|auto |                  |

> - visible：溢出显示
> - hidden：隐藏溢出
> - scroll：总显示滚动条
> - auto：超出是显示滚动条

# css高阶

## 精灵图

- 移动背景可以用background-position
- 往右下正值，往左上负值

## 字体图标

- http://icomoon.io
- http://www.iconfont.cn/

## CSS三角

```html
div{
	width:0;
	height:0;

	line-height:0;
	font-size:0;
	/*照顾低版本浏览器*/

	border:10px solid transparent;
	border-top:10px solid pink;
	/*画一个三角形*/
}
```

<img src="image\3.png"/>   → <img src="image\4.png"/>

## 用户界面样式

#### 鼠标样式

| 样式        | 描述 |
| ----------- | ---- |
| default     | 默认 |
| pointer     | 小手 |
| move        | 移动 |
| text        | 文本 |
| not-allowed | 禁止 |

> li {cursor:xxx}

#### 表单轮廓线

> {outline：0;}或{outline：none;}

#### 防止拖拽文本域

> {resize:none;。。}

#### 文字居中对齐

| 值       | 描述           |
| -------- | -------------- |
| baseline | 默认，基线对齐 |
| top      | ·顶端对齐      |
| middle   | 中线对齐       |
| bottom   | 底端对齐       |

> 只针对行内元素或行内块元素
>
> {vertical-align：xxx}

<img src="image\5.png"/>

#### 去除图片底部空白

> 1. 因为默认是基线对齐，所以改为top|middle|bottom即可
> 2. 转换为块级元素（对齐方式只对行内元素起作用）

#### 溢出文字省略号显示

- **单行文本**
  1. white-space：nowrap;强制一行显示文字
  2. overflow:hidden;隐藏超出部分
  3. text-overflow:ellipsis;省略号代替超出部分

- **多行文本**

  兼容问题，用的不多

## 布局技巧

#### margin负值的运用

- 边框合并{margin-left:-1px;},向左移动1像素
- 边框合并后，后一个会压住前一个，
  1. 若无定位，在hover添加相对定位，提高层级
  2. 若有定位，直接提高层级z-index

#### 文字环绕

float原本是为文字环绕服务，为图片设置浮动可以将文字挤开

#### 进阶三角形

<img src="image\6.png"/> 

上边框加倍，可以将左右边框拉长，设置transparent，得到独立三角形

#### CSS初始化

# HTML5和CSS3提高

## HTML5新特性

#### 语义化标签

- \<header\>：头部标签
- \<nav\>：导航标签
- \<article\>：内容标签
- \<senction\>：定义某个文档区域
- \<aside\>：侧边栏标签
- \<footer\>：尾部标签

#### 视频标签

> \<video src="文件地址" controls="controls">\</video>

| 属性     | 描述                                        |
| -------- | ------------------------------------------- |
| autoplay | 自动播放（谷歌浏览器需要添加muted实现自动） |
| controls | 显示播放控件                                |
| width    | 宽度                                        |
| height   | 高度                                        |
| loop     | 循环播放                                    |
| preload  | 是否预加载                                  |
| src      | 视频地址                                    |
| poster   | 加载等待画面                                |
| muted    | 静音播放                                    |

#### 音频标签

> \<audio src="文件地址" controls="controls">\</audio>

| 属性     | 描述         |
| -------- | ------------ |
| autoplay | 自动播放     |
| controls | 显示播放控件 |
| loop     | 循环播放     |
| src      | 音频地址     |

#### input标签

| 属性   | 说明     |
| ------ | -------- |
| number | 数字     |
| tel    | 手机号码 |
| search | 搜索框   |

- 还有Email|URL|日期|时间|颜色等

#### 表单属性

| 属性         | 值        | 说明               |
| ------------ | --------- | ------------------ |
| required     | required  | 该位置必须填写     |
| autofocus    | autofocus | 自动聚焦此处       |
| autocomplete | off/on    | 记录之前提交的值   |
| multiple     | multiple  | 使文件可以多选提交 |
| placeholder  |           | 提示文本           |

> 更改提示文本字体颜色
>
> input：：placeholder {
>
> ​     color：pink }

#### 属性选择器

| 选择符        | 简介                     |
| ------------- | ------------------------ |
| E[att]        | 有E元素有att属性         |
| E[att="val"]  | 选择具有att属性的值为val |
| E[att^="val"] | 以val开头的              |
| E[att$="val"] | 以val结尾的              |
| E[att*="val"] | 含有val的                |

#### 结构伪类选择器

| 选择符          | 简介             |
| --------------- | ---------------- |
| E：first-child  | 选择第一个子元素 |
| E：last-child   | 最后一个子元素   |
| E：nth-child(n) | 第N个子元素      |

E：nth-child(n)

> - n可以是数字
>
> - 关键字：even偶数，odd奇数
>
> - 公式
>
>   | 公式 | 取值      |
>   | ---- | --------- |
>   | 2n   | 偶数      |
>   | 2n+1 | 奇数      |
>   | 5n   | 5，10，15 |
>   | n+5  | 从5开始   |
>   | -n+5 | 前五个    |

| 选择符            | 简介             |
| ----------------- | ---------------- |
| E：Frist-of-type  | 指定类型的第一个 |
| E：last-of-type   | 最后一个         |
| E：nth-of-type(n) | 第n个            |

> **区别**：先选择第n个，再检查是否匹配，不匹配不生效
>
> ​			先匹配，在其中选择第n个

#### 伪元素选择器

| 选择符  | 简介               |
| ------- | ------------------ |
| ::befer | 在元素内部前面插入 |
| ::after | 在元素内部后面插入 |

- 必须加content,意思是该标签的内容
- 为行内元素，不可设置高度

#### CSS3盒子模型

| 代码                   | 说明                 |
| ---------------------- | -------------------- |
| box-sizing:content-box | width+padding+border |
| box-sizing:border-box  | width                |

#### 图片模糊

> filter：blur(数值px);	数值越大越模糊

#### 宽度函数

> width：calc(100%-30px);		

#### css过度

配合：hover使用

transition:变化的属性(width hight all)	花费时间	运动曲线	何时开始

<img src="image\7.png"/> 

#### favicon图标

- 将图片转化为ioc图片，http://www.bitbug.net/

#### 2D转换

- **translate	不会影响其他元素，对行内元素是无效的**

1. transform:translate(x,y);
2. transform:translateX(n);
3. transform:translateY(50%);		移动值为自生的一半

- rotate

1. transform:rotate(度数45deg);
2. transform-origin：
   - left|right|top|bottom	两两组合
   - px|%                                  默认是50% 50%