
Setting environment for using XAMPP for Windows.
karan@PRAVEEN c:\xampp
# mysql.exe -u root
Welcome to the MariaDB monitor.  Commands end with ; or \g.
Your MariaDB connection id is 10
Server version: 10.4.25-MariaDB mariadb.org binary distribution

Copyright (c) 2000, 2018, Oracle, MariaDB Corporation Ab and others.

Type 'help;' or '\h' for help. Type '\c' to clear the current input statement.

MariaDB [(none)]> show databases;
+--------------------+
| Database           |
+--------------------+
| information_schema |
| mysql              |
| nari               |
| performance_schema |
| phpmyadmin         |
| prav               |
| praveen            |
| test               |
+--------------------+
8 rows in set (0.001 sec)

MariaDB [(none)]> use praveen;
Database changed
MariaDB [praveen]> create table employee(empid int(11),name varchar(9),phno int(11));
Query OK, 0 rows affected (0.025 sec)

MariaDB [praveen]> desc employee;
+-------+------------+------+-----+---------+-------+
| Field | Type       | Null | Key | Default | Extra |
+-------+------------+------+-----+---------+-------+
| empid | int(11)    | YES  |     | NULL    |       |
| name  | varchar(9) | YES  |     | NULL    |       |
| phno  | int(11)    | YES  |     | NULL    |       |
+-------+------------+------+-----+---------+-------+
3 rows in set (0.011 sec)

MariaDB [praveen]> alter table employee add(salary int(11));
Query OK, 0 rows affected (0.012 sec)
Records: 0  Duplicates: 0  Warnings: 0

MariaDB [praveen]> desc employee;
+--------+------------+------+-----+---------+-------+
| Field  | Type       | Null | Key | Default | Extra |
+--------+------------+------+-----+---------+-------+
| empid  | int(11)    | YES  |     | NULL    |       |
| name   | varchar(9) | YES  |     | NULL    |       |
| phno   | int(11)    | YES  |     | NULL    |       |
| salary | int(11)    | YES  |     | NULL    |       |
+--------+------------+------+-----+---------+-------+
4 rows in set (0.030 sec)

MariaDB [praveen]> truncate employee;
Query OK, 0 rows affected (0.032 sec)

MariaDB [praveen]> desc employee;
+--------+------------+------+-----+---------+-------+
| Field  | Type       | Null | Key | Default | Extra |
+--------+------------+------+-----+---------+-------+
| empid  | int(11)    | YES  |     | NULL    |       |
| name   | varchar(9) | YES  |     | NULL    |       |
| phno   | int(11)    | YES  |     | NULL    |       |
| salary | int(11)    | YES  |     | NULL    |       |
+--------+------------+------+-----+---------+-------+
4 rows in set (0.011 sec)

MariaDB [praveen]> drop table employee;
Query OK, 0 rows affected (0.057 sec)

MariaDB [praveen]> create table student(stuid int(11),name varchar(9),address varchar(9));
Query OK, 0 rows affected (0.024 sec)

MariaDB [praveen]> desc student;
+---------+------------+------+-----+---------+-------+
| Field   | Type       | Null | Key | Default | Extra |
+---------+------------+------+-----+---------+-------+
| stuid   | int(11)    | YES  |     | NULL    |       |
| name    | varchar(9) | YES  |     | NULL    |       |
| address | varchar(9) | YES  |     | NULL    |       |
+---------+------------+------+-----+---------+-------+
3 rows in set (0.010 sec)

MariaDB [praveen]> insert into student values(01,'nari','andhra'),(02,'praveen','telangana'),(03,'mohan','tamilnadu');
Query OK, 3 rows affected (0.006 sec)
Records: 3  Duplicates: 0  Warnings: 0

MariaDB [praveen]> desc student;
+---------+------------+------+-----+---------+-------+
| Field   | Type       | Null | Key | Default | Extra |
+---------+------------+------+-----+---------+-------+
| stuid   | int(11)    | YES  |     | NULL    |       |
| name    | varchar(9) | YES  |     | NULL    |       |
| address | varchar(9) | YES  |     | NULL    |       |
+---------+------------+------+-----+---------+-------+
3 rows in set (0.013 sec)

MariaDB [praveen]> select * from student;
+-------+---------+-----------+
| stuid | name    | address   |
+-------+---------+-----------+
|     1 | nari    | andhra    |
|     2 | praveen | telangana |
|     3 | mohan   | tamilnadu |
+-------+---------+-----------+
3 rows in set (0.000 sec)

MariaDB [praveen]> select stuid,name from student;
+-------+---------+
| stuid | name    |
+-------+---------+
|     1 | nari    |
|     2 | praveen |
|     3 | mohan   |
+-------+---------+
3 rows in set (0.000 sec)

MariaDB [praveen]> update student set name='leela' where name='mohan';
Query OK, 1 row affected (0.003 sec)
Rows matched: 1  Changed: 1  Warnings: 0

MariaDB [praveen]> select * from student;
+-------+---------+-----------+
| stuid | name    | address   |
+-------+---------+-----------+
|     1 | nari    | andhra    |
|     2 | praveen | telangana |
|     3 | leela   | tamilnadu |
+-------+---------+-----------+
3 rows in set (0.000 sec)


MariaDB [praveen]> delete from student where stuid=01;
Query OK, 1 row affected (0.005 sec)

MariaDB [praveen]> select * from student;
+-------+---------+-----------+
| stuid | name    | address   |
+-------+---------+-----------+
|     2 | praveen | telangana |
|     3 | leela   | tamilnadu |
+-------+---------+-----------+
2 rows in set (0.000 sec)

MariaDB [praveen]>
