### 基本标签
- h1 - h6 元素表示标题。HTML定义了标题元素的层次结构，其中 h1 是排名最高的
- hgroup 元素允许您处理多个标头元素作为单个项目，而不会影响HTML文档的大纲
- hr 元素表示水平规则。一条横跨页面的线
- div 元素是 span 元素的 block 。块元素开始新行，而行内元素保持在同一行
- span元素将一个全局属性应用于内容区域
- p 元素表示一个段落
- 在 pre 元素中，空格不会折叠，并保留格式
- blockquote 元素表示从另一个来源引用的块内容
- q 元素表示从另一个来源引用的内容

### 页面内容
- article元素表示自包含HTML文档中的内容
- section元素应用于包含内容将在文档的大纲或目录中列出，表示文档的一部分
- nav 元素表示文档的一个部分包含到其他页面或同一页面的其他部分的链接
- details 元素创建一个节，用户可以展开该节以获取有关主题的更多详细信息
- header 元素表示节的标题。它可以包含任何您想要表示为头部的内容
- footer 元素是页眉的补充，表示部分的页脚
- aside 元素表示仅与周围元素相关的内容。这类似于书或杂志中的侧边栏

### 超链接
- 超链接为HTML提供了基础，用户可以通过HTML在同一文档内和跨页面浏览内容，可以使用 a 元素创建超链接
- a 元素具有局部属性: href，hreflang，media，rel，target，type
- 可以通过将元素中的href属性设置为以http://开头的URL来创建指向其他HTML文档的超链接
- 如果 href 属性的值不以start开头识别的协议，例如 http:// 那么浏览器将超链接视为相对引用
- 可以创建超链接，使浏览器窗口中的另一个元素进入视图
- 元素的 target 属性告诉浏览器要显示链接资源的位置

### 格式化
- abbr 元素表示缩写，可以使用 title 属性来提供缩写代表的扩展文本
- address 元素标记文档或文章元素的联系信息
- b 元素标记指示任何额外强调或重要性的文本跨度
- bdi 元素标记为了文本方向性而与其他内容隔离的文本
- bdo 元素指定一个明确的文本方向其内容，覆盖通常应用的自动方向性
- 可以使用两个元素来处理内容中的换行符: br 和 wbr 元素
- cite 元素表示引用作品的标题，这样的书，文章或电影
- code 元素标记了一段计算机代码
- del 元素标记删除的文本
- dfn 元素定义一个术语。它解释了词或短语的意义
- u 元素通过添加下划线标记文本
- strong 元素标记重要的文本

### 列表
- ul 元素表示无序列表
- ul 元素中的项目使用 li 元素表示
- ol 元素表示有序列表

### figure
- figure标签规定独立的流内容（图像、图表、照片、代码等等）
- figure元素的内容应该与主内容相关，同时元素的位置相对于主内容是独立的。如果被删除，则不应对文档流产生影响
- figcaption元素被用来为figure元素定义标题

### 图像img 
- 元素允许您将图像嵌入到HTML文档中
- img 元素的常见用途是结合 a 元素创建基于图像的超链接
- 可以创建客户端图像映射：单击图像中的不同区域会导致浏览器导航到不同的URL

### iframe
- iframe 元素在现有元素中嵌入另一个HTML文档