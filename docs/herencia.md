# Herencia

La herencia permite que una clase derive de otra y reutilice su comportamiento.

## Ejemplo de herencia

```java
public class Animal {
    void comer() {
        System.out.println("El animal come");
    }
}

public class Perro extends Animal {
    void ladrar() {
        System.out.println("El perro ladra");
    }
}
```

## `super`

Se usa para acceder a la clase padre:

```java
super.comer();
```

## Beneficios

- Reutilización de código
- Especialización de clases
- Relaciones jerárquicas

Ver más sobre [Herencia](index.md#caracteristicas) en el índice.
