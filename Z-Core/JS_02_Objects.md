---
related: "[[JS_00]]"
links: "[Урок 11](https://www.youtube.com/watch?v=t_B7hl1W65E&list=PL0MUAHwery4qn4Y27iUxmzC-JiauX7vSL&index=11)"
tags:
  - "#js/learn"
---
### Создание объекта
```js
const user = new Object(); // "object constructor" syntax
const user = {}; // "object literal" syntax
```

```js
const user = {
  login: "iamsuperhero",
  password: 123,
  'registration date': '01.01.2024',
  "last-auth": '05.04.2024'
  
  age: 33,
  isAdult: true,
  job: null,
  kids: undefined,
  address: {
    city: "Kharkiv",
    zipCode: 61064
  },
  sayHi: () => console.log('Hello'),
  sayBye() {
    alert(`Bye ${this.login}`)
  },
}
```
Свойства:
- ключ - всегда строка
- значение
Имя свойства с пробелом (с дефисом) в кавычках.
Доступ к свойству объекта через точку: `console.log(user.login)`
console.log(['registration date'])
`user.name = 'Serg'` - добавить свойство
`user['is developer'] = true` - добавить
`delete user.login` - удаление
`delete user['two word']`
### Вычисляемые свойства
```js
const propName = prompt('Имя?')
const propValue = prompt(`Значение для ${propName}?`)

const obj = {
  [propName]: propValue
}
```
`"key" in object` - проверка существования свойства
`for...in` - перебор свойств в объекте
```js
for (const key in obj) {
  alert(`${key}: ${user[key]}`) //name: value
}
```
`Object.keys(obj)` - получить массив ключей
### Копирование объекта
Старый способ:
```js
for (const key in obj1) {
  obj2[key] = obj1[key]
}
```
Современный:
```js
const obj1 = { name: 'Sergo' }
const obj2 = Object.assign( {}, obj1 ) //можно несколько объектов
или
const obj2 = { ...obj1 } //сокращенная запись, спрэд оператор
```
### Опциональная цепочка
```js
console.log(user.address?.city) //если свойства нет, то продолжить код
```
### Деструктуризация объекта
```js
const user = {
  name: 'Sergio',
  age: 41,
  isDeveloper: true
}
  
const name = user.name
const age = user.age
const isDeveloper = user.isDeveloper

или, сокращённая запись:
const {name, age, isDeveloper} = user
```
Пример на функции:
```js
const logAddress = (city, street, houseNumber, apartmentNumber) => {
  console.log(`
    Адрес:
    г.${city}, ул.${street},
    д.${houseNumber}, кв.${apartmentNumber}
    `)
}
  
logAddress('Kharkiv', 'Zhurnalistiv', 24, 72)
```
Упрощаем до такого вида: =>
```js
const logAddress = (address) => {
  console.log(`
    Адрес:
    г.${address.city}, ул.${address.street},
    д.${address.houseNumber}, кв.${address.apartmentNumber}
    `)
}
  
logAddress( {
  city: 'Kharkiv',
  street: 'Zhurnalistiv',
  houseNumber: 24,
  apartmentNumber: 72
})
```
Применяем деструктуризацию и ещё упрощаем =>
```js
const logAddress = (address) => {
  const {city, street, houseNumber, apartmentNumber} = address
  console.log(`
    Адрес:
    г.${city}, ул.${street},
    д.${houseNumber}, кв.${apartmentNumber}
    `)
}
  
logAddress( {
  city: 'Kharkiv',
  street: 'Zhurnalistiv',
  houseNumber: 24,
  apartmentNumber: 72
})
```
Деструктуризацию закидываем в параметры функции и сокращаем ещё код =>
```js
const logAddress = ({ city, street, houseNumber, apartmentNumber }) => {
  console.log(`
    Адрес:
    г.${city}, ул.${street},
    д.${houseNumber}, кв.${apartmentNumber}
    `);
};
  
logAddress( {
  city: 'Kharkiv',
  street: 'Zhurnalistiv',
  houseNumber: 24,
  apartmentNumber: 72
})
```
### Переименование переменных при деструктуризации
```js
const user = { name: 'Srgio'}
const admin = { name: 'Andrio'}
  
const {name: userName} = user
const {name: adminName} = admin
```
Значение по умолчанию при деструктуризации:
```js
const user = { name: 'Serg' }
const { name = 'не указано' } = user //если не указан name то ...
```
Переименование и значение по- умолчанию:
```js
const { city: userCity = 'Не указан' } = user
```
### Остаточные параметры ...rest
```js
const logUser = (user) => {
  const {name, age, city, ...otherInfo} = user
  console.log(`
    Имя: ${name},
    Возраст: ${age},
    Город: ${city}
    `)
    console.log(
      'Дополнительная информация:', otherInfo)
}
  
logUser({
  name: "Sergio",
  age: 41,
  city: "Kharkiv",
  company: "Google",
  jobPost: "Фронт-енд разработчик",
  yearsOfExperience: 30,
  hasCat: true
})
```
