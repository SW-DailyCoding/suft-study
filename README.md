### 🥐 1~3일차 

2일차와 3일차 수업을 제대로 듣지 않았기 때문에 벨로퍼트 블로그와 더불어서 애들 코드 보니까 react-router-dom (?) 설치가 되어있길래 그거에 대해서 12시부터 공부해본 결과. 수많은 오류들이 나를 반겨주었고 해결 하는데 거의 2시간 걸렸다. 심지어 브랜치 이해도가 낮은 편이라서 전에 팠던 main 브랜치가 왜 master에서 코드가 들어가는지 이해가 안 되었었는데 

```git push origin master```
로 하고 있으니까 메인으로 코드가 안 넘어가서 애 먹고 있었다. 레전드라고 생각한다. 뒤 부분이 브랜치명이라는 걸 까먹었던 모양. 이제 브랜치 파고 하나하나 배울 때마다 추가적으로 넣을 예정이다 그때마다 배운 내용으로 README.md 내용이 달라진다. master는 아마 최종적으로 결과냈을 때 병합하지 않을까싶다.

<br>

심지어 나는 다른 애들이 리액트 깔고 있는 동안 구경하고 있었던게 컸는지 리액트를 안 깔고 있어서 설치하는 법을 적어보도록 하겠다.

## 🎆 create-react-app
~~~
$ npx create-react-app Project Name
~~~

## 🎇 react-router-dom
~~~
$ npm install --save react-router-dom
~~~
아마 설치가 되어있다면 
~~~
  "dependencies": {
    "@testing-library/jest-dom": "^5.11.4",
    "@testing-library/react": "^11.1.0",
    "@testing-library/user-event": "^12.1.10",
    "react": "^17.0.1",
    "react-dom": "^17.0.1",
    "react-router-dom": "^5.2.0",
    "react-scripts": "4.0.0",
    "web-vitals": "^0.2.4"
  },
~~~
에서 `"react-router-dom": "^5.2.0"`가 추가되어 있을 것이다.

## ⛳ 리액트 시작
~~~
$ yarn start
~~~
원래 msg.gg에서는 yarn dev로 했었던 거 같은데 어떻게 했는지 그것도 까먹버린 것이다! `npm start`, `npm run start`도 있다는 사실을 잊지말자!

### 💎 App.js
`import {Link} from 'react-router-dom';`에서 
~~~
 <Link className="App-link" to="/page">
~~~
여기서 

### 💍 index.js
~~~
<Route exact path="/" component={App}/>
<Route exact path="/page" component={Page1}/>
~~~
`exact`가 왜 붙는지 이해가 안 되었는데 이게 만약 붙어있다면 경로에 맞게 떨어져야 컴포넌트가 보여준다는 걸 알았다. 정확히는 `/`도 있고 `/page`도 /가 있기 때문에 정확한 판별이 필요한 모양

## ✨ Page1.jsx
처음에 html 아니면 하나의 문자열 문법인 줄 알았는데 아니다. 자바스크립트 문법이라 한다.
