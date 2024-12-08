# Exercici 3. Crea un fitxer .gitignore de manera que s’ignoren tots els fitxers compilats de java. Afegeix-lo al repositori. Posteriorment, crea un fitxer font senzill en Java, compila’l, i prepara tot per confirmar-ho en un commit. Comprova si els fitxers compilats s’han afegit o no

1. Creem en primer lloc el fitxer .gitignore, amb el següent contingut:

        # Ignorem els compilats de java
        *.class        

2. Preparem el fitxer per al següent commit i el confirmem:

        alumno@alumno-VirtualBox:~/projecte$ git add .gitignore
        warning: LF será reemplazado por CRLF en .gitignore.
        El archivo tendrá sus finales de línea originales en tu directorio de trabajo
        alumno@alumno-VirtualBox:~/projecte$ git commit -m "Afegit .gitignore"
        [master 03c9521] Afegit .gitignore
        1 file changed, 2 insertions(+)
        create mode 100644 .gitignore

3. Ara, creem un fitxer en java, per exemple un Hello.java que siga un Hola Món.

    ```
    class Hello {
        public static void main(String[] args) {
        System.out.println("Hola Món!"); 
        }
    }
    ```

4. Compilem:

        alumno@alumno-VirtualBox:~/projecte$ ls -l
        total 8
        -rw-rw-r-- 1 alumno alumno 10 oct 29 12:07 fitxer1.md
        -rw-rw-r-- 1 alumno alumno 97 nov 11 21:10 Hello.java
        -rw-rw-r-- 1 alumno alumno  0 nov 11 20:36 tmp_mv_1.md
        -rw-rw-r-- 1 alumno alumno  0 nov 11 13:41 tmp_mv_2.md
        alumno@alumno-VirtualBox:~/projecte$ javac Hello.java
        alumno@alumno-VirtualBox:~/projecte$ ls -l
        total 12
        -rw-rw-r-- 1 alumno alumno  10 oct 29 12:07 fitxer1.md
        -rw-rw-r-- 1 alumno alumno 414 dic  8 16:41 Hello.class
        -rw-rw-r-- 1 alumno alumno  97 nov 11 21:10 Hello.java
        -rw-rw-r-- 1 alumno alumno   0 nov 11 20:36 tmp_mv_1.md
        -rw-rw-r-- 1 alumno alumno   0 nov 11 13:41 tmp_mv_2.md

5. Següent commit:

        alumno@alumno-VirtualBox:~/projecte$ git add *
        Las siguientes rutas son ignoradas por uno de tus archivos .gitignore:
        Hello.class
        ayuda: Usa -f si realmente quieres agregarlos.
        ayuda: Desactiva este mensaje ejecutando
        ayuda: "git config advice.addIgnoredFile false"
        warning: LF será reemplazado por CRLF en Hello.java.
        El archivo tendrá sus finales de línea originales en tu directorio de trabajo
        alumno@alumno-VirtualBox:~/projecte$ git commit -m "Prova d'exercici 3 Tema 5 EDD"
        [master 76460f9] Prova d'exercici 3 Tema 5 EDD
        1 file changed, 5 insertions(+)
        create mode 100644 Hello.

6. Comprobación: En el codi anterior, el commit mostra clarament com nomes s'ha putjat el Hola.java y no el Hola.class.
