---
title: "Практичні завдання"
weight: 211
---

# Практичні завдання

## Напишіть функцію Sleep (ms), яка зупиняє виконання async-функції на заданий проміжок часу.

## Реалізуйте один з методів масиву (наприклад, splice).

## Напишіть функцію з RegExp для знаходження всіх HTML-посилань у рядку.

## Реалізуйте функцію, яка виконає callback для всіх елементів певної гілки DOM-дерева.

## Реалізуйте таблицю з віртуальним скролом.

## Реалізуйте функцію перетворення URL query рядка в JSON.

```javascript
const inData = "user.name.firstname=Bob&user.name.lastname=Smith&user.favoritecolor=Light%20Blue";


function queryObjectify(arg) {
// ??
}

queryObjectify(inData)
/* Результатом виконання для вхідного рядка, повинен бути наступний об’єкт
{
  'user': {
    'name': {
      'firstname': 'Bob',
      'lastname': 'Smith'
    },
    'favoritecolor': 'Light Blue'
  }
};
*/
```

## Реалізуйте функцію знаходження перетину двох масивів.

```javascript
const first = [1, 2, 3, 4];
const second = [3, 4, 5, 6];

function intersection (a, b) {
// ??
}

intersection(first, second) // -> [3, 4]
```

## Реалізуйте функцію / клас для генерації HTML.

```javascript
const HTMLConstruct = {};

HTMLConstruct.span('foo'); // -> <span>foo</span>
HTMLConstruct.div.span('bar'); // -> <div><span>bar</span></div>

HTMLConstruct.div.p(
HTMLConstruct.span('bar'),
HTMLConstruct.div.span('baz')
); // -> <div><p><span>bar</span><span>baz</span></p></div>
```

## Якщо є проєкт з обмеженими термінами та некритичною продуктивністю, чим будете керуватися при виборі бібліотек, підходів? Чи все ж будете звертати увагу на продуктивність? Або навпаки: терміни нелімітовані, продуктивність важлива. Ваші дії?