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
