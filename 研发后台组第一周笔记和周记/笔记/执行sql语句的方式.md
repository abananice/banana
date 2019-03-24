## 使用executeLargeUpdata方法执行DDL和DML语句
- 执行DDL语句后返回值为0，执行DML语句后返回值为受影响的记录条数
- 执行DDL语句的代码
 ``` java
  public class ExecuteDDL {
	private String driver;
	private String url;
	private String user;
	private String pass;
	
	public void initParam(String paramFile) throws FileNotFoundException, IOException{
		//使用Properties类来加载类属性文件
		//使用了myspl.ini来保存数据库连接信息，当环境改变时修改它就行了
		Properties props = new Properties();
		props.load(new FileInputStream(paramFile));
		driver = props.getProperty("url");
		user = props.getProperty("user");
		pass = props.getProperty("pass");
	}
	
	public void createTable(String sql) throws ClassNotFoundException, SQLException
	{
		Class.forName(driver);
		Connection conn = DriverManager.getConnection(url, user, pass);
		Statement stmt = conn.createStatement();
		stmt.executeUpdate(sql);//执行DDL语句，创建数据表
	}
	
	public static void main(String[] args) throws FileNotFoundException, IOException, ClassNotFoundException, SQLException {
		ExecuteDDL ed = new ExecuteDDL();
		ed.initParam("mysql.ini");
		ed.createTable("creat table jdbc_test" + "( jdbc_id int aut0_increment primary key," + "jdbc_name varchar(255)," + "jdbc_desc text");
		System.out.println("建表成功");
	}

}
```
## 使用execute方法执行sql语句
- Statement的execute()方法几乎可以执行任何sql语句，但执行起来比较麻烦，一般不用，返回boolean值
- getResultSet():获取该Statement执行查询语句所返回的ResultSet对象
- getUpdataCount():获取该Statement()执行DML语句所影响的记录行数
 
## 使用executeQuery方法执行sql语句
- 只能执行查询语句

## 使用PreparedStatement执行sql语句
- 可以预编译sql语句，主要用于执行结构类似的sql语句，效率高
- 可以用于防止sql注入
- 无需拼接sql语句，编程更简单
 ```
 //创建一个PreparedStatement对象，？是占位符
   pstmt = conn.preparedStatement("insert into jdbc_test values(?,null)");
```
- 可以通过setXxx(int index,Xxx value)来传入参数值，index指为第几个问号赋值


