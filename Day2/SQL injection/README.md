<h3>SQL의 정의</h3>

SQL은 데이터베이스와 상호작용하기 위해 사용되는 컴퓨터 언어이며, 데이터베이스에 의해서 해석될 수 있다.<hr>
SQL - Structured Query Language(구조화 질의 언어)<br>
1.표준화되지 않은 질의 언어<br>
2.다양한 버전의 SQL존재. 대부분의 DB는 자체 맞춤형 기능 보유<br>
3.대부분의 제조사는 독점적인 확장 기능을 제공<hr>
DML - 데이터 조작어(SELECT, INSERT, UPDATE, DELETE, etc. )<br>
DML - 데이터베이스에 저장되는 데이터와 관련된 언어, 주로 사용됨<br>
DDL - 데이터베이스 구조와 관련된 언어<br>
DCL - DBMS(Database Management System) 제어와 관련된 언어<hr>
SQL로 만든 문장은 "쿼리" 혹은 "쿼리문"으로 부름<hr>

<h3>SQL 인젝션이란?</h3>

클라이언트에서 SQL 쿼리를 통해 악의적인 데이터를 웹 애플리케이션에 주입하는 공격이다.<hr>
데이터베이스의 민감 데이터를 열람 및 수정<br>
데이터베이스에서 관리 작업을 수행<br>
파일시스템 상에서 특정 파일의 내용을 발견<hr>

<h3>SQL 인젝션의 결과</h3>

신분 위장<br>
데이터 변조<br>
무료 거래나 잔액 변경 같은 부인 문제 발생<br>
시스템 내 데이터의 완전 공개<br>
데이터를 파괴하거나 사용할 수 없게 함<br>
데이터베이스 서버에서 관리자로 행세<hr>
문자형 인젝션의 위협이 존재하는 쿼리<br>
"select * from users where name = '" + userName + "'";<hr>
숫자형 인젝션의 위협이 존재하는 쿼리<br>
"select * from users where employee_id = " + userID;<hr>

