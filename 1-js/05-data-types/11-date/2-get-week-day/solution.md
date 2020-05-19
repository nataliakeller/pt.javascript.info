O método `date.getDay()` retorna um número da semana, começando pelo domingo.

Então, criamos um array dos dias da semana, para que possamos pegar os nomes pelos seus respectivos números:

```js run demo
function getWeekDay(date) {
  let days = ['DOM', 'SEG', 'TER', 'QUAR', 'QUI', 'SEX', 'SAB'];

  return days[date.getDay()];
}

let date = new Date(2014, 0, 3); // 3 Jan 2014
alert( getWeekDay(date) ); // SEX
```
