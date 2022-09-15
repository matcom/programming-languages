# Seminario 1 (C++98, C++0x)

Los requerimientos de cada ejercicio del seminario serán expuestos desde el punto de vista práctico y teórico; es decir, para su exposición, cada equipo se basará en el caso práctico en cuestión para introducir y explicar el elemento teórico requerido. La exposición no es una mera enunciación de código. Preguntas como: _¿Por qué?, ¿Basándose en qué?, ¿Cómo se logra esto en el lenguaje X?_ entre otras, deben hacerse.

Todos los miembros del equipo deben participar en la solución del ejercicio y estar preparados para exponer todo el trabajo. **La persona a exponer** se decide el día de la exposición. Quién no esté presente en la exposición de su equipo tiene `0` en la evaluación. (Note que estas notas se promedian y hay distinción entre `0` y `2`).

---

Implemente una clase `vec` para representar vectores algebraicos en `C++` (con los elementos disponibles en el lenguaje hasta antes de `C++11` `(C++0x)`) que cumpla los siguientes requerimientos:

1. Definir la clase genérica vec en el tipo de escalar y la cantidad de componentes. e.g. `vec<float, 3> , vec<int, 5>`.
2. Definir constructores para crear a partir de arrays, copia o por defecto.
3. Definir constructor para crear a partir de un valor replicado a todas las componentes.
4. La memoria del objeto no puede exceder `sizeof(T) * cantidad_de_componentes`.
5. Se puede acceder a partir de una función al tamaño del vector. e.g. `vec<float,3> v; ...; v.size(); // devuelve 3`.
6. Se puede acceder a los componentes de un vector mediante indización. e.g. `v[0] = 4;`.
7. Se pueden realizar operaciones como + entre vectores de igual tipo y tamaño. e.g. `v1 + v2`.
8. Para los casos particulares de `vec<T, 2>` y `vec<T, 3>` se debe poder acceder a las componentes mediante campos `x`, `y` y `x`, `y`, `z` respectivamente. e.g. `vec<float, 3> v; ...; v[0] = 5` es equivalente a `v.x = 5`.
9. Sobrecargar operadores `<<` y `>>` para poder utilizar la clase con la salida estándar.

Para ello debe abordar los siguientes puntos.

1. Genericidad en `C++` basada en  templates . Tipos de argumentos.
2. Definición de arrays en `C++`.
3. Distintos tipos de constructores en `C++` (defecto y copia).
    a. ¿Qué hace cada uno de ellos?
    b. ¿Cuándo se llaman?
    c. Explicar la inicialización de campos.
    d. ¿Cómo funciona el paso de parámetros cuando se llama a una función?
    e. ¿Cuándo se deben utilizar parámetros por valor, por puntero o por referencia?
    f. Constructores con un solo argumento.
    g. Constructores `explicit`.
4. Funciones `inline` y `const`. (Deberá hacer `const` todas las funciones que puedan ser usadas `const`).
    a. Diferencia entre `const T x;`, `T const x;` y `const T const x;`.
5. Redefinición de operadores `[]` y `+`. Tipos de traspasos en `C++`.
6. Especialización de los `templates`.
7. Tipos union.
