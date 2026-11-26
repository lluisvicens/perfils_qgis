# La creació de perfils topogràfics amb QGIS

A l'hora de dissenyar un perfil topogràfic amb QGIS, per posteriorment incorporar-lo a un *layout* o disseny de mapa, disposem de diverses opcions:

* Dissenyar un perfil topogràfic a la finestra de mapa de QGIS
* Dissenyar el perfil topogràfic, directament des de la finestra de *layout*. 

## 1. Utilitzar complements o *plugins* de QGIS

Són diversos els complements (ArcGeek Calculator, Dual Profile Viewer, Terrain profile, ...) que, una vegada instal·lats a QGIS, permeten la creació i exportació un perfil topogràfic, en format d'imatge. La utilització d'un o altre complement dependrà en bona mesura del tipus de perfil que es vulgui generar.

Per a l'obtenció d'un perfil rectilíni, QGIS disposa de diverses opcions que són realment útils com, per exemple **Dual Profile Viewer** i **Open Topoprofile Studio**.

### 1.1. Dual profile Viewer

Una vegada instal·lat el complement, s'hi pot accedir bé a través del menú *Raster > Dual Profile Viewer* o bé, a través de la icona visible a la zona de barres d'eines.

En accedir a l'eina, es mostra un panell amb diverses opcions que caldrà configurar segons la necessitat. A continuació, es mostra un flux de treball bàsic per obtenir un perfil.

![image](/imatges/p1.png)

*  A l'apartat *Settings*, cal indicar el model digital d'elevacions que prèviament s'haurà carregat al panell de capes de QGIS: **Primary DEM/DTM**
*  A *Samples* cal indicar el nombre de mostres o punts que se situaran al llarg de la línia de perfil, d'on s'obtindrà el valor de cota.
*  Fer un clic sobre l'apartat o botó *Single Line* i dibuixar sobre la finestra de mapa, el punt inicial o final de la línia que es vol utilitzar per calcular el perfil. Una vegada incorporada la línia de perfil, el complement indica que havent finalitzat aquesta tasca, cal fer un clic sobre el botó *Create Profiles*.

![image](/imatges/p2.gif)

* En fer un clic sobre el botó *Create Profiles*, automàticament es mostrarà el perfil topogràfic, podent alternar entre la visualització en mode **web**, o bé en mode **gràfic**. Aquest darrer (desactivant el mode web) permet ajustar-ne alguns paràmetres relatius a les dimensions:

![image](/imatges/p2_bis.gif)

![image](/imatges/p3.gif)

* Així com el textos, color i gruix del perfil topogràfic. Havent realitzat tots els ajustos necessaris, es pot exportar el perfil topogràfic en format imatge (p.e. **.png**) o en format vectorial (**.svg**).

* ![image](/imatges/p4.gif)

El complement Dual Profile Viewer, a més, disposa d'una opció interessant i és que permet construir un layout bàsic, tot incorporant les capes visibles al panell de capes així com el perfil que s'acaba de calcular. Per a executar aquesta opció, cal fer un clic sobre l'opció *Generate layout*, i automàticament es crearà un nou *layout*, accessible des del gestor de *layouts* i des del menú *Project*. Aquest layout bàsic, es pot editar a continuació, per ajustar-los als criteris de disseny necessaris. 

![image](/imatges/p5.png)

### 1.2. Open TopoProfile Studio

Un altre complement de QGIS, que ofereix l'opció de dissenyar perfils topogràfics, especialment, com en el cas anterior, si aquests no són especialment sinuosos, doncs cal dibuixar la línia de manera manual. Una vegada instal·lat el complement, en activar-lo bé a través de la icona situada a la zona de les barres d'eines, bé des del menú *Plugins > TopoProfile Studio*, es mostrarà en una finestra emergent.

![image](/imatges/p6.png)

A continuació, es mostra un flux de treball bàsic per obtenir un perfil.

* Fer un clic sobre el botó *Draw profile path* i dibuixar, sobre la finestra de mapa, la línia de la qual se'n vol obtenir el perfil topogràfic. A continuació, havent indicat a l'apartat Elevations > DTM raster el nom del model digital d'elevacions amb el qual s'està treballant, cal fer un clic sobre el botó **Generate profile**.

* Automàticament es genera un perfil topogràfic on bàsicament, es pot editar el color del perfil, i del farcit del gràfic. També, el valor de les etiquetes de direcció.

![image](/imatges/p7.png)

* Fent un clic sobre el botó *Next*, es passa al darrer pas del complement, des d'on es pot exportar (*Export profile*) el gràfic a imatge raster (**.png**) o bé a gràfic vectorial (**.svg**).

### 1.3. Terrain Profile

En el cas que es necessiti generar un perfil topogràfic que ressegueixi, per exemple, el traçat d'una carretera, camí o recorregut, i que per tant no és especialment rectilini, fet que implicaria dur a terme un procés de pseudo-digitalització si s'utilitzen els complements anteriors, QGIS disposa de **Terrain Profile**. A continuació, es mostra un flux de treball bàsic per obtenir un perfil. 

* En activar aquesta eina, apareixerà un nou panell en el qual caldrà indicar dins l'apartat *Add layer*, quina és la capa relativa al model digital d'elevacions. Per a fer-ho cal, activar la capa en qüestió al panell de capes, i fer clic sobre el botó *Add layer*.
* A continuació, cal activar al panell de capes de QGIS, la capa de línia que representa el traçat, la forma de la qual, se'n vol obtenir el perfil topogràfic. Una vegada activa la capa al panell, dins l'apartat *Options* del panell de l'eina, al paràmetre *Selection* caldrà modificar el valor que es mostra per defecte, per **Selected layer**. Automàticament es genera un perfil que es pot desar en format d'imatge (.png).

![image](/imatges/p8.png)

## 2. Incorporar els perfils obtibnguts amb els complements anteriors.

Sigui quin sigui el complement emprat i el format d'exportació del gràfic (.png vs .svg), el més recomanable en tots els casos és editar les imatges amb un programa d'edició a l'estil de GIMP o Inkscape per tal d'eliminar el *background* (color de fons) blanc dels gràfics. A continuació, havent creat un nou layout, tots aquests gràfics es poden incloure en forma de nova imatge (*Add picture*), indicant en cada cas si es tracta d'una imatge raster (.png) o vectorial (.svg). Per tal de mantenir la llegibilitat del gràfic en redimensionar-lo, i ajustar-lo a la mida del mapa, és recomanable desar els gràfics dels complements en format vectorial (.svg).

![image](/imatges/p9.png)


## 3. Utilitzar l'eina Elevation Profile de la finestra de *layout*

A banda de poder calcular i obtenir perfils topogràfics amb algun dels molts complements que ofereixen aquesta opció a QGIS, des de la finestra de disseny i composició de mapes de QGIS (*layout*), també es poden crear perfils topogràfics, i afegir-los directament a qualsevol composició. A continuació es mostra el flux de treball bàsic per obtenir un perfil topogràfic des de la pàgina de *layout*.

* En primer lloc, al panell de capes de QGIS, cal accedir a les propietats del model digital d'elevacions, i activar l'apartat **Elevation**. Dins de l'apartat *Configuration*, s'ha d'obrir el desplegable on hi mostra el valor **Disabled**, i canviar-lo per **Represents Elevation Surface**. Dins l'apartat *Profile Chart Appearance*, cal indicar si el perfil topogràfic es voldrà representar mitjançant una línia sola, o una línia amb farcit. I en aquest darrer cas, si el farciment es vol aplicar per damunt o per sota de la línia de perfil.
* Dins de *Style*, escollir l'opció **Fill below** i, a continuació, escollir un estil de polígon.
* A continuació, cal obrir o accedir a la finestra de *layout* i activar l'eina **Add Elevation Profile**.

![image](/imatges/p10.gif)

* Abans de crear pròpiament el perfil, és necessari preparar el llenç que l'ha de contenir. És per això que havent seleccionat l'objecte del perfil, a la pestanya de les seves propietats (*Item Properties*), cal modificar els valors relatius als límits del gràfic. Dins de l'apartat **Chart Ranges**, tenint en compte la cota mínima i màxima del model d'elevacions, així com la llargada de la línia que es vol utilitzar per a generar el perfil topogràfic, cal ajustar els següents valors:

![image](/imatges/p11.gif)

* A continuació, a l'apartat **Distance Axis** cal configurar les unitats de la distància (que estan en relació als valors indicats en el pas anterior: 20.000 si són metres, o 20 si són quilòmetres) i definir a quin interval es volen situar les marques de divisió d'ambdós eixos, al gràfic:

![image](/imatges/p12.gif)

* El següent pas consistirà en configurar les divisions i l'etiquetatge de l'eix de les Y, o dels valors d'elevació:

![image](/imatges/p13.gif)

* A continuació, cal activar la pestanya **Atlas** i, activar la casella **Generate an atlas**. Finalment, dins de l'apartat de configuració, cal indicar per al paràmetre *Coverage layer*, la capa que indica el traçat del perfil: capa vectorial del recorregut.
![image](/imatges/p14.gif)

* Per acabar, a la barre d'eines de les funcions d'atles, cal fer un clic sobre la icona **Preview Atlas**. A continuació, dins de les propietats del gràfic, cal activar o marcar la casella **Controled by atlas** i, finalment, marcar la casella del model digital d'elevacions, dins de l'apartat *Layers*.

![image](/imatges/p15.gif)

* Com a tasca final, ja només quedarà ajustar novament tots els detalls que siguin necessaris per configurar el *layout* final.  

![image](/imatges/p16.png)
