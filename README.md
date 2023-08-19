# Zoom 클론코딩
**줌 클론코딩 📽** </br>
**개발기간 : 2023.03.27 ~ 2023.04.02**

## 프로젝트 소개
☑️ JS를 활용해 Zoom 을 클론코딩한다. </br>
☑️ WebSockets, SocketIO, WebRTC에 대해 배운다. </br>
☑️ Only JS 만으로. 채팅방 생성. 화상채팅 그리고 개인 메시지를 구현한다. </br>

## Stacks ⭐
### Environment
![Visual Studio Code](https://img.shields.io/badge/VisualStudioCode-007ACC?style=for-the-badge&logo=VisualStudioCode&logoColor=white)

### Development
![PUG](https://img.shields.io/badge/Pug-A86454?style=for-the-badge&logo=Pug&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=Javascript&logoColor=white)
![Node.js](https://img.shields.io/badge/Node.js-339933?style=for-the-badge&logo=nodedotjs&logoColor=white)
![Socket.io](https://img.shields.io/badge/Socket.io-010101?style=for-the-badge&logo=Socket.io&logoColor=white)
![WebRTC](https://img.shields.io/badge/WebRTC-333333?style=for-the-badge&logo=WebRTC&logoColor=white)


## git connection

```bash
$ mkdir zoom
$ cd zoom
$ npm init -y
$ code .
```

## 환경설정
### package.json 설정
```js
{
  "name": "zoom",
  "version": "1.0.0",
  "description": "Zoom Clone using webRTC and Websockets",
  "license": "MIT"
}
```

### nodemon 설치
```bash
$ npm i nodemon -D
$ npm i @babel/core @babel/cli @babel/node -D
```

### nodemon.json 설정
- src/server.js에 대해 babel-node 명령문을 실행시킨다. 즉, exec는 server.js을 실행시킨다.
```js
{
    "exec":"babel-node src/server.js"
}
```

### babel.config.json 설정
- babel.config.json에서는 "presets"을 설정한다.
```js
{
    "presets":["@babel/preset-env"]
}
```

### preset 설치
```bash
$ npm i @babel/preset -env -D
```

### 의존성 설치
프로젝트 디렉토리에서 다음 명령을 실행하여 필요한 패키지를 설치합니다.
```bash
$ npm install express http socket.io @babel/node @babel/preset-env
```

### paackage.json 설정
- script 추가해준다. 하나는 "div"로 nodemon을 호출하는 기능을 한다. nodemon이 호출되면 nodemon이 nodemon.json을 살펴보고 거기있는 코드들을 실행하게 될 것이다.
```js
{
  "name": "zoom",
  "version": "1.0.0",
  "description": "Zoom Clone using WebRTC and Websockets",
  "license": "MIT",
  "scripts": {
    "dev": "nodemon"
  },
  "devDependencies": {
    "@babel/cli": "^7.21.0",
    "@babel/core": "^7.21.3",
    "@babel/node": "^7.20.7",
    "@babel/preset-env": "^7.20.2",
    "nodeman": "^1.1.2"
  }
}
```

### express, pug 설치
```bash
$ npm i express
$ npm i pug
```

### ws 설치
```bash
$ npm i ws
```

### SocketIO 설치
```bash
$ npm i socket.io
```

### nodemon.json 설정
- views나 서버를 수정할 때만 nodemon이 재시작되도록 설정
```js
{
    "ignore": ["src/public/*"],
    "exec": "babel-node src/server.js"
}
```

### Admin UI 설치
```bash
$ npm i @socket.io/admin-ui
```

## 실행 명령어
```bash
$ npx nodemon nodemon.js
```

## 프로젝트 진행 상황
| 날짜 |     내용      |
| ---- | ------------- |
|2023.03.27 | Server, Fronted 개발환경 설정 |
|2023.03.27~28 | WebSocket 서버 구축 및 닉네임을 사용한 실시간 채팅 프로그램 구현 |
|2023.03.29 | SocketIO 설치 및 실시간 양방향 데이터 전달 주고받기 |
|2023.03.30 | Room 이름 변경 및 메시지 주고받기 |
|2023.03.31 | Room 참가자 닉네임 설정, 생성된 방 목록 출력 |
|2023.03.31 | 사용자 수 확인, AdminUI 사용  |
|2023.04.01 | Video, Audio 버튼 제어 및 카메라 전환 |
|2023.04.01 | WebRTC를 이용한 방입장, 브라우저 연결, offer 전달 |
|2023.04.02 | WebRTC를 이용한 Peer-to-peer 연결 |
|2023.04.02 | Stun Server를 통해 wifi연결 문제 해결 |

## 화면 구성 📺
| 메인 페이지 | Room 입장화면 | Room 입장화면(여러명) |
| :----------------: | :---------------: | :---------------: |
| <img src="/img/메인페이지.png"> | <img src="/img/Room입장화면.png"> | <img src="/img/Room입장화면(여러명).png"> |