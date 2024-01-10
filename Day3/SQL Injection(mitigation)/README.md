<h3>SQL인젝션에 대응하기 위한 방법</h3>
1. 쿼리에 별도로 해석이 필요한 부분을 존재하지 않도록 없앤다.<br>
2. 쿼리를 해석 없이 하나의 독립된 존재로써 다룬다.<br>
<hr>
정적 쿼리<br>
파라미터화된 쿼리<br>
저장 프로시저<br>
order by 절<br>
<hr>
이렇게 오름차순으로 정렬이 가능하다는 건 order by 절을 사용했을 수도 있겠다고 추측할 수 있음 -> order by절에 sql injection을 시도 할 수 있지 않을까?<br>

![image](https://github.com/Bottomdeal/WebGoat/assets/120577570/42fa173c-2fee-4664-ac81-9df6a47facfa)
<hr>
오름차순으로 정렬할 때마다 burp suite에 전송되는걸 확인<br>

![image](https://github.com/Bottomdeal/WebGoat/assets/120577570/a6e90874-18b0-4a21-b819-d180ff763a5b)
<hr>
리피터에서 ip부분을 수정함<br>

![image](https://github.com/Bottomdeal/WebGoat/assets/120577570/4663d5c7-3f16-4ed0-8831-f623f20ec370)
<br>
조건이 맞을때 오름차순으로 정렬되는데, 사진을 보니 order by절이 실제로 적용되고 있다는 걸 알 수 있음<br>

![image](https://github.com/Bottomdeal/WebGoat/assets/120577570/0aad8f47-ae61-49ff-9c8b-9e13ce951367)
<hr>
webgoat-prd라는 요소에서 두번째 str이 0인가 ? -> 참<br>

![image](https://github.com/Bottomdeal/WebGoat/assets/120577570/896add41-29b8-4934-9fb2-7b6c68384f62)
<br>
![image](https://github.com/Bottomdeal/WebGoat/assets/120577570/55179934-cdff-44f5-a065-9249da4854eb)
<hr>
이렇게 세 자리를 구해서 답을 찾음<br>

![image](https://github.com/Bottomdeal/WebGoat/assets/120577570/49c23c02-7385-4bf7-93fa-e41898a3f1fe)





