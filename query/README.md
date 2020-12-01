
### 오라클

# 0. 히스토리
```
  SELECT 
  last_active_time
  ,parsing_schema_name
  ,sql_text 
FROM v$sqlarea
WHERE 
  parsing_schema_name <> 'SYS'
  AND parsing_schema_name <> 'SYSMAN'
  AND parsing_schema_name <> 'DBSNMP'
  AND parsing_schema_name <> 'MDSYS'
  AND parsing_schema_name <> 'EXFSYS'
ORDER BY 
  last_active_time DESC;
```

# 1. 출력개수
```
mssql
select TOP 10

oracle
select ... where rownum <= n;
```
