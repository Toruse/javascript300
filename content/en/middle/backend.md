---
title: "Back-end"
weight: 208
---

# Back-end

## Чому Node.js однопотоковий, а не багатопотоковий?

## Що таке event driven development?

## Порівняйте fork() та spawn() методи.

## Розкажіть про Node.js фреймворки, які використовували. Яка між ними різниця?

## Опишіть словами код ендпоїнта, який повинен зберегти з клієнта файл розміром 4 гігабайти і покласти його на S3 або інший CDN.

## Що таке мікросервіси, навіщо їх використовують?

## У яких випадках ви б обрали моноліт, а в яких — мікросервіси?

## Як зрозуміти, що застосунок у певний момент працює справно?

## Як зрозуміти, що застосунок за останні три дні працював справно?

## Як відбувається перевірка правильності паролю при використанні bcrypt?

## Що таке JWT?

## Джуніор надіслав код на рев’ю. Що тут не так? Як виправити?

```javascript
router.post ( '/ users', async (req, res, next) => {
  const user = await db.createUser (req);

  if (user) {
    return res.json (users);
  }

  res.json ({error: "can not create user"})
})
```