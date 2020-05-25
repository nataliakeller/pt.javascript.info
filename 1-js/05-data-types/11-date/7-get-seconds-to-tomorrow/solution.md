Para obter o número de milissegundos até amanhã, nós podemos subtrair de “amanhã às 00:00:00” a data atual. 

Primeiro, nós geramos esse "amanhã":

```js run
function getSecondsToTomorrow() {
  let now = new Date();

  // data de amanhã
  let tomorrow = new Date(now.getFullYear(), now.getMonth(), *!*now.getDate()+1*/!*);

  let diff = tomorrow - now; // diferença em milissegundos
  return Math.round(diff / 1000); // converte para segundos
}
```

Solução alternativa:

```js run
function getSecondsToTomorrow() {
  let now = new Date();
  let hour = now.getHours();
  let minutes = now.getMinutes();
  let seconds = now.getSeconds();
  let totalSecondsToday = (hour * 60 + minutes) * 60 + seconds;
  let totalSecondsInADay = 86400;

  return totalSecondsInADay - totalSecondsToday;
}
```

Por favor, tome nota que em vários países é utilizado o horário de verão, então é possível que existam dias com 23 ou 25 horas. Podemos tratar estas exceções separadamente.
