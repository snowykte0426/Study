# Redux

> redux는 react의 상태 관리 라이브러리이다.

외부 라이브러리이기 때문에 별도의 설치가 필요하다.

```shell
npm install redux @reduxjs/toolkit react-redux
```

---

## 개념

1. 상태 관리

   react의 경우 상태 관리를 위해 state를 사용한다. 하지만 이 state는 component 내에서 관리되기 때문에 여러 component에서 동일한 상태를 관리해야 하는 경우 이는 상태를 전달하기 위해 중간 component들을 계속 거쳐야 하는 props drilling 이슈가 생길 수 있다. 또한 component가 많아질수록 상태 관리가 복잡해지고 유지보수가 어려워진다.

   redux를 사용하면 store를 통해 어떤 component에서든 상태에 직접 접근할 수 있어 이러한 문제를 해결할 수 있다. 즉, 상태 관리를 component 외부에서 하는 것이다.

2. 요소

   1. store

      Store는 component와 별개로 state를 저장하는 전역 상태 저장소이다. 이 store에 app에서 필요한 state를 저장하고, 필요한 component에서 이 state를 쉽게 불러올 수 있다.

   2. action

      Action은 app에서 store로 운반되는 data이며, JS 객체 형식으로 되어있다.

   3. reducer

      Reducer는 action을 받아 store에 저장된 state를 변경하는 함수이다. `dispatch()` method를 통해 action을 reducer에 전달할 수 있다.

---