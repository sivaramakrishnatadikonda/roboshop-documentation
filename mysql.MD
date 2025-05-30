# MySQL 

Developer has chosen the database MySQL. Hence, we are trying to install it up and configure it.

**Versions of the DB Software you will get context from the developer, Meaning we need to check with developer.**
**Developer has shared the version information as MySQL-8.x**

Install MySQL Server 

```shell 
dnf install mysql-server -y
```

Start MySQL Service 

```shell 
systemctl enable mysqld
systemctl start mysqld  
```

Next, We need to change the default root password in order to start using the database service. Use password **`RoboShop@1`** or any other as per your choice. 

```shell
mysql_secure_installation --set-root-pass RoboShop@1
```
## Verification

We can check data by using client package called mysql.

Usually command to connect mysql server is

```
mysql -h <host-address> -u root -p<password>
```

But if your client and server both are in a single server, you can simply issue.

```
mysql
```

Once you got mysql prompt, you can use below command to check schemas/databases exist.

```
show databases;
```

Once you are in particular schema, you can get the list of tables.

```
show tables;
```

You can get entries of a table using

```
select * from <table_name>;
```
