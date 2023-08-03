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
