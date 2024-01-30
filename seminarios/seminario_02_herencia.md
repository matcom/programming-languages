# Seminario 5 (Herencia Múltiple)

Los requerimientos de cada ejercicio del seminario serán expuestos desde el punto de vista práctico y teórico; es decir, para su exposición, cada equipo se basará en el caso práctico en cuestión para introducir y explicar el elemento teórico requerido. La exposición no es una mera enunciación de código. Preguntas como: _¿Por qué?, ¿Basándose en qué?, ¿Cómo se logra esto en el lenguaje X?_ entre otras, deben hacerse.

Todos los miembros del equipo deben participar en la solución del ejercicio y estar preparados para exponer todo el trabajo. **La persona a exponer**. se decide el día de la exposición. Quién no esté presente en la exposición de su equipo tiene `0` en la evaluación. (Note que estas notas se promedian y hay distinción entre `0` y `2`).

---

En la Universidad, una persona (que se identifica por su Nombre) es plantilla si recibe algún tipo de pago y puede representar diferentes roles:

* Estudiante (Acción: `RecibirClase()` y `CobrarSalario()`)
* Profesor (Acción: `ImpartirClase()`)
* Alumno Ayudante (Estudiante que no es profesor pero actúa como tal en un momento dado, es decir, puede realizar `ImpartirClase()`, además puede cobrar un salario como trabajador separado del salario como estudiante)
* Trabajador (no todo trabajador es profesor, pero sí todos los profesores son trabajadores. Acción: `CobrarSalario()`)
* Profesor Adiestrado (Profesor que aún recibe cursos de adiestramiento, Acción: `RecibirClase()`)

Los valores de salario y horas clase (tiempo en que se recibe o imparte clases) debe poder ser configurable en cualquier entidad.

Ilustre cómo podría ser implementado este diseño de clases en lenguajes `C#`, `C++` y `Python`.

1. Diseñe una jerarquía en `C#` que represente/modele los roles anteriores y sus relaciones. Utilice alguna herramienta para ilustrar dicho modelo (Ejemplo: diseñador de clases de Visual Studio)

1. ¿En qué casos la herencia múltiple puede causar ambigüedad? Ejemplifique.
1. ¿Cómo podemos solucionar estos casos? Analice y compare las distintas soluciones. ¿Cuál es la solución propuesta en `C#`?
1. Explique cómo se representan los objetos en memoria. Ponga un ejemplo de:
    1. Un objeto perteneciente a una clase que no herede de ninguna otra
    1. Un objeto perteneciente a una clase que muestre una herencia simple
    1. Un objeto perteneciente a una clase que utilice herencia múltiple

> Analizar: Herencia Múltiple en C++ y Python. Colisión de interfaces e implementación implicita/explícita en C#. Visibilidad, Redefinición de miembros, Ocultamiento, Representación en Memoria, Polimorfismo, Casteo.
