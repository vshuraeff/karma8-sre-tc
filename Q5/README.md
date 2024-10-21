# 5. Lock timeout 

check `innodb_lock_wait_timeout` value

```sql
SHOW VARIABLES LIKE 'innodb_lock_wait_timeout';
```
скорее всего значение по умолчанию не достаточно для применения транзакции
можно увеличить значение и убедиться что проблема в этом

```sql
SET GLOBAL innodb_lock_wait_timeout = 200;
START SLAVE;
```
если да, то добавить в my.cnf