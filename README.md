# Practica_04_ChristianTorresGonzalez

  En esta cuarta práctica, tendré que implementar una escena en la cual se encuentran diversos objetos y que proporcionaran poderes al jugador. Para ello, tendré jugar con las físicas que se le pueden añadir a los objetos que situados en la escena. Para la realización de esta practica, la dividiré en varias partes, una primera parte inicial, en la que desarrollaremos una escena básica con un plano, una esfera, y un cubo. Serán a estos objetos, a los que le añadiré todas estas opciones que deberemos implementar en la practica. Para este primer punto, trabajaremos simplemente con el inspector de nuestra escena, ya será en la segunda parte de la practica, donde trabajaremos con scripts.
  - 1. Desarrollamos nuestra escena básica, en la que incluiremos un plano sobre el que se situarán y podrán mover los objetos, para que en los puntos posteriores, al aplicarle las físicas a los objetos, puedan apreciarse esas propiedades.
  
  ![Alt text](/img/escena.png)
  
  - 1.a) Una vez situados los objetos en la escena, tengo que añadirle las físicas, ya que si no, estos se quedarán flotando en el aire y lo que es mas importante, no podrán colisionar con el resto de objetos, siendo este el punto clave de la práctica. Para ello, añadiré a todos los objetos la opción de Rigidbody, con la que quedarán añadidas las físicas a los objetos.

- Con esto quedaría terminado el primer punto de la practica, el cual ha consistido en formar nuestra escena con objetos sencillos y ubicarlos por nuestro plano, clasificándolos en objetos con movimiento rectilíneo y objetos que no se moverán, es decir, estáticos.


### Ejercicio 2
- 2.) En este segundo ejercicio, se nos pide que un grupo de los objetos que he colocado en la escena, al colisionar con el jugador, este salga desplazado una cantidad proporcional al poder del jugador, en la dirección en la que el jugador colisiona con el objeto.
- Para el desarrollo de este segundo punto, he implementado un script, con el cual se detectara si el objeto, en este caso he decidido que serán los cubos los que se desplazaran una cantidad proporcional al poder, ha entrado en contacto con el jugador. En caso de que hayan colisionado, se aplicará dicho desplazamiento en función del poder que tenga el jugador en ese momento. 
- He desarrollado dos script, uno perteneciente al jugador, que será el encargado de ir registrando el poder, además de contener las funciones encargadas de incrementar el poder y la función encargada de retornar el poder para usarlo en el siguiente script.
  
  ![Alt text](/img/poder.png)
  
- El siguiente script que he desarrollado para este segundo apartado, es el encargado de detectar la colisión con el jugador. En caso de que el cubo colisione con el jugador, se calculará la dirección en la que tiene que salir disparado el cubo y se aplicara dicha fuerza.
  
  ![Alt text](/img/colisionCubo.png)

- Tras el desarrollo de los scripts anteriores, este seria el resultado final

![Alt text](/img/cubo.gif)

### Ejercicio 3
- 3. Para el tercer ejercicio y cuarto ejercicio, ya que este consiste en trabajar con el mismo conjunto de objetos los explicare en este mismo punto del informe. Se pide que a los otros objetos que nos quedan en la escena, estos se moverán al entrar en contacto con el jugador, pero además de esto,  esto harán que el jugador sume puntos a su poder, por lo que cuando tocamos una esfera, se incrementa el poder, lo cual hará que al tocar un cubo este se desplace una distancia mayor. Además, cuando una esfera entra en contacto, esta deberá cambiar su color degradándolo hasta llegar a un umbral, el cual al ser superado, se eliminara dicha esfera, mientras ocurre esto, la esfera, con cada colisión deberá ir disminuyendo su tamaño.

- Para ello, lo primero que hare será desarrollar un script en el cual se detecte cuando un objeto ha entrado en colisión. En caso de que la esfera haya colisionado con el jugador, se producirán don cosas, primero se sumaran los puntos de poder al jugador, en segundo lugar se llevara a cabo el degradado de color, finalmente la tercera ejecución que se hace cuando se produce la colisión es la disminución de la escala.

![Alt text](/img/colisionEsfera.png)

- El segundo script que he desarrollando es el encargado de ir cambiando el color de la esfera, donde defino el índice de color que se va a ir degradando y el umbral que en caso de superar, provocará que se elimine el objeto. En caso de entrar en colisión, es el anterior script encargado de llamar a la función que cambia el color de la esfera.

![Alt text](/img/color.png)

- Finalmente, tras el desarrollo de los dos script anteriores, este seria el resultado final.

![Alt text](/img/esfera.gif)
