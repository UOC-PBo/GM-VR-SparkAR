En esta sección, veremos qué herramientas nos ofrece Spark AR para hacer un seguimiento de una cara y poder aplicar efectos en ella.

Antes de empezar, vamos a aclarar qué significa _face tracking_ en este contexto. Spark AR está pensado para desarrollar aplicaciones que se ejecuten en dispositivos móviles, usando la cámara para mostrar información o efectos digitales sobre el mundo real. En el caso de Face Tracking cuando la cámara detecte un rostro, activará las funciones que se hayan programado. Internamente, un sistema de _face tracking_ detecta la posición y orientación de la cara respecto de la cámara, y ofrece esta información a los sistemas que se hayan integrado en la aplicación. Vamos a ver ejemplos prácticos de cómo utilizar el Face Tracking de Spark AR.

Empezaremos abriendo un proyecto nuevo en Spark Studio:

![image](uploads/bb916e710de3206f3bd7e78b81ebadd0/image.png)

Podéis ver que el proyecto ya viene configurado con un ejemplo de vídeo para simular lo que podría estar viendo una cámara. Añadir _face tracking_ es tan simple como apretar el botón derecho del ratón en la zona de la escena.

![image](uploads/97a06d84915b218d275dd792e7b1d796/image.png)

Veréis como, después de añadir el _face tracking_, la imagen en el _viewport_ incluye los ejes que indican la orientación del rostro detectado:

![image](uploads/e478bfab7b175eea2addf2257133794a/image.png)

Añadir _face tracking_ en sí mismo no tiene mucha utilidad. Ahora vamos a incluir todo lo necesario para que nuestro proyecto produzca un primer efecto en la cara detectada por la cámara. Primero añadimos un _face mesh_, que es una representación 3D de la geometría de la cara detectada. No hay más que apretar el botón derecho encima del _face tracker_ y seleccionar Add Object y Face Mesh.

![image](uploads/f273d925a956d76cf5e19d7ee29f31c7/image.png)

Ahora usaremos esta geometría añadiendo materiales que quedarán asociados al _face mesh_. Crear un material es tan sencillo como seleccionar el _face mesh_ que acabamos de crear y, en la sección Materials, en el inspector de propiedades, apretar el botón +.

![image](uploads/2ecfb2a72ba79befda5b5b2630ecbc4d/image.png)

Esta acción crea un material que está asociado al _face mesh_ y que podemos ver en la sección de Assets del proyecto.

![image](uploads/4e3f0bff2864e1437de07a9b36c4e45a/image.png)

Los materiales sirven en esencia para definir texturas y _shaders_. Un _shader_ es un pequeño programa que indica cómo queremos que se visualicen los objetos y sus texturas, aplicando efectos. Un ejemplo clásico de _shaders_ son los que crean efectos de dibujos animados, en contraste con los que intentan generar imágenes realistas. En nuestro caso, seleccionaremos el _shader face paint_, clicando en el material y luego Face paint en el desplegable de Shader Type.

![image](uploads/cfe1288cac2d8adb3d91184a67207791/image.png)

Podréis ver que el efecto del _shader_ resulta en, como indica el nombre, dar la impresión de que se está pintando encima del rostro detectado. Ya solo queda añadir la textura. Qué textura poner depende de vuestra libertad creativa y del efecto que queráis dar. En nuestro caso, simplemente añadiremos un bigote y una barbilla simpáticos. Esta textura la podéis generar a mano, o bien buscarla por internet. En todo caso, para asociarla al material, hay que seleccionar dicho material y, en el apartado Face paint de las propiedades, clicar en Choose file y escoger el fichero que contiene la textura que queremos.

![image](uploads/6549c959dd7c532ac6461dfbbb964705/image.png)

¡Y ya está! Una vez seleccionado, nuestro efecto ya estará terminado.

![image](uploads/d9c1aab75831dca3c35cebb02d9e99f7/image.png)

---
[Página previa](Studio.md) - [página siguiente](Plane-Tracker.md)



# Versió catalana

En aquesta secció veurem quines eines ens ofereix Spark AR per fer un seguiment d'una cara i poder aplicar-hi efectes.

Abans de començar aclarirem què significa _face tracking_ en aquest context. Spark AR està pensat per desenvolupar aplicacions que s'executin en dispositius mòbils usant la càmera per mostrar informació o efectes digitals sobre el món real. En el cas de Face Tracking, quan la càmera detecti un rostre, activarà les funcions que s'hagin programat. Internament, un sistema de _face tracking_ detecta la posició i orientació de la cara respecte de la càmera i ofereix aquesta informació als sistemes que s'hagin integrat en l'aplicació. Veurem exemples pràctics de com utilitzar el Face Tracking d'Spark AR.

Començarem obrint un projecte nou en Spark Studio:

![image](uploads/bb916e710de3206f3bd7e78b81ebadd0/image.png)

Podeu veure que el projecte ja ve configurat amb un exemple de vídeo per simular el que podria estar veient una càmera. Afegir _face tracking_ és tan simple com prémer el botó dret del ratolí en la zona de l'escena.

![image](uploads/97a06d84915b218d275dd792e7b1d796/image.png)

Veureu com, després d'afegir el _face tracking_, la imatge del _viewport_ inclou els eixos que indiquen l'orientació del rostre detectat:

![image](uploads/e478bfab7b175eea2addf2257133794a/image.png)

Afegir _face tracking_ no té per si mateix molta utilitat. Ara inclourem tot el necessari perquè el nostre projecte produeixi un primer efecte en la cara detectada per la càmera. Primer afegim un _face mesh_, que és una representació en 3D de la geometria de la cara detectada. Només cal prémer el botó dret damunt del _face tracker_ i seleccionar Add Object i Face Mesh.

![image](uploads/f273d925a956d76cf5e19d7ee29f31c7/image.png)

Ara usarem aquesta geometria afegint materials que quedaran associats al _face mesh_. Crear un material és tan senzill com seleccionar el _face mesh_ que acabem de crear i, en la secció Materials de l'inspector de propietats, prémer el botó +.

![image](uploads/2ecfb2a72ba79befda5b5b2630ecbc4d/image.png)

Aquesta acció crea un material que està associat al _face mesh_ i que podem veure en la secció d'Assets del projecte.

![image](uploads/4e3f0bff2864e1437de07a9b36c4e45a/image.png)

Els materials serveixen en essència per definir textures i _shaders_. Un _shader_ és un petit programa que indica com volem que es visualitzin els objectes i les seves textures aplicant efectes. Un exemple clàssic de _shaders_ són els que creen efectes de dibuixos animats. En contrast amb ells, intenten generar imatges realistes. En el nostre cas, seleccionarem el _shader face paint_ clicant en el material i després Face paint en el desplegable de Shader Type.

![image](uploads/cfe1288cac2d8adb3d91184a67207791/image.png)

Podreu veure que l'efecte del _shader_ resulta, com indica el nom, en fer l'efecte que s'està pintant damunt del rostre detectat. Ja només queda afegir la textura. La textura que posarem depèn de la vostra llibertat creativa i de l'efecte que vulgueu donar. En el nostre cas, simplement afegirem un bigoti i una barbeta simpàtics. Aquesta textura la podeu generar-la a mà o bé buscar-la per internet. En tot cas, per associar-la al material, cal seleccionar aquest material i, en l'apartat Face paint de les propietats, clicar en Choose file i triar el fitxer que conté la textura que volem.

![image](uploads/6549c959dd7c532ac6461dfbbb964705/image.png)

I ja està! Una vegada seleccionat, el nostre efecte ja estarà acabat.

![image](uploads/d9c1aab75831dca3c35cebb02d9e99f7/image.png)

---
[Pàgina prèvia](Studio.md) - [pàgina següent](Plane-tracker.md)
