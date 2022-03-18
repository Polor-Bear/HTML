# HTML标签(上)
## 1. HTML语法规范
### 1.1 基本语法规范
#### Hyper Text Markup Language

1. HTML标签是由尖括号包围的关键词，例如`<html`
2. HTML标签通常是成对出现的，例如`<html>`和`</html>`，我们称为双标签。标签对中的第一个标签是开始标签，第二个标签是结束标签。
3. 单标签`<br />`(break)

### 标签关系

双标签关系分为包含和并列两种关系

==包含关系==
```html
<head>
    <title> </title>
</head>
```

==并列关系==
```html
<head> </head>
<body> </body>
```

## HTML基本结构标签

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>标题</title>
</head>
<body>
    内容
</body>
</html>
```

| 标签名            | 定义       | 说明                                                   |
| ----------------- | ---------- | ------------------------------------------------------ |
| `<html></html>`   | HTML标签   | 页面中最大的标签，我们称为根标签                       |
| `<head></head>`   | 文档的头部 | 注意在head标签中我们必须要设置的标签是title            |
| `<title></title>` | 文档的头部 | 让页面拥有一个属于自己的网页标题                       |
| `<body></body>`   | 文档的头部 | 元素包含文档的所有内容，页面内容基本都是放到body里面的 |

## 网页开发工具

1. `<!DOCTYPE>`文档类型声明，作用就是告诉浏览器使用哪种html版本来显示网页。
    - 这句话就是告诉浏览器当前页面采用的是html5版本来显示网页。
    - `<!DOCTYPE>`声明位于文档中的最前面的位置，处于`<html`标签之前。
    - `<!DOCTYPE>`不属于html，它就是一个文件类型声明标签。
2. lang=language(语言)
    - en ---------英文
    - zh-CN ----中文
3. charset字符集
    - 常用的charset有：GB2312、BIG5、GBK和UTF-8等，其中UTF-8也被称为万国码，基本包含了全世界所有国家需要用到的字符

## HTML常用标签
### 标题标签

```html
<h1>一级标题</h1>
<h2>二级标题</h2>
<h3>三级标题</h3>
<h4>四级标题</h4>
<h5>五级标题</h5>
<h6>六级标题</h6>
```

<h1>一级标题</h1>
<h2>二级标题</h2>
<h3>三级标题</h3>
<h4>四级标题</h4>
<h5>五级标题</h5>
<h6>六级标题</h6>

### 段落和换行标签(重要)
1. 段落标签`<p>~~~</p>`
   - 段落paragraph [ˈpærəɡræf] 的缩写，意为段落
2. 换行标签`<br />`(单标签)
   - break [breɪk] 的缩写，意为打断、换行

### 文本格式化标签
| 语义   | 标签                             | 说明                     |
| ------ | -------------------------------- | ------------------------ |
| 加粗   | `<strong></strong>`或者`<b></b>` | 更推荐使用`<strong>`标签 |
| 倾斜   | `<em></em>`或者`<i></i>`         | 更推荐使用`<em>`标签     |
| 删除线 | `<del></del>`或者`<s></s>`       | 更推荐使用`<del>`标签    |
| 下划线 | `<ins></ins>`或者`<u></u>`       | 更推荐使用`<ins>`标签    |

### div 和 span 标签
**特点**
1. `<div>`标签用来布局，但是一行只能放一个`<div>`。大盒子
2. `<span>`标签用来布局，一行上可以多个`<span>`。小盒子

### 图像标签和路径(重点)
#### 图像标签
```html <img src="图像URl" /> ```

**img**(单词image的缩写)，意为图像
**src**是`<img>`标签的==必须属性==，它用于==指定图像文件的路径和文件名==
___
**图像标签的其他属性：**
| 属性   | 属性值   | 说明                       |
| ------ | -------- | -------------------------- |
| src    | 图片路径 | 必须属性                   |
| alt    | 文本     | 替换文本(图像不能显示时)   |
| title  | 文本     | 替换文本(鼠标放到图像上时) |
| width  | 像素     | 设置图像的宽度             |
| height | 像素     | 设置图像的高度             |
| border | 像素     | 设置图像的边框粗细         |

#### 路径
**路径可以分为：**
1. 相对路径
2. 绝对路径
**相对路径：**
以==引用文件所有位置==为参考基础，而建立出的目录路径(**图片相对于HTML文件的位置**)

| 相对路径分类 | 符号  |
| ------------ | :---: |
| 同一级路径   |       |
| 下一级路径   |   /   |
| 上一级路径   |  ../  |
**绝对路径：**
是指目录下的绝对位置，直接到达目标位置，通常是从盘符开始的路径。
例如：`D:\web\img\logo.gif`或完整的网络地址`http://www.itcast.cn/images/logo.gif`

### 超链接标签(重点)
**1.链接的语法格式**
```html
<a href="跳转目标" target="目标窗口的弹出方式"> 文本或图像 </a>
```
单词anchor[ˈæŋkə(r)]的缩写，意为：锚
| 属性   | 作用                                                                                |
| ------ | ----------------------------------------------------------------------------------- |
| href   | 用于指定链接目标的url地址，(必须属性)当为标签应用href属性时，它就具有了超链接的功能 |
| target | 用于指定链接页面的打开方式，其中_self为默认值，_blank为在新窗口中打开方式           |
**2.链接分类：**
1. 外部链接：例如`<a href="http://www.baidu.com">百度</a>`
2. 内部链接：网站内部页面之间的相互链接，直接链接内部页面名称即可，例如：`<a href="index.html">首页</a>`
3. 空链接：如果当时没有确定链接目标，可以先使用空链接`<a href="#">首页</a>`
4. 下载链接：如果href里面地址是一个文件或者压缩包，会下载这个文件
5. 网页元素链接：在网页中的各种网页元素，如文本、图像、表格、音频、视频等都可以添加超链接
6. 锚点链接：我们点击链接，可以快速定位到页面中的某个位置
   - 在链接文本的href属性中，设置属性值为#名字的形式，如`<a href="#two">第二集</a>`
   - 找到目标位置标签，里面添加一个id属性刚才的名字，如`h3 id="two">第二集介绍</h3>`

## HTML中的注释和特殊字符
**注释**

HTML中的注释以`<!--`开头，以`-->`结束。

**特殊字符**
| 特殊字符 |  描述  | 字符的代码 |
| :------: | :----: | :--------: |
|  &nbsp;  | 空格符 |  `&nbsp;`  |
|   &lt;   | 空格符 |   `&lt;`   |
|   &gt;   | 空格符 |   `&gt;`   |
|  &amp;   | 空格符 |  `&amp;`   |
|  &yen;   | 空格符 |  `&yen;`   |
|  &copy;  | 空格符 |  `&copy;`  |
|  &reg;   | 空格符 |  `&reg;`   |
|  &deg;   | 空格符 |  `&deg;`   |
| &plusmn; | 空格符 | `&plusmn;` |
| &times;  | 空格符 | `&times;`  |
| &divide; | 空格符 | `&divide;` |
|  &sup2;  | 空格符 |  `&suo2;`  |
|  &sup3;  | 空格符 |  `&sup3;`  |
重点记住：**空格**、**大于号**、**小于号**这三个，其余的使用很少，如果需要回头查阅即可

# HTML标签(下)
## 表格标签
### 表格的基本语法

```html
<table>
    <thead>
        <tr>
            <th> </th>
            <th> </th>
            <th> </th> 
        </tr>
    </thead>
    <tbody>
        <tr>
            <td> </td>
            <td> </td>
            <td> </td> 
        </tr>
        <tr>
            <td> </td>
            <td> </td>
            <td> </td> 
        </tr>
        <tr>
            <td> </td>
            <td> </td>
            <td> </td> 
            ...
        </tr>
        ...
    </tbody>
</table>
```
1. `<table></table>`是用于定义表格的标签。
2. `<tr></tr>`标签用于定义表格中的行，必须嵌套在`<table></table>`标签中。(table row)
3. `<td></td>`用于定义表格中的单元格，必须嵌套在`<tr></tr>`标签中(table data cell)
4. `<th></th>`标签表示HTML表格中的表头部分(table header cell)
    - 表头单元格通常用于表格第一行，表头单元格内的文本内容会加粗居中显示

| 属性名      | 属性值              | 描述                                             |
| ----------- | ------------------- | ------------------------------------------------ |
| align       | left、center、right | 规定表格相对周围元素的对齐方式。                 |
| border      | 1或""               | 规定表格单元是否拥有边框，默认为""，表示没有边框 |
| cellpadding | 像素值              | 规定单元边沿与其内容之间的空白，默认1像素。      |
| cellspacing | 像素值              | 规定单元格之间的空白，默认2像素。                |
| width       | 像素值或百分比      | 规定表格的宽度                                   |
| height      | 像素值或百分比      | 规定表格的高度                                   |

### 表格结构标签
- 分别用：`<thead></thead>`标签表示表格的头部区域、`<tbody></tbody>`标签表示表格的主体区域这样可以更好的分清表格结构
---
1. `<thead></thead>`：用于定义表格的头部。`<thead>`内部必须拥有`<tr>`标签。一般是位于第一行。
2. `<tbody></tbody>`：用于定义表格的主体，主要用于放数据本体。
3. 以上标签都是放在`<table></table>`标签中。

### 合并单元格
**合并单元格方式：**
- 跨行合并：`rowspan="合并单元格的个数"`
- 跨列合并：`colspan="合并单元格的个数"`

**目标单元格：(写合并代码)**
- **跨行**：**最上侧**单元格为目标单元格，写合并代码
- **跨列**：**最左侧**单元格为目标单元格，写合并代码

**合并单元格步骤：**
1. 先确定是跨行还是跨列合并。
2. 找到目标单元格。写上合并方式=合并的单元格数量。比如：`<td colspan="2"></td>`
3. 删除多余的单元格。

## 列表标签
表格是用来显示数据的，那么**列表就是用来布局的。**
列表最大的特点就是**整齐、整洁、有序**，它作为布局会更加自由和方便。

### 无序列表(重点)
`<ul>`(unordered list)标签表示HTML中的无序列表，一般会以项目符号呈现列表项，而列表项使用`<li>`(list item)标签定义。

```html
<ul>
    <li>列表1</li>
    <li>列表2</li>
    <li>列表3</li>
    ...
</ul>
```

1. 无序列表的各个列表项之间没有顺序级别之分，是并列的。
2. `<ul></ul>`中只能嵌套`<li></li>`，直接在`<ul></ul>`标签中输入其他标签或者文字的做法是不被允许的。
3. `<li>`与``</li>``之间相当于一个容器，可以容纳所有元素。
4. 无序列表会带有自己的样式属性，但在实际使用时，我们会使用CSS来设置

### 有序列表(理解)
`<ol>`(ordered list)标签表示HTML中的有序列表，列表排序以数字来显示，同样使用`<li>`(list item)标签来定义列表项。

```html
<ol>
    <li>列表1</li>
    <li>列表2</li>
    <li>列表3</li>
    ...
</ol>
```

1. `<ol></ol>`中只能嵌套`<li></li>`，直接在`<ol></ol>`标签中输入其他标签或者文字的做法是不被允许的。
2. `<li>`与``</li>``之间相当于一个容器，可以容纳所有元素。
3. 有序列表会带有自己的样式属性，但在实际使用时，我们会使用CSS来设置

### 自定义列表(重点)
自定义列表常用于对**术语**或**名词**进行解释和描述，自定义列表的列表项前没有任何项目符号。

`<dl>`(definition list)标签表示HTML中的列表(或自定义列表)，该标签会与`<dt>`(definition title **定义标题**)和`<dd>`(definition description **定义描述**)一起使用。

```html
<dl>
    <dt>名词1</dt>
    <dd>名词1解释1</dd>
    <dd>名词1解释2</dd>
    ...
</dl>
```

1. `<dl></dl>`里面只能包含`<dt>`和`<dd>`。
2. `<dt>`和`<dd>`个数没有限制，通常是一个`<dt>`对应多个`<dd>`。

### 列表总结
| 标签名      | 定义       | 说明                                                        |
| ----------- | ---------- | ----------------------------------------------------------- |
| `<ul></ul>` | 无序列表   | 里面只能包含li 没有顺序，使用较多。li里面可以包含任何标签   |
| `<ol></ol>` | 有序列表   | 里面只能包含li 有顺序，使用相对较少，li里面可以包含任何标签 |
| `<dl></dl>` | 自定义列表 | 里面只能包含dt和dd，dt和dd里面可以包含任何标签              |

学会什么时候用**自定义列表**，什么时候用**无序列表**。

## 表单标签
### 表单的组成
在HTML中，一个完整的表单通常由**表单域**、**表单控件(也称为表单元素)**和**提示信息**3个部分构成。

#### 表单域
**表单域**是一个==包含表单元素的区域==
在HTML标签中，`<form>`标签用于定义表单域，以实现用户信息的收集和传递。
==`<form>`会把它范围内的表单元素信息提交给服务器。==

```html
<form action="url地址" method="提交方式(get/post)" name="表单域名称">
    各种表单元素控件
</form>
```

**常用属性：**
| 属性   | 属性值   | 作用                                                 |
| ------ | -------- | ---------------------------------------------------- |
| action | url地址  | 用于指定并处理表单数据的服务器的url地址。            |
| method | get/post | 用于设置表单数据的提交方式，其取值为get或post。      |
| name   | 名称     | 用于指定表单的名称，以区分同一个页面中的多个表单域。 |

**总结：**
1. 在我们写表单元素之前，应该有个表单域把他们进行包含。
2. 表单域就是form标签。

#### 表单控件
##### input输入表单元素
input是输入的意思，而在表单元素中`<input>`==标签用于收集用户信息。==
在`<input>`标签中，包含一个type属性，根据不同的type属性值，输入字段拥有很多种形式。
`<input type="属性值 />"`
- `<input />`标签为单标签
- type属性设置不同的属性值用来指定不同的控件类型

**type属性：**
| 属性值   | 描述                                                        |
| -------- | ----------------------------------------------------------- |
| button   | 定义可点击按钮(多数情况下，用于通过JavaScript启动脚本)      |
| checkbox | 定义复选框                                                  |
| file     | 定义输入字段和“浏览”按钮，供文件上传                        |
| hidden   | 定义隐藏的输入字段                                          |
| image    | 定义图像形式的提交按钮                                      |
| password | 定义密码字段.该字段中的字符被掩码                           |
| radio    | 定义单选按钮                                                |
| reset    | 定义重置按钮.重置按钮会清除表单中的所有数据                 |
| submit   | 定义提交按钮.提交按钮会把表单数据发送到服务器               |
| text     | 定义单行的输入字段，用户可在其中输入文本.默认宽度为20个字符 |

除type属性外，`<input>`标签还有其他很多属性，其常用属性如下
| 属性      | 属性值       | 描述                                  |
| --------- | ------------ | ------------------------------------- |
| name      | 由用户自定义 | 定义input元素的名称。                 |
| value     | 由用户自定义 | 规定input元素的值。                   |
| checked   | checked      | 规定此input元素首次加载时应当被选中。 |
| maxlength | 正整数       | 规定输入字段中的字符的最大长度。      |

1. name和value是每个表单元素都有的属性值，主要给后台人员使用。
2. name表单元素的名字，要求==单选按钮和复选按钮要有相同的name值==
3. ==checked属性主要针对于单选按钮和复选框==，主要作用一打开页面，就要可以默认选中某个表单元素。
4. maxlength是用户可以在表单元素输入的最大字符数。一般较少使用。

**`<label>`标签**
`<label>`标签为**input**元素定义标注(标签)。
`<label>`标签用于绑定一个表单元素，当点击`<label>`标签内的文本时，浏览器会自动将焦点(光标)转到或者选择对应的表单元素上，用来增加用户体验。

```html
<label for="sex">男</label>
<input type="radio" name="sex" in="sex" />
```

**核心：**`<label>`标签的==for属性==应当与相关元素的==id属性相同==

```html
    <form action="demo.php" method="get" name="name1">
        <label for="username">用户名:</label>
        <input type="text" value="请输入用户名" name="username" id="username" maxlength="8"><br />
        <label for="password">密码:</label>
        <input type="password" name="password" id="password"> <br /> 性别:
        <label for="man">男</label>
        <input type="radio" name="sex" value="男" id="man">
        <label for="woman">女</label>
        <input type="radio" name="sex" value="女" id="woman" checked><br>爱好:
        <label for="eat">吃饭</label>
        <input type="checkbox" name="hobby" id="eat">
        <label for="sleep">睡觉</label>
        <input type="checkbox" name="hobby" id="sleep">
        <label for="hit">打豆豆</label>
        <input type="checkbox" name="hobby" id="hit" checked><br>
        <input type="submit" value="免费注册">
        <input type="reset" value="重新填写">
        <input type="button" value="获取短信验证码"><br> 上传头像:
        <input type="file" value="浏览">
    </form>
```

---
**效果如下：**
<form action="demo.php" method="get" name="name1">
    <label for="username">用户名:</label>
    <input type="text" value="请输入用户名" name="username" id="username" maxlength="8"><br />
    <label for="password">密码:</label>
    <input type="password" name="password" id="password"> <br /> 性别:
    <label for="man">男</label>
    <input type="radio" name="sex" value="男" id="man">
    <label for="woman">女</label>
    <input type="radio" name="sex" value="女" id="woman" checked><br>爱好:
    <label for="eat">吃饭</label>
    <input type="checkbox" name="hobby" id="eat">
    <label for="sleep">睡觉</label>
    <input type="checkbox" name="hobby" id="sleep">
    <label for="hit">打豆豆</label>
    <input type="checkbox" name="hobby" id="hit" checked><br>
    <input type="submit" value="免费注册">
    <input type="reset" value="重新填写">
    <input type="button" value="获取短信验证码"><br> 上传头像:
    <input type="file" value="浏览">
</form>

---

##### select下拉表单元素
在页面中，如果有多个选项让用户选择，并且想要节约页面空间时，我们可以使用`<select>`标签控件定义==下拉列表==。

```html
<select>
    <option selected="1">选项1</option>
    <option>选项2</option>
    <option>选项3</option>
    ...
</select>
```

**注意事项：**
1. `<select>`中至少包含一对`<option>`
2. 在`<option>`中定义select="select"时，当前项即为默认选中项。

##### textarea文本域元素
当用户输入内容较多的情况下，我们就不能使用文本框表单了，此时我们可以使用`<textarea>`标签。
在表单元素中，`<textarea>`标签是用于定义多行文本输入的控件。

```html
<textarea rows="3" cols="20">
    文本内容blabla...
</textarea>
```

---
**注册页面综合案例:：**
<h4>青春不常在，抓紧谈恋爱</h4>
<form action="xxx.php">
    <table width="600">
        <tbody>
            <tr>
                <td>性别:</td>
                <td>
                    <label for="man">
                        <input type="radio" name="sex" id="man"> <img src="./images/man.jpg" alt="男"> 男
                    </label>
                    <label for="woman">
                        <input type="radio" name="sex" id="woman"> <img src="./images/women.jpg" alt="女"> 女
                    </label>
                </td>
            </tr>
            <tr>
                <td>生日:</td>
                <td>
                    <select name="birthday" id="year">
                        <option selected="1" >--请选择年份--</option>
                        <option >2001</option>
                        <option >2002</option>
                        <option >2003</option>
                    </select>
                    <select name="birthday" id="month">
                        <option selected="1">--请选择月份--</option>
                        <option >01</option>
                        <option >02</option>
                        <option >03</option>
                        <option >04</option>
                        <option >05</option>
                        <option >06</option>
                        <option >07</option>
                        <option >08</option>
                        <option >09</option>
                        <option >10</option>
                        <option >11</option>
                        <option >12</option>
                    </select>
                    <select name="birthday" id="year">
                        <option selected="1">--请选择日期--</option>
                        <option >01</option>
                        <option >02</option>
                        <option >03</option>
                        <option >04</option>
                        <option >05</option>
                        <option >06</option>
                        <option >07</option>
                        <option >08</option>
                        <option >09</option>
                        <option >10</option>
                        <option >11</option>
                        <option >12</option>
                        <option >13</option>
                        <option >14</option>
                        <option >15</option>
                        <option >16</option>
                        <option >17</option>
                        <option >18</option>
                        <option >19</option>
                        <option >20</option>
                        <option >21</option>
                        <option >22</option>
                        <option >23</option>
                        <option >24</option>
                        <option >25</option>
                        <option >26</option>
                        <option >27</option>
                        <option >28</option>
                        <option >29</option>
                        <option >30</option>
                        <option >31</option>
                    </select>
                </td>
            </tr>
            <tr>
                <td>所在地区:</td>
                <td>
                    <input type="text" value="黑龙江">
                </td>
            </tr>
            <tr>
                <td>婚姻状况:</td>
                <td>
                    <input type="radio" name="marriage" id="unmarried" checked="1"><label for="unmarried">未婚</label>
                    <input type="radio" name="marriage" id="married"><label for="married">已婚</label>
                    <input type="radio" name="marriage" id="divorce"><label for="divorce">离婚</label>
                </td>
            </tr>
            <tr>
                <td>学历:</td>
                <td>
                    <input type="text" value="博士后">
                </td>
            </tr>
            <tr>
                <td>喜欢的类型:</td>
                <td>
                    <input type="checkbox" name="type" id="charming"><label for="charming">妩媚的</label>
                    <input type="checkbox" name="type" id="cute"><label for="cute">可爱的</label>
                    <input type="checkbox" name="type" id="fresh"><label for="fresh">小鲜肉</label>
                    <input type="checkbox" name="type" id="bacon"><label for="bacon">老腊肉</label>
                    <input type="checkbox" name="type" id="all" checked="1"><label for="all">都喜欢</label>
                </td>
            </tr>
            <tr>
                <td>个人介绍</td>
                <td>
                    <textarea name="synopsis" id="synopsis" cols="20" rows="2">个人简介</textarea>
                </td>
            </tr>
            <tr>
                <td></td>
                <td>
                    <input type="submit" value="免费注册">
                </td>
            </tr>
            <tr>
                <td></td>
                <td>
                    <input type="checkbox" name="agree" checked="1"> 我同意注册条款和会员加入标准
                </td>
            </tr>
            <tr>
                <td></td>
                <td>
                    <a href="#">我是会员，立即登录</a>
                </td>
            </tr>
            <tr>
                <td></td>
                <td>
                    <h4>我承诺</h4>
                </td>
            </tr>
            <tr>
                <td></td>
                <td>
                    <ul>
                        <li>年满18岁、单身</li>
                        <li>抱着严肃的态度</li>
                        <li>真诚寻找另一半</li>
                    </ul>
                </td>
            </tr>
        </tbody>
    </table>
</form>


- 百度:[http://www.baidu.com](http://www.baidu.com)
- W3C:[http://www.w3school.com.cn](http://www.w3school.com.cn)
- MDN:[http://developer.mozilla.org/zh-CN/](http://developer.mozilla.org/zh-CN/)
