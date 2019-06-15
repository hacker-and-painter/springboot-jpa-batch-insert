> 原项目地址 [sb-jpa-batch-insert-demo](https://github.com/Cepr0/sb-jpa-batch-insert-demo)
> 原文地址 [how-to-do-bulk-multi-row-inserts-with-jparepository](https://stackoverflow.com/questions/50772230/how-to-do-bulk-multi-row-inserts-with-jparepository)

使用 Spring Data JPA 在应用程序中批量插入的示例

1. 将spring.jpa.properties.hibernate.jdbc.batch_size选项设置为您需要的值。
2. 使用 `repo` 的 `saveAll()` 方法插入的实体集合。

运行此应用程序并查看日志：

```
2: insert into application$model (number, id) values (1, '<byte[]>') 3: insert into application$model 
(number, id) values (2, '<byte[]>') 4: insert into application$model (number, id) values (3, 
'<byte[]>') 5: insert into application$model (number, id) values (4, '<byte[]>') 

2019-06-16 01:05:08.372  INFO 98762 --- [           main] jdbc.sqlonly                             : batching 5 statements: 1: insert into application$model (number, id) values (5, '<byte[]>') 
2: insert into application$model (number, id) values (6, '<byte[]>') 3: insert into application$model 
(number, id) values (7, '<byte[]>') 4: insert into application$model (number, id) values (8, 
'<byte[]>') 5: insert into application$model (number, id) values (9, '<byte[]>') 
```




