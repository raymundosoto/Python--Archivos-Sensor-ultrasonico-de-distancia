# Sensor-ultrasonico-de-distancia

Este repositorio contiene el procedimiento para conectar el sensor ultrasónico de distancia HC-SRO4 a la raspberry pi 4 usando los GPIO y las bibliotecas de Python 3.9. Los datos del sensor de distancia son mostrados en la terminal de las raspberry pi y guradados en un archivo de texto.

El sensor HC-SR04 es un sensor de distancia que utiliza ultrasonido para determinar la distancia de un objeto en un rango de 2 a 450 cm. Destaca por su pequeño tamaño, bajo consumo energético, buena precisión y excelente precio. El sensor HC-SR04 es el más utilizado dentro de los sensores de tipo ultrasonido, principalmente por la cantidad de información y la comunidad de desarrollo que hay en la web. De igual forma, es el más empleado en proyectos de robótica como robots laberinto o sumo y en proyectos de automatización como sistemas de medición de nivel o distancia.

El sensor HC-SR04 posee dos transductores: un emisor y un receptor piezoeléctricos, además de la electrónica necesaria para su operación. El funcionamiento del sensor es el siguiente: el emisor piezoeléctrico emite 8 pulsos de ultrasonido(40KHz) luego de recibir la orden en el pin TRIG, las ondas de sonido viajan en el aire y rebotan al encontrar un objeto, el sonido de rebote es detectado por el receptor piezoeléctrico, luego el pin ECHO cambia a Alto (5V) por un tiempo igual al que demoró la onda desde que fue emitida hasta que fue detectada, el tiempo del pulso ECO es medido por el microcontrolador y asi se puede calcular la distancia al objeto. El funcionamiento del sensor no se ve afectado por la luz solar o material de color negro (aunque los materiales blandos acústicamente como tela o lana pueden llegar a ser difíciles de detectar).

La distancia se puede calcular utilizando la siguiente formula:

Distancia(m) = {(Tiempo del pulso ECO) * (Velocidad del sonido=340m/s)}/2

## Material necesario
- Sensor HC-SR=$
- Raspberry pi 4
- Protoboard
. Cables jumpers
- Cable de conexión Para Raspberry 2x20 Pines
- Resistencias de 1 K y 2.2 K

## Software necesario
- Python 3.9.x
- Biblioteca GPIO para python

## Esquema de conexión
Se construye el siguiente circuito entre el Raspberry pi 4, el protoboard y el sensor HC-SRO4.
![image](https://user-images.githubusercontent.com/72757419/192899998-d550ded6-f15b-4d68-85ef-00650463a791.png)

## Esquema físico
![image](https://user-images.githubusercontent.com/72757419/192899706-f1e2d92e-3890-45ca-a3f5-b25faf223482.png)

![image](https://user-images.githubusercontent.com/72757419/192899751-7a2320f1-b625-4c4b-92ff-7cc3c0fe468d.png)

## Datos de salida
Salida en consola del script de python mostrando la salida de datos
![imagen](https://user-images.githubusercontent.com/72757419/192619774-3a65889a-dc3c-40dc-998f-34e2ab7be106.png)

