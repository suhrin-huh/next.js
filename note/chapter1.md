# Next.js를 소개합니다

## 1.1 Next.js를 소개합니다

### Framework와 Library

기능 구현의 주도권이 누구에게 있는가?

- Framework : 주도권을 Framework가 가진다. 프레임워크가 제공하는 기능을 이용하거나 허용하는 범위 내에서만 추가 도구를 사용할 수 있다.
- Library : 주도권을 개발자가 가진다. 기능 구현을 원하는 방향으로 진행한다. 쓰고싶은 도구, 쓰고싶으 기술을 쓴다.

=> Next는 페이지 라우팅 기능을 구현시에 Next.js가 제공하는 라우터를 사용해야한다.

## 1.2 Next.js 사전렌더링 이해하기

### 사전 렌더링(Pre Rendering) - (14분대부터 다시 듣기!)

브라우저의 요청에 사전에 렌더링이 완료된 HTML을 응답하는 렌더링 방식
CSR의 단점을 보완할 수 있다.

- CSR(Client Side Rendering) : 브라우저가 화면 구성에 필요한 모든 요소들을 렌더링한다. 페이지 이동이 매우 빠르고 쾌적하다. 그러나 초기 접속 속도(FCP)가 느려진다.

- 사전 렌더링 : 서버에서 미리 JS를 실행해서 렌더링(React code를 HTML로 변환)한다. 브라우저는 유저에 화면이 렌더링(HTML 코드를 브라우저가 화면에 렌더링)한다.

- 페이지 이동의 경우 클라이언트 사이드 렌더링 방식으로 처리(서버에서 브라우저에 전송하는 파일은 사실상 React Code와 같다.)

## 1.3 실습용 백엔드 서버 세팅하기

### 왜 실습용 서버가 필요한걸까?

실전과 같은 환경을 연습하기 위해 서버를 준비한다.

- supabase로 DB 관리
- .env 파일 "엔브" 라고 읽는다!

- supabase에 연결 후 .env에 환경변수 설정한다.

```bash
npm i

// 만약에 "unknown command"라고 뜬다면
npm install prisma --save-dev
npx prisma generate

npm prisma db push // Generated Prisma Client
```

## 1.4 본격적인 학습에 앞서
