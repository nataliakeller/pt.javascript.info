importance: 4

---

# Qual dia do mês foi a alguns dias atrás?

Crie uma função `getDateAgo(date, days)` para retornar o dia do mês (`days`) de dias atrás da data (`date`). 

Por exemplo, se hoje é dia 20, então `getDateAgo(new Date(), 1)` deve ser dia 19 e `getDateAgo(new Date(), 2)` deve ser dia 18. 

Deve funcionar também de forma confiável se `days=365` (ou maior):

```js
let date = new Date(2015, 0, 2);

alert( getDateAgo(date, 1) ); // 1, (1 Jan 2015)
alert( getDateAgo(date, 2) ); // 31, (31 Dec 2014)
alert( getDateAgo(date, 365) ); // 2, (2 Jan 2014)
```

P.S. A função não deve modificar o objeto `date`.
