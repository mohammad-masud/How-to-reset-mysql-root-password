reset mysql pass

run: sudo mysql -u root


Welcome to the MySQL monitor.  Commands end with ; or \g.
Your MySQL connection id is 2
Server version: 5.7.26-0ubuntu0.18.04.1 (Ubuntu)

Copyright (c) 2000, 2019, Oracle and/or its affiliates. All rights reserved.

Oracle is a registered trademark of Oracle Corporation and/or its
affiliates. Other names may be trademarks of their respective
owners.

Type 'help;' or '\h' for help. Type '\c' to clear the current input statement.


run:  mysql> use mysql;


Reading table information for completion of table and column names
You can turn off this feature to get a quicker startup with -A

Database changed

run:  mysql> update user set authentication_string=PASSWORD('masud270') where user='root';

Query OK, 1 row affected, 1 warning (0.04 sec)
Rows matched: 1  Changed: 1  Warnings: 1

mysql> update user set plugin='mysql_native_password' where user='root';
Query OK, 1 row affected (0.01 sec)
Rows matched: 1  Changed: 1  Warnings: 0

mysql> flush privileges;
Query OK, 0 rows affected (0.00 sec)

mysql> exit
Bye
