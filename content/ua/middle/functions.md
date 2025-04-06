---
title: "Функції"
weight: 203
---

# Функції

## Поясніть, що означає currying. Наведіть приклад використання на практиці.

## Наведіть приклад функції з мемоізацією. Коли варто застосовувати цю техніку?

## Що таке чейнінг функцій? Напишіть приклад з використанням цього підходу.

## У чому різниця між function і arrow function? Яким буде результат виконання коду?

```javascript
const pluckDeep = key => obj => key.split('.').reduce((accum, key) => accum[key], obj)

const compose = (...fns) => res => fns.reduce((accum, next) => next(accum), res)

const unfold = (f, seed) => {
    const go = (f, seed, acc) => {
        const res = f(seed)
        return res ? go(f, res[1], acc.concat([res[0]])) : acc
    }
    return go(f, seed, [])
}
```