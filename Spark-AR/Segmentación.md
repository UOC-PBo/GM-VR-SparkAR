En esta sección veremos cómo implementar una de las funcionalidades más populares de los efectos de Spark: la segmentación

Con este término nos referimos a aquellos efectos que distingan el fondo de objetos en primer plano. Normalmente en primer plano solemos tener a personas, y queremos cambiar el fondo. A continuación haremos un ejemplo de esto.

Vamos a empezar con un proyecto de ejemplo, el Face Decoration, y en la sección de Scene añadiremos un ractángulo ![image](uploads/a28f75897c580a7d45e20741d315b67f/image.png) Queremos que este rectángulo ocupe toda la pantalla, con lo que editaremos las propiedades de width y height para que rellenen todo el espacio con Fill width y Fill Height ![image](uploads/64464cc0dd3cc5813c3c13b0967f895c/image.png) Es posible que los ejemplos de Spark AR no funcionen bien y tengáis que habilitar la cámara de vuestro ordenador. ![image](uploads/3d9665c0153a9c0b8f37df347cabc57d/image.png) Una vez hechos estos pasos, vamos a crear un material para el rectángulo. 

![image.png](uploads/e98e423431a73e1ffe6dfeeabd7a24c7/image.png)Una vez creado, vamos a ponerle una imágen como textura, podéis usar la que queráis. Será lo que se muestre de fondo

![image.png](uploads/4b21a91abc8ebcd59607b7dd5ae98331/image.png)

Ahora seleccionamos la cámara, añadiremos un Segmentation, que es el sistema de Spark para reconocer caras y personas. 

![image.png](uploads/df6cada3b4a1ee2904e4b3ea3c86a9bd/image.png)Finalmente, sólo queda seleccionar de nuevo el material, activar el Alpha, seleccionar la textura segmentationMask (que la acabamos de crear en la operación anterior), e invertir el Alpha

Y ya tenemos nuestro efecto de segmentación!