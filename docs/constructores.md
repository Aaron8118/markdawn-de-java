# Constructores

Un constructor se usa para inicializar objetos cuando se crean.

## Constructor predeterminado

Es un constructor sin parámetros que Java proporciona automáticamente si no defines ninguno. Inicializa los campos con valores por defecto (0 para números, null para referencias, false para booleanos). Si defines constructores personalizados, el predeterminado desaparece.

```java
public class Persona {
    String nombre;  // null por defecto
    int edad;       // 0 por defecto

    // Constructor predeterminado implícito
}
```

Si necesitas inicializar con valores específicos, define uno explícito como se muestra arriba.

## Constructor con parámetros

Permite inicializar un objeto con valores específicos al momento de creación. Los parámetros se pasan al crear la instancia con `new`.

```java
public class Persona {
    String nombre;
    int edad;

    public Persona(String nombre, int edad) {
        this.nombre = nombre;
        this.edad = edad;
    }
}

// Uso:
Persona p = new Persona("Ana", 25);
```

## Constructor de copia

Crea un nuevo objeto copiando los valores de otro objeto existente. Útil para crear duplicados independientes.

```java
public class Persona {
    String nombre;
    int edad;

    public Persona(String nombre, int edad) {
        this.nombre = nombre;
        this.edad = edad;
    }

    // Constructor de copia
    public Persona(Persona otra) {
        this.nombre = otra.nombre;
        this.edad = otra.edad;
    }
}

// Uso:
Persona original = new Persona("Ana", 25);
Persona copia = new Persona(original);
```

## Sobrecarga de constructores

Puedes definir varios constructores con diferentes parámetros. Java elige el constructor apropiado basado en los argumentos proporcionados.

```java
public class Persona {
    String nombre;
    int edad;

    // Constructor sin parámetros
    public Persona() {
        this.nombre = "Desconocido";
        this.edad = 0;
    }

    // Constructor con nombre
    public Persona(String nombre) {
        this.nombre = nombre;
        this.edad = 0;
    }

    // Constructor con nombre y edad
    public Persona(String nombre, int edad) {
        this.nombre = nombre;
        this.edad = edad;
    }
}

// Uso:
Persona p1 = new Persona();              // Desconocido, 0
Persona p2 = new Persona("Juan");        // Juan, 0
Persona p3 = new Persona("Ana", 25);     // Ana, 25
```

Ver más sobre [POO](index.md#poo) en el índice.
