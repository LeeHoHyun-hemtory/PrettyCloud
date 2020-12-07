# Pretty & Handsome

---

## 프로젝트 소개

다양한 라이프공간을 예약할 수 있는 서비스 사이트인 Space Cloud를 클론 프로젝트

<br>

## 개발 인원 및 기간

### 기간: 2020.08.30 - 2020.09.11 (약 2주)
### 개발 인원: 
#### 프론트엔드 - 김영지, 박진아, 조윤민, 조은별 
#### 백엔드 - 이용민(PM) 이호현

<br>

### 데모 영상

[https://www.youtube.com/watch?v=2wgGwFHDjRU&feature=youtu.be](https://www.youtube.com/watch?v=2wgGwFHDjRU&feature=youtu.be)

<br>

## 사용 기술

<br>

### 공통

1) HTTP

2) Git

3) VScode

4) Trello

프로젝트 스크럼 툴 (링크)
5) PostMan

API 테스트 및 결과 내용 공유

<br>

### 프론트엔드

1) React.js

react-router-dom : 브라우저에서 사용되는 리액트 라우터
node-sass : Sass(.scss) 파일을 css 파일로 컴파일
styled-Component : js 파일 하나로 Component 스타일을 동시에 작성

2) SCSS

SASS의 모든 기능을 지원하면서 CSS 구문과 완전히 호환됨

<br>

### 백엔드

1) Node.js

express : Node.js용 웹서버 개발 프레임워크
bcrypt : 회원가입 패스워드 단방향 hash로 암호화
sequelize : Raw-Query가 아닌 method를 이용할 수 있는 ORM 라이브러리
dotenv : 서버 개발에 필요한 환경변수를 파일로 분리해 관리
jsonwebtoken : 로그인할 때 필요한 토큰 발행
mysql2 : MySQL과 sequelize를 이어주는 드라이버

2) MySQL

DB 구축 및 데이터 업로더 제작

<br>

## 담당 작업 내용

<br>

###Back-End
#### DB Modeling

- DataBase Schema 작성

#### DB ORM

- DB 테이블을 객체로 관리하기 위해 코드 작성

#### EndPoint

- Router를 이용해 만들어질 API의 경로 설정

#### 회원가입 API

- 가입 시 DB에 등록되어있는 e-mail이면 에러 response 보냄
- 가입 완료 시 password를 bcrypt 암호화 해서 저장

#### 로그인 API

- request에 담긴 password 정보를 DB내용과 bcrypt의 compare method로 비교
- 로그인 시 DB 정보와 불일치하면 에러 response 보냄
- 로그인 성공 시 jsonwebtoken으로 토큰 발행해서 response 보냄

#### 예약리스트 추가 API

- Front-End에서 보낸 토큰 확인 후 정상이면 DB에 추가
- MyPage에서 예약내용 확인할 수 있게 조회
