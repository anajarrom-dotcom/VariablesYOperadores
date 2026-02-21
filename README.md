VariablesYOperadores

# Descripción
Este proyecto tiene como objetivo comprender cómo declarar variables en Java, asignarles valores y manipularlas usando operadores matemáticos y lógicos.

---


¿Para qué se utilizan los operadores lógicos en programación?

Los operadores lógicos se utilizan para combinar condiciones y tomar decisiones en el programa. Permiten evaluar múltiples expresiones al mismo tiempo utilizando operadores como AND (&&) y OR (||).

---

¿Por qué es importante declarar correctamente el tipo de dato de una variable?

Es importante porque cada tipo de dato ocupa diferente espacio en memoria y permite realizar distintas operaciones. Declarar correctamente el tipo evita errores, mejora el rendimiento y asegura que los datos se manejen de forma adecuada.

---


Clasificación de edad

Se utilizó la estructura if-else porque permite evaluar rangos de valores (menor que, mayor que, entre valores). Es más adecuada cuando se trabajan condiciones con comparaciones numéricas.

---

Día de la semana

Se utilizó switch porque se evalúa un valor exacto del 1 al 7. Switch es más organizado y claro cuando se comparan valores específicos.

---

Verificación de acceso

Se utilizó if-else porque se deben evaluar múltiples condiciones combinadas (usuario y contraseña). Permite usar operadores lógicos como && y ! para validar correctamente las credenciales.


import java.util.Scanner;

public class Main {

    public static final int EDAD_MINIMA = 18;

    public static void main(String[] args) {

        Scanner sc = new Scanner(System.in);

        // 1️ DECLARACIÓN Y USO DE VARIABLES

        System.out.print("Ingrese un valor entero: ");
        int valorEntero = sc.nextInt();

        System.out.print("Ingrese un valor decimal: ");
        double valorDecimal = sc.nextDouble();

        sc.nextLine(); // limpiar buffer

        System.out.print("Ingrese un texto: ");
        String texto = sc.nextLine();

        System.out.print("Ingrese true o false: ");
        boolean estado = sc.nextBoolean();

        System.out.println("\n--- Valores Ingresados ---");
        System.out.println("Entero: " + valorEntero);
        System.out.println("Decimal: " + valorDecimal);
        System.out.println("Texto: " + texto);
        System.out.println("Boolean: " + estado);


        // 2️ OPERACIONES MATEMÁTICAS

        System.out.print("\nIngrese primer numero: ");
        int a = sc.nextInt();

        System.out.print("Ingrese segundo numero: ");
        int b = sc.nextInt();

        System.out.println("Suma: " + (a + b));
        System.out.println("Resta: " + (a - b));
        System.out.println("Multiplicacion: " + (a * b));

        if (b != 0) {
            System.out.println("Division: " + (a / b));
        } else {
            System.out.println("No se puede dividir entre cero");
        }

        System.out.println("La division entre enteros elimina los decimales.");

        double d1 = a;
        double d2 = b;
        System.out.println("Division con double: " + (d1 / d2));

        float f1 = a;
        float f2 = b;
        System.out.println("Division con float: " + (f1 / f2));

        short s1 = (short) a;
        short s2 = (short) b;
        if (s2 != 0) {
            System.out.println("Division con short: " + (s1 / s2));
        }

        byte by1 = (byte) a;
        byte by2 = (byte) b;
        if (by2 != 0) {
            System.out.println("Division con byte: " + (by1 / by2));
        }


        // 3 OPERACIONES LÓGICAS

        System.out.println("\n=== OPERACIONES LOGICAS ===");

        System.out.println("a > b: " + (a > b));
        System.out.println("a < b: " + (a < b));
        System.out.println("a == b: " + (a == b));

        System.out.println("AND (a > 0 && b > 0): " + (a > 0 && b > 0));
        System.out.println("OR (a > 0 || b > 0): " + (a > 0 || b > 0));


        // 4️ CLASIFICACIÓN DE EDAD

        System.out.print("\nIngrese su edad: ");
        int edad = sc.nextInt();

        if (edad < 12) {
            System.out.println("Nino");
        } else if (edad <= 17) {
            System.out.println("Adolescente");
        } else if (edad <= 59) {
            System.out.println("Adulto");
        } else {
            System.out.println("Adulto mayor");
        }


        // 5️ DÍA DE LA SEMANA

        System.out.print("\nIngrese un numero del 1 al 7: ");
        int dia = sc.nextInt();

        switch (dia) {
            case 1:
                System.out.println("Lunes");
                break;
            case 2:
                System.out.println("Martes");
                break;
            case 3:
                System.out.println("Miercoles");
                break;
            case 4:
                System.out.println("Jueves");
                break;
            case 5:
                System.out.println("Viernes");
                break;
            case 6:
                System.out.println("Sabado");
                break;
            case 7:
                System.out.println("Domingo");
                break;
            default:
                System.out.println("Numero invalido");
        }


        // 6️ VERIFICACIÓN DE ACCESO

        sc.nextLine(); // limpiar buffer

        System.out.print("\nUsuario: ");
        String usuario = sc.nextLine();

        System.out.print("Contrasena: ");
        String contrasena = sc.nextLine();

        if (usuario.equals("Antony") && contrasena.equals("1234")) {
            System.out.println("Acceso concedido");
        }
        else if (usuario.equals("Antony") && !contrasena.equals("1234")) {
            System.out.println("Contrasena incorrecta");
        }
        else {
            System.out.println("Usuario no registrado");
        }

        sc.close();
    }
