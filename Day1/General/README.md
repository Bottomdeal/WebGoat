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
