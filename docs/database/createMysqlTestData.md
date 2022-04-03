---
layout : default
title : mysql 테스트데이터 생성
parent : 데이터베이스
nav_order : 2
---

## Mysql 테스트/예제 데이터 생성
--- 

1) [Mysql test_db](https://github.com/datacharmer/test_db)에서  Download Zip으로 해당 프로젝트 로컬에 설치


2) 압축 해제 후 해제한 디렉토리 위치에서 cmd 실행


3) mysql 접속
   
```
C:\_DEV_\test_db-master\test_db-master> mysql -u root -p
Enter password: ************
Welcome to the MySQL monitor.  Commands end with ; or \g.
Your MySQL connection id is 35
Server version: 8.0.18 MySQL Community Server - GPL

Copyright (c) 2000, 2019, Oracle and/or its affiliates. All rights reserved.

Oracle is a registered trademark of Oracle Corporation and/or its
affiliates. Other names may be trademarks of their respective
owners.

Type 'help;' or '\h' for help. Type '\c' to clear the current input statement.
```
<br>


4) source 명령어 실행

```
mysql> source employees.sql

Query OK, 1 row affected (0.01 sec)

Database changed
+-----------------------------+
| INFO                        |
+-----------------------------+
| CREATING DATABASE STRUCTURE |
+-----------------------------+
1 row in set (0.00 sec)

Query OK, 0 rows affected, 6 warnings (0.01 sec)

Query OK, 0 rows affected (0.00 sec)

```

<br>

테이블이 제대로 들어갔는지 확인
```
mysql> show tables;
+----------------------+
| Tables_in_employees  |
+----------------------+
| current_dept_emp     |
| departments          |
| dept_emp             |
| dept_emp_latest_date |
| dept_manager         |
| employees            |
| salaries             |
| titles               |
+----------------------+
8 rows in set (0.02 sec)

```
