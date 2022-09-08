***SQL 对象模式 被锁的查询和解锁***
---
***查询锁表的Session ***
```sql
select sess.sid,
    sess.serial#,
    lo.oracle_username,
    lo.os_user_name,
    ao.object_name,
    lo.locked_mode
    from v$locked_object lo,
    dba_objects ao,
    v$session sess
where ao.object_id = lo.object_id and lo.session_id = sess.sid;
```
---
```
--杀死进程                 'sid,serial#'
alter system kill session '470,12791'; 
```

***查询DDL 操作被锁***
```sql
select b.SID,b.SERIAL#,a.name
From dba_ddl_locks a,v$session b Where a.session_id = b.SID
and a.name = 'PKG_EQU_MARGIN_VALUE';
--杀死进程                 'sid,serial#'
alter system kill session '632,53'; 
```
