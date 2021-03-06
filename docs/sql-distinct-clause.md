# SQL |独特子句

> 原文:[https://www.geeksforgeeks.org/sql-distinct-clause/](https://www.geeksforgeeks.org/sql-distinct-clause/)

distinct 关键字与 select 关键字结合使用。当需要避免任何特定列/表中出现重复值时，这很有帮助。当我们使用 distinct 关键字时，只获取**唯一值**。

**语法:**

```sql
SELECT DISTINCT column1, column2 
FROM table_name 

```

**第 1 列，第 2 列:**表中字段的名称。

**表名:**我们要从中获取记录的表。

该查询将返回表中具有字段 column1、column2 的行的所有唯一组合。

**注意:**如果 distinct 关键字用于多列，则在结果集中显示 distinct 组合。

**表─**学生

<figure class="table">电话 SURESH

| 【卷号】 | 【 Name 】 | [Address] | [Delhi] | 【XXXXXX】 |  |  |
| 【su JIT】

&#124;  &#124;

 |

</figure>

**查询**

*   从名称字段提取唯一名称–

```sql
SELECT DISTINCT NAME 
FROM Student;

```

**输出:**

<figure class="table">

|  |
| --- |
| 公羊 |

</figure>

*   从整个表中获取唯一的行组合–

```sql
SELECT DISTINCT * 
FROM Student;

```

**输出:**

<figure class="table">

| **【滚 _ 号】** | **Name** | 【xxxxxxx】 | 【20】 |
| 【xxxxxxx】

&#124; 【Suresh】 &#124; -什么 &#124;

 |

</figure>

**注意:**在上述两个示例中，如果没有 distinct 关键字，将会获取 6 条记录，而不是 4 条，因为在原始表中有 6 条记录具有重复值。

本文由 [**哈什·阿加瓦尔**](https://www.facebook.com/harsh.agarwal.16752) 供稿。如果你喜欢 GeeksforGeeks 并想投稿，你也可以使用[contribute.geeksforgeeks.org](http://www.contribute.geeksforgeeks.org)写一篇文章或者把你的文章邮寄到 contribute@geeksforgeeks.org。看到你的文章出现在极客博客主页上，帮助其他极客。

如果你发现任何不正确的地方，或者你想分享更多关于上面讨论的话题的信息，请写评论。