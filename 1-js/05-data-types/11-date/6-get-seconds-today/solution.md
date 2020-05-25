Para conseguirmos o número de segundos, nós podemos gerar uma data usando o dia atual e hora 00:00:00, então subtrai-lo de “agora”.

A diferença é o número de milissegundos passados desde o começo do dia, que devemos dividir por 1000 para obter os segundos. 

```js run
function getSecondsToday() {
  let now = new Date();

  // crie um objeto usando o dia/mês/ano atual
  let today = new Date(now.getFullYear(), now.getMonth(), now.getDate());

  let diff = now - today; // diferença em milissegundos
  return Math.round(diff / 1000); // transforma em segundos
}

alert( getSecondsToday() );
```

Uma solução alternativa seria pegar as horas/minutos/segundos e converte-los para segundos.

```js run
function getSecondsToday() {
  let d = new Date();
  return d.getHours() * 3600 + d.getMinutes() * 60 + d.getSeconds();
}
```
