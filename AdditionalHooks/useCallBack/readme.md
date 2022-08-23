# useCallback

Usado para memoize una función.

Cuando defino una funcion en un componente, un objeto de una funcion es creado cada vez que el componente es renderizado, esto generalmente no es un problema, pero a veces es necesario memoizar una funcion.

Un uso bastante comun es cuando paso la misma funcion a muchos componentes hijos (especialmente con listas grandes).

Haciendo un wrapping de la funcion en un _useCallback_ , puedo prevenir renders innecesarios de los hijos porque siempre estarían usando el mismo objeto de la función.

function App() {

    const [count, setCount] = useState(60);

    const showCount = useCallback(() => {
        alert(`Count ${count}`)
    }, [count])

    return <> <SomeChild handler={showCount} /> </>;

}
