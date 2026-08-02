---
related: "[[JS_00]]"
links: "[Урок 15](https://www.youtube.com/watch?v=n9K4P420uh0&list=PL0MUAHwery4qn4Y27iUxmzC-JiauX7vSL&index=15)"
tags:
  - "#js/learn"
---
### Declaration
```js
const arr = new Array();
const arr = [];
```
```js
const arr = [
  'Привет',
  1000,
  true,
  { name: 'Александр' },
  () => console.log('some message...'),
  [true, true, true],
];
```
`arr[0]` - вернёт 1 элемент массива // Привет
`arr[3]`.name // Александр или arr`[3]['name']`
`arr[4]()` - some message...
`arr[5][0]` - true
### Многомерный массив
```js
const matrix = [
  [1, 2, 3],
  [4, 5, 6],
  [7, 8, 9],
];

console.log(matrix[1][0]); // 4
```
`arr[2] = 'Пока';` // Замена значения в элементе
arr.length - длинна массива
arr[arr.length -1] - последний элемент
arr.at(-1) - последний элемент
### Methods arrays
<span style="color: #52EEA3;">arr.push()</span> - добавить <span style="color: red;">элемент(ы)!</span> в конец массива ('a', 'b')
<span style="color: #54B6F8;">arr.unshift()</span> - добавить <span style="color: red;">элемент(ы)!</span> в начало массива ('a', 'b')
<span style="color: #52EEA3;">arr.pop()</span> - удалит <span style="color: red;">и вернёт!</span> последний элемент из массива. В аргументы ничего передавать не нужно. `console.log(arr.push()) //вернёт удалённый элемент`
<span style="color: #54B6F8;">arr.shift()</span> - удалит <span style="color: red;">и вернёт!</span> первый элемент из массива.
arr.toString() - массив к строке. Аргументы пусто!
arr.join() - массив к строке. Если в аргументах пусто, работает как `toString()`
arr.join(', ') - добавить украшательства (запятую и пробел)
### Копирование массивов
```js
const arr1 = [1, 2, 3];
const arr2 = [...arr1];
variant_2
arr2 = arr1.slice();
```
arr2 = arr1.slice(0, 2); //копировать часть массива с 0 - 2
### Объединение массивов
```js
const totalArr = [...arr1, ...arr2];
Variant_2
const totalArr = arr1.concat(arr2);
```
Array.isArray(value1) - проверяет является ли value1 массивом
