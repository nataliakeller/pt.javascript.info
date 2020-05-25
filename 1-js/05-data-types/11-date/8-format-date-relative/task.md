importance: 4

---

# Formate a data

Escreva uma função `formatDate(date)` que deve seguir o formato `date` a seguir:

- Se desde `date` passou menos de um segundo, então retorne `"right now"`.
- Caso contrário, se desde `date`passou menos de 1 minuto, então retorne `"n sec. ago"`.
- Caso contrário, se passou menos de uma hora, então retorne `"m min. ago"`.
- Caso contrário, a data inteira no formato `"DD.MM.YY HH:mm"`. Ou seja: `"day.month.year hours:minutes"`, todos em formato de 2 dígitos, por exemplo, `31.12.16 10:00`.

Por exemplo:

```js
alert( formatDate(new Date(new Date - 1)) ); // "right now"

alert( formatDate(new Date(new Date - 30 * 1000)) ); // "30 sec. ago"

alert( formatDate(new Date(new Date - 5 * 60 * 1000)) ); // "5 min. ago"

// data de ontem no formato 31.12.2016, 20:00
alert( formatDate(new Date(new Date - 86400 * 1000)) );
```
