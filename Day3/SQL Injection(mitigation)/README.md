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

