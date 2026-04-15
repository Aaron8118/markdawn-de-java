# Tipos de datos

En Java, los tipos de datos se dividen en dos categorías principales:

- **Primitivos**: almacenan valores simples.
- **Referencias**: almacenan direcciones a objetos.

## Tipos primitivos

| Tipo | Descripción |
|---|---|
| byte | Entero de 8 bits |
| short | Entero de 16 bits |
| int | Entero de 32 bits |
| long | Entero de 64 bits |
| float | Coma flotante de 32 bits |
| double | Coma flotante de 64 bits |
| char | Carácter Unicode de 16 bits |
| boolean | Verdadero o falso |

## Tipos de referencia

Los tipos de referencia almacenan referencias (direcciones de memoria) a objetos, no los valores directamente. A diferencia de los tipos primitivos, que almacenan el valor real, los tipos de referencia permiten trabajar con objetos complejos y pueden ser `null`.

- String: Cadena de caracteres inmutable.
- Arrays: Colecciones de elementos del mismo tipo.
- Clases personalizadas: Objetos definidos por el usuario.
- Interfaces: Contratos para clases que las implementan.

## Ejemplos

```java
// Tipo primitivo
int numero = 42; // Almacena directamente 42

// Tipo de referencia
String texto = "Hola"; // Almacena una referencia al objeto String
int[] arreglo = {1, 2, 3}; // Referencia a un array
```