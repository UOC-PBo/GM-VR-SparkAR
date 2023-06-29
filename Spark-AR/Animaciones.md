En esta sección aprenderemos a trabajar con animaciones. El primer paso será bajarnos [este ejemplo](https://sparkar.facebook.com/ar-studio/learn/tutorials/3d-objects-animation) de Meta (la empresa creadora de Spark) para tener una base con los elementos necesarios para ver los diversos aspectos.

Las animaciones en Spark AR se controlan mediante un Animation Playback Controller. Creamos uno haciendo click derecho en la sección de Assets y seleccionando Add Asset -\> Playback Controller -\> Animation Playback Controller: ![image](uploads/184f005fc66e4969e5922e8bce190462/image.png)

Ahora le vamos a indicar al Animation Playback Controller que queremos que gestione la animación que tenemos en el proyecto para el osos de peluche ![image](uploads/0f61b22d5bf2f7110d977f1a9b5b2dc2/image.png)

Ahora en la sección de Scene vamos a asociar este Animation Playback Controller al oso de peluche. Seleccionamos el objeto Teddy y en el desplegable de la configuración de Animation, hacemos click en el objeto que acabamos de crear. ![image](uploads/fbec6bb9245acb36d3d159ef378ebc24/image.png)

Veréis que nada más añadir el controller, el oso de peluche comenzará a animarse. Tenéis varias opciones disponibles en el Animation Playback Controller para controlar las animaciones, la mayoría son bastante autoexplicativas.

![image.png](uploads/fd3bcb6cf6d5d022975c2f647245900e/image.png)

Una opción aún más interesante es aprender a generar animaciones manualmente. Antes hacerlo, debemos entender la base de cómo funcionan las animaciones.

El primer concepto a entender es el de keyframes. Podemos entender una animación como una serie de posiciones una detrás de la otra durante un intervalo de tiempo. Sería impracticable definir para cada instante, porque el tiempo es contínuo. Incluso aunque decidiésemos discretizar el tiempo, tendríamos que decidir cada cuanto tiempo definir cada muestra. Si decidiésemos definirlo, por ejemplo a una velocidad de 60Hz, en pantallas de 120Hz tendríamos errores, pero tampoco podríamos estar constantemente subiendo de valor porque el límite sería infinito.

Los keyframes son la solución a este problema. Son en esencia las posiciones relevantes, donde hay algún cambio, y una animación interpola todas las posiciones entre esos keyframes. Es decir, si tenemos un keyframe A, B y C, todas las posiciones intermedias entre A y B se calculan con la interpolación de los valores, y lo mismo entre B y C.

El segundo concepto es el de skeleton (esqueleto). Supongamos que tenemos un objeto 3D con miles de vértices y lo queremos animar por partes, como por ejemplo en un humanoide mover los brazos independientemente de las piernas. Si tuviéramos que definir cómo se mueven todos los vértices uno a uno, generar animaciones para objetos complejos sería impracticable. Para facilitarnos la tarea necesitamos un skeleton. Esta es una estructura de datos que define de manera muy simplificada cómo se mueven los vértices en relación a un punto de referencia, o articulación. Por ejemplo, cuando giramos el codo, el antebrazo se desplaza, pero el hombro no. La generación de esqueletos es tarea de quien modele el objeto, y se sale del alcance de este tutorial

En nuestro ejemplo tenemos el Teddy con el esqueleto ya definido. Si vamos recorriendo el objeto seleccionando las flechas, veremos donde está cada articulación.

![image.png](uploads/2844fb11141bc72d9dd918f2cd975485/image.png)Ahora vamos a crear una animación a mano, sin utilizar las animaciones ya definidas en el modelo. El primer paso es borrar el Animation Playback Controller, porque sino Spark AR siempre lo tomará como el sistema que controla el movimiento del objeto. Seguidamente, haremos click en la articulación a animar. En este caso, vamos a animar el brazo derecho, por lo que seleccionaremos arm_r. Cuando hagamos click en la flecha de la propiedad de rotación, se nos creará un Patch, y veremos el patch editor en la parte inferior de Spark Studio.

![image.png](uploads/b02e8b809db60b416246c677f4618a5c/image.png)Patch editor será nuestro sistema de control de animaciones, donde definiremos cómo se comporta la animación. Si queremos que salude, necesitaremos que la animación se repita, por lo que vamos a añadir un Loop Animation a nuestro patch, haciendo click derecho, seleccionando Loop Animation y Add Patch

![image.png](uploads/72d6b9d69a6b9214223a682da6270f6c/image.png)A continuación, vamos a indicarle al Patch editor que queremos cambiar valores de algún componente. Lo podemos hacer añadiendo un Transition, que tendremos que conectar

![image.png](uploads/a2e2013ac14ff6cc7d28699a9395ce22/image.png)La idea del Patch editor es poder hacer cambios visualmente, sin tener que editar código, y consiste en conectar nodos unos con otros. En nuestro caso, queremos que la animación se repita, con lo que vamos a conectar Loop Animation con Transition, en la parte de Progress. Esto le indica a Spark que Loop controla que Transition se repita. También queremos que Transition afecte al brazo, y esto lo indicamos conectando la salida de Transition con arm_r, que recordemos controla el brazo de Teddy

Ahora para indicarle a Spark que queremos que el brazo se mueva, hay que editar los campos de Start y End en el nodo Transition. En concreto, haciendo pruebas podemos ver que si indicamos que End tenga los valores 0,0,30 queda una animación parecida a un saludo. Sólo queda arreglar un problema, y es que al acabar, la animación vuelve instantáneamente al inicio. Lo que queremos es que vuelva al principio suavemente, y eso lo podemos hacer marcando la opción de Mirrored en el Loop Animation

![image.png](uploads/d776975fed07995c74b30e1a69bd8ed0/image.png)Y ya tenemos la animación completa!