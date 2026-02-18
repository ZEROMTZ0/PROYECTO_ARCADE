### SRS
# Sistema Arcade con ESP32
## 1. Introducción
### 1.1 Propósito

El presente documento define los requerimientos funcionales y no funcionales del sistema Arcade basado en ESP32. Este documento servirá como referencia para el desarrollo, validación y pruebas del sistema embebido.

### 1.2 Alcance del Sistema

El sistema Arcade con ESP32 permitirá la interacción del usuario mediante joystick y botones físicos para controlar un videojuego ejecutado en un microcontrolador. El sistema mostrará la interfaz gráfica en una pantalla integrada y responderá en tiempo real a las entradas del usuario.

### 1.3 Definiciones

ESP32: Microcontrolador principal del sistema.

Joystick: Dispositivo analógico para control de movimiento.

Botones: Entradas digitales para acciones del juego.

PCB: Placa de circuito impreso diseñada para integrar el hardware.

## 2. Descripción General del Sistema
### 2.1 Perspectiva del Producto

El sistema es un dispositivo autónomo embebido que integra:

Módulo de entrada (Joystick + Botones)

Módulo de procesamiento (ESP32)

Módulo de salida (Pantalla)

Módulo de alimentación

Arquitectura general:

Entradas → Procesamiento (ESP32) → Renderizado en pantalla

### 2.2 Funciones del Sistema

Lectura de entradas digitales y analógicas

Procesamiento de lógica del videojuego

Renderizado gráfico en pantalla

Gestión de energía

Control de estados del juego

## 3. Requerimientos Funcionales
RF-01

El sistema deberá encenderse mediante un botón físico de encendido.

RF-02

El sistema deberá leer las posiciones del joystick mediante entradas analógicas del ESP32.

RF-03

El sistema deberá detectar la presión de botones digitales en tiempo real.

RF-04

El sistema deberá ejecutar la lógica del videojuego según las entradas del usuario.

RF-05

El sistema deberá actualizar la pantalla con una tasa mínima de 20 FPS.

RF-06

El sistema deberá incluir un menú inicial antes de comenzar el juego.

RF-07

El sistema deberá reiniciar la partida cuando el usuario presione el botón de reinicio.

RF-08

El sistema deberá mostrar puntuación en pantalla.

## 4. Requerimientos No Funcionales
RNF-01 (Rendimiento)

El sistema deberá responder a entradas del usuario en un tiempo menor a 100 ms.

RNF-02 (Estabilidad)

El sistema deberá operar sin reinicios inesperados durante al menos 30 minutos continuos.

RNF-03 (Consumo Energético)

El sistema deberá operar con batería durante al menos 1 hora continua.

RNF-04 (Usabilidad)

La interfaz deberá ser intuitiva y clara para el usuario.

RNF-05 (Portabilidad)

El sistema deberá estar contenido en una estructura compacta tipo arcade portátil.

RNF-06 (Mantenibilidad)

El código deberá estar modularizado y documentado.

## 5. Restricciones del Sistema

- El sistema debe utilizar ESP32 como microcontrolador principal.

- El desarrollo deberá realizarse en Arduino IDE o PlatformIO.

- La pantalla deberá ser compatible con el ESP32.

- El sistema debe funcionar con alimentación de 3.3V o 5V según diseño.

## 6. Consideraciones de Seguridad

- No debe existir exposición de cables energizados.

- La batería debe contar con protección contra sobrecarga.

- El sistema debe evitar sobrecalentamiento.

## 7. Criterios de Aceptación

- El sistema será considerado funcional cuando:

- Todos los RF estén implementados.

- Se realicen pruebas exitosas de funcionamiento continuo.

- La pantalla responda correctamente a las entradas.

- El sistema no presente fallas eléctricas ni reinicios inesperados.

## 8. Roles del Equipo
- Ensamblaje: ARMANDO

- Electrónica: Ana, ARMANDO

- Responsable de conexiones: PABLO, ARMANDO

- Responsable de energia: Abraham, Diego Gael

- Diseño PCB: ARMANDO

- Responsable del diseño: Diego Gael

- Programación : ARMANDO

- Documentación: PABLO

- Presupuesto para el proyecto: Pablo