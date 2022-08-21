# useState

Se denomina **estado** a cualquier informacion que cambia en la aplicacion. _useState_ me sirve para que la informacion que ha cambiado pueda verse reflejada para el usuario.

El _useState_ ayuda a que el UI se actualice cuando el estado cambia. EL _useState_ se ve asi:

```
const [count, setCount] = useState(0)
```

Se utiliza un array para que sea facil desestructurar los valores que tienen en su interior. Dentro de los parentesis del _useState_ se coloca el valor inicial del estado.

El primer elemento del array es el _valor reactivo_ el cual sufrira los cambios durante la aplicacion, cuando eso pase, React se encargara de renderizar el UI con los ultimos cambios.

Por otra parte, el segundo elemento de array se denomina _setter_ el cual es el encargdo de modificar el _valor reactivo_

Una implementacion mas clara del _useState_ es la siguiente:

```
//Importante siempre importarlo
import { useState } from 'react';

function App() {

    //inicializar el useState
    const [count, setCount] = useState(0)

    return (
                               //uso del setter para cambiar el valor reactivo
        <button onClick={() => setCount(count + 1)}>
        {count}
        </button>
    )
}

```
