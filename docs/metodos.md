# Métodos

Los métodos definen el comportamiento de una clase.

## Sintaxis básica

```java
public int sumar(int a, int b) {
    return a + b;
}
```

## Componentes de un método

1. Modificador de acceso (`public`, `private`, etc.)
2. Tipo de retorno (`int`, `void`, etc.)
3. Nombre del método
4. Parámetros
5. Cuerpo del método

```java
public static void main(String[] args) {
    System.out.println("Hola mundo");
}
```

Los métodos estáticos pertenecen a la clase, no a instancias. Se llaman usando el nombre de la clase y pueden acceder solo a variables estáticas.

## Tipos de métodos

### Métodos de instancia

Son los métodos más comunes. Pertenecen a objetos específicos y pueden acceder a variables de instancia y otros métodos de la instancia.

```java
public class Persona {
    private String nombre;

    public void saludar() {  // Método de instancia
        System.out.println("Hola, soy " + nombre);
    }

    public void setNombre(String nombre) {
        this.nombre = nombre;
    }
}
```

### Métodos estáticos

Pertenecen a la clase en sí. No requieren una instancia para ser llamados y solo pueden acceder a miembros estáticos.

```java
public class Matematicas {
    public static int cuadrado(int numero) {
        return numero * numero;
    }
}

// Uso: int resultado = Matematicas.cuadrado(5);
```

### Métodos abstractos

Declarados sin implementación en clases abstractas o interfaces. Las subclases deben proporcionar la implementación.

```java
public abstract class Figura {
    public abstract double calcularArea();  // Método abstracto
}

public class Circulo extends Figura {
    private double radio;

    @Override
    public double calcularArea() {
        return Math.PI * radio * radio;
    }
}
```

### Métodos finales

No pueden ser sobreescritos por subclases. Se usan para prevenir modificaciones.

```java
public class Vehiculo {
    public final void detener() {  // Método final
        System.out.println("Vehículo detenido");
    }
}

public class Coche extends Vehiculo {
    // No se puede sobreescribir detener()
}
```

## Ventajas

- Reutilización de código
- Organización
- Legibilidad

Ver más sobre [POO](index.md#poo) en el índice.
