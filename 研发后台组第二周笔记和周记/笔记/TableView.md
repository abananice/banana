我们可以使用来自JavaFX API的TableView，TableColumn和TableCell类以表格形式表示数据。
通过实现数据模型和应用单元工厂来填充表中的数据。
表类可以按列排序数据，并在必要时调整列大小。

### 创建表
- 表控件是通过实例化TableView类创建的。
    - TableView table = new TableView(); 
    - table.setEditable(true);
- 然后使用TableColumn类创建列，加入到表
    - TableColumn firstNameCol = new TableColumn("First Name");
    - table.getColumns().addAll(firstNameCol);
- 调用setVisible方法隐藏列

### 嵌套标头
- 使用JavaFX表视图，我们可以轻松创建嵌套列。

### 添加新行
- 向表视图中添加数据。 
- 创建JavaFX JavaBean以保存单个行的值。

### 列排序
- TableView类具有列的内置排序功能
- 要禁止对列进行排序，请调用该列上的setSortable(false)方法

### 编辑表中的数据
- 通过调用setEditable方法，我们可以启用表内容的编辑
- setCellFactory方法安装在TextFieldTableCell类中定义的文本字段为每个表单元格
- setOnEditCommit方法更新表单元格，并且数据绑定需要考虑设置数据回到JavaFX JavaBean，它用作表视图的下划线数据模型

### 表编辑提交事件
- 如果我们只是双击并键入一些值，并单击单元格外，commit事件不会运行，旧的值将被填充

### 将数据映射添加到表中
- 可以使用MapValueFactory类将Map数据添加到表中