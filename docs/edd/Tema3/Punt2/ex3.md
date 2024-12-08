
# Activitat 3: Diferències entre RCS i Subversion

## Introducció

RCS (Revision Control System) i Subversion (SVN) són sistemes de control de versions amb funcionalitats similars però enfocaments diferents.

| Característica        | RCS                                     | Subversion                          |
|-----------------------|-----------------------------------------|-------------------------------------|
| **Arquitectura**      | Emmagatzema versions locals de fitxers. | Basat en un repositori centralitzat. |
| **Treball col·laboratiu** | No es pot treballar amb diversos dispositius.       | Pensat per al treball en equip.      |
| **Gestió de fitxers** | Gestiona canvis en fitxers individuals.        | Canvis de tot el projecte.        |
| **Branques i etiquetes** | No disponible.                        | Disponibles i gestionades.          |

## Comanda breu de les ordres

### Per a RCS

- **`co` (checkout):** Obre una versió del fitxer que està sota el control de versions per a poder modificarlo.
- **`ci` (check-in):** Registra un fitxer nou en el sistema de control de versions o confirma els canvis fets a un fitxer ja està sota el control de versions.

### Per a Subversion

- **`svn co` (checkout):** Clona un repositori complet o una branca específica.
- **`svn ci` (commit):** Desa els canvis al repositori.
- **`svn st` (status):** Mostra l'estat dels fitxers locals respecte al repositori.
- **`svn add`:** Afegeix fitxers nous al control de versions.
- **`svn up` (update):** Sincronitza el repositori local amb el central.

## co i ci fan exactament el mateix en un sistema que en altre? Quines diferències tenen?

No fan exactament el mateix, en *rsc* actuen en front d'un sol fitxer mentre que en *subversion* actua amb tot el projecte.

Ambdós sistemes serveixen per gestionar versions, però SVN és més complet per al treball en equip.
