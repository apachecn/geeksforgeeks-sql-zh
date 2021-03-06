# SQL 面试问题

> 原文:[https://www.geeksforgeeks.org/sql-interview-questions/](https://www.geeksforgeeks.org/sql-interview-questions/)

**1。** **什么是 SQL？**
SQL 代表结构化查询语言。它是一种用于与数据库交互的语言，即创建数据库、在数据库中创建表、检索数据或更新数据库中的表等。SQL 是 ANSI(美国国家标准协会)标准。使用 SQL，我们可以做很多事情。例如，我们可以执行查询，可以将记录插入表中，可以更新记录，可以创建数据库，可以创建表，可以删除表，等等。

**2。什么是数据库？**
数据库被定义为以有组织的方式存储在计算机或数据数据库中的数据的结构化形式，并且可以以各种方式访问。它也是模式、表、查询、视图等的集合。数据库帮助我们轻松地存储、访问和操作保存在计算机上的数据。数据库管理系统允许用户与数据库交互。

**3。SQL 支持编程语言特性吗？**
的确 SQL 是一种语言，但是它不支持编程，因为它不是编程语言，它是命令语言。我们在 SQL 中没有像 for 循环或 if 这样的条件语句..否则，我们只有可以用来查询、更新、删除等的命令。数据库中的数据。SQL 允许我们操作数据库中的数据。

**4。SQL 和 PL/SQL 有什么区别？**
Ans:SQL 和 PL/SQL 的一些常见区别如下:

<figure class="table">

| 结构化查询语言 | PL/SQL |
| SQL 是一种查询执行或命令语言 | PL/SQL 是一种完整的编程语言 |
| SQL 是一种面向数据的语言。 | PL/SQL 是一种过程语言 |
| SQL 本质上是非常声明性的。 | PL/SQL 具有过程性。 |
| 它用于操作数据。 | 它用于创建应用程序。 |
| 我们可以在 SQL 中一次执行一条语句 | 我们可以在 PL/SQL 中执行语句块 |
| SQL 告诉数据库，该怎么办？ | PL/SQL 告诉数据库怎么做。 |
| 我们可以在 PL/SQL 中嵌入 SQL | 我们不能在 SQL 中嵌入 PL/SQL |

</figure>

**5。SQL 中的 between 和 IN 运算符有什么区别？**
 **之间**之间的运算符用于根据一系列值获取行。
例如，****

```sql
**SELECT * FROM Students 
WHERE ROLL_NO BETWEEN 20 AND 30;**
```

****该查询将从表中选择所有这些行。ROLL_NO 字段的值在 20 和 30 之间的学生。
 ****运算符用于检查特定集合中包含的值。
例如，********

```sql
****SELECT * FROM Students 
WHERE ROLL_NO IN (20,21,23);****
```

******该查询将从学生表中选择字段 ROLL_NO 的值为 20、21 或 23 的所有行。******

********6。编写一个 SQL 查询来查找以“A”开头的员工姓名？**
SQL 的 LIKE 运算符就是为此而使用的。它用于通过在 where 子句中搜索特定模式来获取筛选数据。
使用 LIKE 的语法是，****** 

```sql
****SELECT column1,column2 FROM table_name WHERE column_name LIKE pattern;** 

**LIKE**: operator name
**pattern**: exact value extracted from the pattern to get related data in
result set.**
```

****所需的查询是:****

```sql
**SELECT * FROM Employees WHERE EmpName like 'A%' ;**
```

****关于 LIKE 运算符的更多细节，可以参考本文 [WHERE 子句](https://www.geeksforgeeks.org/sql-where-clause/)。****

******7。在 SQL 中，CHAR 和 VARCHAR2 数据类型有什么区别？**
这两种数据类型都用于字符，但是 varchar2 用于可变长度的字符串，而 char 用于固定长度的字符串。例如，如果我们将类型指定为 char(5)，那么我们将不被允许在这个变量中存储任何其他长度的字符串，但是如果我们将这个变量的类型指定为 varchar2(5)，那么我们将被允许存储可变长度的字符串。我们可以在这个变量中存储一个长度为 3、4 或 2 的字符串。****

******8。说出 SQL 中可用的不同类型的案例操作函数。**
SQL 中有三种类型的案例操作函数。他们是，****

*   ******low**:这个函数的目的是以小写形式返回字符串。它将字符串作为参数，并通过将其转换为小写字母来返回字符串。
    语法:**** 

```sql
**LOWER('string')**
```

*   ******UPPER** :这个函数的目的是返回大写的字符串。它将字符串作为参数，并通过将其转换为大写形式来返回字符串。
    语法:****

```sql
**UPPER('string')**
```

*   ******INITCAP** :这个函数的目的是返回第一个字母大写，其余字母小写的字符串。
    语法:**** 

```sql
**INITCAP('string')**
```

******9。数据定义语言是什么意思？**
数据定义语言或 DDL 允许执行像 CREATE、DROP 和 ALTER 这样的查询。这就是那些定义数据的查询。****

******10。数据操作语言是什么意思？**
数据操作语言或 DML 用于访问或操作数据库中的数据。
它允许我们执行下列功能:****

*   ****在数据库中插入数据或行****
*   ****从数据库中删除数据****
*   ****检索或获取数据****
*   ****更新数据库中的数据。****

******11 时。** **主键和唯一约束有什么区别？**
主键不能有空值，唯一约束可以有空值。表中只有一个主键，但可以有多个唯一约束。主键会自动创建聚集索引，但唯一键不会。****

******12 时。SQL 中的视图是什么？******

****SQL 中的视图是一种虚拟表。视图也有行和列，因为它们位于数据库中的真实表上。我们可以通过从数据库中的一个或多个表中选择字段来创建视图。视图可以包含表的所有行，也可以包含基于特定条件的特定行。****

****SQL 的 CREATE VIEW 语句用于创建视图。****

****基本语法:****

```sql
**CREATE VIEW view_name AS
SELECT column1, column2.....
FROM table_name
WHERE condition;

**view_name**: Name for the View
**table_name**: Name of the table
**condition**: Condition to select rows**
```

****关于如何创建和使用视图的更多细节，请参考[这篇](https://www.geeksforgeeks.org/sql-views/)文章。****

******13。你说的外键是什么意思？**
外键是可以唯一标识另一个表中每一行的字段。此约束用于将字段指定为外键。也就是说，该字段指向另一个表的主键。这通常会在两个表之间创建一种链接。
考虑如下所示的两个表:
T5】Orders****

<figure class="table">****T8T10O _ IDT13】ORDER _ NOT15】C _ IDT17T19】1T21】2253T23T25T272Three thousand three hundred and twenty-fiveT31****</figure>

******客户******

<figure class="table">

| C_ID | 名字 | 地址 |
| one | RAMESH | 德里 |
| Two | SURESH | 无聊死了 |
| three | 达摩克利斯 | 古尔冈 |

</figure>

****我们可以清楚地看到，Orders 表中的字段 C_ID 是 Customers 表中的主键，即它唯一地标识 Customers 表中的每一行。因此，它是订单表中的外键。
语法:****

```sql
**CREATE TABLE Orders
(
O_ID int NOT NULL,
ORDER_NO int NOT NULL,
C_ID int,
PRIMARY KEY (O_ID),
FOREIGN KEY (C_ID) REFERENCES Customers(C_ID)
)**
```

******14。什么是 SQL 中的联接？联接的类型有哪些？**
一条 SQL Join 语句用于根据两个或多个表之间的公共字段组合它们的数据或行。不同类型的连接有:**** 

*   ******INNER JOIN**:INNER JOIN 关键字选择两个表中的所有行，只要条件满足。此关键字将通过组合两个表中满足条件的所有行来创建结果集，即公共字段的值相同。****
*   ******LEFT join** :该 join 返回该 JOIN 左侧表的所有行以及该 JOIN 右侧表的匹配行。对于右侧没有匹配行的行，结果集将为空。左连接也称为左外连接****
*   ******右连接**:右连接类似于左连接。此联接返回联接右侧表的所有行以及联接左侧表的匹配行。对于左侧没有匹配行的行，结果集将包含 null。右连接也称为右外连接。****
*   ******完全连接**:完全连接通过组合左连接和右连接的结果来创建结果集。结果集将包含两个表中的所有行。对于不匹配的行，结果集将包含空值。****

******15。什么是指数？**
数据库索引是一种数据结构，它以额外写入和使用更多存储空间来维护额外的数据副本为代价，提高了数据库表上数据检索操作的速度。数据只能以一种顺序存储在磁盘上。为了根据不同的值支持更快的访问，需要像二分搜索法那样更快地搜索不同的值。为此，在表上创建索引。这些索引需要磁盘上的额外空间，但它们允许根据不同的频繁搜索值进行更快的搜索。****

******16。什么是表和字段？**T3】****

******表格:**表格由行和列组合而成。行称为记录，列称为字段。在 MS SQL Server 中，表是在数据库和模式名称中指定的。****

******字段:**在 DBMS 中，数据库字段可以定义为–记录中的一条信息。****

******17。什么是主键？**T3】****

****A [<u>主键</u>](https://www.geeksforgeeks.org/difference-between-primary-and-candidate-key/) 是候选键之一。其中一个候选键被选为最重要的，并成为主键。一张表中不能超过一个主键。****

******18。什么是** **a** **默认约束？******

******DEFAULT** 约束用于用默认值和固定值填充列。当没有提供其他值时，该值将被添加到所有新记录中。更多详情请参考 [SQL |默认约束](https://www.geeksforgeeks.org/sql-default-constraint/?ref=rp)一文。****

******19。什么是删除级联约束？**T3】****

****MySQL 中使用了一个“ON DELETE CASCADE”约束，当父表中的行被删除时，该约束会自动删除子表中的行。更多详情，请阅读[MySQL–关于删除级联约束](https://www.geeksforgeeks.org/mysql-on-delete-cascade-constraint/) 文章。****

******20。什么是常态化？**T3】****

****是基于给定关系模式的功能依赖和主键来分析给定关系模式的过程，以实现以下期望的属性:
1)最小化冗余
2)最小化插入、删除和更新异常
不满足属性的关系模式被分解成可以满足期望属性的较小关系模式。****

******21。什么是反规范化？**T3】****

****反规范化是一种数据库优化技术，其中我们向一个或多个表中添加冗余数据。这可以帮助我们避免关系数据库中代价高昂的连接。请注意，非规范化并不意味着不进行规范化。这是一种优化技术，在进行规范化后应用。****

****在传统的规范化数据库中，我们将数据存储在单独的逻辑表中，并试图最大限度地减少冗余数据。我们可能会努力在数据库中只保留一份数据副本。****

******22。用 SQL 解释 WITH 子句？**T3】****

****WITH 子句为提供了一种方式的关系来定义一个临时关系，该关系的定义只对 WITH 子句所在的查询可用。在组形成之后，SQL 在 WITH 子句中应用谓词，因此可以使用聚合函数。**** 

******23。索引有哪些不同的属性？**T3】****

****索引有各种属性:****

*   ******访问类型**:指基于值的搜索、范围访问等访问类型。****
*   ******访问时间**:指查找特定数据元素或元素集所需的时间。****
*   ******插入时间**:指找到合适的空间并插入新数据所花费的时间。****
*   ******删除时间**:查找一个项目并删除以及更新索引结构所花费的时间。****
*   ******空间开销**:指索引需要的额外空间。****

******24。什么是光标？**T3】****

****光标是临时存储器或临时工作站。它由数据库服务器在用户对表执行 DML 操作时分配。游标用于存储数据库表。****

******25。用 SQL 写下各种类型的** 关系 **？******

****有各种关系，即:****

*   ****一对一的关系。****
*   ****一对多的关系。****
*   ****多对一关系。****
*   ****自我参照关系。****

******26。什么是查询？**T3】****

****一个 [**<u>SQL</u>**](https://www.geeksforgeeks.org/sql-tutorial/) 查询用于从数据库中检索所需数据。但是，可能有多个 SQL 查询产生相同的结果，但效率水平不同。低效的查询可能会耗尽数据库资源，降低数据库速度，或者导致其他用户失去服务。因此优化查询以获得最佳的数据库性能是非常重要的。****

******27。什么是子查询？**T3】****

****在 SQL 中，子查询可以简单地定义为另一个查询中的一个查询。换句话说，我们可以说子查询是嵌入在另一个 SQL 查询的 WHERE 子句中的查询。****

******28。****SQL 中有哪些不同的运算符？******

****SQL 中有三种运算符，即:****

1.  ****算术运算符****
2.  ****逻辑运算符****
3.  ****比较运算符****

******29。什么是触发器？**T3】****

******Trigger** 是当数据库有任何修改时，系统自动执行的语句。在触发器中，我们首先指定何时执行触发器，然后指定触发器执行时要执行的操作。触发器用于指定某些不能使用 SQL 的约束机制指定的完整性约束和引用约束。****

******30。DELETE 和 TRUNCATE 命令有什么区别？******

<figure class="table">

| DELETE statement deletes one row at a time and records an entry in the transaction log for each deleted row. | TRUNCATE TABLE removes data by deallocating data pages used to store table data, and only the page deallocation is recorded in the transaction log. |
| The DELETE command is slower than the TRUNCATE command. | The TRUNCATE command is faster than the DELETE command. |
| To use DELETE, you need to have Delete permission on the table. | To use Truncate on a table, we need at least ALTER permission on the table. |
| The identity of the column is retained after the DELETE statement is used in the table. | If the table contains an identity column, the identity of the column will be reset to its seed value. |
| This deletion can be used with indexed views. | Truncate cannot be used for indexed views. |

</figure>

******31。什么是局部变量和全局变量及其区别？**T3】****

*   ******全局变量:******

****相反，全局变量是在函数之外定义的变量。这些变量具有全局作用域，因此任何函数都可以使用它们，而无需将它们作为参数传递给函数。****

*   ******局部变量:******

****局部变量是在函数中定义的变量。它们有局部作用域，这意味着它们只能在定义它们的函数中使用。****

******32。什么是约束？**T3】****

****约束是我们可以应用于表中数据类型的规则。也就是说，我们可以使用约束来指定可以存储在表的特定列中的数据类型的限制。更多详情请参考[SQL |约束](https://www.geeksforgeeks.org/sql-constraints/)一文。****

******33。什么是** **数据** **诚信？******

****数据完整性被定义为数据库中包含的数据既正确又一致。为此，存储在数据库中的数据必须满足某些类型的过程(规则)。数据库中的数据必须正确且一致。因此，存储在数据库中的数据必须满足某些类型的过程(规则)。数据库管理系统提供了不同的方法来实现这种类型的约束(规则)。这提高了数据库中的数据完整性。更多详情请参考[数据安全与数据完整性的区别](https://www.geeksforgeeks.org/difference-between-data-security-and-data-integrity/)一文。****

******34。什么是自动增量？**T3】****

****有时，在创建表时，表中没有唯一的标识符，因此我们在选择主键时会遇到困难。为了解决这样的问题，我们必须手动为每条记录提供唯一的密钥，但这通常也是一项繁琐的任务。因此，我们可以使用自动增量功能，为插入的每一条新记录自动生成一个数字主键值。所有数据库都支持自动增量功能。更多详情请参考 [SQL 自动递增](https://www.geeksforgeeks.org/sql-auto-increment/)一文。****

******35。集群索引和非集群索引有什么区别？******

<figure class="table"> ****| Aggregation index | Non-aggregation index |
| --- | --- |
| The aggregation index is faster. | Non-clustered indexes are slow. |
| Clustered indexes require less memory to operate. | Non-clustered indexes require more memory for operation. |
| In a clustered index, the index is the primary data. | In a nonclustered index, the index is a copy of the data. |
| A table can only have one clustered index. | A table can have multiple nonclustered indexes. |
| Clustered indexes have the inherent ability to store data on disk. | Non-clustered indexes do not have the inherent ability to store data on disk. |
| A clustered index stores pointers to blocks rather than data. | A nonclustered index stores values and pointers to actual rows that hold data. |
| The leaf node in the clustered index is the actual data itself. | In a nonclustered index, the leaf node is not the actual data itself, but only contains the contained columns. |
| In the clustering index, the clustering key defines the order of data in the table. | In a nonclustered index, the index key defines the order of data in the index. |
| A clustered index is an index type that physically reorders table records to match the index. | A nonclustered index is a special type of index, in which the logical order of indexes does not match the physical storage order of the disk uplink. |**** </figure>

****更多详情请参考[聚集索引和非聚集索引的区别](https://www.geeksforgeeks.org/difference-between-clustered-and-non-clustered-index/)一文。****

******36。什么是 MySQL 排序规则？**T3】****

****MySQL 排序规则是一组定义明确的规则，用于通过使用相应的编码来比较特定字符集的字符。MySQL 中的每个字符集可能有多个排序规则，并且至少有一个默认排序规则。两个字符集不能有相同的排序规则。更多详情请参考[MySQL 中什么是排序规则和字符集？](https://www.geeksforgeeks.org/what-is-collation-and-character-set-in-mysql/)条。****

******37。什么是用户定义的函数？**T3】****

****我们可以使用 PL/SQL 或 Java 中的用户定义函数来提供 SQL 或 SQL 内置函数中没有的功能。SQL 函数和用户定义函数可以出现在任何地方，也就是表达式出现的任何地方。****

****例如，它可以用于:****

*   ****选择 Select 语句列表。****
*   ****WHERE 子句的条件。****
*   ****连接方式、订购方式、开始方式和分组方式****
*   ****INSERT 语句的 VALUES 子句。****
*   ****UPDATE 语句的 SET 子句。****

******38。什么是所有类型的用户定义函数？**T3】****

****用户自定义函数允许人们定义自己的 T-SQL 函数，这些函数可以接受 0 个或更多参数，并返回单个标量数据值或一个表数据类型。
创建的不同类型的用户定义函数有:****

******1。标量用户定义函数**标量用户定义函数返回标量数据类型之一。不支持文本、ntext、图像和时间戳数据类型。这些是大多数开发人员在其他编程语言中习惯使用的用户定义函数类型。将 0 传递给许多参数，就会得到一个返回值。****

******2。内联表值用户定义函数**内联表值用户定义函数返回一个表数据类型，并且是视图的一个特殊替代，因为用户定义函数可以将参数传递到一个 T-SQL select 命令中，并且本质上为我们提供了一个基础表的参数化的、不可更新的视图。****

******3。多语句表-值用户定义函数**多语句表-值用户定义函数返回一个表，也是视图的一个例外，因为该函数可以支持多个 T-SQL 语句来构建最终结果，而视图仅限于单个 SELECT 语句。此外，将参数传递到 TSQL 选择命令或一组命令中的能力使我们能够在本质上创建底层表中数据的参数化、不可更新的视图。在 create function 命令中，您必须定义正在返回的表结构。创建这种类型的用户定义函数后，可以在 T-SQL 命令的 FROM 子句中使用它，这与使用也可以返回记录集的存储过程时的行为不同。****

******39。说出用来删除** **一个** **字符串末尾空格的函数？******

****在 SQL 中，字符串末尾的空格由修剪函数删除。****

```sql
****Syntax:**
       Trim(s)
       Where s is a any string.**
```

******40。什么是存储过程？**T3】****

******存储过程**是为了在数据库上执行一个或多个 DML 操作而创建的。它只不过是一组 SQL 语句，接受一些参数形式的输入，执行一些任务，可能返回值，也可能不返回值。有关更多详细信息，请参考[什么是 SQL 中的存储过程](https://www.geeksforgeeks.org/what-is-stored-procedures-in-sql/)文章。****

******41。什么是联合、减和交互命令？**T3】****

****SQL 中的集合运算消除了重复的元组，并且只能应用于联合兼容的关系。SQL 中可用的集合操作有:****

*   ****集合并集****
*   ****设置交集****
*   ****设置差异****

******联合操作:**该操作包括存在于任一关系中的所有元组。例如:找到所有在银行有贷款或账户或两者都有的客户。****

```sql
 **SELECT CustomerName FROM Depositor 
 UNION 
 SELECT CustomerName FROM Borrower ;**
```

****联合操作会自动消除重复项。如果所有的副本都应该保留，则使用 UNION ALL 代替 UNION。****

******交集运算:**该运算包括存在于两个关系中的元组。例如:要查找在银行有贷款和账户的客户:****

```sql
 **SELECT CustomerName FROM Depositor 
 INTERSECT
 SELECT CustomerName FROM Borrower ;**
```

****相交操作会自动消除重复。如果所有副本都应该保留，则使用“全部相交”代替“相交”。****

******EXCEPT Operation:** 此操作包括存在于一个关系中但不应存在于另一个关系中的元组。例如:要查找在银行有账户但没有贷款的客户:****

```sql
 **SELECT CustomerName FROM Depositor 
 EXCEPT
 SELECT CustomerName FROM Borrower ;**
```

****“例外”操作会自动消除重复项。如果所有副本都应该保留，则在“例外”处使用“例外全部”。****

******42。什么是 ALIAS 命令？**T3】****

****别名是为了特定的 SQL 查询而赋予表或列的临时名称。当使用的列或表的名称不是其原始名称，但修改后的名称只是临时名称时，就会使用它。****

*   ****创建别名是为了使表名或列名更易读。****
*   ****重命名只是暂时的更改，表名在原始数据库中不会改变。****
*   ****当表名或列名很大或可读性不强时，别名很有用。****
*   ****当查询中涉及多个表时，这些是首选的。****

****更多详情请阅读 [SQL|别名](https://www.geeksforgeeks.org/sql-aliases/)文章。****

******43。TRUNCATE 和 DROP 语句有什么区别？******

<figure class="table"> ****| serial number | 滴 | 缩短 |
| --- | --- | --- |
| 1。 | The DROP command is used to delete the table definition and its contents. | The TRUNCATE command is used to delete all rows in the table. |
| 2。 | In the DROP command, the tablespace is released from memory. | The TRUNCATE command does not free the tablespace from memory. |
| 3。 | DROP is a DDL (Data Definition Language) command. | TRUNCATE is also a DDL (Data Definition Language) command. |
| 4。 | In the DROP command, the view of the table does not exist. | In this command, the table view exists. |
| 5。 | In the DROP command, the integrity constraint will be removed. | In this command, the integrity constraint will not be removed. |
| 6。 | In the DROP command, undo space is not used. | In this command, undo space is used, but it is less than DELETE. |
| 7。 | The DROP command executes quickly, but it will cause complications. | Although this command is faster than DROP. |**** </figure>

****更多详情，请阅读 [SQL](https://www.geeksforgeeks.org/difference-between-drop-and-truncate-in-sql/) 文章中 [DROP 和【TRUNCATE 的区别。](https://www.geeksforgeeks.org/difference-between-drop-and-truncate-in-sql/)****

******44。什么是聚合函数和标量函数？**T3】****

****为了对数据进行操作，SQL 有许多内置函数，它们被分为两类，并在每一类下进一步细分为七个不同的函数。这些类别是:****

******聚合函数:**
这些函数用于对列的值进行运算，并返回单个值。****

******标量函数:**
这些函数是基于用户输入的，这些太返回  一个单值。****

****更多详情，请阅读 [SQL | Functions(聚合和标量函数)](https://www.geeksforgeeks.org/sql-functions-aggregate-scalar-functions/) 一文。****

******45。模式匹配查询中使用哪种运算符？**T3】****

****LIKE 运算符:它用于通过在 where 子句中搜索特定模式来获取过滤后的数据。****

```sql
****Syntax:**

**SELECT column1,column2 FROM table_name WHERE column_name LIKE pattern;**

LIKE: operator name** 
```

******46。通过语句定义 SQL 顺序？******

****SQL 中的 ORDER BY 语句用于根据一列或多列对提取的数据进行升序或降序排序。****

*   ****默认情况下，ORDER BY 按**升序对数据进行排序。******
*   ****我们可以使用关键字 DESC 对数据进行降序排序，使用关键字 ASC 对数据进行升序排序。****

****更多详情请阅读 [SQL | ORDER BY](https://www.geeksforgeeks.org/sql-order-by/) 文章。****

******47。解释 SQL Having 语句？******

****HAVING 用于为 select 语句中使用的组或聚合函数指定条件。WHERE 子句在分组之前选择。HAVING 子句在分组后选择行。与 HAVING 子句不同，WHERE 子句不能包含聚合函数。(详见 [<u>本</u>](http://newtonapples.com/difference-clause-clause/) 举例)。参见[T5【有 vs 哪里从句？](https://www.geeksforgeeks.org/having-vs-where-clause-in-sql/)****

******48。用例子解释 SQL AND OR 语句？******

****在 SQL 中，AND & OR 运算符用于过滤数据并根据条件获得精确的结果。****

****AND 和 OR 运算符与 WHERE 子句一起使用。****

****这两个运算符称为合取运算符。****

******和运算符:**该运算符仅显示条件**条件 1 和条件 2 评估为真的那些记录。******

******或运算符:** 此运算符显示条件 1 和条件 2 中任一条件评估为真的记录。即 **条件 1 为真或条件 2 为真。******

****更多详情请阅读 [SQL | AND 和 OR](https://www.geeksforgeeks.org/sql-and-and-or-operators/) 运算符一文。****

******49。在 SQL 中定义 BETWEEN 语句？******

****“介于”条件允许您轻松测试表达式是否在一个值范围内(包括值)。这些值可以是文本、日期或数字。它可以用在 SELECT、INSERT、UPDATE 或 DELETE 语句中。“介于”条件将返回表达式在值 1 和值 2 范围内的记录。****

****更多详情请阅读 [SQL |介于& I 运算符](https://www.geeksforgeeks.org/sql-between-in-operator/)一文。****

******50。为什么我们使用提交和回滚命令？******

<figure class="table">

| 犯罪 | 击退 |
| --- | --- |
| COMMIT permanently saves the changes made by the current transaction. | Rollback the changes made by the current transaction. |
| Changes cannot be undone after a COMMIT transaction is executed. | After the transaction is rolled back, it is restored to the previous state. |
| After the transaction is successful, apply COMMIT. | Rollback occurs when the transaction is aborted. |

</figure>

****有关更多详细信息，请阅读 SQL 文章中[提交和回滚的区别。](https://www.geeksforgeeks.org/difference-between-commit-and-rollback-in-sql/)****

******51。什么是 ACID 属性？******

****一个[](https://www.geeksforgeeks.org/sql-transactions/)<u>事务是一个单一的逻辑工作单元，它访问并可能修改数据库的内容。事务使用读写操作访问数据。为了保持数据库中的一致性，在事务之前和之后，遵循某些属性。这些被称为**酸性**性质。 [<u>ACID</u>](http://en.wikipedia.org/wiki/ACID) (原子性、一致性、隔离性、持久性)是保证数据库事务得到可靠处理的一组属性。更多详情请阅读[数据库管理系统](https://www.geeksforgeeks.org/acid-properties-in-dbms/)文章中的[酸性属性。](https://www.geeksforgeeks.org/acid-properties-in-dbms/)</u>****

****<u>**52。什么是 T-SQL？**</u>****

****<u>是事务结构查询语言的缩写。它是微软的产品，是用来与关系数据库交互的 SQL 语言的扩展。它被认为在微软的 SQL 服务器上表现最好。T-SQL 语句用于对数据库执行事务。由于与 SQL 服务器实例的所有通信都是通过向服务器发送 TransacT-SQL 语句来完成的，因此 t-SQL 具有巨大的重要性。用户也可以使用 T-SQL 定义函数。</u>****

****<u>测试 SQL 函数的类型有:</u>****

*   ****<u>**聚合**功能。</u>****
*   ****<u>**排名**功能。有不同类型的排名函数。</u>****
*   ****<u>**行集**功能。</u>****
*   ****<u>**标量**功能。</u>****

****<u>**53。空值和** **一样是零还是空格？**</u>****

****<u>在 SQL 中，零或空格可以与另一个零或空格进行比较。而一个零可能不等于另一个零。null 表示可能未提供数据或没有数据。</u>****

****<u>**54。SQL 中对分组函数的需求是什么？**</u>****

****<u>在数据库管理中，分组函数，也称为聚合函数，是一种函数，其中多行的值被分组在一起，作为特定标准的输入，以形成具有更重要意义的单个值。</u>****

****<u>**各种组功能**</u>****

```sql
**<u>1) Count()
2) Sum()
3) Avg()
4) Min()
5) Max()</u>**
```

****<u>有关更多详细信息，请阅读 SQL 文章中的[聚合函数。](https://www.geeksforgeeks.org/aggregate-functions-in-sql/)</u>****

****<u>**55。对 **MERGE 语句的需求是什么？****</u>****

**<u>SQL 中的 **MERGE** 命令实际上是三个 SQL 语句的组合: **INSERT、UPDATE 和 DELETE** 。简而言之，SQL 中的 MERGE 语句提供了一种方便的方式来一起执行所有这三个操作，这在处理大型运行数据库时非常有帮助。但与 INSERT、UPDATE 和 DELETE 语句不同，MERGE 语句需要一个源表来对所需的表执行这些操作，该表称为一个目标表。更多详情请阅读[SQL | MERGE 语句](https://www.geeksforgeeks.org/sql-merge-statement/) 文章。</u>**

**<u>**56。如何从两个表中获取公共记录？**</u>**

**<u>下面的语句可以用来从多个表中获取数据，因此，我们需要使用 join 从多个表中获取数据。</u>**

**<u>**语法:**</u>**

```sql
<u>SELECT tablenmae1.colunmname, tablename2.columnnmae    
FROM tablenmae1  
JOIN tablename2  
ON tablenmae1.colunmnam = tablename2.columnnmae
ORDER BY columnname;</u> 
```

**<u>有关更多详细信息和示例，请阅读 [SQL |从多个表中选择数据](https://www.geeksforgeeks.org/sql-select-data-from-multiple-tables/)文章。</u>**

**<u>**57。PL/SQL 函数有什么优点？**</u>**

**<u>PL / SQL 函数的优点如下:</u>**

*   **<u>我们可以对数据库进行一次调用来运行一个语句块。因此，它提高了多次运行 SQL 的性能。这将减少数据库和应用程序之间的调用次数。</u>**
*   **<u>我们可以将整个工作分成几个小模块，这变得非常容易管理，也增强了代码的可读性。</u>**
*   **<u>它促进了可重用性。</u>**
*   **<u>它是安全的，因为代码留在数据库内部，因此对应用程序(用户)隐藏了内部数据库的细节。用户只调用 PL/SQL 函数。因此，确保了安全性和数据隐藏。</u>**

**<u>**58。显示当前日期的 SQL 查询是什么？**T3】</u>**

**<u>CURRENT_DATE 返回当前日期。 如果在一条语句中多次执行该函数，则该函数返回相同的值，这意味着该值是固定的，即使在获取游标中的行之间有很长的延迟。</u>**

### **<u>语法:</u>**

```sql
<u>CURRENT_DATE
     or
CURRENT DATE</u>
```

**<u>**59。什么是 SQL 中的 ETL？**T3】</u>**

**<u>ETL 是数据仓库中的一个过程，它代表**提取**、**转换**和**加载**。这是一个过程，在这个过程中，ETL 工具从各种数据源系统中提取数据，在暂存区中对其进行转换，最后将其加载到数据仓库系统中。这是三个数据库功能，它们被合并到一个工具中，用于从一个数据库中提取数据，并将数据放入另一个数据库。</u>**

**<u>**60。什么是嵌套触发器？**T3】</u>**

**<u>触发器本身也可以包含 INSERT、UPDATE 、和 DELETE 逻辑，因此当触发器因为数据修改而被触发时，它也可以导致另一个数据修改，从而触发另一个触发器。本身包含数据修改逻辑的触发器称为嵌套触发器。</u>**

**<u>**61。如何在** **表中找到可用的约束信息？**</u>**

**<u>在 SQL Server 中，**数据字典**是一组用于存储数据库定义信息的数据库表。可以使用这些数据字典来检查已经存在的表上的约束，并对其进行更改(如果可能的话)。有关更多详细信息，请阅读 [SQL |检查表的现有约束](https://www.geeksforgeeks.org/sql-checking-existing-constraints-on-a-table-using-data-dictionaries/)文章。</u>**

**<u>**62。什么是 SQL 注入？**T3】</u>**

**<u>SQL 注入是一种通过将 SQL 命令作为语句注入网页输入来利用用户数据的技术。基本上，这些语句可以被恶意用户用来操纵应用程序的 web 服务器。</u>**

*   **<u>SQL 注入是一种代码注入技术，可能会破坏您的数据库。</u>**
*   **<u>SQL 注入是最常见的网络黑客技术之一。</u>**
*   **<u>SQL 注入是通过网页输入在 SQL 语句中放置恶意代码。</u>**

**<u>更多详情请阅读 [SQL |注入](https://www.geeksforgeeks.org/sql-injection-2/)文章。</u>**

**<u>**63。如何在 SQL 中复制** **表** **？**</u>**

**<u>有时，在 SQL 中，我们需要创建一个已经定义(或创建)的表的精确副本。[<u>【MySQL】</u>](https://www.geeksforgeeks.org/sql-tutorial/#mysql)使您能够执行此操作。因为我们可能需要这样的重复表来测试数据，而不会对原始表和存储在其中的数据产生任何影响。</u>**

```sql
<u>CREATE TABLE Contact List(Clone_1) LIKE Original_table;</u>
```

**<u>更多详情，请阅读 [MySQL](https://www.geeksforgeeks.org/cloning-table-in-mysql/) 文章中的[克隆表。](https://www.geeksforgeeks.org/cloning-table-in-mysql/)</u>**

**<u>**64。我们能禁用触发器吗？如果是，怎么做？**T3】</u>**

**<u>是的，我们可以在 PL/SQL 中禁用一个触发器。如果 c 考虑暂时禁用触发器，并且下列条件之一为真:</u>**

*   **<u>触发器引用的对象不可用。</u>**
*   **<u>我们必须执行大数据加载，并希望它在不触发触发器的情况下快速进行。</u>**
*   **<u>我们正在将数据加载到触发器适用的表中。</u>**
*   **<u>我们使用带有 disable 选项的 ALTER TRIGGER 语句来禁用触发器。</u>**
*   **<u>我们可以使用带有 disable all triggers 选项的 ALTER TABLE 语句同时禁用与表关联的所有触发器。</u>**

**<u>**65。什么是活动锁？**T3】</u>**

**<u>**活锁**发生在两个或多个进程响应其他进程的变化而不断重复相同的交互，而不做任何有用的工作的时候。这些进程不处于等待状态，它们同时运行。这与死锁不同，因为在死锁中，所有进程都处于等待状态。</u>**

**<u>**66。在不使用 distinct 关键字的情况下，我们如何避免在查询中获得重复条目** **？**</u>**

**<u>DISTINCT 在某些情况下很有用，但是它有一些缺点，即它会增加查询引擎执行排序的负载(因为它需要将结果集与自身进行比较来删除重复项)。我们可以使用以下选项删除重复条目:</u>**

*   **<u>使用行号删除重复项。</u>**
*   **<u>使用自联接删除重复项。</u>**
*   **<u>使用分组依据删除重复项。更多详细信息，请阅读 [SQL |删除无明显重复的](https://www.geeksforgeeks.org/sql-remove-duplicates-without-distinct/)文章。</u>** 

**<u>**67。NVL 函数和 NVL2 函数的区别？**T3】</u>**

**<u>这些函数适用于任何数据类型，并且适用于表达式列表中空值的使用。这些都是单行函数，即每行提供一个结果。</u>**

**<u>**NVL(expr1，expr2):** 在 SQL 中，NVL()将空值转换为实际值。可以使用的数据类型有日期、字符和数字。数据类型必须相互匹配。即 expr1 和 expr2 必须是相同的数据类型。</u>** 

```sql
<u>**Syntax:**

**NVL (expr1, expr2)**</u>
```

**<u>**NVL2(expr1，expr2，expr 3):**NVL2 函数检查第一个表达式。如果第一个表达式不为空，则 NVL2 函数返回第二个表达式。如果第一个表达式为空，则返回第三个表达式，即如果 expr1 不为空，则 NVL2 返回 expr2。如果 expr1 为空，NVL2 将返回 expr3。参数 expr1 可以有任何数据类型。</u>**

```sql
<u>**Syntax:**

**NVL2 (expr1, expr2, expr3)**</u>
```

**<u>更多详情请阅读 [SQL 通用函数| NVL、](https://www.geeksforgeeks.org/sql-general-functions-nvl-nvl2-decode-coalesce-nullif-lnnvl-nanvl/) [NVL2、 DECODE、COMPLETE、NULLIF、LNNVL](https://www.geeksforgeeks.org/sql-general-functions-nvl-nvl2-decode-coalesce-nullif-lnnvl-nanvl/) 、 [和 NANVL](https://www.geeksforgeeks.org/sql-general-functions-nvl-nvl2-decode-coalesce-nullif-lnnvl-nanvl/) 文章。</u>**

**<u>**68。什么是 SQL 中的 Case WHEN？**T3】</u>**

**<u>控制语句是大多数语言的重要组成部分 ，因为它们控制其他语句集的执行。这些也可以在 SQL 中找到，应该通过仔细选择符合我们要求的元组来用于查询过滤和查询优化等用途。在这篇文章中，我们探讨了 SQL 中的 Case-Switch 语句。CASE 语句是 SQL 处理 if/then 逻辑的方式。</u>**

```sql
<u>syntax: 1
CASE case_value
    WHEN when_value THEN statement_list
    [WHEN when_value THEN statement_list] ...
    [ELSE statement_list]
END CASE</u>
```

```sql
<u>syntax: 2
CASE
    WHEN search_condition THEN statement_list

    [WHEN search_condition THEN statement_list] ...
    [ELSE statement_list]
END CASE</u>
```

**<u>更多详情请阅读 [SQL | Case Statement](https://www.geeksforgeeks.org/sql-case-statement/) 文章。</u>**

**<u>**69。聚结()&和 ISNULL()有什么区别？**T3】</u>**

**<u>**聚结():**SQL 中的聚结函数返回其参数中的第一个非空表达式。如果所有表达式的计算结果都为 null，那么 function 函数将返回 null。
语法:</u>**

```sql
<u>SELECT column(s), CAOLESCE(expression_1,....,expression_n)
FROM table_name;</u>
```

**<u>**ISNULL():**ISNULL 函数在 SQL Server 和 MySQL 中有不同的用法。在 SQL Server 中，ISNULL()函数用于替换空值。
**语法:**</u>**

```sql
<u>SELECT column(s), ISNULL(column_name, value_to_replace)
FROM table_name;</u>
```

**<u>更多详情请阅读 [SQL | Null 函数](https://www.geeksforgeeks.org/sql-null-functions/)一文。</u>**

**<u>**70。命名查询中用于附加两个字符串的运算符？**</u>**

**<u>在附加两个字符串的 SQL 中，使用了“集中运算符”，其符号是“||”。</u>**