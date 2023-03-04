# next-connect in Next.js
* Next.js API route 기능을 보다 직관적으로 사용하기 위한 모듈 (라우팅, 미들웨어 구현에 사용)

## Common errors
1. 동일한 인스턴스를 재사용하지 말 것
```js
// middleware/common
export default nc().use(a).use(b);

// api/foo
import Handler from "middleware/common";
export default Handler.get(x);

// api/bar
import Handler from "middleware/common";
export default Handler.get(y);
```

위 코드를 사용하지 않는 이유는 각각의 API route에서 동일한 NextConnect 인스턴스가 변형이 되어 undefined behavior를 발생시킨다. 

그렇기 때문에, 동일한 인스턴스를 재사용하지 않도록 한다. 아래와 같이 factory function을 활용 가능하다. 

```js
// middleware/common
export default function base() {
  return nc().use(a).use(b);
}

// api/foo
import base from "middleware/common";
export default base().get(x);

// api/bar
import base from "middleware/common";
export default base().get(y);
```


## Reference
https://www.npmjs.com/package/next-connect