# MYSQL
## SQL通用语法

#:代表注释（单行）

/**/:（多行）

不区分大小写

### DDL:数据定义语言(操作数据库，表等)

### DML:数据操作语言(对表中数据进行增删改)

### DQL:数据查询语言(对表中数据进行查询)

### DCL:数据控制语言(对数据库进行权限控制)

show databases: ==> 查看所有数据库名称

create database db1; ==>创建一个数据库

create database if not exists db1; ==>判断语句（若没有则创建）

drop database db1; ==>删除数据库操作

drop database if exists db1; ==>删除数据库(若存在则删除)

use db1; ==>使用数据库

select database();==>查看当前数据库

show tables; ==> 查询数据库中的表

desc 表名; ==>查看表（结构信息）

create table 表名(
    字段名1 数据类型1,
    字段名2 数据类型2,
    ...
    字段名n 数据类型n,
); ==>创建表

![alt text](image-1.png)

drop table 表名; ==>删除表

drop table if exists 表名; ==>删除表时判断表是否存在

alter table 表名 rename to 新的表名; ==>修改表名

alter table 表名 add 列名 数据类型;==>添加一列

alter table 表名 modify 列名 新数据类型;==>修改数据类型

alter table 表名 change 列名 新列名 新数据类型;==>修改列名和数据类型

alter table 表名 drop 列名;==>删除列

![alt text](image-3.png)

![alt text](image-4.png)

![alt text](image-5.png)

![alt text](image-6.png)

![alt text](image-7.png)

select 字段列表 from 表名 order by 排序字段名[排序方式1],排序字段名2,[排序方式2]...;

ASC:升序排列（默认值）

DESC:降序排列

select 聚合函数名(列名) from 表;

聚合函数分类:
count（列名）==> 统计数量（一般选用不为null的列）

max（列名）==> 最大值

min（列名）==> 最小值

sum（列名）==> 求和

avg（列名）==> 评价值

select 字段列表 from 表名 [while 分组前条件限定] group by 分组字段名 [having 分组后条件过滤]; ==>分组查询

select 字段列表 from 表名 limit 起始索引，查询条目数; ==>分页查询语法
### 约束

alter table 从表名 add constraint 外键名 foreign key(主键名)==> 添加外键
