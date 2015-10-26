Hasta ahora trabajamos con individuos _simples_, de dos tipos:

* átomos, como por ejemplo `joffrey` o `sansa`
* números, como por ejemplo `42` o `65`

Con sólo estas dos cosas pudimos resolver muchos problemas.

Por ejemplo, si queremos modelar personajes de [Game Of Thrones](https://es.wikipedia.org/wiki/Game%20of%20Thrones), de los que conocemos su edad y sexo, podríamos construir nuestra base de conocimientos
de la siguiente forma:

```prolog
edad(jonSnow,18).
edad(sansa, 15).

sexo(jonSnow, hombre).
sexo(sansa, mujer).
```

Con lo que podemos consultar la base de conocimientos de la siguiente forma (para saber la edad de [Jon Snow](https://es.wikipedia.org/wiki/Jon%20Snow)):

```prolog
> edad(jonSnow, EdadJon), sexo(jonSnow, SexoJon).
EdadJon = 18,
SexoJon = hombre.
```

Sin embargo, como vemos es un poco engorroso trabajar de esta manera porque:

* para cada propiedad de cada persona tenemos que tener una cláusula
* consultar por sus propiedades es engorroso

Por eso a continuación veremos una forma alternativa de modelar en Prolog:
usando _individuos compuestos_, en particular: **functores**.
