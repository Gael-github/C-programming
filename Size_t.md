# Size_t

## ¿Qué es `size_t`?

`size_t` es **el tipo estándar en C para representar tamaños de objetos en memoria.**

- Lo devuelve `sizeof()`.
- Lo usan funciones como `malloc`, `calloc`, `memcpy`, etc.
- Es un **entero sin signo (`unsigned`)**.
- Varía según la arquitectura:
    - En sistemas de 32 bits: 4 bytes (hasta 4,294,967,295)
    - En sistemas de 64 bits: 8 bytes (hasta 18 trillones)

---

## ¿Por qué no usar `int` o `unsigned int`?

Porque:

- `int` puede ser negativo → no tiene sentido tener un tamaño negativo.
- `unsigned int` puede no ser lo suficientemente grande en sistemas de 64 bits.

`size_t` **siempre se ajusta** al sistema, por eso es más seguro.

---

## Tipos

| Tipo | Descripción rápida | Uso común |
| --- | --- | --- |
| `size_t` | Tamaños y conteo de elementos en memoria | `sizeof`, `malloc`, bucles de arrays |
| `ssize_t` | Como `size_t` pero con signo | Cantidades que pueden ser negativas (`read`) |
| `ptrdiff_t` | Resultado de restar dos punteros | Operaciones con punteros (`p2 - p1`) |
| `uintptr_t` | Entero sin signo del mismo tamaño que un puntero | Casos raros: guardar punteros como enteros |
| `intptr_t` | Igual que arriba, pero con signo | Muy bajo nivel, raramente usado |

---

### Recuerda

 `size_t`  **no va a darte negativo**… te da un valor gigante porque es sin signo.