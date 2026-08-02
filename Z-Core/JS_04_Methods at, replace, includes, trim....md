---
related: "[[JS_00]]"
tags:
  - "#methods"
  - "#js/learn"
links: "[Урок 14](https://www.youtube.com/watch?v=MGrpBVpctNo&list=PL0MUAHwery4qn4Y27iUxmzC-JiauX7vSL&index=14)"
---
str.length - длинна строки
str`[0]` - получить первый символ
str(str.length -1) - получить последний символ
str.at(0) - получить первый символ
str.at(-1) - получить последний символ
str.toLowerCase() - в нижний регистр
str.toUpperCase() - в верхний регистр
str.trim() - обрезает пробелы в начале и в конце строки
str.trimStart() - убрать пробелы в начале
str.trimEnd() - убрать пробелы в конце
str.indexOf() - получить индекс первого символа подстроки в строке
str.includes() - вернёт true \ false если подстрока есть \ нету
str.startsWith() - начало на ...
str.endsWith() - окончание на ...
str.substring() - обрезать строку
str.slice() - обрезать строку
str.repeat(n) - повторить строку n раз, вернёт новую строку
str.replace(что меняем, на что) - замена подстроки
str.replaceAll() - заменить все вхождения
str.replace( <span style="color: #43CFEA;">/</span>что<span style="color: #43CFEA;">/g</span>, на что ) - то-же изменит все вхождения
str.replace( <span style="color: #43CFEA;">/</span>что<span style="color: #43CFEA;">/gi</span>, на что ) - (без учёта регистра)
```js
const str = '+38 (050) 000-00-00' //заменить все цифры на #
str.replace( /\d/g, '#' ) //+## (###) ###-##-##
```
str.split( ', ' ) - разбить строку на массив, по разделителю `", "`
```js
let message = '  Привет!  '
  
console.log(`
  Сообщение до:
  "${message}"
  `) /*Сообщение до:
      "  Привет!  "*/
  
message = message.trim().toUpperCase().slice(0, 4)
  
console.log(`
  Сообщение после:
  "${message}"
  `) /*Сообщение после:
       "ПРИВ"*/
```
