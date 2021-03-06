# 马里亚数据库中的时间和时间至秒函数

> 原文:[https://www . geesforgeks . org/time-and-time _ to _ sec-function-in-Maria db/](https://www.geeksforgeeks.org/time-and-time_to_sec-function-in-mariadb/)

**1。时间函数:**
在马里亚数据库中，时间函数返回日期时间表达式的时间部分。在这个函数中，第一个参数是日期时间。该函数返回给定日期时间的时间。在这个函数中，我们将在其中传递日期时间表达式，它将作为结果返回日期时间表达式的时间。如果表达式不是时间或日期时间值，时间函数将返回“00:00:00”。如果表达式为空，时间函数将返回空值。

**语法:**

```sql
TIME( expression )

```

**参数:**

*   **Datetime 表达式–**应该从中提取时间的时间值。

**返回:**
它将返回日期时间表达式的时间部分。

**示例-1 :**

```sql
SELECT TIME('2020-10-16 06:18:01.000001');

```

**输出:**

```sql
'06:18:01.000001'

```

**示例-2 :**

```sql
SELECT TIME('10:35:05');

```

**输出:**

```sql
10:35:05

```

**示例-3 :**

```sql
SELECT TIME(NULL);

```

**输出:**

```sql
NULL

```

**2。时间到秒函数:**
在马里亚数据库中，时间到秒函数用于将时间值转换为数字秒。在这个函数中，第一个参数是时间。这个函数将返回要转换成数字秒的时间值。它的工作原理与秒到时间函数相反。

**语法:**

```sql
TIME_TO_SEC( time )

```

**参数:**

*   **时间–**要转换为数字秒的时间值。

**返回:**
返回以数字秒为单位的时间。

**示例-1 :**

```sql
SELECT TIME_TO_SEC('00:00:02');

```

**输出:**

```sql
2

```

**示例-2 :**

```sql
SELECT TIME_TO_SEC('00:00:01.999999');

```

**输出:**

```sql
1

```

**示例-3 :**

```sql
SELECT TIME_TO_SEC('-12:30:59');

```

**输出:**

```sql
-45059

```