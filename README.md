# 🔪 Laboratorio No. 4: Cinemática Directa del Phantom X con ROS 2

## 🤖 Robot Manipulador: Phantom X Pincher

## 👥 Integrantes

* Juan Manuel Rojas Luna
* Miguel Ángel Ortiz Mejía
* Dixon Alberto Cuesta Segura

---

## 📌 Introducción

Este laboratorio tiene como propósito aplicar los conceptos de **cinemática directa** en un entorno práctico utilizando el robot Phantom X Pincher. Mediante el uso de **ROS 2**, **Python** y los servomotores **Dynamixel AX-12**, se busca comprender cómo los modelos matemáticos se relacionan con el movimiento físico del robot.

Se desarrolló una interfaz gráfica (HMI) con Python para enviar poses predefinidas al robot, visualizar en tiempo real la posición de cada articulación y validar los resultados con los cálculos de la matriz de transformación homogénea (MTH) obtenida con el modelo DH modificado.

---

## ❓ Planteamiento del Problema

Se busca:

* Medir físicamente el robot para extraer sus parámetros geométricos.
* Implementar los Joint Controllers en ROS 2.
* Controlar secuencialmente cada articulación.
* Validar el modelo matemático con el comportamiento real del robot.

---

## 🎯 Objetivos del Laboratorio

* ✅ Crear controladores articulares con ROS 2 para los motores Dynamixel AX-12.
* ✅ Manipular tópicos y servicios para cada articulación.
* ✅ Conectar el robot Phantom X Pincher con Python usando ROS 2.
* ✅ Crear una interfaz gráfica (GUI) funcional.
* ✅ Graficar la configuración en el toolbox y comparar con el robot físico.

---

## 🛠️ Requisitos

* Ubuntu 22.04 LTS
* ROS 2 Humble + `colcon build`
* [Dynamixel Workbench](https://github.com/labsir-un/ROB_Intro_ROS2_Humble_Phantom_Pincher_X100.git)
* Python 3
* Paquete Phantom X Pincher
* Phantom X con base de madera

---

## 🖐️ Cinemática Directa del Phantom X

Se utilizó el modelo **Denavit-Hartenberg modificado (DHmod)** para definir los parámetros cinemáticos del manipulador.

![Marcos de referencia robot](img/marcos.jpg)

### 🖼️ Parámetros DH Modificado

| $i$ | $a_{i-1}$ | $\alpha_{i-1}$ | $d_i$ | $\theta_i$ |
|---|---|---|---|---|
| 1 | 0 | 0 | $l_1$ | $q_1^*$ |
| 2 | 0 | $-\pi/2$ | 0 | $q_2^* - \pi/2$ |
| 3 | $l_2$ | 0 | 0 | $q_3^*$ |
| 4 | $l_3$ | 0 | 0 | $q_4^* - \pi/2$ |
| 5 | 0 | $-\pi/2$ | 0 | $q_5^*$ |
| 6 | 0 | 0 | $l_4$ | $\pi/2$ |

### longitud de los eslabones

* $l_1 = 42$ mm
* $l_2 = 104$ mm
* $l_3 = 104$ mm
* $l_4 = 65$ mm

Total: $315$ mm
---

### 🖼️ Matriz de Transformación Homogénea Final

Para simplificar la legibilidad de la matriz de transformación, definimos los siguientes términos comunes:

![Imagen de terminos](img/terminos.jpg)

Utilizando estas definiciones, la matriz de transformación es:

![Imagen de la Matriz](img/mth.jpg)

## 💻 Modelo Cinematica Directa en MATLAB
![Cinematica Directa](img/CinematicaDirecta.jpg)
---

## 💻 Implementación en Python y ROS 2

El script `control_servo.py` implementa una interfaz gráfica para enviar configuraciones articulares al robot, leer el estado actual y visualizarlo en tiempo real.

### ⚙️ Funcionalidades de la GUI

* Conexión vía puerto serial al motor.
* Ejecución secuencial de las poses.
* Carga de imágenes de cada configuración.
* Lectura y visualización de ángulos actuales.
* Conversión entre grados y valores Dynamixel.

### 📦 Poses predefinidas utilizadas

| Configuración | q1  | q2  | q3  | q4  | q5 |
| ------------- | --- | --- | --- | --- | -- |
| Home          | 0   | 0   | 0   | 0   | 0  |
| Config 1      | 25  | 25  | 20  | -20 | 0  |
| Config 2      | -35 | 35  | -30 | 30  | 0  |
| Config 3      | 85  | -20 | 55  | 25  | 0  |
| Config 4      | 80  | -35 | 55  | -45 | 0  |

---

## Configuración Home

<img src="img/hoome.jpg" alt="Configuración Home" width="60%">

## Configuración 1

<img src="img/Posicion1.jpg" alt="Configuración 1" width="60%">

## Configuración 2

<img src="img/Posicion2.jpg" alt="Configuración 2" width="60%">

## Configuración 3

<img src="img/Posicion3.jpg" alt="Configuración 3" width="60%">

## Configuración 4

<img src="img/posicion4.jpg" alt="Configuración 4" width="60%">

## 🖥️ Interfaz Gráfica (HMI)

![GUI](img/gui.jpg)
> La interfaz permite seleccionar poses, observar valores actuales de las articulaciones, y ver las imágenes asociadas a cada configuración.

---

## 📄 Instrucciones de Uso

### 1. Ejecutar la GUI

```bash
python3 control_servo.py
```

### 2. Configuración previa

* Conectar el robot vía USB.
* Verificar que el puerto sea correcto (`/dev/ttyUSB0`).
* Tener los motores conectados y alimentados.

---
## Videos.

Se adjunta el video correspondiente del brazo alcanzando cada posición solicitada y simultaneamente la demostracipón de uso de la interfaz de usuario.

[Video](https://youtu.be/Ski5qsBnYsE)

---
## 📚 Conclusiones

El desarrollo del presente laboratorio permitió implementar una interfaz gráfica funcional en Python para el control del robot Phantom X Pincher utilizando ROS 2. Se alcanzó un control secuencial de las articulaciones, visualización en tiempo real de los valores articulares y ejecución confiable de múltiples poses predefinidas.

Este enfoque práctico facilitó la comprensión de los conceptos de comunicación con servomotores, el manejo de tópicos y servicios en ROS 2, así como el diseño de interfaces de usuario para robots reales. En conjunto, el laboratorio fortaleció la capacidad para desarrollar soluciones completas que integran software, hardware y control en tiempo real.

---

## 📌 Anexos

* Diagrama de flujo en Mermaid:

```mermaid
graph TD
    Start --> Conectar[Conectar a Dynamixel]
    Conectar --> MostrarGUI[Mostrar GUI]
    MostrarGUI --> SelecciónPose[Seleccionar pose]
    SelecciónPose --> EnviarÁngulos[Enviar valores Dynamixel]
    EnviarÁngulos --> MovimientoSecuencial[Movimiento secuencial]
    MovimientoSecuencial --> LecturaEstados[Leer estado final]
    LecturaEstados --> End
```

* Archivos relevantes:

  * `control_servo.py`
  * Imagen de la tabla DH
  * Imagen MTH final
  * Fotos de cada configuración del robot

* Proyecto Completo:

Encontrarás el archivo .zip del proyecto completo en esta dirección: [Phantom Proyect](https://drive.google.com/file/d/1rNUlMyVqoanhyzUjluZ1DpTWe5xKenj-/view?usp=sharing)
---

## 🧠 Recomendaciones

* Validar siempre los límites articulares antes de ejecutar una pose.
* Evitar obstáculos físicos en el workspace.
* Grabar cada pose para comparar contra el modelo gráfico.

---

## 📌 Referencias

* Craig, J. J. (2005). *Introduction to Robotics: Mechanics and Control.*
* [Documentación Dynamixel + ROS](https://emanual.robotis.com/docs/en/software/dynamixel/dynamixel_workbench/#ros-tutorials)
* Laboratorio Robótica Industrial – 2025-I


