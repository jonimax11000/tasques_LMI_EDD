#Identificar característiques dels llenguatges de marques en diferents documents (svg, html, xml...)

* **Logo.svg:**
     + **Etiquetes:**
        - ``` <svg></svg> ```: Elemenet principal que definix un àrea de dibuix SVG.
        - ``` <g></g> ```: Agupació de elements SVG per a l'aplicació de transformacions o estils en conjunt.
        - ``` <path></path> ```: conjunts de linees, arcs o curves que definixen una forma.
     + **Elements:**
        - **svg:**: 
         ```<svg
            width="198mm"
            height="166mm"
            viewBox="0 0 198 166"
            version="1.1"
            xmlns="http://www.w3.org/2000/svg">
            <g transform="matrix(2.2373964,0,0,2.2374086,-1351.9834,-2209.4334)">
               <path
               style="fill:#fb9c08"
               d="m 647.75482,988.4343 -14.19848,24.169 h 6e-5 l -6.8e-4,17.3938 h -10.21745 l -18.15292,30.901 h -10e-5 l 42.56957,10e-5 z" />
               <path
               style="fill:#653097"
               d="m 623.33811,1012.6033 v 17.3938 l 10.21823,-17.3938 z" />
               <path
               style="fill:#653097"
               d="m 663.88003,1012.6033 v 17.3938 h 10.21813 l 18.15101,30.9009 h -42.5676 v -72.4637 z" />
               <path
               style="fill:#fb9c08"
               d="m 674.0981,1012.6033 v 17.3938 l -10.21825,-17.3938 z" />
            </g>
         </svg>
         ```
        - **g:**  
         ```<g transform="matrix(2.2373964,0,0,2.2374086,-1351.9834,-2209.4334)">
         <path
            style="fill:#fb9c08"
            d="m 647.75482,988.4343 -14.19848,24.169 h 6e-5 l -6.8e-4,17.3938 h -10.21745 l -18.15292,30.901 h -10e-5 l 42.56957,10e-5 z" />
         <path
            style="fill:#653097"
            d="m 623.33811,1012.6033 v 17.3938 l 10.21823,-17.3938 z" />
         <path
            style="fill:#653097"
            d="m 663.88003,1012.6033 v 17.3938 h 10.21813 l 18.15101,30.9009 h -42.5676 v -72.4637 z" />
         <path
            style="fill:#fb9c08"
            d="m 674.0981,1012.6033 v 17.3938 l -10.21825,-17.3938 z" />
         </g>
         ```
        - **path 1:**  
         ```<path
            style="fill:#fb9c08"
            d="m 647.75482,988.4343 -14.19848,24.169 h 6e-5 l -6.8e-4,17.3938 h -10.21745 l -18.15292,30.901 h -10e-5 l 42.56957,10e-5 z" />
         ```
        - **path 2:**  
         ```<path
            style="fill:#653097"
            d="m 623.33811,1012.6033 v 17.3938 l 10.21823,-17.3938 z" />
         ```
        - **path 3:**  
         ```<path
      style="fill:#653097"
      d="m 663.88003,1012.6033 v 17.3938 h 10.21813 l 18.15101,30.9009 h -42.5676 v -72.4637 z" />
         ```
        - **path 4:**  
         ```<path
            style="fill:#fb9c08"
            d="m 674.0981,1012.6033 v 17.3938 l -10.21825,-17.3938 z" />```
    + **Propietats**:
        - ```width```: atribut del ```<svg></svg>``` que definix el ample del llenç en milimetres.
        - ```height```: atribut del ```<svg></svg>``` que definix l'altura del llenç en milimetres.
        - ```viewbox```: atribut del ```<svg></svg>``` que definix l'àrea de visualització per a establir l'escalabilitat.
        - ```version```: atribut del ```<svg></svg>``` que definix la versió del ```SVG```.
        - ```xmlns```: atribut del ```<svg></svg>``` que especifica el ```XML namespace``` per a ```SVG```.
        - ```transform```: atribut del ```<g></g>``` que aplica transformacions (escalat, translació,etc.) als elements dins d'aquest.
        - ```style```: atribut del ```<path></path>``` que aplica estils CSS als elements.
        - ```d```: atribut del ```<path></path>``` amb els comand i coordenades per a descriure la geometria de la forma del path.

* **llenguatges.odt:** on se especifica mirar el document content.xml
    + **Etiquetes:**
        - ```<?xml version="1.0" encoding="UTF-8"?>```: Declara que el document és un fitxer XML i especifica la versió i la codificació utilitzada.
        - ```<office:document-content>```: Element arrel que encapsula el contingut del document en format Open Office, que pot incloure text, imatges i estils.
        - ```<office:scripts/>```: Conté scripts que es poden executar en el context del document, encara que està buit en aquest cas.
        - ```<office:font-face-decls>```: Declara les fonts utilitzades en el document, especificant les propietats de cada font.
        - ```<style:font-face>```: Defineix una font específica que es pot utilitzar en el document, incloent propietats com el nom i l'estil de la font.
        - ```<office:automatic-styles>```: Conté estils automàtics que s'apliquen als elements del document, incloent estils de text i paràgraf.
        - ```<style:style>```: Defineix un estil particular que es pot aplicar als elements del document, incloent propietats específiques.
        - ```<style:paragraph-properties>```: Especifica propietats relacionades amb la presentació d'un paràgraf, com l'alineació del text.
        - ```<style:text-properties>```: Defineix propietats específiques del text, com l'estil de font i el pes del text.
        - ```<text:list-style>```: Descriu l'estil d'una llista en el document, incloent l'aparença de les viñetes o numeracions.
        - ```<text:list-level-style-bullet>```: Defineix l'estil de viñetes per a un nivell particular d'una llista, especificant el caràcter de viñeta i el seu format.
        - ```<text:list-item>```: Representa un ítem dins d'una llista, contenint el contingut de l'element de la llista.
        - ```<office:body>```: Conté el cos principal del document, que inclou text i altres elements.
        - ```<office:text>```: Especifica que el contingut dins d'aquest element és text que s'ha de processar i mostrar.
        - ```<text:sequence-decls>```: Declara les seqüències de text que poden ser utilitzades en el document, com taules o il·lustracions.
        - ```<text:sequence-decl>```: Defineix una seqüència de text específica, indicant com s'ha de manejar i mostrar
        - ```<text:h>```: Representa un encapçalament o títol, utilitzat per estructurar el contingut del document.
        - ```<text:p>```: Indica un paràgraf de text, que pot contenir text i altres elements.
        - ```<text:span>```: Un contenidor per aplicar estils a un fragment de text dins d'un paràgraf.
        - ```<text:list>```: Representa una llista que pot contenir diversos ítems, ja siguen enumerats o amb viñetes.
     + **Elements:** Sols he possat alguns dels elements, ja que el document es molt llarg.
        - **xml:**  
         ```<?xml version="1.0" encoding="UTF-8"?><?xml version="1.0" encoding="UTF-8"?>
         ```
        - **text:sequence-decl:**  
         ``` <text:sequence-decl text:display-outline-level="0" text:name="Illustration"/>```
        - **text:h:**  
         ```<text:h text:style-name="P1" text:outline-level="1">Com parlen els ordinadors?</text:h>```
        - **text:p:**  
         ```<text:p text:style-name="P5">Els ordinadors són màquines molt complexes que ens permeten fer moltes coses.</text:p>```
        - **text:list:**  
         ```<text:list xml:id="list759559877" text:style-name="L1">```
        - **text:list-item:** 
         ```<text:list-item><text:p text:style-name="P6">Els <text:span text:style-name="T1">llenguatges de programació</text:span>, com Python, Java o C++.</text:p></text:list-item>```
     + **Propietats:** Com en els elements, sols he possat unes poques.
        - ```xmlns:office```: Defineix l'espai de noms per als elements de la especificació OpenDocument, que s'utilitzen en documents d'oficina.
        - ```text:style-name```: Indica el nom de l'estil aplicat a un element, permetent la consistència en la presentació del contingut.
        - ```text:outline-level```: Defineix el nivell d'un encapçalament dins de l'estructura del document, ajudant a organitzar el contingut jeràrquicament.
        - ```fo:text-indent```: Estableix la quantitat d'espai que es deixa al començament d'un paràgraf, afectant l'alineació del text.
        - ```xml:id```: Proporciona un identificador únic per a un element dins del document, útil per a referències i estils específics.
        - ```xmlns:svg```: atribut del ```<g></g>``` que aplica transformacions (escalat, translació,etc.) als elements dins d'aquest.
        - ```style```: Defineix l'espai de noms per als elements SVG, que permeten la inclusió de gràfics vectorials escalables en el document.
        - ```xmlns:xlink```: Especifica l'espai de noms per als enllaços en el document, que s'utilitzen per a crear referències a altres recursos o documents.

* **llenguatges.docx:** on se especifica mirar el document word/document.xml
    + **Etiquetes:**
        - ```<?xml version="1.0" encoding="UTF-8" standalone="yes"?>```: Declara que el document és un fitxer XML i especifica la versió i la codificació utilitzada.
        - ```<w:document>```: Element arrel que encapsula el contingut del document en format MS Word.
        - ```<w:body>```: Representa el cos del document, conté tots els paràgrafs i contingut textual.
        - ```<w:p>```: Un paràgraf del document.
        - ```<w:pPr>```: Defineix les propietats del paràgraf on es troba com l'estil i l'alineació.
        - ```<w:pStyle>```: Estableix l'estil del paràgraf (com a encapçalament, normal, etc.)
        - ```<w:bidi>```: Indica si el text es mostra en direcció bidireccional (escriptura d’esquerra a dreta o de dreta a esquerra).
        - ```<w:spacing>```: Estableix l'espaia abans i després d'un paràgraf.
        - ```<w:jc>```: Defineix la justificació del paràgraf (esquerra, dreta, centrat, o justificat).
        - ```<w:r>```: Conté un "run", és a dir, un segment de text dins d’un paràgraf.
        - ```<w:rPr>```: Defineix les propietats d’un "run" de text, com la negreta o la cursiva.
        - ```<w:t>```: Conté el text dins d’un "run".
        - ```<w:b>```: Aplica la negreta al text.
        - ```<w:bCs>```: Aplica estil de negreta específic per a llengües complexes.
        - ```<w:i>```: Aplica la cursiva al text.
        - ```<w:iCs>```: Com el ```<w:bCs``` pero per a la cursiva.
        - ```<w:numPr>```: Defineix les propietats per a la numeració i les llistes.
        - ```<w:ilvl>```: Indica el nivell d’una llista numerada o de vinyetes.
        - ```<w:numId>```: Identificador de la numeració associada amb un paràgraf.
        - ```<w:sectPr>```: Estableix el tipus de secció, com "pàgina següent" o "contínua".
        - ```<w:type>```: Estableix la grandària de la pàgina del document.
        - ```<w:pgSz>```: Estableix la grandària de la pàgina del document.
        - ```<w:pgMar>```: Defineix els marges de la pàgina (esquerra, dreta, superior, inferior).
        - ```<w:pgNumType>```: Defineix el format de la numeració de les pàgines (decimal, romà, etc.).
        - ```<w:formProt>```: Indica si la protecció del formulari està activada en el document.
        - ```<w:textDirection>```: <w:textDirection>: Estableix la direcció del text dins del document (esquerra a dreta o viceversa).
    + **Elements:** Sols he possat alguns dels elements, ja que el document es molt llarg.
        - **w:t:**  
         ```<w:t xml:space="preserve">Com parlen els ordinadors?</w:t>```
        - **w:pStyle:** 
         ``` <w:pStyle w:val="Heading1"/>```
        - **w:bidi:**
         ```<w:bidi w:val="0"/>```
        - **w:rPr:**
         ```<w:rPr></w:rPr>```
        - **w:numPr:**
         ```<w:numPr><w:ilvl w:val="0"/><w:numId w:val="2"/></w:numPr>```
        - **w:sectPr:**
         ```<w:sectPr><w:type w:val="nextPage"/></w:sectPr>```
     + **Propietats:** Com en els elements, sols he possat unes poques.
        - ```xmlns```:  Defineix l'espai de noms per a elements relacionats amb Microsoft Office.
        - ```w:val="both"```: Aquest atribut es troba dins de l'etiqueta ```<w:jc>``` i indica que el text està justificat a ambdós costats.
        - ```w```: Indica el valor d'un paràmetre o configuració dins d'una etiqueta.
        - ```xml```: Defineix com gestionar els espais en blanc dins d'un element de text.
        - ```mc```:  Assenyala quins espais de noms poden ser ignorats per processadors de documents.
        - ```w:before="240"```: atribut del ```<g></g>``` que aplica transformacions (escalat, translació,etc.) als elements dins d'aquest.
        - ```style```: Defineix l'espai de noms per als elements SVG, que permeten la inclusió de gràfics vectorials escalables en el document.
        - ```xmlns:xlink```: Especifica l'espai de noms per als enllaços en el document, que s'utilitzen per a crear referències a altres recursos o documents.

* **MainActivity.xml:**
     + **Etiquetes:**
        - ``` <?xml version="1.0" encoding="utf-8"?> ```: Declara que el document és un fitxer XML i especifica la versió i la codificació utilitzada.
        - ``` <LinearLayout> </LinearLayout>```:  Contenidor que organitza els elements fills en una disposició lineal (vertical o horitzontal).
        - ``` <TextView /> ```: Etiqueta utilitzada per mostrar text a la interfície d'usuari.
        - ``` <Button /> ```: Element de la interfície d'usuari que permet als usuaris fer clic per interactuar amb l'aplicació.
     + **Elements:**
        - **xml:**
         ```<?xml version="1.0" encoding="utf-8"?>```
        - **LinearLayou:** 
         ```
         <LinearLayout
         xmlns:android="http://schemas.android.com/apk/res/android"
         android:layout_width="match_parent"
         android:layout_height="match_parent"
         android:orientation="vertical"
         android:padding="16dp">
         ```
        - **TextView:**
         ```
         <TextView
        android:id="@+id/textView"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="Hola, món!"
        android:textSize="18sp"
        android:layout_marginBottom="16dp"/>
        ```
        - **Button:**
         ```
         <Button
            android:id="@+id/button"
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:text="Prem aquí"/>
         ```
    + **Propietats:**
        - ```version```: atribut del ```<?xml version="1.0" encoding="utf-8"?>``` que definix la versió de *l'XML*.
        - ```encoding```: atribut del ```<?xml version="1.0" encoding="utf-8"?>``` que definix la codificació dels caracters.
        - ```layout_width```: controla l'amplaria del elements com el ``` <LinearLayout> </LinearLayout>```, ``` <TextView> </TextView>``` o ``` <Button> </Button>```.
        - ```layout_height```: controla l'altura del elements com el ``` <LinearLayout> </LinearLayout>```, ``` <TextView> </TextView>``` o ``` <Button> </Button>```.
        - ```orientation```: atribut que estableix la direcció en què es disposen els elements fills dins del ```LinearLayout ```.
        - ```xmlns```: Defineix l'espai de noms per a elements relacionats amb sistemes Android.
        - ```text```: Atribut per definir el text que es mostra en ```TextView``` i ```Button```
        - ```transform```: atribut del ```<g></g>``` que aplica transformacions (escalat, translació,etc.) als elements dins d'aquest.
        - ```textSize```: Aplica la mida del text dins de ```TextView``` en unitats sp (18sp).
        - ```layout_marginBottom```: Afegeix un marge inferior de 16dp al ```TextView```.
* **AndroidManifest.xml:**
     + **Etiquetes:**
        - ``` <?xml version="1.0" encoding="utf-8"?> ```: Declara que el document és un fitxer XML i especifica la versió i la codificació utilitzada.
        - ``` <LinearLayout> </LinearLayout>```:  Contenidor que organitza els elements fills en una disposició lineal (vertical o horitzontal).
        - ``` <TextView /> ```: Etiqueta utilitzada per mostrar text a la interfície d'usuari.
        - ``` <Button /> ```: Element de la interfície d'usuari que permet als usuaris fer clic per interactuar amb l'aplicació.
     + **Elements:**
        - **xml:**
         ```<?xml version="1.0" encoding="utf-8"?>```
        - **LinearLayou:** 
         ```
         <LinearLayout
         xmlns:android="http://schemas.android.com/apk/res/android"
         android:layout_width="match_parent"
         android:layout_height="match_parent"
         android:orientation="vertical"
         android:padding="16dp">
         ```
        - **TextView:**
         ```
         <TextView
        android:id="@+id/textView"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="Hola, món!"
        android:textSize="18sp"
        android:layout_marginBottom="16dp"/>
        ```
        - **Button:**
         ```
         <Button
            android:id="@+id/button"
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:text="Prem aquí"/>
         ```
    + **Propietats:**
        - ```version```: atribut del ```<?xml version="1.0" encoding="utf-8"?>``` que definix la versió de *l'XML*.
        - ```encoding```: atribut del ```<?xml version="1.0" encoding="utf-8"?>``` que definix la codificació dels caracters.
        - ```layout_width```: controla l'amplaria del elements com el ``` <LinearLayout> </LinearLayout>```, ``` <TextView> </TextView>``` o ``` <Button> </Button>```.
        - ```layout_height```: controla l'altura del elements com el ``` <LinearLayout> </LinearLayout>```, ``` <TextView> </TextView>``` o ``` <Button> </Button>```.
        - ```orientation```: atribut que estableix la direcció en què es disposen els elements fills dins del ```LinearLayout ```.
        - ```xmlns```: Defineix l'espai de noms per a elements relacionats amb sistemes Android.
        - ```text```: Atribut per definir el text que es mostra en ```TextView``` i ```Button```
        - ```transform```: atribut del ```<g></g>``` que aplica transformacions (escalat, translació,etc.) als elements dins d'aquest.
        - ```textSize```: Aplica la mida del text dins de ```TextView``` en unitats sp (18sp).
        - ```layout_marginBottom```: Afegeix un marge inferior de 16dp al ```TextView```.