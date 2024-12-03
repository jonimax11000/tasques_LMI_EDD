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
