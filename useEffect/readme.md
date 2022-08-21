# useEffect

Este hook es uno de los mas complejos de entender, pero haremos todo lo posible por hacerlo.

Es primordial conocer primero el ciclo de vida de vida de los componentes.

## Ciclo de vida de los componentes

En codigo, es algo parecido a esto:

```
componentDidMount() {
    //El componente se agrega al UI o se monta, esto solo puede suceder una vez.
}


componenteDidUpdate() {
    //La informacion es actualizada. Puede suceder varias veces.
}


componenteWillUnmount() {
    //El componente se remueve del UI o se desmonta. Solo pasa una vez.
}
```

El _useEffect_ me permite agregarle logica a cada uno de los procesos anteriores.

Ahora estudiemos la estructura del _useEffect_

1. Como primer argumento toma una funcion definida por mi.

React corre esta funcion cuando el componente es montado o cuando el estado cambia.

2. El segundo argumento es un **array** de dependencias.

- Si se agrega un **array vacio** quiere decir que no hay dependencias, esto significa que solo se correra una vez: cuando el componente es inicializado.

- Agregar el estado. Agregar el estado en el array significa que React seguira este valor y correra la funcion que definimos cada vez que el estado cambie.

```
useEffect(() => {
    //Alguna funcion construida por mi
}, [//array con dependencias])
```

Finalmente, tambien se puede correr codigo cuando el componente es destruido, esto se implementa retornando una funcion desde el **callback** del _useEffect_

```
useEffect(() => {

    return () => alert('adios!')
})
```
