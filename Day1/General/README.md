http 메시지에서 url에 파라미터를 실어서 보내는 건 GET

body부분에 실어서 보내는 건 POST

프록시 서버 사용해서 WebGoat 접속

기존에는 웹브라우저와(client) WebGoat(server)가 직접 http메시지를 주고받지만,
프록시 서버를 사용하면 client와 server 중간에서 http메시지를 전달한다.

POST 방식
![image](https://github.com/Bottomdeal/WebGoat/assets/120577570/b580ad8a-8454-489a-b0e2-e11f95d6ac73)

MAGIC NUM = 79를 확인

![image](https://github.com/Bottomdeal/WebGoat/assets/120577570/3b5e8f68-9f67-4ccd-89a2-2038a71b14c0)

POST와 79를 입력하면 성공

![image](https://github.com/Bottomdeal/WebGoat/assets/120577570/42607c46-1254-494e-b332-a14da971c118)

USE THE INTERCEPT

파라미터가 존재하는 것만 골라내기

![image](https://github.com/Bottomdeal/WebGoat/assets/120577570/d746f16a-4ac4-49c9-b275-92165f3bec35)

인터셉트에서 post를 get으로, changeme를 변경

![image](https://github.com/Bottomdeal/WebGoat/assets/120577570/9bfa2f46-fdf8-43bd-aad8-9958f3f19506)

get은 url에 포함되어야 하기 때문에, 이렇게 수정

![image](https://github.com/Bottomdeal/WebGoat/assets/120577570/5c4cbac2-5460-41b4-bb84-f525a97f17a1)

성공

![image](https://github.com/Bottomdeal/WebGoat/assets/120577570/ad9ba4e6-d3d5-46cb-ade5-eb0be4f48c24)
