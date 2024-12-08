# Activitat 1. Desenvolupament col·laboratiu

## Mecanismes utilitzats

Per al que respecta en aquest exercici, se comparen el **rsc** i el **Subversion**.

Per garantir la col·laboració efectiva entre Joan i Miquel, utilitzarem un sistema de control de versions centralitzat com **Subversion**. Els avantatges principals inclouen:

- **Col·laboració en temps real:** Permet treballar en equip amb diversos dispositius.
- **Historial de versions:** Permet consultar i revertir canvis si cal.
- **Branques i etiquetes:** Possibilitat de treballar en funcionalitats aïllades.
- **Actualitzacions i fusionament:** Sincronització de treball entre desenvolupadors.

## Procediment detallat

1. **Preparació:**
    1. **Registre en SourceForge:** Joan accedeix a [https://sourceforge.net/user/registration](https://sourceforge.net/user/registration) i es registra acceptant el correu de confirmció.
    2. **Creació del repositori:** Inicia sesió en el servidor i crea un nou projecte nou on  selecciona *Subversion* com a sistema de control de versions.
2. **Configuració inicial:**
    - Crea un repositori central amb una estructura bàsica (`/trunk`, `/branches`, `/tags`).
    - Joan i Miquel instalen el paquet *subversion* en els seus dispositius.```sudo apt install subversion```
    - Joan i Miquel clonen el repositori localment. ```svn checkout --username=Usuari Repositori_Remot Directori_Local```
3. **Treball diari:**
    - **Abans de començar a treballar:** Actualitzaran el repositori local amb l'ordre update de *subversion*: ```svn up```
    - **Desenvolupament:**
     1. Modificar el codi font localment.
     2. Realitzar proves per assegurar-se que les modificacions funcionen.

    - **En acabar el treball:**
        1. Afegir nous fitxers si cal:

            ```svn add <nom_fitxer>```

        2. Comprovar els canvis pendents:

            ```svn st```

        3. Confirmar els canvis al repositori:

        ```bash
        svn ci -m "Missatge explicatiu dels canvis"
        ```

4. **Resolució de conflictes:**
    - En cas de conflictes, utilitzar les eines que proporciona SVN per fusionar manualment els canvis.

Amb aquesta metodologia, Joan i Miquel poden treballar de manera coordinada i evitar sobrescriure el treball de l'altre.
