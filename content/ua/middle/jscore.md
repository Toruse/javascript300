---
title: "JS Core"
weight: 202
---

# JS Core

## Які типи даних бувають у JavaScript? Який буде результат виконання коду?

```javascript
let firstObj = { name: 'Hello' };

let secondObj = firstObj;

firstObj = { name: 'Bye' };

console.log(secondObj.name);
```

## Що таке temporal dead zone?

## Як працює boxing / unboxing у JavaScript?

## У чому різниця між оператором in і методом hasOwnProperty?

## Опишіть, за допомогою чого в JS реалізуються такі ООП-парадигми, як інкапсуляція, поліморфізм, абстракція?

## Що таке прототип? Як працює прототипне наслідування в JS? Поясніть роботу коду.

```javascript
function Main () {}
Main.prototype = { protected: true };

const obj = new Main();
Main.prototype = { protected: false };

console.log('Object protection: ', obj.protected); 
```

## Яка різниця між композицією та наслідуванням?

## Чому не варто використовувати конструктори типу new String?

## Розкажіть про базовий пристрій і механізм роботи Event loop.

## Що таке записи (records) і кортежі (tuples)? Чим вони відрізняються від звичайних об’єктів?

## Які відмінності в поведінці ES5 функції-конструктора та ES2015 класу?

## Як реалізувати патерн «Модуль»?

## Чому typeof null повертає object?

## Що таке приведення (перетворення) типів у JS?

## Що таке явне і неявне приведення (перетворення) типів даних у JS? Як відбувається перетворення типів у таких прикладах:

```javascript
{}+[]+{}+[1]
!!"false" == !!"true"
['x'] == 'x'
```

## Що таке Garbage Collector?

## Опишіть основні принципи роботи «збирача сміття» у JS-рушіях (engines).

## Опишіть призначення і принципи роботи з колекціями WeakMap і WeakSet? Чим вони відрізняються від колекцій Map і Set відповідно?

## Чим відрізняється Observable від Promise?

## Що таке Promise? Назвіть порядок виконання then і catch у ланцюжку.

```javascript
Promise.resolve(10)
  .then(e => console.log(e)) // ??
  .then(e => Promise.resolve(e))
  .then(console.log) // ??
  .then(e => {
    if (!e) {
      throw 'Error caught';
    }
  })
  .catch(e => {
    console.log(e); // ??
    return new Error('New error');
  })
  .then(e => {
    console.log(e.message); // ??
  })
  .catch(e => {
    console.log(e.message); // ??
  });
```

## Розкажіть про послідовне і паралельне виконання асинхронних функцій. У чому різниця між Promise.all () і Promise.allSettled ()?

## Що таке дескриптори властивостей об’єктів? Розкажіть про їхнє практичне застосування.

## Назвіть кілька способів створення незмінного об’єкта в JavaScript.

## Як створити властивість в об’єкта, яку не можна буде змінити?

## Навіщо потрібен конструктор Proxy? Наведіть приклад використання.

## Що таке ArrayBuffer? У чому різниця між Uint32Array і Float32Array? Який результат виконання коду?

```javascript
const uint32Array = new Uint32Array();
Array.isArray(uint32Array);
```

## Яким буде результат порівняння?

```javascript
const url = “HTTPs://xyz.com/path<to>page.html”;
encodeURI(url) == encodeURIComponent(url); 
```

## Розкажіть про генератори та ітератори.

## Поясніть, що робить наведений код:

```javascript
function * fn(num) {
  for (let i = 0; i < num; i += 1) {
    yield console.log(i);
  }
}
const loop = fn(5);
loop.next();
loop.next();
```

## Розкажіть про тип даних Symbol і його практичне застосування. Як перевести число з 10-розрядної системи в 16(2,8)-розрядну систему числення?