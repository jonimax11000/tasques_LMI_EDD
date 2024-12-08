# Exemples de traducció

Depenent del idioma en el que es traballa, el tractament dels còdics font es distint, ja que, entre altres coses, el idioma pot ser compilat, interpretata o un hibrid de ambdos.
A continuació anem a vore Per a què serveix l'ordre python3? I cc? I java i javac.

## Ordere python3

Python es un idioma interpretat per lo que no es crea ningun fitxer executable ja que el codi font es el executable per se.
L'ordre **python3** s'utilitza per executar scripts escrits en llenguatge de programació Python. Quan executes un fitxer amb l'ordre **python3**, l'intèrpret de Python llegeix i executa el codi que conté. Si el fitxer conté errors, l'intèrpret mostrarà missatges d'error per ajudar a solucionar-los.
Ex: ```python3 script.py```.
Al fer us del comand **file** en aquest *script.py* (```file script.py```) mostraria èl següent:

```
    script.py: Python script, ASCII text
```

## Ordere cc

C es un idioma compilat, per lo que es te que crear un fitxer executable.
L'ordre **cc** és un compilador per a llenguatge de programació C. Es fa servir per compilar fitxers de codi font en C a fitxers executables. Quan compiles un fitxer amb l'ordre **cc**, el compilador tradueix el codi font en un fitxer executible que pot ser executat pel sistema operatiu. Si hi ha errors de sintaxi, el compilador els mostrarà en la consola.
Ex: ```cc programa.c -o program```. Açò crea l'executable *programa*.
Al fer us del comand **file** en aquest *programa.c* i *programa* (```file programa.c programa```) mostraria èl següent:

```
    programa.c: C source, ASCII text
    programa: ELF 64-bit LSB executable, x86-64, version 1 (SYSV), dynamically linked, interpreter /lib64/ld-linux-x86-64.so.2, for GNU/Linux 2.6.32, BuildID[sha1]=..., with debug_info, not stripped
```

## Ordere java

Java es un idioma hibrid, per lo que es te que crear un fitxer executable.
L'ordre **java** S'utilitza per executar aplicacions *Java*. Aquesta ordre busca el bytecode compilat (fitxers .class) i el carrega per a la seva execució. Quan executes una classe Java amb *java NomClasse*, l'intèrpret de Java (JVM) carrega el bytecode i el tradueix en instruccions que el sistema operatiu pot executar. Els fitxers .class contenen el bytecode generat pel compilador **javac**.
Ex: ```java NomClasse.class```.
Al fer us del comand **file** en aquest *programa.c* i *programa*(```file NomClasse.class```) mostraria èl següent:

```
    NomClasse.class: Java class file, version 52.0 (Java 8)
```

## Ordere javac

Java es un idioma hibrid, per lo que es te que crear un fitxer executable.
L'ordre **javac** és el compilador per a llenguatge de programació *Java*. S'encarrega de compilar fitxers de codi font ```.java``` a fitxers de bytecode ```.class```. Quan compiles un fitxer amb **javac**, aquest analitza el codi font per detectar errors i genera fitxers ```.class``` que contenen el bytecode. Si es troben errors, **javac** els mostrarà per a la seva correcció.
Ex: ```javac NomClasse.java```. Açò crea l'executable *NomClasse.class*.
Al fer us del comand **file** en aquest *NomClasse.java* (```file NomClasse.java```) mostraria èl següent:

```
    NomClasse.java: Java source, ASCII text
```
