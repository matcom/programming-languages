# Seminario 9 (Python y la metaprogramación)

Los requerimientos de cada ejercicio del seminario serán expuestos desde el punto de vista práctico y teórico; es decir, para su exposición, cada equipo se basará en el caso práctico en cuestión para introducir y explicar el elemento teórico requerido. La exposición no es una mera enunciación de código. Preguntas como: _¿Por qué?, ¿Basándose en qué?, ¿Cómo se logra esto en el lenguaje X?_ entre otras, deben hacerse.

Todos los miembros del equipo deben participar en la solución del ejercicio y estar preparados para exponer todo el trabajo. **La persona a exponer*1. se decide el día de la exposición. Quién no esté presente en la exposición de su equipo tiene `0` en la evaluación. (Note que estas notas se promedian y hay distinción entre `0` y `2`).

---

1. Explique en qué consiste la programación por contratos? Y muestre un ejemplo en `C#` utilizando la biblioteca `CodeContract`.
2. Usando decoradores proponga e implemente un mecanismo de contratos al estilo `CodeContract`. Las precondiciones y postcondiciones se deben poder especificar como en el siguiente ejemplo:

    ```python
    @contract(require=lambda x: x > 0, ensure=lambda result: result > 0)
    def some_function(x):
        pass
    ```

    El argumento con nombre `require` debe ser una función o cualquier otro objeto invocable que verifique el cumplimiento de las precondiciones y lance excepción en caso de que no se cumplan. De manera análoga el argumento con nombre `ensure` debe ser un objeto invocable que verifique el cumplimiento de las postcondiciones.

    La signatura de los argumentos del objeto invocable asignado en el argumento `require` debe ser compatible con la signatura de la función decorada (`some_function`), en caso de no serlo, se debe lanzar una excepción personalizada con un mensaje descriptivo.

    En el caso en que el objeto invocable asignado en el argumento `ensure` reciba como argumento más de un argumento posicional sin valor por defecto o algún argumento de solo palabra clave sin valor por defecto se debe lanzar una excepción personalizada con un mensaje descriptivo. El siguiente ejemplo muestra un grupo de objetos invocables que válidos y otros inválidos:

    ```python
    def f0(x):  # Bien
        return True

    def f1(x, y):  # Mal
        return True

    def f2(x, y=0):  # Bien
        return True

    def f3(x, *, y):  # Mal
        return True

    def f4(x, *, y=0):  # Bien
        return True

    def f5(x, y, *, z):  # Mal
        return True

    def f6(x, y, *, z=0):  # Mal
        return True

    def f7(x, y=0, *, z):  # Mal
        return True

    def f8(x, y=0, *, z=0):  # Bien
        return True

    # print(f0(1))  # True
    # print(f1(1))  # TypeError: f1() missing 1 required positional argument: 'y'
    # print(f2(1))  # True
    # print(f3(1))  # TypeError: f3() missing 1 required keyword-only argument: 'y'
    # print(f4(1))  # True
    # print(f5(1))  # TypeError: f5() missing 1 required positional argument: 'y'
    # print(f6(1))  # TypeError: f6() missing 1 required positional argument: 'y'
    # print(f7(1))  # TypeError: f7() missing 1 required keyword-only argument: 'z'
    # print(f8(1))  # True
    ```

3. Implemente en **Python** los siguientes patrones utilizando metaclases:

    * `Singleton`: Clase de la que solo se puede crear una instancia, por lo que todos los intentos de instanciación deben resultar en un mismo objeto (el del primer intento).Tenga en cuenta en su implementación que las clases que hereden de esta clase deberán heredar también el comportamiento `Singleton`.
    * Implemente la clase `ObjetoInmutable` en `Python`. Un objeto inmutable, una vez creado, **no podrá ser modificado**. No ser modificado significa que después de su creación no se puede hacer `o.t = valor` ni `del(o.t)`, siendo `o` una instancia de `ObjetoInmutable`. Realice su diseño de forma tal que cualquier clase que herede de `ObjetoInmutable` tenga el mismo comportamiento.
