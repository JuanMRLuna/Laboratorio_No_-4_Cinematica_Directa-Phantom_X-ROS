# 🧪 Laboratorio No. 4: Cinemática Directa del Phantom X con ROS 2

## 🤖 Robot Manipulador: Phantom X Pincher

## 👥 Integrantes:
- Juan Manuel Rojas Luna  
- Miguel Ángel Ortiz Mejía  
- Dixon Alberto Cuesta Segura  

---

## 📌 Introducción

Este laboratorio tiene como propósito principal aplicar los conceptos de cinemática directa en un entorno práctico, utilizando el manipulador Phantom X Pincher. A través de herramientas como **ROS 2** y **Python**, se logra el control de los servomotores **Dynamixel AX-12**, permitiendo explorar la relación entre modelos matemáticos y el comportamiento físico del robot.

Durante el desarrollo, se trabajará con **tópicos y servicios de ROS 2** para lograr un control secuencial sobre cada articulación del manipulador, además de realizar mediciones físicas necesarias para determinar correctamente los **parámetros Denavit-Hartenberg (DH)** del sistema.

---

## ❓ Planteamiento del Problema

Se busca modelar y controlar con precisión la cinemática directa del robot Phantom X Pincher. Para ello, se deben:

- Identificar los parámetros geométricos del robot mediante medición física.
- Implementar controladores articulares a través de ROS 2.
- Validar la correspondencia entre el modelo teórico (cinemático) y los movimientos reales del manipulador.

El desafío principal es lograr una integración efectiva entre **hardware**, **ROS 2** y **Python**, asegurando que el robot pueda ejecutar poses específicas de forma coherente y secuencial.

---

## 🎯 Objetivos

- ✅ Crear controladores articulares (Joint Controllers) con ROS 2 para los motores Dynamixel AX-12.
- ✅ Manipular tópicos de estado y comando de cada articulación.
- ✅ Utilizar servicios disponibles en los paquetes de ROS 2 para operar el manipulador.
- ✅ Controlar el robot desde Python mediante interfaces ROS 2.

---

## 🛠️ Requisitos de la Práctica

- Sistema operativo: **Ubuntu 22.04 LTS** (preferiblemente)
- Espacio de trabajo ROS 2 correctamente configurado (usando `colcon build`)
- Paquetes necesarios:
  - [`Dynamixel Workbench`](https://github.com/labsir-un/ROB_Intro_ROS2_Humble_Phantom_Pincher_X100.git)
  - Paquete del robot Phantom X
- Lenguaje de programación: **Python 3**
- Hardware: **1 manipulador Phantom X Pincher con base de soporte en madera**

---

## 📐 Cinemática Directa

Se utilizó el método **Denavit-Hartenberg modificado (DHmod)** para modelar la cinemática directa del Phantom X. A partir de las mediciones físicas del manipulador, se establecieron los parámetros necesarios y se construyó la **Matriz de Transformación Homogénea (MTH)** final.

### 🖼️ Espacio para imagen: Parámetros DH modificado

> _[Aquí insertar imagen de la tabla de parámetros DHmod con mediciones]_  

---

### 🖼️ Espacio para imagen: MTH final obtenida a mano

> _[Aquí insertar imagen de la MTH final escrita a mano paso a paso]_  

---

## ✅ Resultados y Validación

> _[Aquí se documentarán las pruebas realizadas: ejecución de poses, comparación entre modelo teórico y comportamiento real, problemas encontrados y cómo se resolvieron.]_

---

## Videos.

Se adjunta el video correspondiente del brazo alcanzando cada posición solicitada y simultaneamente la demostracipón de uso de la interfaz de usuario.

[Video](https://youtu.be/Ski5qsBnYsE)

## 📚 Conclusiones

> _[Resumen de aprendizajes obtenidos, análisis de desempeño del sistema y sugerencias para futuras prácticas.]_

---

## 📎 Anexos

> _[Aquí puedes colocar capturas de terminal, diagramas de nodos en ROS 2, enlaces adicionales o cualquier material complementario.]_

---


