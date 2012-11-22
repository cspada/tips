Manage databases
================

### Create database

    mysql> create database db_name


### Drop database

    mysql> drop database db_name


Manage Users
============

### List current users

    mysql> use mysql;
    mysql> select user, host, grant_priv from user;

### Create a new super user

    mysql> GRANT ALL PRIVILEGES ON *.* TO 'user_name'@'localhost' IDENTIFIED BY 'passwd' WITH GRANT OPTION;


### Add a new user without privileges

    mysql> GRANT USAGE ON *.* TO 'user_name'@'localhost';


### Add/Revoke privileges to a user on a specific database

    mysql> GRANT ALL PRIVILEGES ON database_name.* TO 'user_name'@host_name;

    mysql> REVOKE ALL PRIVILEGES ON database_name.* TO 'user_name'@host_name;


### Drop user

    mysql> DROP USER 'user_name'@'host_name';


### Change user password

    mysql> SET PASSWORD FOR 'user_name'@'host_name' = PASSWORD('new_passwd');



Backup/restore
==============

### Backup DB

    shell> mysqldump --databases db1 db2 db3 > dump.sql


### Restore DB

    shell> mysql datababe < dump.sql


Client connection
=================

### Connect with different user name

    shell> mysql -u user_name [database]

### Connect easily to client

Create a `.my.cnf` file in your home directory with the following content:

    [client]
    password=your_passwd


Useful functions
================

### Change current DB

    mysql> use db_name;

### Show all tables in current DB

    mysql> show tables;

### Describe a table 

    mysql> desc table_name;


