# mysql

+ 启动数据库
```shell
/usr/local/mysql/bin/mysql -u root -p
```

+ 查询当前数据库版本
```sql
select version();
```

+ 查看当前使用的数据库
```sql
select database();
```

+ 选择并使用数据库
```sql
use hello_sql;
```

+ 创建数据库
```sql
create database hello_sql;
```

+ 删除数据库
```sql
drop database hello_sql;
```

+ 创建数据表
```sql
create table good( hello int );
```

+ 查看数据表
```sql
show tables;
```

+ 查看表格内容
```sql
select * from table_name;
```

+ 查看表结构
```sql
desc table_name;
```

