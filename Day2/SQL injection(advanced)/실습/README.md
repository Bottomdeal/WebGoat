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
![image](https://github.com/Bottomdeal/WebGoat/assets/120577570/6d4f045b-2e95-46ef-a41f-43749b3c9eb9)<hr>
REGISTER에서 아이디를 만든 후 동일한 아이디를 입력했을때 나오는 메시지<br>
이미 아이디가 존재하는지 아닌지를 확인할 수 있다는 건 어딘가에 SELECT문이 숨어있다는 뜻<br>
![image](https://github.com/Bottomdeal/WebGoat/assets/120577570/95664ece-744b-495a-9d5c-668bd951dde0)<hr>
SQL 인젝션은 실패<br>
![image](https://github.com/Bottomdeal/WebGoat/assets/120577570/2e13f72d-8b3f-4dd0-be80-d84ed394a003)<hr>
BLIND 인젝션을 시도<br>
![image](https://github.com/Bottomdeal/WebGoat/assets/120577570/c1748c08-f411-484e-93f4-bb07ed9fe2bf)<br>
이 반응이 방어 기재로서의 내보내는 말인지 아닌지를 알 수 없음 -> 거짓 조건을 넣어 반응을 살펴봄<br>
![image](https://github.com/Bottomdeal/WebGoat/assets/120577570/b966d85a-d48e-4a78-9628-fe32e5769581)<br>
계정이 생성된 것을 보아 블라인드 SQL 인젝션의 거짓 반응에 해당한다고 생각할 수 있음<hr>
참일 때는 계정이 중복되었다, 거짓일 때는 계정이 생성되었다 라고 반응한다고 생각하고 접근<br>
![image](https://github.com/Bottomdeal/WebGoat/assets/120577570/f1787d33-3f57-47ea-b9bd-9ac7e8a7f818)<br>
참에 대한 반응<hr>
ctrl + shift + c 를 눌러 개발자 모드에서 attribute에 대한 힌트를 찾아보기<br>
![image](https://github.com/Bottomdeal/WebGoat/assets/120577570/0a683606-76b8-4a6d-89a2-c436fcf2a050)<hr>
userid라는 attribute 명이 테이블에 존재한다는 것을 유추<br>
![image](https://github.com/Bottomdeal/WebGoat/assets/120577570/8f7332cf-172a-41e7-9449-321e31b05e4d)<hr>
tom의 패스워드가 23 자리니? -> 참인 반응<br>
![image](https://github.com/Bottomdeal/WebGoat/assets/120577570/f7a1ff7a-6dff-4e64-8536-586971d3ed4e)<hr>
첫 번째 글자가 a니 -> 거짓 . 이렇게 모든 경우의 수를 다 넣으면서 해야 함<br>
![image](https://github.com/Bottomdeal/WebGoat/assets/120577570/2a8705bc-59be-4a76-8989-6f6541462a10)<hr>
경우의 수가 너무 많으므로 자동화의 힘을 빌려서 해결 해 보자<hr>

















