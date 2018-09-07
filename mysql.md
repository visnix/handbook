# mysql

## 基本命令

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

## mysql数据类型

> text data types

|Data type | Description |
|------- | ------- |
|char(size) | Holds a fixed length string (can contain letters, numbers, and special characters). The fixed size is specified in parenthesis. Can store up to 255 characters |
|varchar(size) | Holds a variable length string (can contain letters, numbers, and special characters). The maximum size is specified in parenthesis. Can store up to 255 characters. `Note`: If you put a greater value than 255 it will be converted to a TEXT type |
|tinytext | Holds a string with a maximum length of 255 characters |
|text | Holds a string with a maximum length of 65,535 characters |
|blob | For BLOBs (Binary Large OBjects). Holds up to 65,535 bytes of data |
|mediumtext | Holds a string with a maximum length of 16,777,215 characters |
|mediumblob | For BLOBs (Binary Large OBjects). Holds up to 16,777,215 bytes of data |
|longtext | Holds a string with a maximum length of 4,294,967,295 characters |
|longblob | For BLOBs (Binary Large OBjects). Holds up to 4,294,967,295 bytes of data |
|enum(x,y,z,etc.) | Let you enter a list of possible values. You can list up to 65535 values in an ENUM list. If a value is inserted that is not in the list, a blank value will be inserted. `Note`: The values are sorted in the order you enter them.You enter the possible values in this format: ENUM('X','Y','Z') |
|set | Similar to ENUM except that SET may contain up to 64 list items and can store more than one choice |


> Number data types

| Data type | Description |
|------- | ------- |
| tinyint(size) | -128 to 127 normal. 0 to 255 UNSIGNED*. The maximum number of digits may be specified in parenthesis |
| smallint(size) | -32768 to 32767 normal. 0 to 65535 UNSIGNED*. The maximum number of digits may be specified in parenthesis |
| mediumint(size) | -8388608 to 8388607 normal. 0 to 16777215 UNSIGNED*. The maximum number of digits may be specified in parenthesis |
| int(size) | -2147483648 to 2147483647 normal. 0 to 4294967295 UNSIGNED*. The maximum number of digits may be specified in parenthesis |
| bigint(size) | -9223372036854775808 to 9223372036854775807 normal. 0 to 18446744073709551615 UNSIGNED*. The maximum number of digits may be specified in parenthesis |
| float(size,d) | A small number with a floating decimal point. The maximum number of digits may be specified in the size parameter. The maximum number of digits to the right of the decimal point is specified in the d parameter |
| double(size,d) | A large number with a floating decimal point. The maximum number of digits may be specified in the size parameter. The maximum number of digits to the right of the decimal point is specified in the d parameter |
| decimal(size,d) | A DOUBLE stored as a string , allowing for a fixed decimal point. The maximum number of digits may be specified in the size parameter. The maximum number of digits to the right of the decimal point is specified in the d parameter |

> Date data types

| Data type | Description |
|------- | ------- |
| date() | A date. Format: YYYY-MM-DD. Note: The supported range is from '1000-01-01' to '9999-12-31' |
| datetime() | *A date and time combination. Format: YYYY-MM-DD HH:MI:SS. Note: The supported range is from '1000-01-01 00:00:00' to '9999-12-31 23:59:59' |
| timestamp() | *A timestamp. TIMESTAMP values are stored as the number of seconds since the Unix epoch ('1970-01-01 00:00:00' UTC). Format: YYYY-MM-DD HH:MI:SS. Note: The supported range is from '1970-01-01 00:00:01' UTC to '2038-01-09 03:14:07' UTC |
| time() | A time. Format: HH:MI:SS. Note: The supported range is from '-838:59:59' to '838:59:59' |
| year() | A year in two-digit or four-digit format.. Note: Values allowed in four-digit format: 1901 to 2155. Values allowed in two-digit format: 70 to 69, representing years from 1970 to 2069 |