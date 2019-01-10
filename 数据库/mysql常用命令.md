## ssh终端登录，进入mysql
```
mysql -uroot -proot
```
>注意：-u和用户名之间没有空格

## 查看MySql数据库物理文件存放位置
```
show global variables like "%datadir%";
```
> 注意一定要用;结尾，然后回车

 
### 显示数据库
```
 show databases;
```
