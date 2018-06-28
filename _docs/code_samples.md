---
title: Code samples
permalink: /docs/code_samples/
---

Examples of code in the same order as documentation.
<br>Templates and code bellow.

#### Registration

* cURL template
```
curl -H "Content-Type:application/json" -d '{"username":"", "password":"", "name":"", "surname":"", "email":"", "age":}' -X POST http://51.38.129.50:8085/api/v1/registration
```

* Complete request
```
curl -H "Content-Type:application/json" -d '{"username":"testSpotMaker", "password":"testPassword", "name":"Jan", "surname":"Kowalski", "email":"karol.meksula@onet.pl", "age":25}' -X POST http://51.38.129.50:8085/api/v1/registration
```

#### Email verification

* cURL template
```
curl -H "Content-Type:application/json" -d '{"spotMakerId" : "", "verificationCode" : ""}' -X POST http://51.38.129.50:8085/api/v1/verification
```

#### Spot creation

* cURL template
```
curl --user username:password -H "Content-Type:application/json" -d '{"name":"", "description":"", "searchEnable":true, "city":"", "street":"", "buildingNumber":""}' -X POST http://51.38.129.50:8085/api/v1/spot
```

* Complete request
```
curl --user username:password -H "Content-Type:application/json" -d '{"name":"Muzeum Lubelskie w Lublinie", "description":"Muzeum w Lublinie, należy do najstarszych i największych muzeów we wschodniej Polsce. Ma cztery oddziały na terenie Lublina i pięć zamiejscowych. Główna siedziba muzeum i większość jego oddziałów to wysokiej klasy zabytki.", "searchEnable":true, "city":"Lublin", "street":"Zamkowa", "buildingNumber":"9"}' -X POST http://51.38.129.50:8085/api/v1/spot
```

#### Picture upload

<i>In this case is better to use Postman, because request is more complicated than other.</i>

* cURL fake example
```
curl -X POST \
  http://51.38.129.50:8085/api/v1/spot/picture/5b36919c918b3e7f85b0f6ff \
  -H 'Authorization: Basic a2Fyb2xhZG1pbjo1MTI5MTE5ODY=' \
  -H 'Cache-Control: no-cache' \
  -H 'Postman-Token: 8a615e02-bfab-4fc8-8f53-93996bf1c438' \
  -H 'content-type: multipart/form-data; boundary=----WebKitFormBoundary7MA4YWxkTrZu0gW' \
  -F file=@/home/.../.../....jpg
```

#### Explorer personalization

* cURL template 
```
curl --user PROXY_CLIENT_3d2dc3df22:PROXY_CLIENT_3d2dc3df22 -H "Content-Type:application/json" -d '{"explorerId":"", "nickname":"", "email":"", "name":"", "surname":""}' -X PUT http://localhost:8085/api/v1/explorer/personalization
```

* Complete request
```
curl --user PROXY_CLIENT_3d2dc3df22:PROXY_CLIENT_3d2dc3df22 -H "Content-Type:application/json" -d '{"explorerId":"admin", "nickname":"karoladmin", "email":"karol.meksula@onet.pl", "name":"Jan", "surname":"Nowak"}' -X PUT http://localhost:8085/api/v1/explorer/personalization
```

#### Find Spot nearest/city/district
<i>In URL replace value: `nearest`, `city`, `district`</i>

* cURL template
```
curl --user PROXY_CLIENT_3d2dc3df22:PROXY_CLIENT_3d2dc3df22 -H "Content-Type:application/json" -d '{"lat":, "lng":}' -X POST http://51.38.129.50:8085/api/v1/spot/exploration/nearest
```

* Complete request
```
curl --user PROXY_CLIENT_3d2dc3df22:PROXY_CLIENT_3d2dc3df22 -H "Content-Type:application/json" -d '{"lat":51.236375, "lng":22.595732}' -X POST http://51.38.129.50:8085/api/v1/spot/exploration/nearest
```
