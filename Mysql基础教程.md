## Mysql基础教程
### 基础篇
♠ 连接mysql数据库  
mysql -u root -p  
♠ 创建数据库  
create database 数据库名;  
♠ 选择数据库  
use 数据库名;  
♠ 删除数据库  
drop 数据库名;  
♠ 创建数据表  
create table 表名(
列名及填写需求
)engine=innodb charset=utf8;  
create table test_1(

    -> id int not null auto_increment,

    -> title varchar(100) not null,

    -> author varchar(100) not null,

    -> submission_date date,

    -> primary key (id)

    -> )engine=innodb charset=utf8;
♠ 展示数据库表  
show tables;  
♠ 展示具体的数据表  
desc 数据表名;  
♠ 删除数据库表  
drop table 数据库表名;  
♠ 查询数据库表中所有字段数据  
select * from 数据表名;  
♠ 插入数据（单条&多条）  
insert into test_1(title,author,submission_date) values ('学习Python','菜鸟教程',now());  
> insert into test_1(title,author,submission_date) values ('学习Mysql','菜鸟教程',now()),('学习Java','菜鸟教程','2018-04-30’);

♠ 单独查询某一列  
select 列名 from 数据表名;  
♠ 条件查询（and、or、）  
select 列名 from 数据表名 where 条件;  
♠ 限定返回数据表数据条数  
select 列名 from 数据表名 limit 返回数据条数;  
♠ 更新字段取值  
update 数据表名 set 列名 = 'PHP' where 条件;  
♠ 批量替换  
update 表名 set 列名 = replace(列名, '老字符串','新字符串’);  
♠ 删除数据表中的数据  
delete from 数据表名 where 条件;  
♠ 模糊查找like(%)  
select 列名 from 数据表名 where 列名 like '匹配字符串';  
♠ 联表查询union  

♠ 从文件中导入数据  
load data local infile '/Users/lihongying/Desktop/test.txt' into table apps;  
 




