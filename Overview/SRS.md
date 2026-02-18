### SRS
# Sistema Arcade Embebido con ESP32
## 1. Introduction

### 1.1 Purpose

El propósito de este documento es establecer formalmente los requerimientos del Sistema Arcade Embebido basado en ESP32

Este documento define los requerimientos funcionales, no funcionales, de interfaz, de tiempo real y de seguridad necesarios para el diseño, implementación, integración y validación del sistema

Sirve como referencia técnica para el equipo de desarrollo y como base para futuras actividades de prueba y mantenimiento

### 1.2 Scope

El sistema consiste en una consola arcade embebida desarrollada sobre un microcontrolador ESP32.

El problema que se busca resolver es la implementación de una plataforma interactiva capaz de ejecutar videojuegos simples utilizando recursos limitados de hardware, garantizando respuesta en tiempo real y estabilidad operativa

El sistema permitirá:

- Detectar entradas físicas mediante botones y joystick

- Procesar dichas entradas en tiempo real

- Renderizar gráficos en una pantalla integrada

- Ejecutar al menos un videojuego funcional

- Operar de manera independiente sin conexión a sistemas externos

### 1.3 Definitions, Acronyms, and Abbreviations

- ESP32 – Microcontrolador 
- GPIO – General Purpose Input/Output 
- SPI – Serial Peripheral Interface
- I2C – Inter-Integrated Circuit
- UART – Universal Asynchronous Receiver-Transmitter
- SRS – Software Requirements Specification
- FR – Functional Requirement (Requerimiento Funcional)
- NFR – Non-Functional Requirement (Requerimiento No Funcional)
- RTOS – Real-Time Operating System

### 1.4 References

- Hoja de datos oficial del ESP32

- Plantilla del Proyecto de Sistemas Embebidos – GitHub

- Documentación del framework Arduino / ESP-IDF

- Datasheet del módulo de pantalla utilizado TFT

- Documentación técnica de los protocolos SPI e I2C

### 1.5 Document Overview

Este documento se organiza de la siguiente manera:

- La Sección 1 presenta el propósito, alcance y referencias del sistema

- La Sección 2 describe la visión general del producto

- La Sección 3 detalla los requerimientos específicos del sistema

- Las Secciones 4 y 5 corresponderán a verificación y trazabilidad
- La Sección 6 detalla los roles de equipo

## 2. Overall Description
### 2.1 Product Perspective

El sistema es un producto independiente que no forma parte de un sistema mayor

Está compuesto por:

- Microcontrolador ESP32

- Pantalla basica 

- Botones de acción

- vJoystick direccional

- Sistema de alimentación

El sistema opera de manera autónoma y no depende de conexión a internet ni servicios externos

### 2.2 Product Functions

Las funciones principales del sistema incluyen:

- Encendido y apagado mediante botón físico

- Detección de múltiples botones de acción

- Detección de dirección del joystick

- Procesamiento en tiempo real de las entradas

- Visualización gráfica en pantalla

- Ejecución de al menos un videojuego (emulado)

### 2.3 User Characteristics

El sistema está dirigido a usuarios generales sin necesidad de conocimientos técnicos avanzados

Características del usuario:

- Familiaridad básica con videojuegos

- Capacidad de interactuar mediante botones y palanca

- No requiere configuración técnica previa

### 2.4 Constraints

El sistema presenta las siguientes restricciones:

- Memoria RAM limitada del ESP32

- Capacidad de procesamiento limitada

- Número limitado de pines GPIO

- Restricciones energéticas

- Restricciones de costo propias de un proyecto académico.

- Tiempo limitado de desarrollo

### 2.5 Assumptions and Dependencies

#### Suposiciones:

- El hardware funcionará correctamente

- La pantalla es compatible con SPI o I2C

- El joystick y botones están correctamente conectados

- El sistema será programado en C/C++

#### Dependencias:

- Librerías del ESP32

- Librerías de control de pantalla

- Framework Arduino o ESP-IDF

- Datasheets oficiales del hardware

## 3. Specific Requirements
### 3.1 Functional Requirements

FR-01: El sistema deberá encender y apagar mediante un botón físico dedicado

FR-02: El sistema deberá detectar correctamente la presión de múltiples botones de acción

FR-03: El sistema deberá detectar las direcciones del joystick (arriba, abajo, izquierda, derecha)

FR-04: El sistema deberá procesar las entradas del usuario con una latencia menor a 100 ms

FR-05: El sistema deberá renderizar gráficos en una pantalla integrada.
FR-06: El sistema deberá ejecutar al menos un videojuego completamente funcional

FR-07: El sistema deberá permitir reiniciar el juego sin reiniciar el hardware

FR-08: El sistema deberá mantener estabilidad durante sesiones prolongadas

FR-09: El sistema deberá iniciar automáticamente el menú principal al encenderse

### 3.2 Non-Functional Requirements

NFR-01: El tiempo máximo de respuesta ante una entrada del usuario no deberá superar 100 ms

NFR-02: El consumo máximo de energía deberá ser compatible con alimentación USB estándar (5V)

NFR-03: El sistema deberá operar de manera estable durante al menos 30 minutos continuos sin fallos

NFR-04: El firmware deberá estar estructurado de manera modular

NFR-05: El código deberá permitir mantenimiento y expansión futura

### 3.3 External Interface Requirements
### 3.3.1 User Interfaces

- Pantalla gráfica TFT

- Botones físicos de acción

- Joystick direccional

- Indicadores LED (si se implementan)

### 3.3.2 Hardware Interfaces

- GPIO digitales para botones

- GPIO analógicos o digitales para joystick

- Comunicación SPI o I2C para pantalla

- Puerto USB para alimentación y programación

- UART para depuración

### 3.3.3 Software Interfaces

- Librerías del ESP32

- Librerías gráficas para pantalla

- Framework Arduino o ESP-IDF

- Herramientas de compilación y carga de firmware

### 3.4 Real-Time Requirements

- El sistema deberá procesar entradas físicas con una latencia máxima de 100 ms

- La actualización gráfica deberá realizarse a una frecuencia suficiente para evitar parpadeo perceptible

- El procesamiento del juego no deberá bloquear la detección de entradas

### 3.5 Safety and Regulatory Requirements

Dado que se trata de un proyecto académico, no se aplican normativas industriales obligatorias

- Sin embargo, se deberán considerar:

- Uso correcto de niveles de voltaje (3.3V)

- Protección básica contra cortocircuitos

- Conexiones seguras y aisladas

- Buenas prácticas de manejo eléctrico

## 4. Verification and Validation

NOT FOR THIS RELEASE

Esta sección se desarrollará en una futura versión del documento e incluirá:

- Casos de prueba para cada FR

- Pruebas de rendimiento

- Validación de latencia

- Pruebas de estabilidad

- Inspección de código y arquitectura

## 5. Requirements Traceability Matrix

NOT FOR THIS RELEASE

En futuras versiones se incluirá una matriz que relacione:

- Cada requerimiento funcional y no funcional

- Su método de verificación

- Su resultado esperado

- Evidencia de cumplimiento

## 6. Roles del Equipo
- Ensamblaje: ARMANDO

- Electrónica: Ana, ARMANDO

- Responsable de conexiones: PABLO, ARMANDO

- Responsable de energia: Abraham, Diego Gael

- Diseño PCB: ARMANDO

- Responsable del diseño: Diego Gael

- Programación : ARMANDO

- Documentación: PABLO

- Presupuesto para el proyecto: Pablo