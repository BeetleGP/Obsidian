---
related: "[[JS_00]]"
links: "[Урок 12](https://www.youtube.com/watch?v=cYx5ckAYhK8&list=PL0MUAHwery4qn4Y27iUxmzC-JiauX7vSL&index=12)"
tags:
  - "#methods"
  - "#js/learn"
---
Глобальный this - это объект window в браузере (с "use strict" = undefined).
this в методе объекта - вернёт этот объект.
У стрелочных функций, нет своего this.
## Methods of primitives
### .toFixed()
```js
const price = 99.5555
price.toFixed() //100
price.toFixed(1) //99.6
price.toFixed(2) //99.56
```
.toFixed() - округление до целого
- 2..toFixed(2) - 2 знака после запятой //2.00
- (2.011)..toFixed(2) //2.01
### .toPrecision
(100.055).toPrecision(4) //100.1 округляет с первой цифры
### .toString()
Приводит к строке (например число)
100..toString(2) //1100100 переводит в двоичную систему (можно от 2 до 36)
### Объект Math
Math.random() - получить рандомное число
Math.abs(-100) //100 - получить из отрицательного положительное
Math.pow(2, 10) //1024 - возведение в степень 2 ** 10
Math.sqrt(16) //4 - извлечь квадратный корень из числа
Math.cbrt(125) //5 - извлечь кубический корень из числа
Math.max(1, 5, 200) //200 - вернёт максимальное число
Math.min(2, 6, -4) //-4 - вернёт минимальное число
Math.round() - округляет до ближайшего целого
Math.floor(-1.1) //-2 - округляет до ближайшего целого вниз
Math.ceil() - округляет до ближайшего целого вверх
Math.trunc(-1.1) //-1 - округляет до целого в меньшую сторону
[Таблица с округлениями](https://javascript.info/number#rounding)
### parseInt()
parseInt('100px') //100 - вернёт число из строки
### parseFloat()
parseFloat('1.2em') //1.2 - вернёт число с запятой из строки