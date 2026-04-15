# Estructuras de control y lógica

Las estructuras de control permiten tomar decisiones y repetir acciones en Java.

## Estructuras condicionales

### if-else

Ejecuta un bloque de código si una condición es verdadera.

```java
int edad = 18;

if (edad >= 18) {
    System.out.println("Eres mayor de edad");
} else {
    System.out.println("Eres menor de edad");
}
```

### if-else if-else

Permite múltiples condiciones.

```java
int nota = 85;

if (nota >= 90) {
    System.out.println("Excelente");
} else if (nota >= 80) {
    System.out.println("Muy bien");
} else if (nota >= 70) {
    System.out.println("Bien");
} else {
    System.out.println("Necesitas mejorar");
}
```

### switch

Útil para múltiples opciones basadas en un valor.

```java
int dia = 3;
String nombreDia;

switch (dia) {
    case 1:
        nombreDia = "Lunes";
        break;
    case 2:
        nombreDia = "Martes";
        break;
    case 3:
        nombreDia = "Miércoles";
        break;
    case 4:
        nombreDia = "Jueves";
        break;
    case 5:
        nombreDia = "Viernes";
        break;
    case 6:
        nombreDia = "Sábado";
        break;
    case 7:
        nombreDia = "Domingo";
        break;
    default:
        nombreDia = "Día inválido";
        break;
}
System.out.println("Hoy es " + nombreDia);
```

## Bucles

### for

Repite un bloque de código un número específico de veces.

```java
for (int i = 1; i <= 5; i++) {
    System.out.println("Iteración: " + i);
}
```

### while

Repite mientras una condición sea verdadera.

```java
int contador = 1;

while (contador <= 5) {
    System.out.println("Contador: " + contador);
    contador++;
}
```

### do-while

Ejecuta al menos una vez, luego repite mientras la condición sea verdadera.

```java
int numero = 1;

do {
    System.out.println("Número: " + numero);
    numero++;
} while (numero <= 5);
```

### for-each

Útil para iterar sobre arrays o colecciones.

```java
int[] numeros = {1, 2, 3, 4, 5};

for (int num : numeros) {
    System.out.println("Número: " + num);
}
```

## Otras estructuras

### break y continue

- `break`: Sale del bucle actual.
- `continue`: Salta a la siguiente iteración.

```java
for (int i = 1; i <= 10; i++) {
    if (i == 5) {
        continue;  // Salta el 5
    }
    if (i == 8) {
        break;     // Sale cuando llega a 8
    }
    System.out.println(i);
}
```

### Operador ternario

Forma concisa de if-else.

```java
int edad = 20;
String mensaje = (edad >= 18) ? "Mayor de edad" : "Menor de edad";
System.out.println(mensaje);
```