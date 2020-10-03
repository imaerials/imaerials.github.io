---
title: "Un vistazo a Node-Red"
date: 2020-10-03
categories:
  - blog
tags:
  - iot
  - nodered
---

Allá por el 2013, cuando comencé a meterme con el mundo de Internet de las cosas(IoT), me era un tanto tedioso tener que armar una plataforma para realizar las pruebas de los dispositivos que en ese entonces estaba desarrollando. 
A pesar de que tengo conocimientos en programación y podía desarrollar un server procesar y visualizar los mensajes de los dispositivos, la idea era enfocarme en el progreso del dispositivo y no perder tiempo armando la plataforma. 

Había leído en internet que uno de los lenguajes más amigados con IoT era Javascript. En una de las búsquedas di con esta fácil, potente y estable herramienta llamada Node-Red.

¿Qué es Node Red? 

[Node Red](https://nodered.org/) es un entorno de programación visual basada en [Node JS](https://nodejs.org/es/) y orientada a aplicaciones conducidas por eventos (Event Driven Applications).

Básicamente, Node-Red nos permite construir casi cualquier tipo de aplicación en solo unos clicks y con solo unas pocas(casi nulas) líneas de código.

Entonces, yo lo que necesitaba era  un servidor web que procese los mensajes de los dispositivos, en su mayoría sensores de temperatura, humedad y algunos accionadores, los guarde en una base de datos y los muestre de una manera bonita e intuitiva. Node Red me hizo lograr este objetivo en unos pocos clicks.

Armar dicho servidor es cosa de arrastrar distintos “nodos” que cumplen distintas funciones, unirlos y guardar los cambios realizados.

En la siguiente captura pueden ver los “nodos” en colores unidos por líneas. 

![Node Red Flows](/assets/images/NR2.png)

El primer nodo llamado “Inject Info” tiene unas configuraciones que lo único que hacen es enviar un “pulso” cada 5 segundos.

El segundo nodo llamado “process” tiene una función en Javascript que se dispara con el pulso del nodo anterior y devuelve un número aleatorio entre 0 y 100. 

Luego los nodos “Gauge” y “chart” son solo componentes visuales, uno es una especie de medidor de aguja y el otro un cuadro de líneas que se muestran en un panel web publicado en el servidor Node-Red.


Esta simple unión de nodos, resulta en un bonito panel que muestra los números aleatorios generados por los nodos anteriormente mencionados.

![Node Red Dashboard](/assets/images/NR1.png)

El panel puede ser accedido vía web apuntando el navegador hacia la dirección IP de donde está instalado Node Red.

Las posibilidades que ofrece Node-Red son infinitas, la comunidad crece cada dia mas y hay muchas cosas ya hechas que se pueden usar a gusto y manera. Ademas de los miles de nodos adicionales que pueden descargar para sus proyectos. 

A medida que pueda, iré subiendo como yo utilizo Node-Red y más informacion.

Para mi es una herramienta que vale la pena dedicarle algo de tiempo.