# JavaScript Style Guide

<aside>
๐ก ๋ณธ๋ฌธ์ ๋ญ๋ง(Nangman)์ JavaScript ์คํ์ผ ๊ฐ์ด๋ ์๋๋ค. ๊ตฌ๊ธ JavaScript ๊ฐ์ด๋๋ฅผ ์ฐธ๊ณ ํ์ฌ ์์ฑํ์์ต๋๋ค.

</aside>

## ๋ชฉ์ฐจ
---

### [1. ์๊ฐ(Intro)](https://github.com/Nangman-corp/JavaScript-Style-Guide/blob/main/README.md#1-%EC%86%8C%EA%B0%9Cintro-1)
### [2. ์ด๋ฆ(Name)](https://github.com/Nangman-corp/JavaScript-Style-Guide/blob/main/README.md#2-%EC%9D%B4%EB%A6%84name-1)
- [2.1 ๋ช๋ช ๊ท์น(Naming rules)](https://github.com/Nangman-corp/JavaScript-Style-Guide/blob/main/README.md#21-%EB%AA%85%EB%AA%85-%EA%B7%9C%EC%B9%99naming-rules)
- [2.2 ํ์ผ ๋ฐ ํจํค์ง(File and package)](https://github.com/Nangman-corp/JavaScript-Style-Guide/blob/main/README.md#22-%ED%8C%8C%EC%9D%BC-%EB%B0%8F-%ED%8C%A8%ED%82%A4%EC%A7%80file-and-package)
- [2.3 ๋ณ์(Variable)](https://github.com/Nangman-corp/JavaScript-Style-Guide/blob/main/README.md#23-%EB%B3%80%EC%88%98variable)
- [2.4 ํจ์(Funtion)](https://github.com/Nangman-corp/JavaScript-Style-Guide/blob/main/README.md#24-%ED%95%A8%EC%88%98funtion)
- [2.5 ๊ฐ์ฒด(Object)](https://github.com/Nangman-corp/JavaScript-Style-Guide/blob/main/README.md#25-%EA%B0%9D%EC%B2%B4object)
- [2.6 ํด๋์ค(Class)](https://github.com/Nangman-corp/JavaScript-Style-Guide/blob/main/README.md#26-%ED%81%B4%EB%9E%98%EC%8A%A4class)
### [3. ํ(Type)](https://github.com/Nangman-corp/JavaScript-Style-Guide/blob/main/README.md#3-%ED%98%95type-1)
- [3.1 ํ (Types)](https://github.com/Nangman-corp/JavaScript-Style-Guide/blob/main/README.md#31-%ED%98%95types)
- [3.2 ์ฐธ์กฐ(References)](https://github.com/Nangman-corp/JavaScript-Style-Guide/blob/main/README.md#32-%EC%B0%B8%EC%A1%B0references)
- [3.3 ์ค๋ธ์ ํธ (Object)](https://github.com/Nangman-corp/JavaScript-Style-Guide/blob/main/README.md#33-%EC%98%A4%EB%B8%8C%EC%A0%9D%ED%8A%B8-object)
- [3.4 ๋ฐฐ์ด(Arrays)](https://github.com/Nangman-corp/JavaScript-Style-Guide/blob/main/README.md#34-%EB%B0%B0%EC%97%B4arrays)
- [3.5 ๊ตฌ์กฐ ๋ถํด ๋์(Destructuring)](https://github.com/Nangman-corp/JavaScript-Style-Guide/blob/main/README.md#35-%EA%B5%AC%EC%A1%B0-%EB%B6%84%ED%95%B4-%EB%8C%80%EC%9E%85destructuring)
- [3.6 ๋ฌธ์์ด(String)](https://github.com/Nangman-corp/JavaScript-Style-Guide/blob/main/README.md#36-%EB%AC%B8%EC%9E%90%EC%97%B4string)
- [3.7 ๋ณ์ (Variables)](https://github.com/Nangman-corp/JavaScript-Style-Guide/blob/main/README.md#37-%EB%B3%80%EC%88%98-variables)
### [4. ํจ์(Functions)](https://github.com/Nangman-corp/JavaScript-Style-Guide/blob/main/README.md#4-%ED%95%A8%EC%88%98functions-1)
- [4.1 ํจ์(Functions)](https://github.com/Nangman-corp/JavaScript-Style-Guide/blob/main/README.md#41-%ED%95%A8%EC%88%98functions)
- [4.2 ํ์ดํํจ์(Arrow Functions)](https://github.com/Nangman-corp/JavaScript-Style-Guide/blob/main/README.md#42-%ED%99%94%EC%82%B4%ED%91%9C%ED%95%A8%EC%88%98arrow-functions)
### [5. ํด๋์ค์ ๋ชจ๋(Class and module)](https://github.com/Nangman-corp/JavaScript-Style-Guide/blob/main/README.md#5-%ED%81%B4%EB%9E%98%EC%8A%A4%EC%99%80-%EB%AA%A8%EB%93%88class-and-module-1)
- [5.1 ํด๋์ค์ ๊ตฌ์กฐ์ฒด(Classes and structures)](https://github.com/Nangman-corp/JavaScript-Style-Guide/blob/main/README.md#51-%ED%81%B4%EB%9E%98%EC%8A%A4%EC%99%80-%EA%B5%AC%EC%A1%B0%EC%B2%)B4classes-and-structures)
- [5.2 ๋ชจ๋(Modules)](https://github.com/Nangman-corp/JavaScript-Style-Guide/blob/main/README.md#52-%EB%AA%A8%EB%93%88modules)
### [6. ์ ์ด๋ฌธ(Control statements)](https://github.com/Nangman-corp/JavaScript-Style-Guide/blob/main/README.md#6-%EC%A0%9C%EC%96%B4%EB%AC%B8control-statements-1)
- [6.1 ๋ฐ๋ณต๋ฌธ(loops)](https://github.com/Nangman-corp/JavaScript-Style-Guide/blob/main/README.md#61-%EB%B0%98%EB%B3%B5%EB%AC%B8loops)
- [6.2 ์ค์์น๋ฌธ(switch)](https://github.com/Nangman-corp/JavaScript-Style-Guide/blob/main/README.md#62-%EC%8A%A4%EC%9C%84%EC%B9%98%EB%AC%B8switch)
- [6.3 ์กฐ๊ฑด์๊ณผ ๋ฑ๊ฐ์(Comparison Operators and Equality)](https://github.com/Nangman-corp/JavaScript-Style-Guide/blob/main/README.md#63-%EC%A1%B0%EA%B1%B4%EC%8B%9D%EA%B3%BC-%EB%93%B1%EA%B0%80%EC%8B%9Dcomparison-operators-and-equality)
### [7. ๊ธฐํ(The Others)](https://github.com/Nangman-corp/JavaScript-Style-Guide/blob/main/README.md#7-%EA%B8%B0%ED%83%80the-others-1)
- [7.1ย ์ดํฐ๋ ์ดํฐ์ ์ ๋๋ ์ดํฐ(Iterators and Generators)](https://github.com/Nangman-corp/JavaScript-Style-Guide/blob/main/README.md#71-%EC%9D%B4%ED%84%B0%EB%A0%88%EC%9D%B4%ED%84%B0%EC%99%80-%EC%A0%9C%EB%84%88%EB%A0%88%EC%9D%B4%ED%84%B0iterators-and-generators)
- [7.2 ํ๋กํผํฐ(Properties)](https://github.com/Nangman-corp/JavaScript-Style-Guide/blob/main/README.md#72-%ED%94%84%EB%A1%9C%ED%8D%BC%ED%8B%B0properties)
- [7.3 ๋ธ๋ก(Block)](https://github.com/Nangman-corp/JavaScript-Style-Guide/blob/main/README.md#73-%EB%B8%94%EB%A1%9Dblock)
- [7.4 ์ฝ๋ฉํธ(Comments)](https://github.com/Nangman-corp/JavaScript-Style-Guide/blob/main/README.md#74-%EC%BD%94%EB%A9%98%ED%8A%B8comments)
- [7.5 ๊ณต๋ฐฑ(whitespace)](https://github.com/Nangman-corp/JavaScript-Style-Guide/blob/main/README.md#75-%EA%B3%B5%EB%B0%B1whitespace)

---

# 1. ์๊ฐ(Intro)

---

๋ณธ ๋ฌธ์๋ Nangman์ JavaScript ์คํ์ผ์ ์ค๋ชํฉ๋๋ค. ๋ณธ ๋ฌธ์์ ๊ฐ์ด๋๋ฅผ ์ดํดํ์  ํ ์ฌ์ฉํ์๋ ๊ธฐ์  ๋ฌธ์๋ก ์ด๋ํ์ฌ ๊ธฐ์ ์ ํด๋นํ๋ ๊ฐ์ด๋๋ฅผ ์์งํ์ธ์!

# 2. ์ด๋ฆ(Name)

### 2.1 ๋ช๋ช ๊ท์น(Naming rules)

---

1. ๋จ์ผ ๊ธ์๋ก ์ด๋ฆ์ ์ง์ง ์๊ณ  ์ด๋ฆ์ ํตํด ์ฐ์์๋ฅผ ์ ์ ์๋๋ก ์์ฑํฉ๋๋ค.

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

2. ์ด๋ฆ์ ๋งจ ์์ด๋ ๋งจ ๋ค์ ๋ฐ์ค(_)์ ์ฌ์ฉํ์ง ์์ต๋๋ค.

```
(X)
this.__firstName__ = 'Panda';
this.firstName_ = 'Panda';
this._firstName = 'Panda';

(O)
this.firstName = 'Panda';
```

3. this๋ฅผ ๋ณ์์ ๊ฐ์ผ๋ก ์ฌ์ฉํ์ง ์์ต๋๋ค. ํ์ํ  ๊ฒฝ์ฐ ํ์ดํ ํจ์(Arrow Function)์ด๋ ๋ฐ์ธ๋ฉ์ ํตํด ์ฌ์ฉํ์ญ์์ค.

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

4. ๊ฐ๋์ฑ์ ์ํด ์ฝ์ด๋ Camel Case๋ก ํ๊ธฐํฉ๋๋ค.

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

5. ํ์ผ์ 1๊ฐ์ ํด๋์ค๋ก export ํ๋ ๊ฒฝ์ฐ ํ์ผ๋ช์ ํด๋์ค๋ช๊ณผ ์์ ํ ์ผ์น์์ผ์ฃผ์ธ์.

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

5-1. export๋๋ ํ์ผ ๋ด์ ๋ชจ๋  ์์๋ ๋ชจ๋ ๋๋ฌธ์๋ก ํ๊ธฐํ๋ ๊ฒ์ ๊ถ์ฅํฉ๋๋ค.

```
(X)
const PRIVATE_VARIABLE = 'should not be unnecessarily uppercased within a file';

(X)
export const THING_TO_BE_CHANGED = 'should obviously not be uppercased';

(X)
export let REASSIGNABLE_VARIABLE = 'do not use let with uppercase variables';

// ---

//ํ์ฉ๋์ง๋ง sematic ๊ฐ์ ์ง์ํ์ง ์์ต๋๋ค.
export const apiKey = 'SOMEKEY';

// ํด๋น ๋ณ์๋ช์ ๊ถ์ฅํฉ๋๋ค.
export const API_KEY = 'SOMEKEY';

// ---

(X) - Map ๋ด์์ key์ naming์ ๋ถํ์ํ๊ฒ ๋๋ฌธ์๋ก ํ์ง ๋ง์ญ์์ค.
export const MAPPING = {
  KEY: 'value'
};

(O)
export const MAPPING = {
  key: 'value'
};
```

5-2. default export๊ฐ ํจ์์ผ ๊ฒฝ์ฐ, camelCase๋ฅผ ์ฌ์ฉํด์ฃผ์ธ์. ๋ฌผ๋ก  ํ์ผ๋ช์ ํจ์๋ช๊ณผ ๋์ผํด์ผ ํฉ๋๋ค.

```jsx
(O)
function makeStyleGuide() {
}

export default makeStyleGuide;
```

6. ์ด๋ฆ์ ๋ณต์ํ์ ํ๊ธฐํ์ง ์์ต๋๋ค.

```
(X)
let delivery_notes = ["one", "two"];

(O)
let delivery_note_list = ["one", "two"];
```

7. ์ค์๋ง์ ์ฌ์ฉํ์ง ์์ต๋๋ค.

```
(X)
let del_note = 1;

(O)
let delivery_note = 1;
```

8. private ํ๋กํผํฐ๋ช์ ์์ ์ธ๋์ค์ฝ์ด `_`ย ๋ฅผ ์ฌ์ฉํด์ฃผ์ธ์.

```jsx
(O)
this._firstName = 'Panda';
```

### 2.2 ํ์ผ ๋ฐ ํจํค์ง(File and package)

---

1. ํ์ผ์ ์ด๋ฆ์ ์๋ฌธ์๋ก ํ๊ธฐํฉ๋๋ค.

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

2. ํจํค์ง์ ์ด๋ฆ์ lowerCamelCase๋ก ํ๊ธฐํฉ๋๋ค.

```
(X)
my.examplecode.deepspace
my.example_code.deep_space

(O)
my.exampleCode.deepSpace
```

3. ํ์ผ์ ์ด๋ฆ์ default export์ ์ด๋ฆ๊ณผ ์ผ์นํด์ผ ํฉ๋๋ค.

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
import CheckBox from './CheckBox';  // import/export/filename ๋ชจ๋ pascal case
import helloWorld from './helloWorld'; // import/export/filename ๋ชจ๋ camel case 
import insideDirectory from './insideDirectory'; //import/export/filename ๋ชจ๋ camel case
```

### 2.3 ๋ณ์(Variable)

---

1. ๋ณ์์ ์ด๋ฆ์ lowerCamelCase๋ก ํ๊ธฐํด์ฃผ์ธ์.
    
    ๋จ,  export ๋๋ ํ์ผ ๋ด์ ์์๋ ์์ธ์๋๋ค!
    
2. ๋ณ์์ ์ด๋ฆ์ ์ํ๋ฒณ์ผ๋ก ์์ํด์ผํฉ๋๋ค.

```jsx
(X)
let 123Number = 123;
let HELLO_WORLD = "Hello World";

(O)
let number = 369;
let helloString = "Hello World";
```

### 2.4 ํจ์(Funtion)

---

1. ํจ์๋ lowerCamelCase๋ก ํ๊ธฐํด์ฃผ์ธ์.

```jsx
(X)
function MyFunction() {...}

(O)
function myFunction() {...}
```

2. ํจ์์ ์ด๋ฆ์ ๋์ฌ ๋๋ ๋์ฌ ๊ตฌ๋ฌธ์ผ๋ก ํ๊ธฐํด์ฃผ์ธ์.

```jsx
(X)
function whereIsCamera() { ... }

(O)
function findCamera() { ... }
function getFoo() { ... } // getter
function setBar() { ... } // setter
function hasCoo() { ... } // booleans
```

3. ํจ์์ ํ๋ผ๋ฏธํฐ๋ lowerCamelCase๋ก ํ๊ธฐํด์ฃผ์ธ์.
    
    ๋จ, ํ๊ธ์์ ํ๋ผ๋ฏธํฐ๋ public ๋ฉ์๋์์๋ ์ฌ์ฉํ์ง ์์ต๋๋ค.
    

```jsx
(X)
function someFunction(SOMEVALUE, SOMEARRAY) { ... }

(O)
function someFunction(someValue, someArray) { ... }
```

### 2.5 ๊ฐ์ฒด(Object)

---

1. ๊ฐ์ฒด์ ์ด๋ฆ์ lowerCamelCase๋ก ํ๊ธฐํด์ฃผ์ธ์.

```coq
(O)
const thisIsMyObject = {};
function thisIsMyFunction() {}
```

2. ๊ฐ์ฒด๋ฅผ export ํ  ๋๋ PascalCase๋ก ํ๊ธฐํฉ๋๋ค.

```jsx
(O)
const NangmanStyleGuide = {
  es6: {
  },
};

export default NangmanStyleGuide;
```

### 2.6 ํด๋์ค(Class)

---

1. ํด๋์ค๋ ์์ฑ์์ ์ด๋ฆ์ PascalCase๋ก ํ๊ธฐํด์ฃผ์ธ์. export์์๋ ๋์ผํ๊ฒ ํ๊ธฐํด์ฃผ์ธ์!

```jsx
(O)
class User {
  constructor(options) {
    this.name = options.name;
  }
}

const good = new User({
  name: 'ํ๊ธธ๋',
});
```

2. ํด๋์ค์ ์ด๋ฆ์ ๋ช์ฌ ๋๋ ๋ช์ฌ ๊ตฌ๋ฌธ์ผ๋ก ํ๊ธฐํด์ฃผ์ธ์.
    
    ๋ํ, ์ธํฐํ์ด์ค์ ๊ฒฝ์ฐ ๋ช์ฌ ๋์  ํ์ฉ์ฌ ๋๋ ํ์ฉ์ฌ ๊ตฌ๋ฌธ์ผ๋ก ํ๊ธฐํ  ์ ์์ต๋๋ค!
    

# 3. ํ(Type)

### 3.1 ํ(Types)

---

1. Primitives: Primitive type์ ๊ทธ ๊ฐ์ ์ง์  ์กฐ์ํฉ๋๋ค.

Primitive type์ ๋ํ ์์๋ ์๋์ ๊ฐ์ต๋๋ค.

- `string`
- `number`
- `boolean`
- `null`
- `undefined`
2. Complex: ์ฐธ์กฐํ(Complex)๋ ์ฐธ์กฐ๋ฅผ ํตํด ๊ฐ์ ์กฐ์ํฉ๋๋ค.

Complex type์ ๋ํ ์์๋ ์๋์ ๊ฐ์ต๋๋ค.

- `object`
- `array`
- `function`

### 3.2 ์ฐธ์กฐ(References)

---

1. ๋ชจ๋  ์ฐธ์กฐ๋ย `const`ย ๋ฅผ ์ฌ์ฉํ๊ณ ,ย `var`ย ๋ฅผ ์ฌ์ฉํ์ง ๋ง์ญ์์ค.

<aside>
โ ์ฐธ์กฐ๋ฅผ ์ฌํ ๋น ํ  ์ ์์ผ๋ฏ๋ก, ๋ฒ๊ทธ๋ก ์ด์ด์ง๊ณ  ์ดํดํ๊ธฐ ์ด๋ ค์ด ์ฝ๋๊ฐ ๋๋ ๊ฒ์ ๋ฐฉ์งํ๊ธฐ ์ํจ์๋๋ค!

</aside>

```
(X)
var a = 1;
var b = 2;

(O)
const a = 1;
const b = 2;
```

2. ์ฐธ์กฐ๋ฅผ ์ฌํ ๋น ํด์ผํ๋ค๋ฉด var ๋์  let์ ์ฌ์ฉํด์ผ ํฉ๋๋ค.

<aside>
โ `var` ๊ฐ์ ํจ์ ์ค์ฝํ๋ณด๋ค๋ ๋ธ๋ก์ค์ฝํ์ `let` ์ด ๋ ์ ๋ฆฌํ๊ธฐ ๋๋ฌธ์๋๋ค!

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
๐ก `let`ย ๊ณผย `const`ย ์ ์ ์ธ๋ ๋ธ๋ก ์์์๋ง ์กด์ฌํ๋ ๊ฒ์ ์ ์ํ์ธ์!

</aside>

### 3.3 ์ค๋ธ์ ํธ (Object)

---

1. ์ค๋ธ์ ํธ๋ฅผ ์์ฑํ  ๋๋ ๋ฆฌํฐ๋ด ๊ตฌ๋ฌธ์ ์ฌ์ฉํ์ธ์.

```
(X)
const item = new Object();

(O)
const item = {};
```

2. ์์ฝ์ด ๋์  ์๊ธฐ์ฌ์ด ๋์์ด๋ฅผ ์ฌ์ฉํ์ธ์.

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

3. ์ค๋ธ์ ํธ ๋ด ๋ฉ์๋๋ฅผ ์ฌ์ฉํ  ๊ฒฝ์ฐ ๋จ์ถ๊ตฌ๋ฌธ์ ์ฌ์ฉํ์ธ์.

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

4. ํ๋กํผํฐ์ ๋จ์ถ ๊ตฌ๋ฌธ์ ์ค๋ธ์ ํธ ์ ์ธ์ ์์๋ถ๋ถ์ ๊ทธ๋ฃนํํ์ฌ ์ฌ์ฉํ์ธ์.

```
const name = 'ํ๊ธธ๋';
const age = 16;

(X)
const obj = {
  shcool : '๋ฐฉํ ์ด๋ฑํ๊ต',
  grade : 5,
  name,
  age,
};

(O)
const obj = {
	name,
  age,  
	shcool : '๋ฐฉํ ์ด๋ฑํ๊ต',
  grade : 5,
};
```

<aside>
โ ์ด๋ค ํ๋กํผํฐ๊ฐ ๋จ์ถ๊ตฌ๋ฌธ์ ์ด์ฉํ๊ณ  ์๋์ง๊ฐ ๋ชํํ๊ธฐ ๋๋ฌธ์๋๋ค!

</aside>

### 3.4 ๋ฐฐ์ด(Arrays)

---

1. ๋ฐฐ์ด์ ์์ฑ ํ  ๋๋ ๋ฆฌํฐ๋ด ๊ตฌ๋ฌธ์ ์ฌ์ฉํด์ฃผ์ธ์.

```
(X)
const items = new Array();

(O)
const items = [];
```

2. ์ง์  ๋ฐฐ์ด์ ํญ๋ชฉ์ ๋์ํ์ง ๋ง๊ณ , Array.push๋ฅผ ์ฌ์ฉํด์ฃผ์ธ์.

```
const someStack = [];

(X)someStack[someStack.length] = 'abracadabra';

(O)someStack.push('abracadabra');
```

3. ๋ฐฐ์ด์ ๋ณต์ฌํ  ๋๋ ๋ฐฐ์ด์ spread ์ฐ์ฐ์์ธ `...` ๋ฅผ ์ฌ์ฉํด์ฃผ์ธ์.

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

### 3.5 ๊ตฌ์กฐ ๋ถํด ๋์(Destructuring)

---

1. ํ๋์ ์ค๋ธ์ ํธ์์ ๋ค์์ ํ๋กํผํฐ๋ฅผ ํ ๋นํ  ๋๋ ์ค๋ธ์ ํธ ๊ตฌ์กฐ ๋ถํด ๋์์ ์ฌ์ฉํด์ฃผ์ธ์.

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
โ ๊ตฌ์กฐ ๋ถํด ๋์์ ์ฌ์ฉํ๋ ๊ฒ์ด ํ๋กํผํฐ๋ฅผ ์ํ ์์ ์ฐธ์กฐ ์์ฑ์ ์ค์ผ ์ ์๊ธฐ ๋๋ฌธ์๋๋ค!

</aside>

2. ๋ฐฐ์ด์ ๊ตฌ์กฐ ๋ถํด ๋์์ ์ฌ์ฉํด์ฃผ์ธ์.

```
const arr = [1, 2, 3, 4];

(X)
const first = arr[0];
const second = arr[1];

(O) 
const [first, second] = arr;
```

### 3.6 ๋ฌธ์์ด(String)

---

1. ๋ฌธ์์ด์๋ ์ฑ๊ธ ์ฟผํธ `''` ๋ฅผ ์ฌ์ฉํด์ฃผ์ธ์.

```
(X)
const name = "Capt. Janeway";

(O)
const name = 'Capt. Janeway';
```

2. 100๋ฌธ์ ์ด์์ ๋ฌธ์์ด์ ๋ฌธ์์ด ์ฐ๊ฒฐ์ ์ฌ์ฉํด์ ๋ณต์ํ์ ๊ฑธ์ณ ๊ธฐ์ ํด์ฃผ์ธ์.

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
๐จ ๋ฌธ์ ์ฐ๊ฒฐ์ ๊ณผ์ฉํ๋ฉด ์ฑ๋ฅ์ ์ํฅ์ ๋ฏธ์น  ์ ์์ผ๋ ์ ์ํด์ฃผ์ธ์!

</aside>

3. ํ๋ก๊ทธ๋๋ฐ ๋ด์์ ๋ฌธ์์ด์ ์์ฑํ๋ ๊ฒฝ์ฐ, ๋ฌธ์์ด ์ฐ๊ฒฐ์ด ์๋ template strings๋ฅผ ์ฌ์ฉํด์ฃผ์ธ์.

```
(X)
function sayHi(name) {
  return '์  ์ด๋ฆ์' + name + '์๋๋ค.';
}
(X)
function sayHi(name) {
  return ['์  ์ด๋ฆ์ ', name, '์๋๋ค.'].join();
}

(O)
function sayHi(name) {
  return `์  ์ด๋ฆ์ ${name}์๋๋ค.`;
}
```

<aside>
โ Template strings ๋ ๋ฌธ์์ด ๋ณด๊ฐ ๊ธฐ๋ฅ๊ณผ ์ ์ ํ ์ค ๋ฐ๊ฟ์ ๊ฐ์ถ ๊ตฌ๋ฌธ์ด ๊ฐ๋์ฑ์ด ์ข๊ธฐ ๋๋ฌธ์๋๋ค!

</aside>

4. `eval()` ํจ์์ ์ฌ์ฉ์ ๋ฐ๋์ ๊ธ์งํฉ๋๋ค!!

### 3.7 ๋ณ์ (Variables)

---

1. ๋ณ์๋ฅผ ์ ์ธ ํ  ๋๋ ํญ์ `const` ๋ฅผ ์ฌ์ฉํด์ฃผ์ธ์. ๋จ, ๋ณ์์ ๊ฐ์ด ๋ฐ๋๋ ๊ฒฝ์ฐ let์ ์ฌ์ฉํฉ๋๋ค.

```
(X)
superPower = new SuperPower();

(O)
const superPower = new SuperPower();
```

2. ํ๋์ ๋ณ์์ ์ธ์ ๋ํด ํ๋์  `const` ๋ฅผ ์ฌ์ฉํด์ฃผ์ธ์.

<aside>
โ ์ด ๋ฐฉ๋ฒ์ ๊ฒฝ์ฐ, ๊ฐ๋จํ ์ ๋ณ์๋ฅผ ์ถ๊ฐํ๋๊ฒ ๊ฐ๋ฅํ๊ธฐ ๋๋ฌธ์๋๋ค!

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

3. ์ง์ญ ๋ณ์๋ ๊ทธ ๋ณ์๋ฅผ ํฌํจํ๋ ๋ธ๋ก ์์์์ ์ ์ธํ์ง ์๊ณ  ์ฌ์ฉ ๋ฒ์๋ฅผ ์ต์ํํ๊ธฐ ์ํด ์ฌ์ฉ๋๋ ์ง์ ๊ณผ ๊ฐ์ฅ ๊ฐ๊น์ด ๊ณณ์์ ์ ์ธํด์ฃผ์ธ์.

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
// ํ์์๋ ํจ์ ํธ์ถ
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

4. JSDoc์ ์ํ ์ฃผ์์ ๋ณ์ ์ ์ธ ์ด์  ํน์ ๋ณ์ ์ด๋ฆ ์ด์ ์ ์์ฑํฉ๋๋ค.

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

# 4. ํจ์(Functions)

### 4.1 ํจ์(Functions)

---

1. ํจ์์ ๋ณด๋ค ํจ์ ์ ์ธ์ ์ฌ์ฉํด์ฃผ์ธ์.

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

	โ ์ด๋ฆ์ด ๋ถ์ฌ๋ ํจ์์ ์ธ์ ์ฝ์คํ์์ ๊ฐ๋จํ๊ฒ ํ์ธํ๋ ๊ฒ์ด ๊ฐ๋ฅํ๋ฉฐ ํจ์์ ์ธ์ ํจ์์ ๋ณธ์ฒด๊ฐ hoist ๋์ด์ง๋๋ค. ๊ทธ์ ๋ฐํด ํจ์์์ ์ฐธ์กฐ๋ง์ด hoist ๋์ด์ง๋๋ค.
</aside> 

์ด ๋ฃฐ์ ์ํด ํจ์์์ ๋ถ๋ถ์ ํญ์ [Arrowํจ์](https://github.com/tipjs/javascript-style-guide#arrow%ED%95%A8%EC%88%98arrow-functions)
์์ ์ด์ฉํ๋๊ฒ์ด ๊ฐ๋ฅํฉ๋๋ค.



2. ํจ์ ์ด์ธ์ ๋ธ๋ก (if๋ while ๋ฑ) ์์์ ํจ์๋ฅผ ์ ์ธํ์ง ๋ง์ญ์์ค.

3. ์ ๋ ํ๋ผ๋ฏธํฐ์ `arguments`ย ๋ฅผ ์ง์ ํ์ง ๋ง์ญ์์ค. ํจ์์ค์ฝํ์ ์ ํด์ง๋  `arguments`ย ์ค๋ธ์ ํธ์ ์ฐธ์กฐ๋ฅผ ๋ฎ์ด ์์ ๋ฒ๋ฆฝ๋๋ค.

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

4. ์ ๋ `arguments`ย ๋ฅผ ์ด์ฉํ์ง ๋ง์ญ์์ค. ๋์ ์ rest syntaxย `...`ย ๋ฅผ ์ฌ์ฉํด์ฃผ์ธ์.

<aside>
โ `...`์ ์ด์ฉํ๋ ๊ฒ์ผ๋ก ๋ช๊ฐ์ ํ๋ผ๋ฉํฐ๋ฅผ ์ด์ฉํ๊ณ  ์ถ์๊ฐ๋ฅผ ํ์คํ๊ฒ ํ  ์ ์์ต๋๋ค. ๋ํ rest ํ๋ผ๋ฉํฐ๋ย `arguments`ย ์ ๊ฐ์ Array-like ์ค๋ธ์ ํธ๊ฐ ์๋ ์ง์ง Array ์๋๋ค.

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

5. ํจ์์ ํ๋ผ๋ฏธํฐ๋ฅผ ๋ณ๊ฒฝํ์ฌ ์ฌ์ฉํ๋ ๊ฒ๋ณด๋ค default ํ๋ผ๋ฏธํฐ๋ฅผ ์ฌ์ฉํด์ฃผ์ธ์.

```
(X) really bad !!!
function handleThings(opts) {
  // ๊ฒฝ๊ณ !! ํจ์์ ํ๋ผ๋ฏธํฐ๋ฅผ ๋ณ๊ฒฝ์ํค๋ฉด ์๋ฉ๋๋ค.
  // ๋ง์ฝ opts๊ฐ falsy ํ๋ค๋ฉด ์ค์ ๋๋ก ์ค๋ธ์ ํธ๊ฐ ํ ๋น๋ฉ๋๋ค.
  // ์ด๋ ๋ฒ๊ทธ๋ฅผ ์ผ์ผํฌ์ง๋ ๋ชจ๋ฆ๋๋ค.
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

5-1 default ํ๋ผ๋ฏธํฐ๋ ํญ์ ๋ค์ชฝ์ ์์นํด์ฃผ์ญ์์ค.

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

### 4.2 ํ์ดํํจ์(Arrow Functions)

---

1. ๋ฌด๋ช ํจ์ ์์ ์ฌ์ฉํ๋ ๊ฒฝ์ฐ arrow ํจ์ ํ๊ธฐ๋ฅผ ์ฌ์ฉํด์ฃผ์ธ์.

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
โ arrow ํจ์๋ ๊ทธ context์ `this` ์์ ์คํํ๋ ๋ฒ์ ์ ํจ์๋ฅผ ์์ฑํฉ๋๋ค. ์ด๋ ๊ฒ ์์ฑํ  ์์ ์ํ๋ ๋์์ ํ  ์ ์๊ณ , ๋ณด๋ค ๊ฐ๊ฒฐํ ๊ตฌ๋ฌธ์ด๊ธฐ ๋๋ฌธ์๋๋ค!

</aside>

2. ํจ์ ์์ด ๋ณต์ํ์ผ๋ก ๊ฑธ์ณ์์ ๊ฒฝ์ฐ์๋ ๊ฐ๋์ฑ์ ์ํด ์๊ดํธ ()๋ก ๊ฐ์ธ์ฃผ์ธ์.

```
(O)
[1, 2, 3].map(number => (
  `As time went by, the string containing the ${number} became much ` +
  'longer. So we needed to break it over multiple lines.'
));
```

3. ํจ์์ ์ธ์๊ฐ ํ๋์ธ ๊ฒฝ์ฐ ์๊ดํธ()๋ฅผ ์๋ตํ  ์ ์์ต๋๋ค.

```
(O)
[1, 2, 3].map(x => x * x);
```

# 5. ํด๋์ค์ ๋ชจ๋(Class and module)

### 5.1 ํด๋์ค์ ๊ตฌ์กฐ์ฒด(Classes and structures)

---

- ์์ฑ์๋ ์ ํ์ ์ผ๋ก ์์ฑํฉ๋๋ค. ํ์ง๋ง ํ์ ํด๋์ค๋ ํ๋๋ฅผ ์ค์ ํ๊ธฐ ์ ์ ๋ฐ๋์ super()๋ฅผ ํธ์ถํด์ผํฉ๋๋ค. (๊ทธ๋ ์ง ์์ผ๋ฉด this์ ์ ๊ทผํ  ๊ฒ์๋๋ค!) ์ธํฐํ์ด์ค์ ๊ฒฝ์ฐ ๋ฉ์๋๊ฐ ์๋ ์์ฑ์ ์์ฑ์์์ ๋ฐ๋์ ์ ์ธํด์ผ ํฉ๋๋ค.

- ์ ์  ๋ฉ์๋ ์ฌ์ฉ๋ณด๋ค๋ ๋ชจ๋ ํจ์๋ฅผ ๋ ์งํฅํฉ๋๋ค.
    - ์ ์  ๋ฉ์๋๋ ํด๋์ค ๋ด์์๋ง ํธ์ถ๋์ด์ผ ํฉ๋๋ค.
    - ๋์  ์ธ์คํด์ค๋ฅผ ํฌํจํ๋ ๋ณ์๋ ํ์ ํด๋์ค์ ์์ฑ์ ๋ด๋ถ์์ ํธ์ถ๋์๋ ์ ๋ฉ๋๋ค.
    - ํ์ ํด๋์ค ๋ด์ ์ ์ธ๋์ง ์์ ์ ์  ๋ฉ์๋๋ ํธ์ถ๋์๋ ์ ๋ฉ๋๋ค.

1. ์์์ย `extends`ย ๋ฅผ ์ฌ์ฉํด์ฃผ์ธ์.

```
(O)
class PeekableQueue extends Queue {
  peek() {
    return this._queue[0];
  }
}
```

2. prototype์ ์ง์  ์กฐ์ํ์ง ์๊ณ  class๋ฅผ ์ฌ์ฉํด์ฃผ์ธ์.

3. toString() ๋ฉ์๋๋ฅผ ์ค๋ฒ๋ผ์ด๋ฉ ํ๋ ๊ฒ์ ํ์ฉํ์ง๋ง ์ฌ์ด๋ ์ดํํธ๊ฐ ๋ํ๋์ง ์๋๋ก ์ฃผ์ํด์ฃผ์ธ์.

### 5.2 ๋ชจ๋(Modules)

---

1. ๋นํ์ค ๋ชจ๋ ์์คํ์ด ์๋ ํญ์ (`import`/`export`)๋ฅผ ์ฌ์ฉํด์ฃผ์ธ์. 

```
(O)
import { es6 } from './NangmanStyleGuide';
export default es6;
```

2. wildcard import๋ ์ฌ์ฉํ์ง ๋ง์ญ์์ค.

```
(X)
import * as NangmanStyleGuide from './NangmanStyleGuide';
```

<aside>
โ single default export์์ ์ฃผ์ํด์ผ ํ  ํ์๊ฐ ์๊ธฐ ๋๋ฌธ์๋๋ค!

</aside>

3. import ๋ฌธ์ผ๋ก๋ถํฐ ์ง์  export ํ๋ ๊ฒ์ ํผํด์ฃผ์ธ์.

```
(X)
export { es6 as default } from './NangmanStyleGuide';

(O)
import { es6 } from './NangmanStyleGuide';
export default es6;
```

<aside>
โ ๊ฐ๊ฒฐํ ๋ฌธ์ฅ์ด์ง๋ง import์ export ๋ฐฉ๋ฒ์ ์ผ๊ด์ฑ์ ์ ์งํ๊ธฐ ์ํจ์๋๋ค!

</aside>

# 6. ์ ์ด๋ฌธ(Control statements)

### 6.1 ๋ฐ๋ณต๋ฌธ(loops)

---

1. ์ผ๋ฐ์ ์ธ for๋ฌธ๋ณด๋ค for-of ์ฌ์ฉ์ ๊ถ์ฅํฉ๋๋ค. ๊ฐ๋ฅํ๋ค๋ฉด map(), reduce()์ ๊ฐ์ ๊ณ ๊ธ ํจ์๋ฅผ ์ฌ์ฉํ์ญ์์ค. (5.1์ ๋ํ ์ด์ )

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

### 6.2 ์ค์์น๋ฌธ(switch)

---

1. ๋ค์ case ๊ตฌ๋ฌธ์ด ์คํ๋์ด์ผ ํ๋ค๋ฉด ์ฃผ์์ผ๋ก ์ด๋ฅผ ์ค๋ชํฉ๋๋ค.
2. default๋ฌธ์ ํญ์ ๋ง์ง๋ง์ ์์นํด์ผํฉ๋๋ค.

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

### 6.3 ์กฐ๊ฑด์๊ณผ ๋ฑ๊ฐ์(Comparison Operators and Equality)

---

1. `==`ย ์ด๋ย `!=`๋ณด๋คย `===`ย ์ย `!==`ย ์ ์ฌ์ฉํด ์ฃผ์ญ์์ค

2. if๋ฌธ๊ณผ ๊ฐ์ ์กฐ๊ฑด์์ `ToBoolean`ย ๋ฉ์๋์ ์ํ ๊ฐ์  ํ๋ณํ์ผ๋ก ํ๊ฐ๋์ด ํญ์ ๋ค์๊ณผ ๊ฐ์ ๊ฐ๋จํ ๋ฃฐ์ ๋ฐ๋ฆ๋๋ค.
- **์ค๋ธ์ ํธ**ย ๋ย **true**ย ๋ก ํ๊ฐ๋ฉ๋๋ค.
- **undefined**ย ๋ย **false**ย ๋ก ํ๊ฐ๋ฉ๋๋ค.
- **null**ย ์ย **false**ย ๋ก ํ๊ฐ๋ฉ๋๋ค.
- **๋ถ์ธ๊ฐ**ย ์ย **booleanํ์ ๊ฐ**ย ์ผ๋ก ํ๊ฐ๋ฉ๋๋ค.
- **์์น**ย ๋ย **true**ย ๋ก ํ๊ฐ๋ฉ๋๋ค. ํ์ง๋งย **+0, -0, or NaN**ย ์ ๊ฒฝ์ฐ๋ย **false**ย ์๋๋ค.
- **๋ฌธ์์ด**ย ์ย **true**ย ๋ก ํ๊ฐ๋ฉ๋๋ค. ํ์ง๋ง ๋น๋ฌธ์ย `''`ย ์ ๊ฒฝ์ฐ๋ย **false**ย ์๋๋ค.

3. ๋จ์ถํ์ ์ฌ์ฉํด์ฃผ์ธ์.

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

# 7. ๊ธฐํ(The Others)

### 7.1 ****์ดํฐ๋ ์ดํฐ์ ์ ๋๋ ์ดํฐ(Iterators and Generators)****

---

1. iterators๋ฅผ ์ฌ์ฉํ์ง ๋ง์ญ์์ค. `for-of`ย ๋ฃจํ ๋์ ์ย `map()`ย ๊ณผย `reduce()`ย ์ ๊ฐ์ JavaScript ๊ณ ๊ธํจ์(higher-order functions)๋ฅผ ์ฌ์ฉํด์ฃผ์ธ์.

<aside>
โ ๊ณ ๊ธํจ์๋ immutable(๋ถ๋ณ)๋ฃฐ์ ์ ์ฉํฉ๋๋ค. ๋ฐ๋ผ์ ๊ฐ์ ๋ฐํํ๋ ์์ ํจ์๋ฅผ ๋ค๋ฃจ๋ ๊ฒ์ด ๊ฐ๋จํ๊ธฐ ๋๋ฌธ์๋๋ค!

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

2. ํ ์์ ์์๋ generators๋ ์ฌ์ฉํ์ง ๋ง์ญ์์ค.

<aside>
โ ES5๋ก ํธ๋์คํ์ผ์ ์ ํ์ง ์๊ธฐ ๋๋ฌธ์๋๋ค!

</aside>

### 7.2 ํ๋กํผํฐ(Properties)

---

1. ํ๋กํผํฐ์ ์ ๊ทผํ  ๊ฒฝ์ฐ ์  `.` ์ ์ฌ์ฉํด์ฃผ์ธ์.

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

2. ๋ณ์๋ฅผ ์ฌ์ฉํ์ฌ ํ๋กํผํฐ์ ์ ๊ทผํ  ๊ฒฝ์ฐ ๋๊ดํธ `[]`๋ฅผ ์ฌ์ฉํด์ฃผ์ธ์.

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

### 7.3 ๋ธ๋ก(Block)

---

1. ๋ณต์ํ์ ๋ธ๋ก์๋ ์ค๊ดํธ ({})๋ฅผ ์ฌ์ฉํด์ฃผ์ธ์.

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

2. ๋ณต์ํ ๋ธ๋ก์ `if`ย ์ย `else`ย ๋ฅผ ์ด์ฉํ๋ ๊ฒฝ์ฐย `else`๋ย `if`ย ๋ธ๋ก ๋์ ์ค๊ดํธ(})์ ๊ฐ์ ํ์ ์์น์์ผ ์ฃผ์ญ์์ค.

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

### 7.4 ์ฝ๋ฉํธ(Comments)

---

1. ๋ณต์ํ ์ฝ๋ฉํธ๋ `/** ... */`ย ์ ์ฌ์ฉํด ์ฃผ์ธ์. ๊ทธ ์์๋ ์ค๋ช๊ณผ ๋ชจ๋  ํ๋ผ๋ฏธํฐ, ๋ฐํ ๊ฐ์ ๋ํด ํ์ด๋ ๊ฐ์ ๊ธฐ์ ํด์ฃผ์ธ์!

```jsx
(O)
/**
 * make() ํจ์๋ ์ ๋ฌ๋ฐ์ tag ์ด๋ฆ์ ๋ฐ๋ผ
 * ์๋ก์ด element๋ฅผ ๋ฐํํฉ๋๋ค.
 *
 * @param {String} tag
 * @return {Element} element
 */
function make(tag) {

  // ...stuff...

  return element;
}
```

2. ๋จ์ผํ ์ฝ๋ฉํธ์๋ `//`ย ์ ์ฌ์ฉํด ์ฃผ์ธ์. ์ฝ๋ฉํธ๋ฅผ ์ถ๊ฐํ๊ณ  ์ถ์ ์ฝ๋์ ์์ ์์ฑํด์ฃผ์ธ์. ๋ํ ์ฝ๋ฉํธ ์์ ๋นํ์ ๋ฃ์ด์ฃผ์ธ์.

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

3. ๋ฌธ์ ์ ๋ํ ์ฌํญ์ ๋ํด์๋ `FIXME -- ํด๊ฒฐ์ด ํ์` ๋ฅผ ์ฌ์ฉํด์ฃผ์ธ์.

```jsx
class Calculator extends Abacus {
  constructor() {
    super();

    // FIXME: ๊ธ๋ก๋ฒ๋ณ์๋ฅผ ์ฌ์ฉํด์๋ ์๋จ.
    total = 0;
  }
}
```

4. ๋ฌธ์ ์ ํด๊ฒฐ์ฑ์ ๋ํ ์ฃผ์์ผ๋ก `// TODO:`ย ๋ฅผ ์ฌ์ฉํด ์ฃผ์ธ์.

```jsx
class Calculator extends Abacus {
  constructor() {
    super();

    // TODO: total ์ ์ต์ ํ๋ผ๋ฉํฐ๋ก ์ค์ ํด์ผํจ.
    this.total = 0;
  }
}
```

### 7.5 ๊ณต๋ฐฑ(whitespace)

---

1. ํญ์๋ ์คํ์ด์ค 2๊ฐ๋ฅผ ์ค์ ํด์ฃผ์ธ์.

```jsx
(O)
function() {
โโconst name;
}
```

2. ์ฃผ์ ์ค๊ดํธ ({}) ์์๋ ์คํ์ด์ค 1๊ฐ๋ฅผ ๋ฃ์ด์ฃผ์ธ์.

```jsx
(O)
function test() {
  console.log('test');
}
```

3. ์ ์ด๊ตฌ๋ฌธ (`if`๋ฌธ์ด๋ย `while`๋ฌธ ๋ฑ)์ ์๊ดํธ (()) ์์๋ ์คํ์ด์ค 1๊ฐ๋ฅผ ๋ฃ์ด์ฃผ์ธ์. (ํจ์ ์ ์ธ์ด๋ ํจ์ ํธ์ถ ์ ์ธ์ ๋ฆฌ์คํธ์ ์์๋ ์คํ์ด์ค๋ฅผ ๋ฃ์ง ๋ง์์ฃผ์ธ์.)

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

4. ์ฐ์ฐ์ ์ฌ์ด์ ์คํ์ด์ค๋ฅผ 1๊ฐ ๋ฃ์ด์ฃผ์ธ์.

```jsx
(O)
const x = y + 5;
```

5. ๋ฉ์๋๋ฅผ ๊ธธ๊ฒ ์ฑ์ด๋ ํ๋ ๊ฒฝ์ฐ์๋ ์ธ๋ดํธ๋ฅผ ์ฌ์ฉํด์ฃผ์ธ์. ํ์ด ์๋ก์ด ๋ฌธ์ด ์๋ ๋ฉ์๋ ํธ์ถ์ธ ๊ฒ์ ๊ฐ์กฐํ๊ธฐ ์ํด์ ์  (.)์ ๋ฃ์ด์ฃผ์ธ์.

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

6. ๋ฌธ์ ์๊ณผ ๋ธ๋ก์ ๋ค์๋ ๋นํ์ ๋จ๊ฒจ์ฃผ์ธ์.

```jsx
(O)
const arr = [
  function foo() {
  },
	//๋นํ!!
  function bar() {
  },
];
	//๋นํ!!
return arr;
```

7. ๋ธ๋ก์๋ ๋นํ์ ๋ฃ์ง ๋ง์์ฃผ์ธ์.

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

8. ์๊ดํธ() ์์ชฝ์๋ ์คํ์ด์ค๋ฅผ ๋ฃ์ง ๋ง์์ฃผ์ธ์.

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

9. ๋๊ดํธ ([])์ ์์ชฝ์๋ ์คํ์ด์ค๋ฅผ ์ถ๊ฐํ์ง ๋ง์์ฃผ์ธ์.

```jsx
(X)
const foo = [ 1, 2, 3 ];
console.log(foo[ 0 ]);

(O)
const foo = [1, 2, 3];
console.log(foo[0]);
```

10. ์ค๊ดํธ ({})์ ์์ชฝ์๋ ์คํ์ด์ค๋ฅผ ์ถ๊ฐํด์ฃผ์ธ์.

```jsx
(X)
const foo = {clark: 'kent'};

(O)
const foo = { clark: 'kent' };
```

---
### Contributors
---
[์ดํ์](https://github.com/orgs/Nangman-corp/people/seok20)์ด ์์ฑํ์์ต๋๋ค.

- [Contributors](https://github.com/Nangman-corp/JavaScript-Style-Guide/graphs/contributors)
