
```sql
select @@tx_isolation
set [ global | session ] transaction isolation level Read uncommitted | Read committed | Repeatable | Serializable;
如果选择global，意思是此语句将应用于之后的所有session，而当前已经存在的session不受影响。
如果选择session，意思是此语句将应用于当前session内之后的所有事务。

begin;  
sql;
commit work;
```