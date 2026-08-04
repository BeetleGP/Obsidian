---
related: "[[JS_00]]"
links: "[Урок 16](https://www.youtube.com/watch?v=SjTTDZX2hIA&list=PL0MUAHwery4qn4Y27iUxmzC-JiauX7vSL&index=16)"
tags:
  - "#js/learn"
  - "#methods"
---
### Деструктуризация
```js
const data = ['Александр', 20];

const name = data[0];
const age = data[1];
or
const [name, age] = data; //порядок важен!
```
### Перебор .forEach()
```js
arr.forEach(function(item, index, array) {
  ...some code
});
```
```js
const letters = ["А", "Б", "В", "Г", "Д"];
//старый способ  
for (let i = 0; i < letters.length; i++) {
  console.log(letters[i]);
}
//современный
letters.forEach((item) => {
  alert(item);
});
```
### .indexOf()
```js
const prices = [100, 200, 444, 500, 444, 670];
  
console.log(prices.indexOf(444, 3)); //найти 444 с 3 позиции 
```
.lastIndexOf(444, 3) - с конца ищет
### .includes(444, 3)
.reduce() - суммирует элементы
.reverse() - поменять наоборот элементы массива
.sort() - сортирует массив
