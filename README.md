# mysql master-slave-demo

## config

* grant 

```code
GRANT replication slave ON *.* TO'root'@'%' identified by 'root';
```

* flush privaliges

```code

```

* view master info

```code
show master status
```
* config  slave 

```code
change master to master_host='mysql',master_user='root',master_port=3306,master_password='root',master_log_file='mysql-bin.000003',master_log_pos=1027
```

* start slave

```code
start slave
```

* view slave status

```code
show slave status
```

## java mysql binlog connector demo

* build

```code
cd java-binlog
mvn clean package
```

* running

```code
java -jar target/mysql-binglog-app.jar
```