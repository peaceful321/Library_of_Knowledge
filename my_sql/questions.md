# Mac通过Homebrew安装MySQL使用MySQL命令无法启动和关闭服务

Homebrew 安装MySQL想启动和关闭服务需要使用以下命令
 
// 启动 mysql, 并设置为开机启动
brew services start mysql
 
// 关闭 mysql
brew services stop mysql
 
// 重启 mysql
brew services restart mysql


# mysql 如何实现数据备份 

使用mysqldump 工具就可以实现数据库的导出；
> mysqldump -u root -p password [databaseName] [dump_file]


# mysql 设置 root账户 远程连接权限
> use mysql;   

> update user set Host='%' WHERE `user` = 'root' and `HOST` = 'localhost';
> flush privileges;
> select `user`, `HOST` from user;


root321. 



