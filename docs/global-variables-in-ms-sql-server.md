# MS SQL Server 中的全局变量

> 原文:[https://www . geesforgeks . org/global-variables-in-ms-SQL-server/](https://www.geeksforgeeks.org/global-variables-in-ms-sql-server/)

**全局变量**是预定义的系统变量。以 **@@** 开头。它提供了有关 SQL Server 当前用户环境的信息。SQL Server 提供了多个全局变量，在 Transact-SQL 中使用非常有效。以下是一些常用的全局变量–

*   @@SERVERNAME
*   @@CONNECTIONS
*   @@MAX_CONNECTIONS
*   @@CPU_BUSY
*   @@ERROR
*   @@IDLE
*   @@LANGUAGE
*   @@TRANCOUNT
*   @@VERSION

这些解释如下。

1.  **@@SERVERNAME :**
    This is used to find the name of the machine/computer on which SQL Server is running.
    **Example –**

    ```
    Select @@servername
    ```

    **输出–**

    ```
    SERVERXX\CTRXREST
    ```

2.  **@@CONNECTIONS :**
    This is used to find number of logins or attempted logins since SQL Server was last started.
    **Example –**

    ```
    Select @@connections
    ```

    **输出–**

    ```
    59846824
    ```

3.  **@@MAX_CONNECTIONS :**
    This is used to find the maximum number of simultaneous connections that can be made with SQL Server or instance in this computer environment.
    **Example –**

    ```
    select @@max_connections
    ```

    **输出–**

    ```
    32767
    ```

4.  **@@CPU_BUSY :**
    This is used to find the amount of time, in microseconds, that the CPU has spent doing SQL Server work since the last time SQL Server was running.
    **Example –**

    ```
    Select @@cpu_busy
    ```

    **输出–**

    ```
    887468
    ```

5.  **@@ERROR :**
    This is used to check the error status (succeeded or failed) of the most recently executed statement. It contains Zero (0) if the previous transaction succeeded, else, it contains the last error number generated by the system.
    **Example –**

    ```
    Select @@error
    ```

    **输出–**

    ```
    0
    ```

6.  **@@IDLE :**
    The amount of time, in microseconds, that SQL Server has been idle since it was last started.
    **Example –**

    ```
    Select @@idle
    ```

    **输出–**

    ```
    123691249
    ```

7.  **@@LANGUAGE :**
    This is used to find the name of the language that is currently used by the SQL Server.
    **Example –**

    ```
    Select @@language
    ```

    **输出–**

    ```
    us_english
    ```

8.  **@@TRANCOUNT :**
    This is used to count the number of open transactions in the current session.
    **Example –**

    ```
    Select @@trancount
    ```

    **输出–**

    ```
    0
    ```

9.  **@@VERSION :**
    This is used to find the current version of the SQL Server Software.
    **Example –**

    ```
    Select @@version
    ```

    **输出–**

    ```
    Microsoft SQL Server 2014 (SP3-CU-GDR) (KB4535288) - 12.0.6372.1 (X64)
    Dec 12 2019 15:14:11
    Copyright (c) Microsoft Corporation
    Standard Edition (64-bit) on Windows NT 6.3 <X64> (Build 9600: ) (Hypervisor)
    ```