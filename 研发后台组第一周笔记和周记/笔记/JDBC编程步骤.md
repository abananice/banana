## 具体步骤
- 加载数据库驱动
- 通过DriverManager获取数据库连接
- 通过Connection对象创建Statement对象
- 使用Statement执行SQL语句
- 操作结果集
- 回收数据库资源，包括关闭ReasultSet、++Statement和Connection等资源
     #### 相关代码
``` java
public class ConnMySql {
	public static void main(String[] args) throws Exception {
		//1.加载驱动
		Class.forName("com.mysql.cj.jdbc.Driver");
		//2.使用DriverManager获取数据库连接
		Connection conn = DriverManager.getConnection("jdbc:mysql://localhost:3306/mydb?useSSL=false&serverTimezone=UTC","root","123456");
		//3.使用Connection来创建一个Statement对象
		Statement stmt = conn.createStatement();
		//4.执行sql语句
		//test_jdbc是一张表
		ResultSet rs = stmt.executeQuery("select *" + "from test_jdbc");
		//next()看是否有		
		while(rs.next())
		{
			System.out.println(rs.getInt(1));
			System.out.println(rs.getInt(2));
		}
		//关闭资源
		stmt.close();
		conn.close();
	}
}
