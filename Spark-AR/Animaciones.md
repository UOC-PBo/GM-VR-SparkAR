En esta sección aprenderemos a trabajar con animaciones. El primer paso será bajarnos [este ejemplo](https://sparkar.facebook.com/ar-studio/learn/tutorials/3d-objects-animation) de Meta (la empresa creadora de Spark) para tener una base con los elementos necesarios para ver los diversos aspectos.

Las animaciones en Spark AR se controlan mediante un Animation Playback Controller. Creamos uno haciendo click derecho en la sección de Assets y seleccionando Add Asset -\> Playback Controller -\> Animation Playback Controller: ![image](uploads/184f005fc66e4969e5922e8bce190462/image.png)

Ahora le vamos a indicar al Animation Playback Controller que queremos que gestione la animación que tenemos en el proyecto para el osos de peluche ![image](uploads/0f61b22d5bf2f7110d977f1a9b5b2dc2/image.png)

Ahora en la sección de Scene vamos a asociar este Animation Playback Controller al oso de peluche. Seleccionamos el objeto Teddy y en el desplegable de la configuración de Animation, hacemos click en el objeto que acabamos de crear. ![image](uploads/fbec6bb9245acb36d3d159ef378ebc24/image.png)

Veréis que nada más añadir el controller, el oso de peluche comenzará a animarse. Tenéis varias opciones disponibles en el Animation Playback Controller para controlar las animaciones, la mayoría son bastante autoexplicativas.

![image.png](uploads/fd3bcb6cf6d5d022975c2f647245900e/image.png)

Una opción aún más interesante es aprender a generar animaciones manualmente. Antes hacerlo, debemos entender la base de cómo funcionan las animaciones. 

El primer concepto a entender es el de keyframes. Podemos entender una animación como una serie de posiciones una detrás de la otra durante un intervalo de tiempo. Sería impracticable definir para cada instante, porque el tiempo es contínuo. Incluso aunque decidiésemos discretizar el tiempo, tendríamos que decidir cada cuanto tiempo definir cada muestra. Si decidiésemos definirlo, por ejemplo a una velocidad de 60Hz, en pantallas de 120Hz tendríamos errores, pero tampoco podríamos estar constantemente subiendo de valor porque el límite sería infinito. 

Los keyframes son la solución a este problema. Son en esencia las posiciones relevantes, donde hay algún cambio, y una animación interpola todas las posiciones entre esos keyframes. Es decir, si tenemos un keyframe A, B y C, todas las posiciones intermedias entre A y B se calculan con la interpolación de los valores, y lo mismo entre B y C.

El segundo concepto es el de skeleton (esqueleto). 