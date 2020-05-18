O construtor `new Date` usa a hora local por padrão. Então, a única coisa importante para se lembrar é que a contagem dos meses começa do zero.

Portanto, fevereiro é o número 1. 

```js run
let d = new Date(2012, 1, 20, 3, 12);
alert( d );
```
