# Introducción a Java

Java es un lenguaje de programación de propósito general, orientado a objetos y diseñado para ser independiente de la plataforma.

## 1. Instalación y Configuración

Para programar en Java, necesitarás tener Java Development Kit (JDK) instalado en tu ordenador. Puedes descargarlo desde [el sitio oficial de Oracle](https://www.oracle.com/java/technologies/javase-downloads.html).

### Configuración del Entorno de Desarrollo Integrado (IDE)

Recomendamos utilizar un IDE como IntelliJ IDEA, Eclipse o VS Code para facilitar el desarrollo en Java.

## 2. Hola, Mundo!

```java
public class HolaMundo {
    public static void main(String[] args) {
        System.out.println("¡Hola, Mundo!");
    }
}
# Variables y Tipos de Datos

Java es fuertemente tipado, lo que significa que cada variable debe declararse con un tipo de dato específico.

int edad = 25;
double salario = 1000.50;
String nombre = "Juan";
char inicial = 'J';
boolean esEstudiante = true;


int: Tipo de dato para números enteros.
double: Tipo de dato para números decimales.
String: Tipo de dato para texto.
char: Tipo de dato para caracteres.
boolean: Tipo de dato para valores booleanos.

# Estructuras de Control

-Condicionales (if-else):

int numero = 10;

if (numero > 0) {
    System.out.println("El número es positivo");
} else if (numero < 0) {
    System.out.println("El número es negativo");
} else {
    System.out.println("El número es cero");
}

-Bucles (for, while, do-while):
java
Copy code
for (int i = 0; i < 5; i++) {
    System.out.println("Iteración " + i);
}

int j = 0;
while (j < 3) {
    System.out.println("Ciclo " + j);
    j++;
}

int k = 0;
do {
    System.out.println("Ciclo " + k);
    k++;
} while (k < 3);

-Funciones y Métodos

public class Calculadora {
    public static int sumar(int a, int b) {
        return a + b;
    }

    public static void main(String[] args) {
        int resultado = sumar(3, 5);
        System.out.println("La suma es: " + resultado);
    }
}

-Arreglos

Los arreglos son conjuntos de elementos del mismo tipo.

java
Copy code
int[] numeros = {1, 2, 3, 4, 5};

for (int i = 0; i < numeros.length; i++) {
    System.out.println(numeros[i]);
}

-Clases y Objetos

Java es un lenguaje orientado a objetos. Una clase es un plano para crear objetos.

public class Persona {
    String nombre;
    int edad;

    public Persona(String nombre, int edad) {
        this.nombre = nombre;
        this.edad = edad;
    }

    public void saludar() {
        System.out.println("Hola, soy " + nombre + " y tengo " + edad + " años.");
    }

    public static void main(String[] args) {
        Persona persona1 = new Persona("Juan", 25);
        persona1.saludar();
    }
}

 Herencia

public class Estudiante extends Persona {
    String universidad;

    public Estudiante(String nombre, int edad, String universidad) {
        super(nombre, edad);
        this.universidad = universidad;
    }

    @Override
    public void saludar() {
        System.out.println("Hola, soy " + nombre + ", tengo " + edad + " años y estudio en " + universidad + ".");
    }

    public static void main(String[] args) {
        Estudiante estudiante1 = new Estudiante("Maria", 20, "Universidad X");
        estudiante1.saludar();
    }
}