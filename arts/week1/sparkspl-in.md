# Spark SQL IN ClAUSE

When I was using Spark SQL and wrote IN clauses, I found that Spark SQL(Hive) did not support IN / NOT IN.

After googling, I was told that IN can be replaced by left semi-join statements, while NOT IN can be replaced with left outer-join.



## Example

Considering 2 tables:

```sql
Student
id	name	depart
01	Sam		Chinese
02	Simon	CS
03	Tina	Math

Grade
id	grade
02	100
09	80
03	92
```



We wanted to execute the following statements in Spark SQL:

```
SELECT *
FROM Student
WHERE id IN (SELECT id FROM Grade)
```



Since IN was not supported, we can write the following one instead:

```sql
SELECT *
FROM Student LEFT SEMI JOIN Grade ON Student.id=Grade.id
```

An example of NOT IN:

```sql
SELECT A.id FROM A LEFT OUTER JOIN B ON (B.id = A.id) WHERE B.id IS null
```



### Reference

https://www.jianshu.com/p/05d8299b920b

https://stackoverflow.com/questions/40218473/spark-sql-in-clause

http://mail-archives.apache.org/mod_mbox/spark-user/201509.mbox/%3C48faca8b194a46a68985ccd05c8ec90f@exchangemailbox.reality.mine%3E

