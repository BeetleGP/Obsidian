---
related: "[[JS_00]]"
tags:
  - "#js/learn"
links: "[Урок 9](https://www.youtube.com/watch?v=IcgdjdeOziA&list=PL0MUAHwery4qn4Y27iUxmzC-JiauX7vSL&index=10)"
---
`<script src="script.js"></script>` между `<body>` в конце страницы.
`// однострочный комментарий` <span style="color: #9446F8;">CTRL+?</span> `||` `/*многострочный*/` <span style="color: #9446F8;">SHIFT+ALT+A</span>
<span style="color: #EE6748;">Динамическая типизация!</span>
<span style="color: #52eea3;">var, let, const</span> - объявление.
<span style="color: #52eea3;">let</span> <span style="color: #E54F9D;">message</span> = <span style="color: #FFD85E;">"hello"</span> - объявление и присваивание значения переменной.
<span style="color: #51E1E9;">console.log(<span style="color: #E54F9D;">message</span>)</span> - вывод в консоль (F12).
<span style="color: #52eea3;">var</span> - можно использовать до объявления! Результат `undefined`
<span style="color: #52eea3;">let</span> - можно переназначать.
<span style="color: #52eea3;">const</span> - нельзя переназначать.
"use strict" - включает современные правила.
```js
'use strict' // без, будет работать
age = 10
console.log(age) // Ошибка!
```
<span style="color: #52eea3;">let</span> <span style="color: #E54F9D;">1name, my-name</span> - Error! Имя нельзя с цифры начинать, дефис нельзя!
8 - типов данных.
- 6 - примитивов (string, number, boolean, bigint, symbol, undefined)
- 2 - специальных (object, null)
String - заключаются в кавычки `"" '' backticks``
typeof - показать тип 
`typeof (2 + 3)` - выражения в скобки.
`typeof null` - object. БАГ!
### Преобразования
`1 + "2" = "12"` - число + строка = строка
`"16" / "8" = 2` - строка / строка = число (все мат. операторы к числу)
`Number(str) или +"str"` - к числу 
`Boolean(num) или !!0` - к бул.
`String(num)` - к строке,
`Number(true) // 1` `Number(false) // 0` `Number(null) // 0`
`Boolean(0, NaN, '', null, undefined) // 0` остальное true!
### Математика
`**` - возведение в степень (2 ** 10 = 1024)
`%` - остаток от деления (15 % 3 = 3)
Арифметика с присваиванием `num = num + 2` => `num += 2`
`++` - инкремент (`num++` - постфиксная, вернёт старое значение)
`--` - декремент (`num--` - префиксная, вернёт новое значение)
= =    - нестрогое равенство приводит к типам `2 == "2" // true`
= = =    - строгое равенство, не приводит к типам `2 === "2" // false`
### if else
```js
if (cond) {
  code...
} else if (cond) {
  code...
} else {
  code...
}
```
### Тернарный оператор
```js
let result = condition ? value1 : value2
```
### Логические операторы
`||` - или, `&&` - и
`false || false // false`  |  `false && false // false`
`false || true // true`    |  `false && true // false`
`true || false // true`    |  `true && false // false`
`true || true // true`     |  `true && true // true`
### Оператор нулевого слияния
```js
let result = (a !== null && a !== undefined) ? a : b
```
Если а не равно null и не равно undefined
`??` - проверяет что-бы значение не было null или undefined
```js
let result = a ?? b
```
### Prompt
`[]` - необязательный параметр, можно не вводить.
```js
result = prompt(title,[defualt])
```
`Esc` = `null`
`prompt` - вернёт строку! 
`+prompt` - вернёт число.
### Confirm
```js
result = confirm(question)
```
return - `ok presset` true / false - `otherwise (в противном случае, иначе)`
### switch
```js
switch (x) {
  case 'value1': // if (x === 'value1')
    ...
    [break]
  case 'value2':
    ...
    [break]
  default:
    ...
    [break]
}
```
### while
```js
while (condition) {
  code
}
```
### do...while
```js
do {
  //loop body
} while (condition)
```
### for
```js
for (begin; condition; step) {
  //...loop body...
}
```
# function
### function declaration
```js
function showMessage() {
  alert('Hello everyone')
}

showMessage() //call
```
function declaration - можно использовать до её объявления.
### function expressions
```js
let logHello = function() {
  alert('Hello')
}
```
### Arrow functions
```js
let logHello = () => {
  alert('Hello')
}
```
нет arguments
нет this