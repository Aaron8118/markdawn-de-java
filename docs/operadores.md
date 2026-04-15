# Operadores

Los operadores en Java permiten realizar operaciones sobre valores y variables.

## Operadores aritméticos

- `+` suma
- `-` resta
- `*` multiplicación
- `/` división
- `%` módulo
- `++` incremento (aumenta en 1)
- `--` decremento (disminuye en 1)

## Operadores de asignación

- `=` asignación
- `+=`, `-=`, `*=`, `/=`, `%=` asignaciones compuestas

## Operadores de comparación

- `==` igual a
- `!=` distinto de
- `>` mayor que
- `<` menor que
- `>=` mayor o igual
- `<=` menor o igual

## Operadores lógicos

- `&&` y lógico
- `||` o lógico
- `!` negación

## Prioridad de operadores

La prioridad determina el orden en que se evalúan las operaciones. Los operadores con mayor prioridad se evalúan primero. Aquí una lista numerada de mayor a menor prioridad para los operadores mencionados:

| Prioridad | Operadores | Descripción |
|-----------|-----------|-------------|
| 1 | `++`, `--` | Post-incremento/decremento |
| 2 | `++`, `--` | Pre-incremento/decremento |
| 3 | `*`, `/`, `%` | Aritméticos (multiplicación, división, módulo) |
| 4 | `+`, `-` | Aritméticos (suma, resta) |
| 5 | `<`, `>`, `<=`, `>=` | Comparación |
| 6 | `==`, `!=` | Igualdad |
| 7 | `&&` | Y lógico |
| 8 | `\|\|` | O lógico |
| 9 | `=`, `+=`, `-=`, `*=`, `/=`, `%=` | Asignación |

## Ejemplos

```java
int a = 10;
int b = 5;
boolean esMayor = a > b;
int total = a + b;
```

```java
int resultado = 5 + 3 * 2;  // Primero * (3*2=6), luego + (5+6=11)
boolean condicion = a > b && c < d;  // Primero > y <, luego &&
```