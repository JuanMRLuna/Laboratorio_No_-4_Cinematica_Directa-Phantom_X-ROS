# Laboratorio No. 4 Cinemática Directa Phantom X ROS

# Integrantes:

* Juan Manuel Rojas Luna
* Miguel Ángel Ortiz Mejía
* Dixon Alberto Cuesta Segura

## Introducción.

Este laboratorio tiene como propósito principal aplicar conceptos de cinemática directa en un entorno práctico mediante el uso del manipulador Phantom X Pincher. Se integran herramientas de software como ROS 2 y Python para controlar los servomotores Dynamixel AX-12 del robot, permitiendo comprender la relación entre los modelos matemáticos de la cinemática y su implementación real en hardware. Durante el desarrollo del laboratorio, se manipularán tópicos y servicios de ROS para lograr el control secuencial de las articulaciones del manipulador, así como también se realizarán mediciones físicas para establecer correctamente los parámetros de Denavit-Hartenberg (DH) del robot.

## Planteamiento del Problema.

Se requiere modelar y controlar con precisión la cinemática directa del robot Phantom X Pincher. Para ello, es necesario identificar sus parámetros geométricos mediante mediciones físicas, implementar los controladores articulares en ROS 2, y validar los movimientos del robot físico frente al modelo teórico, asegurando coherencia entre ambos. El reto está en lograr una integración efectiva entre hardware, ROS y Python para ejecutar poses específicas de forma controlada y secuencial.

## Objetivos.

* Crear todos los Joint Controllers con ROS para manipular los servomotores Dynamixel AX-12 del robot Phantom X Pincher.

* Manipular los tópicos de estado y comando para todos los Joint Controllers del robot Phantom X Pincher.

* Manipular los servicios para todos los Joint Controllers del robot Phantom X Pincher.

* Conectar el robot Phantom X Pincher con Python usando ROS 2.

## **Para la práctica**

* Ubuntu versión 22.xx preferible 22.04 LTS con ROS.
  
* Espacio de trabajo para colcon build correctamente configurado.

* Paquetes de Dynamixel Workbench. https://github.com/labsir-un/ROB_Intro_ROS2_Humble_Phantom_Pincher_X100.git.
  
* Paquete del robot Phantom X.

* Python.

* Un (1) manipulador Phantom X Pincher con su base en madera.

