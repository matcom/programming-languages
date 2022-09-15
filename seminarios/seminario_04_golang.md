# Seminario 4 (Golang)

Los requerimientos de cada ejercicio del seminario serán expuestos desde el punto de vista práctico y teórico; es decir, para su exposición, cada equipo se basará en el caso práctico en cuestión para introducir y explicar el elemento teórico requerido. La exposición no es una mera enunciación de código. Preguntas como: _¿Por qué?, ¿Basándose en qué?, ¿Cómo se logra esto en el lenguaje X?_ entre otras, deben hacerse.

Todos los miembros del equipo deben participar en la solución del ejercicio y estar preparados para exponer todo el trabajo. **La persona a exponer*1. se decide el día de la exposición. Quién no esté presente en la exposición de su equipo tiene `0` en la evaluación. (Note que estas notas se promedian y hay distinción entre `0` y `2`).

---

1. ¿Cúal es la forma de procesamiento del código fuente utilizada?
1. `Go` es un lenguaje moderno con muchísimas decisiones de diseño intencionales.
    1. ¿Qué ventajas y desventajas le da al lenguaje su forma de procesamiento? Tome en cuenta las plataformas sobre las que se usa para elaborar su respuesta.
1. Realice un sumario sobre las características más interesantes de la sintaxis en `Go`:
    * Presente un Hello World (creatividad apreciada)
    * Creación de variables
    * Ciclos `for`
    * Indentación
    * Condiciones  if` con declaración de variables en la condición
    * Funciones con múltiples retornos
    * Otros elementos de la sintaxis que considere relevante mostrar. (Piense que va a vender el lenguaje a una persona)
1. Presente los tipos nativos.
1. Comente sobre `nil` y valores por defecto.
1. Arrays y slices en `Go`.
    1. Métodos nativos `make`, `append`, `copy`.
    1. ¿Son los `slices` listas dinámicas?
    1. Compare los arrays y slices de `Go` con los array nativos o listas dinámicas de `C#` o `C++`.
1. ¿Los tipos en `Go` son por referencia o por valor?
    1. ¿Qué son los punteros en `Go`?
    1. ¿Qué se puede hacer con ellos?
    1. ¿Son seguros?
    1. ¿Por qué es seguro referenciar en `Go` a una variable local de un método?
    1. Haga una comparación con los punteros de `C` o `C++`.
1. ¿Qué significa el keyword `defer`?
1. Presente los `structs` en `Go` y compárelos con los de `C`.
1. ¿Qué es la composición de tipos?
    1. ¿Qué son las interfaces en `Go`?
    1. Haga una comparación entre composición de tipos y herencia.
    1. Valore ventajas y desventajas de la composición de tipos de `Go` y exprese su preferencia.
1. ¿Se puede decir que `Go` es un lenguaje que ofrece programación orientada a objetos?
1. Implemente una jerarquía de clases del seminario de genericidad (Seminario 3) usando `structs` e `interfaces`. Trate de que los métodos sólo reciban tipos nativos o interfaces.
    1. ¿Le resultó más cómodo que usar herencia?
    1. ¿Le resulta más seguro?
    1. ¿Le resulta más expresivo?
1. Argumente el poder que tiene la programación con interfaces para el desarrollo de software, sobre todo el poder que ofrecen las interfaces de `Go` y `C#`.
1. ¿Cómo maneja `Go` las excepciones y errores en ejecución?
1. ¿Cómo es la genericidad de tipos en `Go`?.
    1. Explique las principales diferencias respecto a la genericidad de `C++` y de `C#`.
