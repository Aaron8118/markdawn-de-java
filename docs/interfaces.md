# Interfaces

Una interfaz declara métodos que una clase debe implementar.

## Definición de interfaz

```java
public interface Vehiculo {
    void arrancar();
    void detener();
}
```

## Implementación

```java
public class Coche implements Vehiculo {
    public void arrancar() {
        System.out.println("El coche arranca");
    }
    public void detener() {
        System.out.println("El coche se detiene");
    }
}
```

## Métodos `default` y `static`

Desde Java 8, las interfaces pueden incluir implementaciones de métodos usando `default` y `static`.

### Métodos `default`

Un método `default` proporciona una implementación por defecto que las clases que implementan la interfaz pueden usar directamente o sobreescribir. Permite agregar funcionalidad nueva a interfaces existentes sin romper clases que ya las implementan.

**Ejemplo:**

```java
public interface Vehiculo {
    void arrancar();
    void detener();

    // Método default con implementación
    default void tocarBocina() {
        System.out.println("Bip bip!");
    }
}

public class Coche implements Vehiculo {
    public void arrancar() {
        System.out.println("El coche arranca");
    }

    public void detener() {
        System.out.println("El coche se detiene");
    }

    // Puede usar el método default o sobreescribirlo
    @Override
    public void tocarBocina() {
        System.out.println("¡Honk honk!");
    }
}
```

Ver más sobre [Abstracción](index.md#caracteristicas) en el índice.
