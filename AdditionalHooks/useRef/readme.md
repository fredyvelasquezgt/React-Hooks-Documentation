# useRef

Este hook me permite crear un objeto mutable el cual tendrá la misma referencia entre renders.

Se puede utilizar cuando manejo un valor que cambia como lo es un _setState_, sin embargo, este hook no vuelve a renderiz el UI cuando existe un cambio en el valor.

Se puede apreciar mejor el funcionamiento con este ejemplo:

```
function App() {
    const count = useRef(0);

    return (
        <button onClick={() => count.current ++}>
            {count.current}
        </button>
    )
}
```

En el código de arriba podemos apreciar como el botón está haciendo referencia al valor actual del _useRef_, inclusive, está en el interior del onClick del botón.

```
function App() {

    const myBtn = useRef(null);

    const clickIt = () => myBtn.current.click()

    return (
        <button ref={myBtn}>
        </button>
    );
}
```

Imaginemos por un momento que estamos manejando un contador. En el código de arriba, por más que presionemos el botón, este nunca cambiaría el valor en el UI, ya que, a diferencia del _setState_, _useRef_ no dispara una nueva renderización.

## Otros usos

El _useRef_ también se puede utilizar para interactuar con elementos nativos de HTML que estén en el JSX.

```
function App() {

    const myBtn = useRef(null);

    const clickIt = () => myBtn.current.click()

    return (
        <button ref={myBtn}> </button>
    );
}
```

Dentro del botón se hace referencia a la referencia establecida en null. Con la constante clickIt apuntamos hacia el botón y su propiedad de hacer _click_
