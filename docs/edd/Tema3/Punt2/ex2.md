# Activitat 2. Control de versions i model iteratiu

## Model de desenvolupament

Seguint el model iteratiu i incremental, el projecte estarà organitzat en cinc iteracions. Cada iteració afegirà noves funcionalitats, i el repositori ha d'estar estructurat per permetre:

- Facilitat de manteniment.
- Accés a versions estables anteriors.
- Flexibilitat per al desenvolupament paral·lel.

## Estructura proposada

En el projecte tindrem la branca principal ```/trunk/``` amb la versió del projecte actual i on es possaran els canvis acceptats.

A banda tindrem un directori ```/branches/``` on es probaran les funcionalitats experimentals i es traballaran les iteracions en paralel.

En el directori ```/tags/``` guardarem les versions estables de cada iteració.

A banda l'equip necesitará documentar el projecte, per el que esta es guardará en ```/docs/```

## Visualització de l'estructura

```plaintext
/projecte
├── trunk/                # Codi principal en desenvolupament.
├── branches/             # Branques per a treball paral·lel.
│   ├── iteracio1/        # Codi específic de la fase 1.
│   ├── iteracio2/        # Codi específic de la fase 2.
│   ├── iteracio3/        # Codi específic de la fase 3.
│   ├── ...               # etc
|   └── ...               # etc
├── tags/                 # Versions estables.
│   ├── v1.0/             # Versió final iteració 1.
│   ├── v2.0/             # Versió final iteració 2.
│   └── v3.0/             # etc.
└── docs/                 # Documentació del projecte.
```
