# NoonSori

## 프로젝트 개요

저희 서비스는 폐쇄형 자막을 제공해주는 배리어프리 자막 서비스입니다. **폐쇄형자막**은 웃음소리, 천둥소리 등 비언어 소리를 자막으로 표시합니다. 이런 폐쇄형 자막이 장애인들에게 필요하지만, 시간과 자원이 많이 필요해 제공하지 않는 경우가 대부분입니다. 

폐쇄형 자막은 장애인 뿐만 아니라 비장애인들도 선호하는데요. 놓치는 것 없이 볼 수 있고 외출 시 이어폰을 들고 나오지 않았을 경우 등 상황에 제약받지 않고 컨텐츠를 즐길 수 있는 장점이 있기 때문입니다. 현재는 폐쇄형 자막 중 비언어적 소리 역시 사람이 입력하여 시간이 오래 걸리는 문제점이 있기 때문에 저희 서비스는 AI를 이용한 자동화로 빠르게 폐쇄형자막을 제공하고자 합니다.



## 프로젝트 아키텍쳐

![image](https://user-images.githubusercontent.com/66551410/171229067-4a5bbd76-e863-4fd2-bb2a-b37e5de55801.png)



## 프로젝트 기술 스택

|                           Frontend                           |                        Backend (API)                         |                         Backend (AI)                         |
| :----------------------------------------------------------: | :----------------------------------------------------------: | :----------------------------------------------------------: |
| ![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white) ![React](https://img.shields.io/badge/React-61DAFB?style=flat-square&logo=react&logoColor=white) ![React Query](https://img.shields.io/badge/React%20Query-FF4154?style=flat-square&logo=react-query&logoColor=white) ![Heroku](https://img.shields.io/badge/Heroku-430098?style=flat-square&logo=heroku&logoColor=white) | ![Nestjs](https://img.shields.io/badge/nestjs-white?style=flat-square&logo=nestjs&color=E0234E) ![GoogleCloud](https://img.shields.io/badge/GoogleCloud-4285F4?style=flat-square&logo=GoogleCloud&logoColor=white) ![AWS](https://img.shields.io/badge/AWS-232F3E?style=flat&logo=amazon-aws&logoColor=white)  ![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=Docker&logoColor=white) ![MySQL](https://img.shields.io/badge/MySQL-4479A1?style=flat-square&logo=MySQL&logoColor=white)  ![MySQL](https://img.shields.io/badge/Redis-DC382D?style=flat-square&logo=redis&logoColor=white)![Sentry](https://img.shields.io/badge/Sentry-362D59?style=flat-square&logo=Sentry&logoColor=white) | ![AWS Lambda](https://img.shields.io/badge/Lambda-white?style=flat-square&logo=amazon-aws&color=FF9900)![AWS Lambda](https://img.shields.io/badge/TensorFlow-white?style=flat-square&logo=tensorflow&color=FF6F00&logoColor=white) |



# Frontend

## 주요기능

<table>
  <tr>
    <td><img width="600" src="https://user-images.githubusercontent.com/66551410/171189936-bd7e1895-7580-4bb1-940b-d582ff1fecc8.png"></td>
    <td><img width="600" src="https://user-images.githubusercontent.com/66551410/171190634-f70327c7-9235-4938-b1c4-17794722d760.png"></td>
  </tr>
  <tr>
    <td align="center"><b>로그인</b></td>
    <td align="center"><b>회원가입</b></td>
  </tr>
</table>
<table>
  <tr>
    <td><img width="600" src="https://user-images.githubusercontent.com/66551410/171226195-a015e47b-f943-43e6-840a-1717862a1b3d.png"></td>
    <td><img width="600" src="https://user-images.githubusercontent.com/66551410/171229868-6518b812-a950-40cb-9fc1-5adbb8dabf10.png"></td>
  </tr>
  <tr>
    <td align="center"><b>동영상 업로드</b></td>
    <td align="center"><b>자막 변환</b></td>
  </tr>
</table>

<table>
  <tr>
    <td><img width="600" src="https://user-images.githubusercontent.com/66551410/171225904-1d1dc09b-b683-4e2a-afdf-73ce47ebd4b3.png"></td>
    <td><img width="600" src="https://user-images.githubusercontent.com/66551410/171226035-d79b8b61-abca-4b5c-a026-55d8bf0668a2.png"></td>
  </tr>
  <tr>
    <td align="center"><b>마이페이지</b></td>
    <td align="center"><b>프로젝트 설명</b></td>
  </tr>
</table>




# Backend (API)

## 사용한 기술

- Google OAuth2.0

- Kakao OAuth2.0 

- Passport.js, JWT

- Redis PUB/SUB  

- CloudWatch

- Sentry / Slack  


## 배포 서버
https://sowooju.herokuapp.com/
- 테스트 이메일 : `test@test.com`
- 테스트 비밀번호 : `test`
  

## 개발 서버

https://api.so-woo-ju.com/api/v1



## API 문서

https://api.so-woo-ju.com/api/v1/docs



## 

`node: 14.16.0`  
`npm: 6.14.11`

### 1. Cloning

```
$ git https://github.com/So-Woo-Ju/sowooju-api-server.git
$ cd sowooju-api-server
$ npm install
```

### 2. Setting dotenv at Root Directory

```
DB_HOST=<DB_HOST>
DB_PORT=<DB_PORT>
DB_USERNAME=<DB_USERNAME>
DB_PASSWORD=<DB_PASSWORD>
DB_NAME=<DB_NAME>
PORT=<PORT>
GMAIL_USER=<GMAIL_USER>
GMAIL_PASS=<GMAIL_PASS>
JWT_SECRET_KEY=<JWT_SECRET_KEY>
GOOGLE_CLIENT_ID=<GOOGLE_CLIENT_ID>
GOOGLE_SECRET=<GOOGLE_SECRET>
KAKAO_KEY=<KAKAO_KEY>
WEB_HOOK=<WEB_HOOK>
AWS_ACCESS_KEY_ID=<AWS_ACCESS_KEY_ID>
AWS_SECRET_ACCESS_KEY=<AWS_SECRET_ACCESS_KEY>
VIDEO_S3_BUCKET_NAME=<VIDEO_S3_BUCKET_NAME>
```

### 3. Run the MySQL with Docker

```
$ docker-compose -f "docker-compose.yml" up -d --build                                   
```

### 4. Start Local Server

```
$ npm run start             
```



## 아키텍쳐

### 서버 아키텍쳐

![Untitled (1)](https://user-images.githubusercontent.com/66551410/171187998-d7af0312-55ea-47e4-9f85-9b9bf798aa04.png)



### CICD 아키텍쳐

![image](https://user-images.githubusercontent.com/66551410/152016992-cff6b052-35d7-416e-868c-b2702a3ef692.png)



### MySQL ERD


![image](https://user-images.githubusercontent.com/66551410/171187448-8a9ec925-6200-4eec-8ba3-40f8b4e692c5.png)


# Backend (AI)

## 사용한 기술

- MFCC
- YAMNet
- AWS Lambda


## Contributors

|                 주효정                 |                  김소미                  |                    박소현                    |               호선우                |
| :------------------------------------: | :--------------------------------------: | :------------------------------------------: | :------------------------------------: |
| [@jhj2713](https://github.com/jhj2713) | [@somii009](https://github.com/somii009) | [@Sohyun-Dev](https://github.com/Sohyun-Dev) | [@hocaron](https://github.com/hocaron) |
|               React, AI                |               Backend, AI                |                 Backend, AI                  |              Backend, AI               |



