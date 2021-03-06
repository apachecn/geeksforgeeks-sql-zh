# SQL Server 中的 SQUARE()函数

> 原文:[https://www . geesforgeks . org/square-function in-SQL-server/](https://www.geeksforgeeks.org/square-function-in-sql-server/)

**SQUARE()函数:**
SQL Server 中的这个函数用来返回指定数字的平方。例如，如果指定的数字是 9，这个函数将返回 81 作为输出。

**特征:**

*   这个函数用于给定数字的平方。
*   这个函数接受正数和负数。
*   这个函数也接受分数。
*   这个函数总是返回正数。
*   该函数使用公式**”(a)<sup>2</sup>=返回值“**，其中 a 是指定的数字。

**语法:**

```sql
SQUARE(number)
```

**参数:**
该方法接受如下参数。

*   **数字–**
    指定要返回其方块的数字。

**返回:**
返回指定数字的平方。

**示例-1 :**
得到结果 16.0，即指定数字 4 的平方。

```sql
SELECT SQUARE(4);
```

**输出:**

```sql
16.0
```

**示例-2 :**
得到结果 4.0，即指定负数-2 的平方。

```sql
SELECT SQUARE(-2);
```

**输出:**

```sql
4.0
```

**示例-3 :**
获取结果 0.0，即指定数字零(0)的平方。

```sql
SELECT SQUARE(0);
```

**输出:**

```sql
0.0
```

**示例-4 :**
得到结果 1.0，即指定数字 1 的平方。

```sql
SELECT SQUARE(1);
```

**输出:**

```sql
1.0
```

**示例-5 :**
得到结果 1.4399999999999999，即指定数字 1.2 的平方。

```sql
SELECT SQUARE(1.2);
```

**输出:**

```sql
1.4399999999999999
```

**应用:**
该函数用于返回指定数字的平方。