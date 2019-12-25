# 第一章 初识数据库MySQL

### 一、数据库的基础知识

Mysql是一个开放源代码的数据库管理系统(DBMS)，它是由Mysql AB公司开发，发布并支持的。Mysql是一个跨平台的开源关系数据库管理系统，广泛地应用在Internet上的中小型网站公司开发中，本章主要介绍数据库的基础知识，通过本章的学习，我们可以了解数据库的基础概念，数据库的构成和Mysql的基础只是

数据库是由一批数据构成的有序的集合，这些数据被存放在结构化的数据表里，数据表之间互相关联，反映了客观事物间的本质联系。数据库系统提供对数据的安全控制和完整性控制。本节将介绍数据库中的一些基础概念，包括：数据库的定义，数据表的定义和数据类型等。

 

 

### 二、 什么是数据库

数据库的概念诞生在60年前，随着信息技术和市场的快速发张，数据库技术层出不穷，随着应用的扩展和深入，数据库的数量和规模越来越大，其诞生和发展给计算机信息管理带来了一场巨大的革命

数据库的发张大致划分为以下几个阶段：人工管理阶段，文件系统阶段，数据库系统阶段，高级数据库阶段，其种类大概有三种：层次式数据库，网络式数据库和关系式数据库。不同种类的数据库按不同过的数据结构来联系和组织

对于数据库的概念，没有一个完全固定的定义，随着数据库历史的发展，定义的内容也有很大的差异，其中一种比较普遍的观点认为，数据库(DataBase, DB)是一个长期存储在计算机内的，有组织的，有共享的，统一管理的数据集合。他简而言之就是一个存储数据的仓库，为了方便数据的存储和管理，它将数据按照特定的规律存储在磁盘上，通过数据库管理系统，可以有效得组织和管理存储在数据库中得数据

数据库得特点包括：实现数据共享，减少数据冗余，采用特定得数据类型，具有较高得数据独立性，具有统一得数据控制功能



### 三、  表

在关系型数据库中，数据得表是一系列二位数组得集合，用来存储数据的操作数据的逻辑结构，它是由纵向的列和横向的行组成，行被称为记录，是组织数据的党委，列被称为字段，每一列表示记录的一个属性，都有相应的描述信息，如数据类型，数据宽度等等。

例如一个有关作者信息的名为authors的表中，每个列包含所有作者的某个特定类型的信息，比如“姓名”，而每行则包含了某个特点作者的所有信息：编号、姓名、性别、专业

##### 如图1.1所示：

| 编号 | 姓名 | 性别 | 专业   |
| ---- | ---- | ---- | ------ |
| 100  | 张三 | f    | 计算机 |
| 101  | 李四 | m    | 会计   |
| 102  | 王五 | f    | 石油   |





### 四、  数据类型

数据类型决定了数据在计算机中的存储格式，代表不同的信息类型，常用的数据类型有：整数数据类型，浮点数数据类型，精确小数类型，二进制数据类型，日期/时间数据类型

 

### 五、 主键

主键(Primary Key)用于唯一地标识表中的每一条记录，可以定义表中的一列或者多列为主键。主键列上不能有两行相同的值，也不能为空值NULL

 

### 六、 数据库技术的构成

数据库系统由硬件部分和软件部分共同构成，硬件主要用于存储数据库中的数据，包括计算机，存储设备等，软件部分则主要包括DBMS、支持DBMS运行的操作系统，以及支持多种语言进行应用开发的访问技术等。

  

### 七、  数据库系统

**数据库系统由3个主要的组成部分**

数据库：用于存储数据的地方

数据管理系统：用于管理数据库的软件

数据库应用程序：为了提高数据库系统的处理能力所使用的管理数据库的软件补充

数据库（DataBase System）提供了一个存储空间一存储各种数据，可以将数据库视为一个存储数据的容器，一个数据库可能包含许多文件，一个数据库系统种通常包含许多数据库

数据库管理系统（DataBase Management System,DBMS）是用户创建维护数据库所使用的软件，位于用户与操作系统之间，对数据库进行统一管理，DBMS能定义数据存储结构，提供数据的操作机制，为何数据库的安全性、完整性、和可靠性

数据库应用程序（Database Application）虽然以及有了DBMS，但是在很多情况下。DBMS无法满足对数据管理的要求，数据库应用程序的使用可以满足对数据管理的更高要求，还可以是数据管理过程更加直观，数据库应用程序负责与DBMS进行通信，访问和管理DBMS中存储的数据，运行用户插入、修改、删除DB中的数据

##### 数据库系统如图1.2所示

![img](image/Mysql/clip_image002.jpg)



### 八、 数据库访问技术

不同程度的设计语言会由各种不同的数据库访问技术，程序语言用过这些技术，执行SQL语句，进行数据库管理。主要的数据库访问技术有:

1.ODBC

Open Database Connectivity(开放数据库互联)技术为访问不同的SQL数据库提供了一个共同的接口，ODBC使用SQL作为访问数据的标准，这一接口提供了最大限度地互操作性，一个应用程序可以通过共同地一组代码访问不同地SQL数据库管理系统DBMS

2.JDBC

Java Data Base Connectivity（java数据库连接）用于java应用程序连接数据库地标准方法，是一种用于执行SQL语句地java API，可以为多种关系数据库提供统一访问，它由一组用java语言编写地类和接口组成

3.ADO.NET：是微软在.NET 框架下开发设计的一组用于 和数据源进行交互的 面向对象 类库。

4.PDO：（php data object） 为php访问数据定义了一个轻量级、一致性的接口。它提供了一个数据访问抽象层



### 九、 SQL语言

**SQL-92 ANSI美国标准机构**

**分为四类：**
 数据定义语言DDL    （Date Definition language）：CREATE（创建）、ALTER（修改）、DROP（删除） 针对数据库或者数据表而言

数据操作语言DML   （Date Manipulation language）：INSERT（写入）、UPDATE（更新）、DELETE（删除） 针对数据而言

数据查询语言DQL  （Date query language）：SELECT（查看）   查看表中数据

数据控制语言DCL    （Date control langualge）：BEGIN（开启事务）、GRANT（授权）、COMMIT（提交事务）、REVOKE（收回权限）    对于用户或者功能的控制情况

 

### 小实验：

```mysql
-- 创建数据库sjk1223
mysql> CREATE DATABASE sjk1223;
Query OK, 1 row affected (0.01 sec)

-- 切换到sjk1223数据库
mysql> USE sjk1223;
Database changed

-- 创建表student
mysql> create table student
    -> (name varchar(30),
    -> sex char(2),
    -> high int,
    -> weight int,
    -> address varchar(50),
    -> primary key(name,sex,high,weight,address));
Query OK, 0 rows affected (0.03 sec)

-- 查看表student
mysql> select * from student;
Empty set (0.00 sec)

-- 往student表中添加数据
mysql> insert into student values('zs','m','180','80','bjhd');
Query OK, 1 row affected (0.01 sec)

-- 查看表student
mysql> select * from student;
+------+-----+------+--------+---------+
| name | sex | high | weight | address |
+------+-----+------+--------+---------+
| zs   | m   |  180 |     80 | bjhd    |
+------+-----+------+--------+---------+
1 row in set (0.00 sec)

```



###   十、 Mysql优势

1.速度快

2.免费

3.操作简单，使用容易

4.移植性强

5.接口丰富，当前所有地主流语言都可以和mysql进行沟通，拥有API接口

5.安全性和连续性



### 十一 、基本操作

###### 创建数据库

CREATE DATABASE 数据库名

###### 创建之后使用数据库

USE 数据库名

###### 查看当前mysql中有那些数据

SHOW DATABASES

在mysql中默认使用（分号）作为结束符用于结束mysql命令，结束符还有\G和\g，其中\g等同于；（分号），\G使用更直观地方式进行查看内容，去掉表结构的方式

###### 删除数据库

（数据库一旦删除，在库中的所有的表以及表中所有的数据都随着数据库的删除一并删除）

DROP DATABASE 数据库名



### 十二、 Mysql数据库的默认4个数据库

test：属于测试库，所有的用户对于该库都拥有root权限，可以增删改查（不会存放重要信息）

mysql：用于存放用户权限，密码信息和关键字等控制和管理信息

information_schema：用于保存关于mysql所维护 的所有数据库的信息，包含数据库名，库中的表明，表中的字段，数据类型等等信息

performance_schema：用于收集服务器性能参数，5.5版本之后才能拥有的数据库



### 十三、 存储引擎

属于mysql底层组件，通过存储引擎支持mysql的增删改查，不同的存储引擎拥有不同的功能，属于mysql的核心

###### 查看存储引擎的语法

SHOW ENGINES\G

存储引擎就是mysql存放数据的合适，不同的存储引擎有的支持全文索引，有的支持外键，需要根据不同的环境选择实弹存储引擎进行使用



Engine: MyISAM					   				#存储引擎名

Support: YES											#mysql是否支持该种存储引擎

Comment: MyISAM storage engine		  #mysql对该种存储引擎的描述

Transactions: NO									  #是否支持事务

XA: NO											    	#是否支持分布式事务

Savepoints: NO										#是否支持事务的保存点



在mysql中不允许出现相同名字的数据库

在库中不允许出现相同名字的表

在表中不允许出现相同名字的字段

在mysql中对库表名有严格的大小写区分，但是对字段没有大小写的区分



##### MyISAM

1.mysql5.5版本之前的默认存储引擎（建表如果不使用存储引擎默认使用MyISAM），在5.5版本之后使用InnoDB

2.MyISAM存储引擎读取速度快，占用资源少，不支持事务，不支持外键，支持全文索引

3.读写相互阻塞

4.只能缓存索引不能缓存数据

###### MyISAM应用场景

1.不需要事务的业务

2.适用于读数据较多的业务

3.并发较低的业务

4.硬件资源较差的服务器



##### InnoDB

1.mysql5.5版本后的默认存储引擎

2.支持外键，行级别锁定，支持事务，支持事务的提交，回滚和崩溃恢复，能处理大并发数据，性能较高

3.具有较高缓存性能，能缓存索引，也能缓存数据

4.使用InnoDB会在数据目录下生成两个名为ib_logfile0和ib_logfile1的5M大小日志文件和一个10M大小名为ibdata1（ibdata1中存放了使用InnoDB存储引擎的表的数据以及索引信息）的自动扩展数据文件

###### InnoDB的应用场景

1.需要支持事务的业务，高并发业务，例如：银行转账

2.数据需要大量更新的场景，例如：微博、论坛等

3.数据一致性要求较高的业务，例如：手机卡充值



###### 查看默认存储引擎

SHOW VARIABLES LIKE 'default_storage_engine';	

###### 查看系统参数的命令

SHOW VARIABLES LIKE ''	



##### Memory

1.使用内存来进行保存数据，为查询和引用提供快速访问

2.支持hash和btree索引，不支持使用biob和text数据类型

3.如果不需要使用memory表中内容，直接将表清空或者以删除表数据的方式可以直接释放内存

###### Memory应用场景

1.只是临时存放数据，数据量不大，不需要较高安全性，可以选择Memory，MySQL使用Memory相当存放查询的中间结果，一般用于存放session







# 第二章 对于数据表的操作

首先，表作为存放数据的基本单位，可以包含一个或者多个字段，可以用于创建、删除或者进行修改，建表的过程相当于给字段设置属性的过程，也是对数据进行约束的过程

### 一、 命令

##### 创建表的语法

CREATE TABLE 表明

{

字段1 数据类型 [完整的约束条件]

字段2 数据类型 [完整的约束条件]...

}

##### 查看当前有那些库

SHOW DATABASES

然后使用USE 库名  使用库

##### 查看当前库有那些表

SHOW TABLES 

### 二、 完整性约束条件是什么

对字段进行限制，允许用户向字段中写入符合约束条件的数据，如果用户写入的数据不满足条件。则会写入失败



### 三、约束条件

PRIMARY KEY			标识该属性为该表的主键，用于唯一的标识数据

FOREIGN KEY			标识该属性为该表的外键，是与之联系的某表的主键

NOT NULL				   标识该属性不能为空

UNIQUE					   标识该属性值唯一

DEFAULT					 给某个字段设置默认值

AUTO_INCREMENT	标识带有该属性的字段值自动增加



##### 主键

需要满足唯一且非空的条件，用于唯一标识数据，可以给数据本身具有唯一特质的字段进行添加，例如身份证号

###### 1.单字段主键（表中只有一个字段被设置为主键）

字段名 数据类型 PRIMARY KEY

```mysql
-- 创建表example并将id字段设置为主键
mysql> CREATE TABLE example (
    -> id INT PRIMARY KEY,
    -> name VARCHAR(30),
    -> sex CHAR(2));
Query OK, 0 rows affected (0.02 sec)

-- 往表中添加数据，id字段要不同，否则无法添加
mysql> INSERT INTO example VALUES(1,'user1','m');
Query OK, 1 row affected (0.00 sec)

mysql> INSERT INTO example VALUES(2,'user1','m');
Query OK, 1 row affected (0.01 sec)

-- 查看
mysql> select * from example;
+----+-------+------+
| id | name  | sex  |
+----+-------+------+
|  1 | user1 | m    |
|  2 | user1 | m    |
+----+-------+------+
```



###### 2.在定义完所有列之后设置主键

PRIMARY KEY (字段名)

```mysql
-- 创建表example1，将s_id设置为主键
mysql> CREATE TABLE example1(
    -> s_id INT,
    -> s_name VARCHAR(30),
    -> s_sex CHAR(2),
    -> PRIMARY KEY (s_id));
Query OK, 0 rows affected (0.01 sec)

```



###### 3.多字段主键（将多个字段放置在一起作为一个主键）

PRIMARY KEY (字段名1,字段名2...)

```mysql
-- 创建表example3，将name,high,weight,birthday,address这几个字段设置成一个主键
mysql> CREATE TABLE example3(
    -> name VARCHAR(30),
    -> high INT,
    -> weight INT,
    -> birthday DATE,
    -> address CHAR(30),
    -> PRIMARY KEY (name,high,weight,birthday,address));
Query OK, 0 rows affected (0.00 sec)

-- 添加数据的时候注意，这5个字段如果全部相同无法添加，只要有一个字段不同就能添加
mysql> INSERT INTO example3 VALUES ('user2',180,80,'1999-01-01','beijing');
Query OK, 1 row affected (0.00 sec)

mysql> INSERT INTO example3 VALUES ('user2',180,80,'1999-01-01','tianjing');
Query OK, 1 row affected (0.00 sec)

```



##### 外键

用来建立表与表之间联系的约束条件，通过字段来建立连接，一旦建立外键会出现父子表概念，谁建立外键谁就是子表，被关联的另外一个表称为父表，一个外键只能有一个父表，但是父表可以有多个子表

子表与父表相关联的字段在写入数据时，父表中连接字段拥有的数据，才能向子表中添加，否则添加失败，为了保证数据的完整性，一个表作为被关联的字段必须作为主键，至于要设置外键的字段是不是主键对于关联不会产生任何影响

###### 语法

[CONSTRAINT 约束名] FOREIGN KEY （设置外键的字段1,字段2...） REFERNECES 父表名 (父表的主键列)  

```mysql
-- 创建父表example4
mysql> CREATE TABLE example4(
    -> id INT PRIMARY KEY,
    -> name VARCHAR(30),
    -> address VARCHAR(30));
Query OK, 0 rows affected (0.05 sec)

-- 创建子表example5，将d_id字段关联到example4的id字段上
mysql> CREATE TABLE example5(
    -> d_id INT,
    -> w_name VARCHAR(30),
    -> w_birthday DATE,
    -> w_address VARCHAR(30),
    -> CONSTRAINT fk_ex5 FOREIGN KEY(d_id) REFERENCES example4(id));
Query OK, 0 rows affected (0.02 sec)

-- 如果父表中id字段不存在1，则无法添加数据
-- 先往父表中添加数据
mysql> INSERT INTO example4 VALUES(1,'kyb','502');
Query OK, 1 row affected (0.00 sec)

-- 然后就可以往子表中添加id为1的数据了
mysql> INSERT INTO example5 VALUES(1,'user1','1999-01-01','beijing');
Query OK, 1 row affected (0.00 sec)

```



###### 建立外键的规则

1.建立外键时，父表中的主键列数据类型需要和外键一致

2.建立外键时，如果关联的父表为联合主键，需要从第一个字段开始关联

3.建立外键时，关联的父表中的字段一定要是父表中的主键

4.书写问题

```mysql
-- 创建联合主键的父表
mysql> CREATE TABLE example6(
    -> id INT,
    -> course_id INT,
    -> grade DECIMAL(10,2),
    -> s_name VARCHAR(30),
    -> PRIMARY KEY (id,course_id,grade,s_name));
Query OK, 0 rows affected (0.01 sec)

-- 创建外键并关联父表
mysql> CREATE TABLE example7(
    -> id INT PRIMARY KEY,
    -> c_id INT,
    -> name VARCHAR(30),
    -> CONSTRAINT fk_ex7 FOREIGN KEY (id,c_id) REFERENCES example6 (course_id,s_name));
ERROR 1215 (HY000): Cannot add foreign key constraint
-- 这里会报错，有两个地方出现了问题:
-- 1.我们的子表中id和c_id是INT类型，而父表中的s_name是VARCHAR类型
-- 2.我们的父表是联合主键，创建外键的时候，需要从第一个字段(id)开始关联,而不是从第二个字段(course_id)

-- 我们再关联一下
mysql> CREATE TABLE example7( 
    -> id INT PRIMARY KEY,
    -> c_id INT,
    -> name VARCHAR(30),
    -> CONSTRAINT fk_ex7 FOREIGN KEY (id,c_id) REFERENCES example6 (id,course_id))
    -> ;
Query OK, 0 rows affected (0.00 sec)

```



##### 非空约束条件

标识该属性的字段不能写入空值

###### 语法

字段名 数据类型 NOT NULL

```mysql
-- 创建表example9
mysql> CREATE TABLE example9(
    -> id VARCHAR(30) NOT NULL);
Query OK, 0 rows affected (0.01 sec)

-- 添加数据失败，此时提示id字段不能为空值
mysql> INSERT INTO example9 VALUES (NULL);
ERROR 1048 (23000): Column 'id' cannot be null


```



##### 唯一性约束条件

标识设置唯一性约束条件的字段不允许写入重复值

###### 语法1

字段名 数据类型 UNIQUE

```mysql
-- 创建表，将name字段设为唯一性约束
mysql> CREATE TABLE example10 (
    -> id INT UNIQUE,
    -> name VARCHAR(30) NOT NULL);
Query OK, 0 rows affected (0.01 sec)

-- 查看唯一约束名为id
mysql> SHOW CREATE TABLE example10\G
*************************** 1. row ***************************
       Table: example10
Create Table: CREATE TABLE `example10` (
  `id` int(11) DEFAULT NULL,
  `name` varchar(30) NOT NULL,
  UNIQUE KEY `id` (`id`)
) ENGINE=InnoDB DEFAULT CHARSET=utf8
1 row in set (0.01 sec)

```



###### 语法2

[CONSTRAINT 约束名] UNIQUE (定义唯一条件的字段) 

```mysql
-- 创建表，并将id设为唯一性，且给设置名字为uni_id
mysql> CREATE TABLE example11 
    -> (id INT,
    -> CONSTRAINT uni_id UNIQUE (id));
Query OK, 0 rows affected (0.00 sec)

-- 查看表结构
mysql> SHOW CREATE TABLE example11\G
*************************** 1. row ***************************
       Table: example11
Create Table: CREATE TABLE `example11` (
  `id` int(11) DEFAULT NULL,
  UNIQUE KEY `uni_id` (`id`)
) ENGINE=InnoDB DEFAULT CHARSET=utf8
1 row in set (0.00 sec)

```



###### 查看表结构的语法

1.DESC 表名

DESCRIBE 表名

2.SHOW CREATE TABLE 表名\G



##### 默认值

事先给某个字段设置好默认值，当不向该字段写数据时，mysql会自动将默认值填入到该字段中

###### 语法

字段名 数据类型 DEFAULT 默认值

```mysql
-- 创建表，一个字段可以有多个约束条件
mysql> CREATE TABLE example12 
    -> (id INT PRIMARY KEY,
    -> name VARCHAR(30) NOT NULL UNIQUE,
    -> class CHAR(20) DEFAULT 'sjk');
Query OK, 0 rows affected (0.01 sec)

-- 只能id，name字段添加数据
mysql> INSERT INTO example12 (id,name) VALUES (1,'user1');
Query OK, 1 row affected (0.00 sec)

-- 查看class默认值为sjk
mysql> select * from example12;
+----+-------+-------+
| id | name  | class |
+----+-------+-------+
|  1 | user1 | sjk   |
+----+-------+-------+
1 row in set (0.00 sec)

```



##### 自增

用于给写入的数据生成一个新的唯一id，一个表中只允许出现一个自增约束条件

###### 语法

字段名 数据类型 AUTO_INCREMENT

在添加自增约束条件时候，需要让带自增条件的字段为唯一性质（主键约束或唯一性约束），否则添加失败，且添加自增的字段必须是整数，字符串不能添加自增

```mysql
-- 创建表，并将id添加为主键加自增约束
mysql> CREATE TABLE example13
    -> (id INT PRIMARY KEY AUTO_INCREMENT,
    -> name VARCHAR(30));
Query OK, 0 rows affected (0.01 sec)

-- 给表中name字段添加三个数据
mysql> INSERT INTO example13(name) VALUES ('a');
Query OK, 1 row affected (0.00 sec)

mysql> INSERT INTO example13(name) VALUES ('a');
Query OK, 1 row affected (0.00 sec)

mysql> INSERT INTO example13(name) VALUES ('a');
Query OK, 1 row affected (0.00 sec)

mysql> select * from example13;
+----+------+
| id | name |
+----+------+
|  1 | a    |
|  2 | a    |
|  3 | a    |
+----+------+
3 rows in set (0.00 sec)
```





 

 

 

 

 

 

 

 