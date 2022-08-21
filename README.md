# React Hooks

Esta es una documentacion sobre los principales Hooks de React.JS y su funcionamiento. Ademas de explicar como construirlos apropiadamente.

## ¿Por qué React Hooks?

Anteriormente, la lógica o información que cambiaba a lo largo de la aplicación era manejada con componentes basados en clases. Esto quiere decir que para trabajar con la información, se debía de construir un componente. Algo asi:

```
class BtnOld extends React.component {
    constructor(props) {
        super(props);
        this.state = {
            count: 0
        };
    }

    render() {
        return (
            <p>{this.state.count}</p>
        );
    }

}
```

Es un principio trabajar con componentes basados en clases era algo aceptable, sin embargo, a medida que la aplicacion escalaba, se generaba una serie de componentes anidados que crecia y crecia. Nada recomendable.

## Aparicion de los React Hooks

Es posible pensar en los hooks como bloques de construccion que me dan caracteristicas muy especiales las cuales no tendria en Vanilla Javascript.

Los hooks en si son **funciones** que siempre comienzan con la palabra _use_, porque estamos usando los superpoderes del framework React.

Sin embargo, antes de comenzar a explicar a detalle es importante conocer cuales son las restricciones de los hooks convencionales (esto no aplica para nuestros propios hooks personalizados).

1. Llamar los hooks en el nivel superior de un componente funcional.

```
function App() {

    //Correcto:
    useHook();

    //Incorrecto:
    const fun = () => {
        useHook();
    }

    //Incorrecto:
    return <button onClick={() => useHook()}> </button>
}
```
## Lista de hooks por abordar

**Hooks basicos**

- useState
- useEffect
- useContext

**Hooks adicionales**

- useReducer
- useCallback
- useMemo
- useRef
- useImperativeHandler
- userLayoutEffect
- useDebugValue
