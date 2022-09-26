> 本页内容主要是在阅读该书时，所摘录或记录的笔记，该书面向完全没有编程和系统开发经验的初学者，介绍了关系数据库以及用来操作关系数据库的 SQL 语言的使用方法。 


## 绪论

### PostgreSQL的配置

+ 安装步骤

  下载链接：http://www.enterprisedb.com/products-services-training/pgdownload#windows  

+ 修改设置文件

  打开`安装路径\PostgreSQL\版本号\data\postgresql.conf`，可以进行一些基本配置，如可以设置 listen_addresses = 'localhost' ，这样就设置成只允许本地机器进行连接。

### 执行SQL语句

+ 连接PostgreSQL（登录）

  打开管理员控制台，输入指令，根据提示输入密码，出现`postgres=#  `即登录且连接成功。

  ```bash
  D:\Program\PostgreSQL\bin\psql.exe -U postgres
  ```

+ 执行SQL语句

  键入 SQL 语句`SELECT 1;  `，返回 *?column? 1 (1 行记录)*，则测试正常。

  > “;”是 SQL 的结束符，如果没有输入的话，即使按下回车键，SQL 语句也不会执行；使用`\q`退出；

+ 创建学习用的数据库

  利用 SQL 语句创建一个之后的学习需要的数据库，成功后返回：CREATE DATABASE

  ```sql
  CREATE DATABASE shop;
  ```

+ 连接学习用的数据库（登录）  

  目前连接的数据库是默认的示例数据库，创建了新的数据库后，通过指令`\q`退出，重新连接：

  ```bash
  D:\Program\PostgreSQL\bin\psql.exe –U postgres –d shop
  ```

  