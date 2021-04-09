# Mysql数据库命令

#### 1.开启mysql数据库： mysql -u root -p

#### 2.数据库命令

```cmd
登陆数据库: mysql -h xxx -uroot -p pass 数据库名称
创建数据库: CREATE DATABASE 数据库名;
删除数据库: drop database <数据库名>;
显示数据库: show databases;
使用数据库: use 数据库名;
```

#### 3.基本操作

```cmd
增删改查

增：insert into xxx(数据表表名) (name, age) values ("summer", 25);
删：drop table xxx(数据表表名);
改： update (数据表表名) set name="zero", age="20";
查：select * from xxx(数据表表名);
```

#### 4.高级操作