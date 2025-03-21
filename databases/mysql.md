# Install MYSQL with Docker 
- https://hub.docker.com/_/mysql

``docker run --name some-mysql -e MYSQL_ROOT_PASSWORD=testpwd -d mysql``

# Import data to MySQL
``mysql -u root -P 3308 -h 10.10.13.31 -p < your_sql_file.sql``

# How to using MYSQL

## 1. Tools for Database Management
- [dbeaver](https://dbeaver.io/download/)  recomendation for Linux OS
- [bytebase](https://www.bytebase.com) for DevOps

## Function

1.  Create function with sql command :
```sql
CREATE FUNCTION tools.getNamaTindakanById(
	get_id integer(20)
) 
RETURNS VARCHAR(100)
DETERMINISTIC
BEGIN
    DECLARE this_name VARCHAR(20);
    SET this_name = (select * from master.tindakan where id = get_id LIMIT 1);
	
	RETURN this_name;
END
```

2. delete function : 
```sql
DROP FUNCTION tools.getNamaRuanganById
```

3. Call Function : 
```sql
select tools.getNamaRuanganById(1);
```