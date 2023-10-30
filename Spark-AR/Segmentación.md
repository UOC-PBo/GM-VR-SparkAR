En esta sección, veremos cómo implementar una de las funcionalidades más populares de los efectos de Spark: la segmentación.

Con este término nos referimos a aquellos efectos que distingan el fondo de objetos en primer plano. Normalmente en primer plano solemos tener a personas y queremos cambiar el fondo. A continuación, mostramos un ejemplo de esto.

Vamos a empezar con un proyecto de ejemplo, el Face Decoration, y en la sección de Scene añadiremos un rectángulo.

![image](uploads/a28f75897c580a7d45e20741d315b67f/image.png) 

Queremos que este rectángulo ocupe toda la pantalla, con lo que editaremos las propiedades de Width y Height para que rellenen todo el espacio con Fill Width y Fill Height.

![image](uploads/64464cc0dd3cc5813c3c13b0967f895c/image.png) 

Es posible que los ejemplos de Spark AR no funcionen bien y tengáis que habilitar la cámara de vuestro ordenador. 

![image](uploads/3d9665c0153a9c0b8f37df347cabc57d/image.png) 

Una vez hechos estos pasos, vamos a crear un material para el rectángulo. 

![image.png](uploads/e98e423431a73e1ffe6dfeeabd7a24c7/image.png)

Una vez creado, vamos a ponerle una imagen como textura, podéis usar la que queráis. Será lo que se muestre de fondo.

![image.png](uploads/4b21a91abc8ebcd59607b7dd5ae98331/image.png)

Ahora seleccionamos la cámara y añadiremos Segmentation, que es el sistema de Spark para reconocer caras y personas. 

![image.png](uploads/df6cada3b4a1ee2904e4b3ea3c86a9bd/image.png)

Finalmente, solo queda seleccionar de nuevo el material, activar el Alpha, seleccionar la textura Segmentation Mask (que la acabamos de crear en la operación anterior) e invertir el Alpha.

¡Y ya tenemos nuestro efecto de segmentación!

---
[Página previa](Patch-Editor.md) - [página siguiente](Sonido.md)



# Versió catalana

En aquesta secció veurem com podem implementar una de les funcionalitats més populars dels efectes d'Spark: la segmentació.

Amb aquest terme, ens referim a aquells efectes que distingeixen el fons d'objectes en primer pla. Normalment, en primer pla solem tenir persones i volem canviar el fons. A continuació et mostrem un exemple.

Començarem amb un projecte d'exemple, el Face Decoration, i en la secció d'Scene afegirem un rectangle.

![image](uploads/a28f75897c580a7d45e20741d315b67f/image.png) 

Volem que aquest rectangle ocupi tota la pantalla, i per això editarem les propietats de Width i Height perquè emplenin tot l'espai amb Fill Width i Fill Height.

![image](uploads/64464cc0dd3cc5813c3c13b0967f895c/image.png) 

És possible que els exemples d'Spark AR no funcionin bé i hàgiu d'habilitar la càmera del vostre ordinador. 

![image](uploads/3d9665c0153a9c0b8f37df347cabc57d/image.png) 

Una vegada fets aquests passos, crearem un material per al rectangle. 

![image.png](uploads/e98e423431a73e1ffe6dfeeabd7a24c7/image.png)

Una vegada creat, li posarem una imatge com a textura. Podeu usar la que vulgueu. Serà el que es mostri de fons.

![image.png](uploads/4b21a91abc8ebcd59607b7dd5ae98331/image.png)

Ara seleccionem la càmera i afegirem Segmentation, que és el sistema d'Spark per reconèixer cares i persones. 

![image.png](uploads/df6cada3b4a1ee2904e4b3ea3c86a9bd/image.png)

Finalment, només queda seleccionar de nou el material, activar l'Alpha, seleccionar la textura Segmentation Mask, que acabem de crear en l'operació anterior, i invertir l'Alpha.

I ja tenim el nostre efecte de segmentació!

---
[Pàgina prèvia](Patch-editor.md) - [pàgina següent](Sonido.md)
