# Alternative to UDAF in PySpark

It does not support UDAF in the latest stable 2.4.0 PySpark. To learn the use of UDAF, you could refer to examples provided in [Spark source code](https://github.com/apache/spark/tree/master/examples/src/main/scala/org/apache/spark/examples/sql), only in Scala and Java. Overally, UDAF is kind of like Mapreduce, including processes similar to map, shuffle and reduce.



Here I want to share my way if I must write python codes and execute in Spark and I need UDAF. The alternative is using UDF. The drawback is the poor performance, because UDF deals with one row on a single core.



When you `group by` your records and want to call UDAF, you could call statements like `COLLECT_LIST` or `CONCAT_WS` to collect all the records together to form a new column and pass it to a UDF. In the UDF, you can split it and do the things you plan to do with pure python codes. You can try my way if you do not really care about the performance.