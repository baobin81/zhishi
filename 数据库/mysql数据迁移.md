## 腾讯云数据迁移，
 
### 源服务器新建迁移账户创建用户说明
1. 用户名：随便取一个
2. 主机：要选择任意主机
3. 密码：输一个自己容易记的
4. 用户数据库：选择无
5. 全局权限：选择全选
###测试结果
1. 数据库版本不一致，腾讯云数据库最低是MysQL5.5 我们的是5.1.52
2. 失败原因：源实例binlog格式为statement
3. 解决方案：设置源实例binlog格式为row或者mixed
4. 解决过程：phpmyadmin进入以后，变量里面能看到binlog format，可以查看binlog格式
4. 失败原因：源实例innodb_stats_on_metadata值为on
5. 解决方案：设置源实例innodb_stats_on_metadata为off

## phpmyadmin 同步数据
### 远程服务器参数说明：
1. 套接字：在远程服务器，查看变量,搜索 socket 会得到结果：/var/lib/mysql/mysql.sock

20181018 试验没有成功