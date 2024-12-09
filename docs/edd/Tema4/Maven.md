# Maven

## Configura el projecte correctament des de la línia d'ordres, partint del l'arquetip quickstart

```bash
jonimax11000@jonimax11000:~/Desktop/DAM/Primero/EDD/Tema4/MavenQick$ mvn archetype:generate -DgroupId=com.jonathan.edd -DartifactId=calculadoraMaven -DarchetypeArtifactId=maven-archetype-quickstart -DarchetypeVersion=1.5 -DinteractiveMode=false
```

```bash
calculadoraMaven/
├── pom.xml
└── src
    ├── main
    │   └── java
    │       └── com
    │           └── jonathan
    │               └── edd
    │                   └── App.java
    └── test
        └── java
            └── com
                └── jonathan
                    └── edd
                        └── AppTest.java

12 directories, 3 files
```

### Compilar el projecte

```bash
jonimax11000@jonimax11000:~/Desktop/DAM/Primero/EDD/Tema4/MavenQick/calculadoraMaven$ mvn compile
[INFO] Scanning for projects...
[INFO] 
[INFO] -----------------< com.jonathan.edd:calculadoraMaven >------------------
[INFO] Building calculadoraMaven 1.0-SNAPSHOT
[INFO] --------------------------------[ jar ]---------------------------------
[INFO] 
[INFO] --- maven-resources-plugin:3.3.1:resources (default-resources) @ calculadoraMaven ---
[INFO] skip non existing resourceDirectory /home/jonimax11000/Desktop/DAM/Primero/EDD/Tema4/MavenQick/calculadoraMaven/src/main/resources
[INFO] 
[INFO] --- maven-compiler-plugin:3.13.0:compile (default-compile) @ calculadoraMaven ---
[INFO] Nothing to compile - all classes are up to date.
[INFO] ------------------------------------------------------------------------
[INFO] BUILD SUCCESS
[INFO] ------------------------------------------------------------------------
[INFO] Total time:  0.323 s
[INFO] Finished at: 2024-12-09T02:16:26+01:00
[INFO] ------------------------------------------------------------------------
```

```bash
calculadoraMaven/
├── pom.xml
├── src
│   ├── main
│   │   └── java
│   │       └── com
│   │           └── jonathan
│   │               └── edd
│   │                   └── App.java
│   └── test
│       └── java
│           └── com
│               └── jonathan
│                   └── edd
│                       └── AppTest.java
└── target
    ├── classes
    │   └── com
    │       └── jonathan
    │           └── edd
    │               └── App.class
    ├── generated-sources
    │   └── annotations
    └── maven-status
        └── maven-compiler-plugin
            └── compile
                └── default-compile
                    ├── createdFiles.lst
                    └── inputFiles.lst
```

### Execució

```bash
jonimax11000@jonimax11000:~/Desktop/DAM/Primero/EDD/Tema4/MavenQick/calculadoraMaven$ java -cp target/classes com.jonathan.edd.App
Hello World!
```

### Netetja del projecte

```bash
jonimax11000@jonimax11000:~/Desktop/DAM/Primero/EDD/Tema4/MavenQick/calculadoraMaven$ mvn clean
[INFO] Scanning for projects...
[INFO] 
[INFO] -----------------< com.jonathan.edd:calculadoraMaven >------------------
[INFO] Building calculadoraMaven 1.0-SNAPSHOT
[INFO] --------------------------------[ jar ]---------------------------------
Downloading from central: https://repo.maven.apache.org/maven2/org/apache/maven/plugins/maven-clean-plugin/3.4.0/maven-clean-plugin-3.4.0.pom
Downloaded from central: https://repo.maven.apache.org/maven2/org/apache/maven/plugins/maven-clean-plugin/3.4.0/maven-clean-plugin-3.4.0.pom (5.5 kB at 5.0 kB/s)
Downloading from central: https://repo.maven.apache.org/maven2/org/apache/maven/plugins/maven-plugins/42/maven-plugins-42.pom
Downloaded from central: https://repo.maven.apache.org/maven2/org/apache/maven/plugins/maven-plugins/42/maven-plugins-42.pom (7.7 kB at 38 kB/s)
Downloading from central: https://repo.maven.apache.org/maven2/org/apache/maven/plugins/maven-clean-plugin/3.4.0/maven-clean-plugin-3.4.0.jar
Downloaded from central: https://repo.maven.apache.org/maven2/org/apache/maven/plugins/maven-clean-plugin/3.4.0/maven-clean-plugin-3.4.0.jar (36 kB at 174 kB/s)
[INFO] 
[INFO] --- maven-clean-plugin:3.4.0:clean (default-clean) @ calculadoraMaven ---
[INFO] Deleting /home/jonimax11000/Desktop/DAM/Primero/EDD/Tema4/MavenQick/calculadoraMaven/target
[INFO] ------------------------------------------------------------------------
[INFO] BUILD SUCCESS
[INFO] ------------------------------------------------------------------------
[INFO] Total time:  1.838 s
[INFO] Finished at: 2024-12-09T02:21:37+01:00
[INFO] ------------------------------------------------------------------------
```

```bash
/calculadoraMaven/
├── pom.xml
└── src
    ├── main
    │   └── java
    │       └── com
    │           └── jonathan
    │               └── edd
    │                   └── App.java
    └── test
        └── java
            └── com
                └── jonathan
                    └── edd
                        └── AppTest.java
```

### Empaquetat

1. **Creació del JAR:**

        jonimax11000@jonimax11000:~/Desktop/DAM/Primero/EDD/Tema4/MavenQick/calculadoraMaven$ mvn package
        [INFO] Scanning for projects...
        [INFO] 
        [INFO] -----------------< com.jonathan.edd:calculadoraMaven >------------------
        [INFO] Building calculadoraMaven 1.0-SNAPSHOT
        [INFO] --------------------------------[ jar ]---------------------------------
        [INFO] 
        [INFO] --- maven-resources-plugin:3.3.1:resources (default-resources) @ calculadoraMaven ---
 



        /calculadoraMaven/
        ├── pom.xml
        ├── src
        │   ├── main
        │   │   └── java
        │   │       └── com
        │   │           └── jonathan
        │   │               └── edd
        │   │                   └── App.java
        │   └── test
        │       └── java
        │           └── com
        │               └── jonathan
        │                   └── edd
        │                       └── AppTest.java
        └── target
            ├── calculadoraMaven-1.0-SNAPSHOT.jar
            ├── classes
            │   └── com
            │       └── jonathan
            │           └── edd
            │               └── App.class
            ├── generated-sources
            │   └── annotations
            ├── generated-test-sources
            │   └── test-annotations
            ├── maven-archiver
            │   └── pom.properties
            ├── maven-status
            │   └── maven-compiler-plugin
            │       ├── compile
            │       │   └── default-compile
            │       │       ├── createdFiles.lst
            │       │       └── inputFiles.lst
            │       └── testCompile
            │           └── default-testCompile
            │               ├── createdFiles.lst
            │               └── inputFiles.lst
            ├── surefire-reports
            │   ├── com.jonathan.edd.AppTest.txt
            │   └── TEST-com.jonathan.edd.AppTest.xml
            └── test-classes
                └── com
                    └── jonathan
                        └── edd
                            └── AppTest.class

2. **Executant el JAR:**

```bash
jonimax11000@jonimax11000:~/Desktop/DAM/Primero/EDD/Tema4/MavenQick/calculadoraMaven$ java -cp target/calculadoraMaven-1.0-SNAPSHOT.jar com.jonathan.edd.App
Hello World!
```
