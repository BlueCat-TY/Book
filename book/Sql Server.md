## Sql Server 常用语句

#### 1. 同步表数据
```sql
update t1 set id = t2.id , t1.name = t2.name , ... from t1 inner join t2 on t1.id = t2.id
```

#### 2. 表备份
```sql
select * into table_back from table  
```
#### 3. Sql事务
```sql
create proc sp_存储过程名
as
    begin tran
    begin try
        select 语句
        commit tran
    end try
    begin catch
        rollback tran
    end catch
go
```  
#### 4. SQL数据库 if...else
```sql
create proc sp_存储过程名
  var 变量名  类型
as
    if 变量名 = 值
    begin
        select 语句
    end
    else
    begin
        select 语句
    end
go
```
#### 5. Sql Server 分页
```sql
create proc sp_存储过程名
as
    declare @pageindex,  --页码
    declare @pagesize    --页大小  

    --执行查询语句
    select * from(
        select
            name1,
            name2,
            ROW_NUMBER() over(order by orderName desc) as rowsid
        from Table
    ) tmp
    where rowsid between @pagesize * (@pageindex - 1) + 1 and @pagesize * @pageindex
go
```
#### 6. Sql Server 向上取整  
```sql
--必须有一个字段是小数
declare  @number float = 25.0
declare @size int = 10

-->floor() 保留整数
@jiguo = floor(@number / @size)
@jieguo=2

--ceiling() 四舍五入取整数
@jiguo = ceiling(@number / @size)
@jieguo=3

```

#### 7. Sql Server 取出自增列最大ID
```sql
select ident_current('表名') as 自定义别名
```
