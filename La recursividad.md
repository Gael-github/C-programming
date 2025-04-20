# La recursividad

### Una función **se llama a sí misma** para resolver un problema.

---

### ¿Cómo funciona?

Tiene **dos partes clave**:

1. **Caso base** (condición para detenerse).
2. **Llamada recursiva** (la función se llama a sí misma con un nuevo valor).

---

### Ejemplo Factorial

```c
int factorial(int n)
{
    if (n <= 1) // CASO BASE
        return 1;
    else
        return n * factorial(n - 1); // LLAMADA RECURSIVA
}

```

```c
factorial(4) = 4 * factorial(3)
factorial(3) = 3 * factorial(2)
factorial(2) = 2 * factorial(1)
factorial(1) = 1  // caso base

```

Luego se resuelve hacia atrás:

```c
factorial(2) = 2 * 1 = 2
factorial(3) = 3 * 2 = 6
factorial(4) = 4 * 6 = 24

```

---

### ¿Para qué se usa?

- Factorial, Fibonacci, recorrer árboles, algoritmos de búsqueda/backtracking, etc.

---

- Siempre debe **tener** un **caso base**, si no se queda llamándose para siempre → **stack overflow**.
- Si podés resolverlo con un bucle, a veces es más eficiente **iterar** que recursar.

---