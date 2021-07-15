## 标题	\<h1>-\<h6>

```html
<h1>我是一级标题</h2>
<h6>我是六级标题</h6>
```

##  段落	\<p>

```html
<p>将这段话分为一段话</p>
```

## 换行	\<br/>

```html
在此处强制换行<br/>
```

## 文本

| 标签          | 说明   |
| ------------- | :----- |
| <strong>和<b> | 加粗   |
| <em>和<i>     | 倾斜   |
| <del>和<s>    | 删除线 |
| <ins>和<u>    | 下划线 |

```html
<strong>加粗</strong>
<b>加粗</b>
```

## 盒子

```html
<div>独占一行</div>
<span>一行可以放多个</span>
```

## 图片

| 属性   | 说明               |
| ------ | ------------------ |
| src    | 图片路径           |
| alt    | 无图片时显示的文本 |
| title  | 鼠标放置显示文字   |
| width  | 宽度               |
| height | 高度               |
| border | 边框               |

```html
<img src="图片url"/>
```

## 超链接 \<a>

| 属性   | 说明                                                 |
| ------ | ---------------------------------------------------- |
| herf   | 跳转目标                                             |
| target | 窗口弹出方式：_self 当前窗口打开   _blank 新窗口打开 |


```html
<a herf="跳转目标">文本或者图片</a>
<a herf="#">空链接</a>
```

### 锚点链接

```html
<a herf="#id">文字</a>
<h1 id="id"></h1>
```

## 注释

```
<!--我是注释-->
```

## 特殊字符

| 字符 | 代码    |
| ---- | ------- |
| 空格 | \&nbsp; |
| 小于 | \&lt;   |
| 大于 | \&gt;   |

------

## 表格

| 属性名      | 描述                        |
| ----------- | --------------------------- |
| align       | 对齐方式：left,center,right |
| border      | 边框粗细                    |
| cellpadding | 与内容之间的空白            |
| cellspacing | 单元格之间的空白            |
| width       | 表格宽度                    |

```html
<table>
    <tr>
        <thead>
            <th>表头</th>
        </thead>
        <tbody>
            <td>普通表格</td>
        </tbody>
    </tr>
</table>
```

### 合并单元格

```html
<table>
    <tr>
        <td colspan="2">向右合并2</td>
        <td rowspan="3">向下合并3</td>
        <td></td>
    </tr>
        <tr>
        <td></td>
        <td></td>
        <td></td>
    </tr>
</table>
```

## 列表

```html
<ul>
    <li>无序列表</li>
</ul>

<ol>
    <li>有序列表</li>
</ol>

<dl>
    <dt>自定义列表表头</dt>
    <dd></dd>
</dl>
```

## 表单

| 属性   | 作用               |
| ------ | ------------------ |
| action | 接收数据的url地址  |
| method | 提交方式：get,post |
| name   | 表单名称           |

```html
<form action="url" method="" name="">
    表单的各种控件
</form>
```

表单控件

1. input输入表单元素
2. select下拉表单元素
3. textarea文本域元素

### \<input>表单元素

```html
<form>
    <input type="" name="" value="" checked="checked" maxlength="">
</form>
```

| input属性 | 说明                   |
| --------- | ---------------------- |
| type      | 要添加的控件           |
| name      | 名字                   |
| value     | 控件的值 或者 提示文字 |
| checked   | 默认选中状态           |
| maxlength | 最大文本字数           |

| type属性 | 说明         |
| -------- | ------------ |
| button   | 按钮         |
| submit   | 提交按钮     |
| text     | 文本框       |
| password | 密码         |
| reset    | 重置按钮     |
| file     | 选择文件按钮 |

| typr属性：选择按钮 |          |
| :----------------- | -------- |
| radio              | 单选按钮 |
| checkbox           | 复选按钮 |

- ##### 单选按钮添加name,可以实现多选一

- ##### 单选按钮和复选按钮可以设置checked属性

```html
<input type="checkbox" checked="checked">
```

### \<lable>标签

- **点击关联内容实现选择**

```html
<lable for="id">关联的内容</lable>
<input type="text" id="xxx">
```

### \<select>下拉表单

```html
<select>
    <option>选项一</option>
    <option>选项二</option>
    <option>选项三</option>
</select>
```

### \<textarea>文本域

```html
<textarea rows="每行字数" cols="行数"></textarea>
```

