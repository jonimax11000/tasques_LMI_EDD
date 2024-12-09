# Calculadora con Ant

## Calculadora.java

```java
package com.Jonathan.edd;

public class Calculadora {
    public static int Sumar(int a, int b){
            return a+b;
        
    }

    public static int Restar(int a, int b){
        return a-b;
    
    }

    public static int Multiplicar(int a, int b){
        return a*b;
    
    }

    public static int Dividir(int a, int b){
        try {
            return a-b;
        } catch (Exception e) {
            System.out.println("Error: No se pot dividir entre 0");
            return b;
        }
        
    
    }
}
```

## Codi Calcula.java

```java
package com.Jonathan.edd;

import java.util.Scanner;

public class Calcula {
    public static void main(String[] args) {
        Scanner teclat = new Scanner(System.in);
        System.out.println("Bienvenidos a una calculadora básica");
        System.out.println("Que quieres hacer? ('s','r','m','d')");
        String accion = teclat.nextLine();
        System.out.println("Cual es el primer número? (entero)");
        int a = teclat.nextInt();
        System.out.println("Cual es el segundo número? (entero)");
        int b = teclat.nextInt();
        
        switch (accion) {
            case "s":
                System.out.println(Calculadora.Sumar(a, b));
                break;
            
            case "r":
                System.out.println(Calculadora.Restar(a, b));
                break;

            case "m":
                System.out.println(Calculadora.Multiplicar(a, b));
                break;

            case "d":
                System.out.println(Calculadora.Dividir(a, b));
                break;
            default:
                break;
        }
    }
}
```

## Build.xml

```xml
<project name="calculaAnt">
    <target name="clean">
        <delete dir="build" />
    </target>

    <target name="compile" depends="clean">
        <mkdir dir="build" />
        <javac includeantruntime="false" 
        srcdir="com/Jonathan/edd" destdir="build" />
    </target>

    <target name="run" depends="compile">
        <java classpath="build" classname="com.Jonathan.edd.Calcula">
        </java>
    </target>
</project>
```

## Estructura Antes del build

```bash
jonimax11000@jonimax11000:~/Desktop/DAM/Primero/EDD/Tema4/src$ tree
.
├── build.xml
└── com
    └── Jonathan
        └── edd
            ├── Calculadora.java
            └── Calcula.java
```

## Compilado

```bash
jonimax11000@jonimax11000:~/Desktop/DAM/Primero/EDD/Tema4/src$ ant compile
Buildfile: /home/jonimax11000/Desktop/DAM/Primero/EDD/Tema4/src/build.xml

clean:

compile:
    [mkdir] Created dir: /home/jonimax11000/Desktop/DAM/Primero/EDD/Tema4/src/build
    [javac] Compiling 2 source files to /home/jonimax11000/Desktop/DAM/Primero/EDD/Tema4/src/build

BUILD SUCCESSFUL
Total time: 0 seconds
```

## Estructura despues del build

```bash
jonimax11000@jonimax11000:~/Desktop/DAM/Primero/EDD/Tema4/src$ tree
.
├── build
│   └── com
│       └── Jonathan
│           └── edd
│               ├── Calcula.class
│               └── Calculadora.class
├── build.xml
└── com
    └── Jonathan
        └── edd
            ├── Calculadora.java
            └── Calcula.java

8 directories, 5 files
```

## Run

```
jonimax11000@jonimax11000:~/Desktop/DAM/Primero/EDD/Tema4/src$ ant run
Buildfile: /home/jonimax11000/Desktop/DAM/Primero/EDD/Tema4/src/build.xml

clean:
   [delete] Deleting directory /home/jonimax11000/Desktop/DAM/Primero/EDD/Tema4/src/build

compile:
    [mkdir] Created dir: /home/jonimax11000/Desktop/DAM/Primero/EDD/Tema4/src/build
    [javac] Compiling 2 source files to /home/jonimax11000/Desktop/DAM/Primero/EDD/Tema4/src/build

run:
     [java] Bienvenidos a una calculadora básica
     [java] Que quieres hacer? ('s','r','m','d')
s
     [java] Cual es el primer número? (entero)
4
     [java] Cual es el segundo número? (entero)
1
     [java] 5

BUILD SUCCESSFUL
Total time: 17 seconds
jonimax11000@jonimax11000:~/Desktop/DAM/Primero/EDD/Tema4/src$
```