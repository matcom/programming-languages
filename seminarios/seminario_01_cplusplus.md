# Seminario 1 (C++)

Los requerimientos de cada ejercicio del seminario serán expuestos desde el punto de vista práctico y teórico; es decir, para su exposición, cada equipo se basará en el caso práctico en cuestión para introducir y explicar el elemento teórico requerido. La exposición no es una mera enunciación de código. Preguntas como: _¿Por qué?, ¿Basándose en qué?, ¿Cómo se logra esto en el lenguaje X?_ entre otras, deben hacerse.

Todos los miembros del equipo deben participar en la solución del ejercicio y estar preparados para exponer todo el trabajo. **La persona a exponer** se decide el día de la exposición. Quién no esté presente en la exposición de su equipo tiene `0` en la evaluación. (Note que estas notas se promedian y hay distinción entre `0` y `2`).

---

Implemente una clase `vec` para representar vectores algebraicos en `C++` (con los elementos disponibles en el lenguaje hasta antes de `C++11` `(C++0x)`) que cumpla los siguientes requerimientos:

1. Definir la clase genérica vec en el tipo de escalar y la cantidad de componentes. e.g. `vec<float, 3> , vec<int, 5>`.
1. Definir constructores para crear a partir de arrays, copia o por defecto.
1. Definir constructor para crear a partir de un valor replicado a todas las componentes.
1. La memoria del objeto no puede exceder `sizeof(T) * cantidad_de_componentes`.
1. Se puede acceder a partir de una función al tamaño del vector. e.g. `vec<float,3> v; ...; v.size(); // devuelve 3`.
1. Se puede acceder a los componentes de un vector mediante indización. e.g. `v[0] = 4;`.
1. Se pueden realizar operaciones como + entre vectores de igual tipo y tamaño. e.g. `v1 + v2`.
1. Para los casos particulares de `vec<T, 2>` y `vec<T, 3>` se debe poder acceder a las componentes mediante campos `x`, `y` y `x`, `y`, `z` respectivamente. e.g. `vec<float, 3> v; ...; v[0] = 5` es equivalente a `v.x = 5`.
1. Sobrecargar operadores `<<` y `>>` para poder utilizar la clase con la salida estándar.

Implemente una clase `linked_list` doblemente enlazada en `C++` (haciendo uso extensivo de los elementos novedosos en el lenguaje desde `C++11`) que cumpla los siguientes requerimientos:

1. Definir las clases genéricas `linked_list` y `node`.
1. Definir miembros de datos necesarios de ambas clases.
    1. ¿Cuáles son los nuevos elementos introducidos a partir de `C++11` que permiten un manejo más `"inteligente" de la memoria?
    1. ¿Cómo deben inicializarse?
    1. ¿Cuál es la filosofía en el uso de la memoria defendida por `C++`?
    1. Usar alias para simplificar nombres de tipos.
1. Definir los constructores clásicos de `C++(C++0x)`, el constructor `move` y las sobrecargas del operador `=`.
    1. ¿Qué hace cada uno de ellos? ¿Cuándo se llaman?
    1. ¿Qué es un `lvalue` y un `rvalue`?
    1. Explique `std::move`.
1. Definir un constructor que permita hacer `list-initialization` lo más parecido a `C#` posible.
    1. Compare la utilización del `{}` v.s `()`.
1. Definir un constructor que reciba un `vector<T>`.
    1. Usar `for_each` con expresiones lambda.
1. Definir el destructor de la clase.
    1. ¿Hace falta?
    1. ¿Para qué casos haría falta un puntero crudo (raw pointer)?
1. Definir funciones `length`, `Add_Last`, `Remove_Last`, `At`, `Remove_At`
    1. Explique `Noexcept`.
    1. Inferencia de tipo en `C++` (`auto`, `decltype`, `decltype(auto)`). Explicar todos, pero no obligatoriamente usarlos.
1. Crear un puntero a función `Function<R, T...>` que devuelve un valor de tipo `R` y recibe un número variable de parámetros de tipo `T`.
    1. Definir una función genérica `Map` a `linked_list` en `T` y `R`, que recibe un puntero a función que transforma un elemento `T` en uno `R`; de manera que `Map` devuelve una instancia de `linked_list<R>` resultado de aplicar a todos los elementos `T` de la lista original la función de transformación.
    1. Crear punteros a funciones usando `alias`.
    1. Crear un puntero a función `Function` que permita cualquier cantidad de parámetros de cualquier tipo.

Para ello debe abordar los siguientes puntos.

1. Genericidad en `C++` basada en  templates . Tipos de argumentos.
1. Definición de arrays en `C++`.
1. Distintos tipos de constructores en `C++` (defecto y copia).
    1. ¿Qué hace cada uno de ellos?
    1. ¿Cuándo se llaman?
    1. Explicar la inicialización de campos.
    1. ¿Cómo funciona el paso de parámetros cuando se llama a una función?
    1. ¿Cuándo se deben utilizar parámetros por valor, por puntero o por referencia?
    1. Constructores con un solo argumento.
    1. Constructores `explicit`.
1. Funciones `inline` y `const`. (Deberá hacer `const` todas las funciones que puedan ser usadas `const`).
    1. Diferencia entre `const T x;`, `T const x;` y `const T const x;`.
1. Redefinición de operadores `[]` y `+`. Tipos de traspasos en `C++`.
1. Especialización de los `templates`.
1. Tipos union.
