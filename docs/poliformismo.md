# Polimorfismo

El polimorfismo permite usar una referencia de tipo padre para referirse a objetos de clases derivadas.

## Ejemplo

```java
Animal animal = new Perro();
animal.comer();
```

## Tipos de polimorfismo

### Polimorfismo en tiempo de compilación: Sobrecarga de métodos

Ocurre cuando hay múltiples métodos con el mismo nombre pero diferentes parámetros (tipo, número o orden). El compilador decide cuál método llamar basado en los argumentos proporcionados.

```java
public class Calculadora {
    // Método con dos parámetros int
    public int sumar(int a, int b) {
        return a + b;
    }

    // Sobrecarga: mismo nombre, diferentes parámetros
    public double sumar(double a, double b) {
        return a + b;
    }

    // Otra sobrecarga: diferente número de parámetros
    public int sumar(int a, int b, int c) {
        return a + b + c;
    }
}

// Uso:
Calculadora calc = new Calculadora();
int resultado1 = calc.sumar(5, 10);        // Llama al primer método
double resultado2 = calc.sumar(5.5, 10.2); // Llama al segundo método
int resultado3 = calc.sumar(1, 2, 3);      // Llama al tercero método
```

### Polimorfismo en tiempo de ejecución: Sobreescritura de métodos

Ocurre cuando una subclase proporciona una implementación específica de un método definido en su superclase. Se resuelve en tiempo de ejecución basado en el tipo real del objeto.

```java
public class Animal {
    public void hacerSonido() {
        System.out.println("El animal hace un sonido");
    }
}

public class Perro extends Animal {
    @Override
    public void hacerSonido() {
        System.out.println("El perro ladra: ¡Guau!");
    }
}

public class Gato extends Animal {
    @Override
    public void hacerSonido() {
        System.out.println("El gato maúlla: ¡Miau!");
    }
}

// Uso con polimorfismo:
Animal animal1 = new Perro();  // Referencia de tipo Animal, objeto Perro
Animal animal2 = new Gato();   // Referencia de tipo Animal, objeto Gato

animal1.hacerSonido();  // Salida: El perro ladra: ¡Guau!
animal2.hacerSonido();  // Salida: El gato maúlla: ¡Miau!
```

En este ejemplo, aunque `animal1` y `animal2` son de tipo `Animal`, el método correcto se llama basado en el objeto real (Perro o Gato).

## Ventajas

- Flexibilidad
- Extensibilidad
- Mantenimiento más sencillo

Ver más sobre [Polimorfismo](index.md#caracteristicas) en el índice.
