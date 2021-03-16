# MySQL 基础

## SELECT 查询
`SELECT`语句用于从 表或视图 中获取数据。
`SELECT`语句的结果成为结果集————行列表，每行都有相同的列数。

### SELECT 语法   
```SQL
SELECT 
    column1_name, column2_name,column3_name...
FROM 
    table1_name
[INNER | LEFT | RIGHT] JOIN table2_name ON conditions
WHERE 
    conditions
GROUP BY column_name
HAVING group_conditions
ORDER BY column_name
LIMIT offset, length;
```

SELECT语句由以下列表中所述的几个子句组成：

* **SELECT** 之后是逗号分隔列或星号(*)的列表，表示要返回所有列。
* **FROM** 指定要查询数据的表或视图。
* **JOIN** 根据某些连接条件从其他表中获取数据。
* **WHERE** 过滤结果集中的行。
* **GROUP BY** 将一组行组合成小分组，并对每个小分组应用聚合函数。
* **HAVING** 过滤器基于GROUP BY子句定义的小分组。
* **ORDER BY** 指定用于排序的列的列表。
* **LIMIT** 限制返回行的数量。

语句中的`SELECT`和`FROM`语句是必须的，其他部分是可选的。

## SELECT DISTINCT 查询子句
**SELECT DISTINCT**查询用于过滤掉重复的记录。

### SELECT DISTINCT 语法

```SQL
SELECT DISTINCT 
    columns_name
FROM 
    table_name
WHERE 
    where_conditions
```

**Tips:** 如果查询的列具有NULL值，并且对该列使用DISTINCT子句，MySQL将保留一个NULL值，并删除其它的NULL值，因为DISTINCT子句将所有NULL值视为相同的值。





