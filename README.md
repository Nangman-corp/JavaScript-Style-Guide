# JavaScript Style Guide

<aside>
💡 본문은 낭만(Nangman)의 JavaScript 스타일 가이드 입니다. 구글 JavaScript 가이드를 참고하여 작성하였습니다.

</aside>

# 1. 소개(Intro)

---

본 문서는 Nangman의 JavaScript 스타일을 설명합니다. 본 문서의 가이드를 이해하신 후 사용하시는 기술 문서로 이동하여 기술에 해당하는 가이드를 숙지하세요!

# 2. 이름(Name)

### 2.1 명명 규칙(Naming rules)

---

1. 단일 글자로 이름을 짓지 않고 이름을 통해 쓰임새를 알 수 있도록 작성합니다.

```
(X)
function q() {
  // ...
}

(O)
function query() {
  // ...
}
```

2. 이름의 맨 앞이나 맨 뒤에 밑줄(_)을 사용하지 않습니다.

```
(X)
this.__firstName__ = 'Panda';
this.firstName_ = 'Panda';
this._firstName = 'Panda';

(O)
this.firstName = 'Panda';
```

3. this를 변수의 값으로 사용하지 않습니다. 필요할 경우 화살표 함수(Arrow Function)이나 바인딩을 통해 사용하십시오.

```
(X)
function foo() {
  const self = this;
  return function () {
    console.log(self);
  };
}

(O)
function bar() {
  return () => {
    console.log(this);
  };
}
```

4. 가독성을 위해 약어는 Camel Case로 표기합니다.

```
(X)
import SMSContainer from './containers/SMSContainer';

(X)
const HTTPRequests = [     
  // ...
];

(O)
import SmsContainer from './containers/SmsContainer';

(O)
const HttpRequests = [
  // ...
];

```

5. 파일을 1개의 클래스로 export 하는 경우 파일명은 클래스명과 완전히 일치시켜주세요.

```jsx
// file contents
class CheckBox {
  // ...
}
export default CheckBox;

// in some other file
(X)
import CheckBox from './checkBox';

(X)
import CheckBox from './check_box';

(O)
import CheckBox from './CheckBox';
```

5-1. export되는 파일 내의 모든 상수는 모두 대문자로 표기하는 것을 권장합니다.

```
(X)
const PRIVATE_VARIABLE = 'should not be unnecessarily uppercased within a file';

(X)
export const THING_TO_BE_CHANGED = 'should obviously not be uppercased';

(X)
export let REASSIGNABLE_VARIABLE = 'do not use let with uppercase variables';

// ---

//허용되지만 sematic 값은 지원하지 않습니다.
export const apiKey = 'SOMEKEY';

// 해당 변수명을 권장합니다.
export const API_KEY = 'SOMEKEY';

// ---

(X) - Map 내에서 key의 naming을 불필요하게 대문자로 하지 마십시오.
export const MAPPING = {
  KEY: 'value'
};

(O)
export const MAPPING = {
  key: 'value'
};
```

5-2. default export가 함수일 경우, camelCase를 사용해주세요. 물론 파일명은 함수명과 동일해야 합니다.

```jsx
(O)
function makeStyleGuide() {
}

export default makeStyleGuide;
```

6. 이름에 복수형을 표기하지 않습니다.

```
(X)
let delivery_notes = ["one", "two"];

(O)
let delivery_note_list = ["one", "two"];
```

7. 줄임말을 사용하지 않습니다.

```
(X)
let del_note = 1;

(O)
let delivery_note = 1;
```

8. private 프로퍼티명은 앞에 언더스코어 `_` 를 사용해주세요.

```jsx
(O)
this._firstName = 'Panda';
```

### 2.2 파일 및 패키지(File and package)

---

1. 파일의 이름은 소문자로 표기합니다.

```css
(X)
LonDon.png
HELLOWORLD.pdf
APP.js

(O)
london.png
helloworld.pdf
app.js
```

2. 패키지의 이름은 lowerCamelCase로 표기합니다.

```
(X)
my.examplecode.deepspace
my.example_code.deep_space

(O)
my.exampleCode.deepSpace
```

3. 파일의 이름은 default export의 이름과 일치해야 합니다.

```jsx
// file 1 contents
class CheckBox {
	//...
}
export CheckBox;

// file 2 contents
export default function helloWrold() { return "Hello World";}

// file 3 contents
export default function insideDirectory() {}

(O)
import CheckBox from './CheckBox';  // import/export/filename 모두 pascal case
import helloWorld from './helloWorld'; // import/export/filename 모두 camel case 
import insideDirectory from './insideDirectory'; //import/export/filename 모두 camel case
```

### 2.3 변수(Variable)

---

1. 변수의 이름은 lowerCamelCase로 표기해주세요.
    
    단,  export 되는 파일 내의 상수는 예외입니다!
    
2. 변수의 이름은 알파벳으로 시작해야합니다.

```jsx
(X)
let 123Number = 123;
let HELLO_WORLD = "Hello World";

(O)
let number = 369;
let helloString = "Hello World";
```

### 2.4 함수(Funtion)

---

1. 함수는 lowerCamelCase로 표기해주세요.

```jsx
(X)
function MyFunction() {...}

(O)
function myFunction() {...}
```

2. 함수의 이름은 동사 또는 동사 구문으로 표기해주세요.

```jsx
(X)
function whereIsCamera() { ... }

(O)
function findCamera() { ... }
function getFoo() { ... } // getter
function setBar() { ... } // setter
function hasCoo() { ... } // booleans
```

3. 함수의 파라미터는 lowerCamelCase로 표기해주세요.
    
    단, 한글자의 파라미터는 public 메소드에서는 사용하지 않습니다.
    

```jsx
(X)
function someFunction(SOMEVALUE, SOMEARRAY) { ... }

(O)
function someFunction(someValue, someArray) { ... }
```

### 2.5 객체(Object)

---

1. 객체의 이름은 lowerCamelCase로 표기해주세요.

```coq
(O)
const thisIsMyObject = {};
function thisIsMyFunction() {}
```

2. 객체를 export 할 때는 PascalCase로 표기합니다.

```jsx
(O)
const NangmanStyleGuide = {
  es6: {
  },
};

export default NangmanStyleGuide;
```

### 2.6 클래스(Class)

---

1. 클래스나 생성자의 이름은 PascalCase로 표기해주세요. export시에도 동일하게 표기해주세요!

```jsx
(O)
class User {
  constructor(options) {
    this.name = options.name;
  }
}

const good = new User({
  name: '홍길동',
});
```

2. 클래스의 이름은 명사 또는 명사 구문으로 표기해주세요.
    
    또한, 인터페이스의 경우 명사 대신 형용사 또는 형용사 구문으로 표기할 수 있습니다!
    

# 3. Types

### 3.1 형 (Types)

---

1. Primitives: Primitive type은 그 값을 직접 조작합니다.

Primitive type에 대한 예시는 아래와 같습니다.

- `string`
- `number`
- `boolean`
- `null`
- `undefined`
2. Complex: 참조형(Complex)는 참조를 통해 값을 조작합니다.

Complex type에 대한 예시는 아래와 같습니다.

- `object`
- `array`
- `function`

### 3.2 참조(References)

---

1. 모든 참조는 `const` 를 사용하고, `var` 를 사용하지 마십시오.

<aside>
❓ 참조를 재할당 할 수 없으므로, 버그로 이어지고 이해하기 어려운 코드가 되는 것을 방지하기 위함입니다!

</aside>

```
(X)
var a = 1;
var b = 2;

(O)
const a = 1;
const b = 2;
```

2. 참조를 재할당 해야한다면 var 대신 let을 사용해야 합니다.

<aside>
❓ `var` 같은 함수 스코프보다는 블록스코프의 `let` 이 더 유리하기 때문입니다!

</aside>

```
(X)
var count = 1;
if (true) {
  count += 1;
}

(O), use the let.
let count = 1;
if (true) {
  count += 1;
}
```

<aside>
💡 `let` 과 `const` 은 선언된 블록 안에서만 존재하는 것을 유의하세요!

</aside>

### 3.3 오브젝트 (Object)

---

1. 오브젝트를 작성할 때는 리터럴 구문을 사용하세요.

```
(X)
const item = new Object();

(O)
const item = {};
```

2. 예약어 대신 알기쉬운 동의어를 사용하세요.

```
(X)
const superman = {
  class: 'alien',
};

(X)
const superman = {
  klass: 'alien',
};

(O)
const superman = {
  type: 'alien',
};
```

3. 오브젝트 내 메소드를 사용할 경우 단축구문을 사용하세요.

```
(X)
const atom = {
  value: 1,

  addValue: function (value) {
    return atom.value + value;
  },
};

(O)
const atom = {
  value: 1,

  addValue(value) {
    return atom.value + value;
  },
};
```

4. 프로퍼티의 단축 구문은 오브젝트 선언의 시작부분에 그룹화하여 사용하세요.

```
const name = '홍길동';
const age = 16;

(X)
const obj = {
  shcool : '방학 초등학교',
  grade : 5,
  name,
  age,
};

(O)
const obj = {
	name,
  age,  
	shcool : '방학 초등학교',
  grade : 5,
};
```

<aside>
❓ 어떤 프로퍼티가 단축구문을 이용하고 있는지가 명확하기 때문입니다!

</aside>

### 3.4 배열(Arrays)

---

1. 배열을 작성 할 때는 리터럴 구문을 사용해주세요.

```
(X)
const items = new Array();

(O)
const items = [];
```

2. 직접 배열에 항목을 대입하지 말고, Array.push를 사용해주세요.

```
const someStack = [];

(X)someStack[someStack.length] = 'abracadabra';

(O)someStack.push('abracadabra');
```

3. 배열을 복사할 때는 배열의 spread 연산자인 `...` 를 사용해주세요.

```
const someStack = [];

(X)
const len = items.length;
const itemsCopy = [];
let i;

for (i = 0; i < len; i++) {
  itemsCopy[i] = items[i];
}

(O)const itemsCopy = [...items];
```

### 3.5 구조 분해 대입(Destructuring)

---

1. 하나의 오브젝트에서 다수의 프로퍼티를 할당할 때는 오브젝트 구조 분해 대입을 사용해주세요.

```
(X)
function getFullName(user) {
  const firstName = user.firstName;
  const lastName = user.lastName;

  return `${firstName} ${lastName}`;
}

(O)
function getFullName(obj) {
  const { firstName, lastName } = obj;
  return `${firstName} ${lastName}`;
}

(O) Best!!!
function getFullName({ firstName, lastName }) {
  return `${firstName} ${lastName}`;
}
```

<aside>
❓ 구조 분해 대입을 사용하는 것이 프로퍼티를 위한 임시 참조 작성을 줄일 수 있기 때문입니다!

</aside>

2. 배열의 구조 분해 대입을 사용해주세요.

```
const arr = [1, 2, 3, 4];

(X)
const first = arr[0];
const second = arr[1];

(O) 
const [first, second] = arr;
```

### 3.6 문자열(String)

---

1. 문자열에는 싱글 쿼트 `''` 를 사용해주세요.

```
(X)
const name = "Capt. Janeway";

(O)
const name = 'Capt. Janeway';
```

2. 100문자 이상의 문자열을 문자열 연결을 사용해서 복수행에 걸쳐 기술해주세요.

```
(X)
const errorMessage = 'This is a super long error that was thrown because of Batman. When you stop to think about how Batman had anything to do with this, you would get nowhere fast.';

(X)
const errorMessage = 'This is a super long error that was thrown because \
of Batman. When you stop to think about how Batman had anything to do \
with this, you would get nowhere \
fast.';

(O)
const errorMessage = 'This is a super long error that was thrown because ' +
  'of Batman. When you stop to think about how Batman had anything to do ' +
  'with this, you would get nowhere fast.';
```

<aside>
🚨 문자 연결을 과용하면 성능에 영향을 미칠 수 있으니 유의해주세요!

</aside>

3. 프로그래밍 내에서 문자열을 생성하는 경우, 문자열 연결이 아닌 template strings를 사용해주세요.

```
(X)
function sayHi(name) {
  return '제 이름은' + name + '입니다.';
}
(X)
function sayHi(name) {
  return ['제 이름은 ', name, '입니다.'].join();
}

(O)
function sayHi(name) {
  return `제 이름은 ${name}입니다.`;
}
```

<aside>
❓ Template strings 는 문자열 보간 기능과 적절한 줄 바꿈을 갖춘 구문이 가독성이 좋기 때문입니다!

</aside>

4. `eval()` 함수의 사용은 반드시 금지합니다!!

### 3.7 변수 (Variables)

---

1. 변수를 선언 할 때는 항상 `const` 를 사용해주세요. 단, 변수의 값이 바뀌는 경우 let을 사용합니다.

```
(X)
superPower = new SuperPower();

(O)
const superPower = new SuperPower();
```

2. 하나의 변수선언에 대해 하나의  `const` 를 사용해주세요.

<aside>
❓ 이 방법의 경우, 간단히 새 변수를 추가하는게 가능하기 때문입니다!

</aside>

```
(X)
const items = getItems(),
    isTrue = true,
    values = 'z';

(X)
const items = getItems(),
    isTrue = true;
    values = 'z';

(O)
const items = getItems();
const isTrue = true;
const values = 'z';
```

3. 지역 변수는 그 변수를 포함하는 블록 시작에서 선언하지 않고 사용 범위를 최소화하기 위해 사용되는 지점과 가장 가까운 곳에서 선언해주세요.

```jsx
(O)
function() {
  test();
  console.log('doing stuff..');

	//...

  const name = getName();

  if (name === 'test') {
    return false;
  }

  return name;
}

(X)
// 필요없는 함수 호출
function(hasName) {
  const name = getName();

  if (!hasName) {
    return false;
  }

  this.setFirstName(name);

  return true;
}

(O)
function(hasName) {
  if (!hasName) {
    return false;
  }

  const name = getName();
  this.setFirstName(name);

  return true;
}
```

4. JSDoc을 위한 주석은 변수 선언 이전 혹은 변수 이름 이전에 작성합니다.

```jsx
(X)
/** Some description. */
const /** !Array<number> */ data = [];

const /** !Array<number> */ data = [];

(O)
/**
 * Some description.
 * @type {!Array<number>}
 */
const data = [];
```

# 4. 함수

### 4.1 함수(Functions)

---

1. 함수식 보다 함수 선언을 사용해주세요.

```
(X)
const foo = function () {
	...
};

(O)
function foo() {
	...
}
```

<aside>
❓ 이름이 부여된 함수선언은 콜스택에서 간단하게 확인하는 것이 가능합니다. 또한 함수선언은 함수의 본체가 hoist 되어집니다. 그에 반해 함수식은 참조만이 hoist 되어집니다. 이 룰에 의해 함수식의 부분을 항상 [Arrow함수](https://github.com/tipjs/javascript-style-guide#arrow%ED%95%A8%EC%88%98arrow-functions)
에서 이용하는것이 가능합니다.

</aside>

2. 함수 이외의 블록 (if나 while 등) 안에서 함수를 선언하지 마십시오.

3. 절대 파라미터에 `arguments` 를 지정하지 마십시오. 함수스코프에 전해지는  `arguments` 오브젝트의 참조를 덮어 씌워 버립니다.

```
(X)
function nope(name, options, arguments) {
	...
}

(O)
function yup(name, options, args) {
  ...
}
```

4. 절대 `arguments` 를 이용하지 마십시오. 대신에 rest syntax `...` 를 사용해주세요.

<aside>
❓ `...`을 이용하는 것으로 몇개의 파라메터를 이용하고 싶은가를 확실하게 할 수 있습니다. 또한 rest 파라메터는 `arguments` 와 같은 Array-like 오브젝트가 아닌 진짜 Array 입니다.

</aside>

```
(X)
function concatenateAll() {
  const args = Array.prototype.slice.call(arguments);
  return args.join('');
}

(O)
function concatenateAll(...args) {
  return args.join('');
}
```

5. 함수의 파라미터를 변경하여 사용하는 것보다 default 파라미터를 사용해주세요.

```
(X) really bad !!!
function handleThings(opts) {
  // 경고!! 함수의 파라미터를 변경시키면 안됩니다.
  // 만약 opts가 falsy 하다면 설정대로 오브젝트가 할당됩니다.
  // 이는 버그를 일으킬지도 모릅니다.
  opts = opts || {};
  ...
}

(X) still bad
function handleThings(opts) {
  if (opts === void 0) {
    opts = {};
  }
  // ...
}

(O)
function handleThings(opts = {}) {
  // ...
}
```

5-1 default 파라미터는 항상 뒤쪽에 위치해주십시오.

```
(X)
function handleThings(opts = {}, name) {
  ...
}

(O)
function handleThings(name, opts = {}) {
  ...
}
```

### 4.2 화살표함수 (Arrow Functions)

---

1. 무명 함수 식을 사용하는 경우 arrow 함수 표기를 사용해주세요.

```
(X)
[1, 2, 3].map(function (x) {
  const y = x + 1;
  return x * y;
});

(O)
[1, 2, 3].map((x) => {
  const y = x + 1;
  return x * y;
});
```

<aside>
❓ arrow 함수는 그 context의 `this` 에서 실행하는 버전의 함수를 작성합니다. 이렇게 작성할 시에 원하는 동작을 할 수 있고, 보다 간결한 구문이기 때문입니다!

</aside>

2. 함수 식이 복수행으로 걸쳐있을 경우에는 가독성을 위해 소괄호 ()로 감싸주세요.

```
(O)
[1, 2, 3].map(number => (
  `As time went by, the string containing the ${number} became much ` +
  'longer. So we needed to break it over multiple lines.'
));
```

3. 함수의 인수가 하나인 경우 소괄호()를 생략할 수 있습니다.

```
(O)
[1, 2, 3].map(x => x * x);
```

# 5. 클래스와 모듈

### 5.1 클래스와 구조체 (Classes & Constructors)

---

- 생성자는 선택적으로 작성합니다. 하지만 하위 클래스는 필드를 설정하기 전에 반드시 super()를 호출해야합니다. (그렇지 않으면 this에 접근할 것입니다!) 인터페이스의 경우 메소드가 아닌 속성을 생성자에서 반드시 선언해야 합니다.

- 정적 메소드 사용보다는 모듈 함수를 더 지향합니다.
    - 정적 메소드는 클래스 내에서만 호출되어야 합니다.
    - 동적 인스턴스를 포함하는 변수나 하위 클래스의 생성자 내부에서 호출되서는 안 됩니다.
    - 하위 클래스 내에 선언되지 않은 정적 메소드는 호출되서는 안 됩니다.

1. 상속은 `extends` 를 사용해주세요.

```
(O)
class PeekableQueue extends Queue {
  peek() {
    return this._queue[0];
  }
}
```

2. prototype을 직접 조작하지 않고 class를 사용해주세요.

3. toString() 메소드를 오버라이딩 하는 것을 허용하지만 사이드 이펙트가 나타나지 않도록 주의해주세요.

### 5.2 모듈(Modules)

---

1. 비표준 모듈 시스템이 아닌 항상 (`import`/`export`)를 사용해주세요. 

```
(O)
import { es6 } from './NangmanStyleGuide';
export default es6;
```

2. wildcard import는 사용하지 마십시오.

```
(X)
import * as NangmanStyleGuide from './NangmanStyleGuide';
```

<aside>
❓ single default export임을 주의해야 할 필요가 있기 때문입니다!

</aside>

3. import 문으로부터 직접 export 하는 것은 피해주세요.

```
(X)
export { es6 as default } from './NangmanStyleGuide';

(O)
import { es6 } from './NangmanStyleGuide';
export default es6;
```

<aside>
❓ 간결한 문장이지만 import와 export 방법을 일관성을 유지하기 위함입니다!

</aside>

# 6. 제어문

### 6.1 반복문 (loops)

---

1. 일반적인 for문보다 for-of 사용을 권장합니다. 가능하다면 map(), reduce()와 같은 고급 함수를 사용하십시오. (5.1에 대한 이유)

```
const numbers = [1, 2, 3, 4, 5];

(X)
let sum = 0;
for (let num of numbers) {
  sum += num;
}

sum === 15;

(O)
let sum = 0;
numbers.forEach((num) => sum += num);
sum === 15;

(O) best (use the functional force)
const sum = numbers.reduce((total, num) => total + num, 0);
sum === 15;
```

### 6.2 스위치문 (switch)

---

1. 다음 case 구문이 실행되어야 한다면 주석으로 이를 설명합니다.
2. default문은 항상 마지막에 위치해야합니다.

```jsx
switch (input) {
  case 1:
  case 2:
    prepareOneOrTwo();
  // fall through
  case 3:
    handleOneTwoOrThree();
    break;
  default:
    handleLargeNumber(input);
}
```

### 6.3 조건식과 등가식 ****(Comparison Operators & Equality)****

---

1. `==` 이나 `!=`보다 `===` 와 `!==` 을 사용해 주십시오

2. if문과 같은 조건식은 `ToBoolean` 메소드에 의한 강제 형변환으로 평가되어 항상 다음과 같은 간단한 룰을 따릅니다.
- **오브젝트** 는 **true** 로 평가됩니다.
- **undefined** 는 **false** 로 평가됩니다.
- **null** 은 **false** 로 평가됩니다.
- **부울값** 은 **boolean형의 값** 으로 평가됩니다.
- **수치** 는 **true** 로 평가됩니다. 하지만 **+0, -0, or NaN** 의 경우는 **false** 입니다.
- **문자열** 은 **true** 로 평가됩니다. 하지만 빈문자 `''` 의 경우는 **false** 입니다.

3. 단축혁을 사용해주세요.

```jsx
(X)
if (name !== '') {
  // ...stuff...
}

(O)
if (name) {
  // ...stuff...
}

(X)
if (collection.length > 0) {
  // ...stuff...
}

(O)
if (collection.length) {
  // ...stuff...
}
```

# 7. 기타

### 7.1 ****이터레이터와 제너레이터(Iterators and Generators)****

---

1. iterators를 사용하지 마십시오. `for-of` 루프 대신에 `map()` 과 `reduce()` 와 같은 JavaScript 고급함수(higher-order functions)를 사용해주세요.

<aside>
❓ 고급함수는 immutable(불변)룰을 적용합니다. 따라서 값을 반환하는 순수 함수를 다루는 것이 간단하기 때문입니다!

</aside>

```
const numbers = [1, 2, 3, 4, 5];

(X)
let sum = 0;
for (let num of numbers) {
  sum += num;
}

sum === 15;

(O)
let sum = 0;
numbers.forEach((num) => sum += num);
sum === 15;

(O) best (use the functional force)
const sum = numbers.reduce((total, num) => total + num, 0);
sum === 15;
```

2. 현 시점에서는 generators는 사용하지 마십시오.

<aside>
❓ ES5로 트랜스파일을 잘 하지 않기 때문입니다!

</aside>

### 7.2 프로퍼티 (Properties)

---

1. 프로퍼티에 접근할 경우 점 `.` 을 사용해주세요.

```
const luke = {
  jedi: true,
  age: 28,
};

(X)
const isJedi = luke['jedi'];

(O)
const isJedi = luke.jedi;
```

2. 변수를 사용하여 프로퍼티에 접근할 경우 대괄호 `[]`를 사용해주세요.

```
const luke = {
  jedi: true,
  age: 28,
};

function getProp(prop) {
  return luke[prop];
}

const isJedi = getProp('jedi');
```

### 7.3 블록(Block)

---

1. 복수행의 블록에는 중괄호 ({})를 사용해주세요.

```jsx
(X)
if (test)
  return false;

(O)
if (test) return false;

(O)
if (test) {
  return false;
}

(X)
function() { return false; }

(O)
function() {
  return false;
}
```

2. 복수행 블록의 `if` 와 `else` 를 이용하는 경우 `else`는 `if` 블록 끝의 중괄호(})와 같은 행에 위치시켜 주십시오.

```jsx
(X)
if (test) {
  thing1();
  thing2();
}
else {
  thing3();
}

(O)
if (test) {
  thing1();
  thing2();
} else {
  thing3();
}
```

### 7.4 코멘트 (Comments)

---

1. 복수행 코멘트는 `/** ... */` 을 사용해 주세요. 그 안에는 설명과 모든 파라미터, 반환 값에 대해 형이나 값을 기술해주세요!

```jsx
(O)
/**
 * make() 함수는 전달받은 tag 이름에 따라
 * 새로운 element를 반환합니다.
 *
 * @param {String} tag
 * @return {Element} element
 */
function make(tag) {

  // ...stuff...

  return element;
}
```

2. 단일행 코멘트에는 `//` 을 사용해 주세요. 코멘트를 추가하고 싶은 코드의 위에 작성해주세요. 또한 코멘트 앞에 빈행을 넣어주세요.

```jsx
(O)
function getType() {
  console.log('fetching type...');

  // set the default type to 'no type'
  const type = this._type || 'no type';

  return type;
}

// also good
function getType() {
  // set the default type to 'no type'
  const type = this._type || 'no type';

  return type;
}
```

3. 문제에 대한 사항에 대해서는 `FIXME -- 해결이 필요` 를 사용해주세요.

```jsx
class Calculator extends Abacus {
  constructor() {
    super();

    // FIXME: 글로벌변수를 사용해서는 안됨.
    total = 0;
  }
}
```

4. 문제의 해결책에 대한 주석으로 `// TODO:` 를 사용해 주세요.

```jsx
class Calculator extends Abacus {
  constructor() {
    super();

    // TODO: total 은 옵션 파라메터로 설정해야함.
    this.total = 0;
  }
}
```

### 7.5 공백(whitespace)

---

1. 탭에는 스페이스 2개를 설정해주세요.

```jsx
(O)
function() {
∙∙const name;
}
```

2. 주요 중괄호 ({}) 앞에는 스페이스 1개를 넣어주세요.

```jsx
(O)
function test() {
  console.log('test');
}
```

3. 제어구문 (`if`문이나 `while`문 등)의 소괄호 (()) 앞에는 스페이스 1개를 넣어주세요. (함수 선언이나 함수 호출 시 인수 리스트의 앞에는 스페이스를 넣지 말아주세요.)

```jsx
(O)
if (isJedi) {
  fight();
}

(O)
function fight() {
  console.log('Swooosh!');
}
```

4. 연산자 사이에 스페이스를 1개 넣어주세요.

```jsx
(O)
const x = y + 5;
```

5. 메소드를 길게 채이닝 하는 경우에는 인덴트를 사용해주세요. 행이 새로운 문이 아닌 메소드 호출인 것을 강조하기 위해서 점 (.)을 넣어주세요.

```jsx
(O)
$('#items')
  .find('.selected')
    .highlight()
    .end()
  .find('.open')
    .updateCount();

(O)
const leds = stage.selectAll('.led')
    .data(data)
  .enter().append('svg:svg')
    .classed('led', true)
    .attr('width', (radius + margin) * 2)
  .append('svg:g')
    .attr('transform', 'translate(' + (radius + margin) + ',' + (radius + margin) + ')')
    .call(tron.led);
```

6. 문의 앞과 블록의 뒤에는 빈행을 남겨주세요.

```jsx
(O)
const arr = [
  function foo() {
  },
	//빈행!!
  function bar() {
  },
];
	//빈행!!
return arr;
```

7. 블록에는 빈행을 넣지 말아주세요.

```jsx
(O)
function bar() {
  console.log(foo);
}

(O)
if (baz) {
  console.log(qux);
} else {
  console.log(foo);
}
```

8. 소괄호() 안쪽에는 스페이스를 넣지 말아주세요.

```jsx
(X)
function bar( foo ) {
  return foo;
}

(O)
function bar(foo) {
  return foo;
}
```

9. 대괄호 ([])의 안쪽에는 스페이스를 추가하지 말아주세요.

```jsx
(X)
const foo = [ 1, 2, 3 ];
console.log(foo[ 0 ]);

(O)
const foo = [1, 2, 3];
console.log(foo[0]);
```

10. 중괄호 ({})의 안쪽에는 스페이스를 추가해주세요.

```jsx
(X)
const foo = {clark: 'kent'};

(O)
const foo = { clark: 'kent' };
```
