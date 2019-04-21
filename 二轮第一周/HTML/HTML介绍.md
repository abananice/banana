### 元素
- I like <code>web</code> and CSS.起始标记为<code>，结束标记为</ code>。标签之间是元素的内容，即web。标签和内容一起形成代码元素。
- 自闭合标签：<code/>
- 空元素：有一些元素必须使用单个标签表示。这些被称为空元素
- HTML注释：HTML中的注释以标签<！-- 开头，并以 --> 结尾

### 属性
- 元素可以通过其属性进行配置

### 结构
- Web文档的基本结构
```
<!DOCTYPE HTML>
<html>
<!--  elements go  here   -->
</html>
```
- <！DOCTYPE HTML> 告诉浏览器这是一个html文档
- 元素可以有多个子元素，但只能有一个父元素

### 实体
- 实体是浏览器替换特殊字符的代码

### 文档
- html 元素或根元素表示HTML的开始
- head 元素包含文档的元数据
- body 元素封装了HTML文档的内容

### 元数据
- title 元素设置文档的标题
- base 元素为相对链接设置基本URL，HTML文档最多只能包含一个base元素
- href 属性指定基本URL将解析文档中的相对URL
- target 属性指示浏览器如何打开网址
- meta 元素定义文档的元数据

### 样式
- style元素允许您在HTML文档中内联定义CSS样式
- style 元素具有局部属性: type，media，scoped

### 资源链接
- link 元素在HTML文档和之间创建关系外部资源，CSS样式表或Javascript文件

### 图标
- link元素可以定义与您的页面相关联的图标

### 脚本
- script元素可以包括您的页面中的脚本，在文档中内联定义或引用外部文件