# Variables

Una variable es un espacio en memoria que almacena un valor.

## Cómo declarar una variable

Para definir una variable en Java, sigue esta sintaxis básica:

```
[modificador] tipo nombre [= valor_inicial];
```

Donde:

1. **modificador**: Opcional, como `public`, `private`, `static`, `final`, etc.
2. **tipo**: El tipo de dato de la variable (ej. `int`, `String`, `boolean`).
3. **nombre**: El identificador de la variable (debe seguir reglas de nomenclatura).
4. **valor_inicial**: Opcional, para inicializar la variable al declararla.

```java
// Variable local simple
int contador;

// Variable con inicialización
String mensaje = "Hola Mundo";

// Variable con modificador
private double precio = 99.99;

// Variable estática
public static final int MAX_VALOR = 100;
```

Las variables deben definirse antes de usarse, y su tipo determina qué valores pueden almacenar.


### Variables con modificadores de acceso

Los modificadores de acceso controlan la visibilidad de las variables en una clase. Se usan principalmente para variables de instancia y de clase.

- **public**: Accesible desde cualquier parte del programa.
- **private**: Solo accesible dentro de la misma clase.
- **protected**: Accesible dentro del mismo paquete y subclases.
- **Sin modificador (default)**: Accesible dentro del mismo paquete.

```java
public class Ejemplo {
    public int variablePublica = 10;     // Accesible desde cualquier lugar
    private String datoPrivado = "secreto"; // Solo dentro de esta clase
    protected double valorProtegido = 3.14; // Accesible en paquete y subclases
    int variableDefault = 5;             // Accesible en el mismo paquete

    public void mostrar() {
        System.out.println(datoPrivado); // OK, dentro de la clase
    }
}
```

En este ejemplo, `variablePublica` puede ser accedida desde otras clases, mientras que `datoPrivado` solo se puede usar dentro de `Ejemplo`.

## Alcance (scope)

- Variables locales: dentro de un método.
- Variables de instancia: dentro de una clase pero fuera de métodos.
- Variables estáticas: compartidas por todas las instancias.

## Tipos de variables

### Variables de instancia

Son variables que pertenecen a cada objeto (instancia) de una clase. Cada objeto tiene su propia copia de estas variables. Se declaran dentro de la clase pero fuera de cualquier método.

```java
public class Persona {
    String nombre; // variable de instancia
    int edad;      // variable de instancia

    public void mostrarInfo() {
        System.out.println("Nombre: " + nombre + ", Edad: " + edad);
    }
}

// Uso:
Persona p1 = new Persona();
p1.nombre = "Ana";
p1.edad = 25;

Persona p2 = new Persona();
p2.nombre = "Juan";
p2.edad = 30;
```

En este ejemplo, `p1` y `p2` tienen sus propias versiones de `nombre` y `edad`.

### Variables locales

Son variables declaradas dentro de un método, constructor o bloque de código. Solo existen durante la ejecución de ese bloque y no son accesibles fuera de él.

```java
public class Calculadora {
    public int sumar(int a, int b) {
        int resultado = a + b; // variable local
        return resultado;
    }

    public void ejemplo() {
        for (int i = 0; i < 5; i++) { // i es una variable local del bucle
            System.out.println(i);
        }
        // i no es accesible aquí
    }
}
```

Las variables locales deben inicializarse antes de usarse.

### Variables de clase (static)

Son variables compartidas por todas las instancias de la clase. Se declaran con la palabra clave `static` y pertenecen a la clase en sí, no a objetos individuales.

```java
public class Contador {
    static int contadorGlobal = 0; // variable de clase

    public Contador() {
        contadorGlobal++;
    }

    public static void mostrarContador() {
        System.out.println("Total de instancias: " + contadorGlobal);
    }
}

// Uso:
Contador c1 = new Contador(); // contadorGlobal = 1
Contador c2 = new Contador(); // contadorGlobal = 2
Contador.mostrarContador(); // Imprime: Total de instancias: 2
```

Todas las instancias comparten la misma variable `contadorGlobal`.

## Buenas prácticas

- Usa nombres descriptivos.
- Usa camelCase en Java.
- Inicializa siempre variables antes de usarlas.
