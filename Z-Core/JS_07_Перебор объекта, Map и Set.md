---
related: "[[JS_00]]"
links: "[Урок 17](https://www.youtube.com/watch?v=vm-M4m-OH0U&list=PL0MUAHwery4qn4Y27iUxmzC-JiauX7vSL&index=17)"
tags:
  - "#js/learn"
---
```js
const user = {
  name: "Serg",
  age: 41,
  city: "Kharkiv"
}
  
const userKeys = Object.keys(user); // получить массив ключей
  
console.log("userKeys: ", userKeys);
  
userKeys.forEach((key) => { // перебор ключей
  console.log("Имя свойства: ", key);
})
```
```js
const user = {
  name: "Serg",
  age: 41,
  city: "Kharkiv"
}
  
const userValues = Object.values(user); // получить массив значений
  
console.log("userValues: ", userValues);
  
userValues.forEach((value) => { // перебор значений
  console.log("Значение свойства: ", value);
})
```
