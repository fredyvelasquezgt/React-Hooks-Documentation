# useMemo

Me ayuda a optimizar los costos de cómputo para mejorar el rendimiento. Lo uso cuando sé que voy a tener que exigir mucho rendimiento.

Memoization: Técnica de optimización que hace a las apps más rápidas. Cache resultante de la llamada de una función.

Precaución: Solo se debe de optimizar el cómputo si es necesario para cálculos costosos.

Volvamos al ejemplo del contador: Asumamos que tenemos un contador pero a la vez existe una función que desempeña una operación compleja (expensiveCount)

```
function App() {

    const [ count, setCount ] = useState(60);

    const expensiveCount = useMemo(() => {
        return count**2;
    })

    return <> </>;

}
```

En lugar de volver a computar en cada renderización, podemos memoize el valor. Escribimos una funcion que retorne el valor computado, luego, como segundo argumento agregamos las dependencias para determinar cuando la computación debería de correrse, en este caso, sería cuando el valor de **count** cambie.
Esto es bueno para un valor memoizado pero también se puede aplicar para una función.

```
function App() {

    const [ count, setCount ] = useState(60);

    const expensiveCount = useMemo(() => {
        return count**2;
    }, [count])

    return <> </>;

}
```
