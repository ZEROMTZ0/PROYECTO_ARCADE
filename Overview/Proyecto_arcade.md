# Sistema Arcade con ESP32
## 1. Descripción del Proyecto

El presente proyecto consiste en el diseño, integración y validación de un sistema arcade basado en un microcontrolador ESP32, el cual permitirá la ejecución de un videojuego interactivo controlado mediante botones físicos y joystick.

El sistema estará compuesto por un módulo principal basado en ESP32, encargado de procesar las entradas del usuario (botones y joystick), ejecutar la lógica del juego y mostrar la información en una pantalla integrada.

El arcade incluirá los siguientes componentes principales:

- Microcontrolador ESP32

- antalla (OLED, TFT o similar)

- Joystick analógico

- Botones de acción

- Botón de encendido/apagado

- Sistema de alimentación (batería o fuente externa)

- PCB diseñada para integrar los componentes

El objetivo del proyecto no es fabricar cada componente desde cero, sino integrar hardware comercial disponible con programación embebida para desarrollar un sistema arcade funcional, optimizando tiempos de desarrollo y complejidad técnica.

# 2. Objetivo del Proyecto
## 2.1 Objetivo General

Desarrollar un sistema arcade funcional basado en ESP32 que permita la interacción del usuario mediante botones y joystick, implementando la lógica de un videojuego en un sistema embebido.

### 2.2 Objetivos Específicos

- Diseñar la arquitectura del sistema embebido.

- Integrar el ESP32 con pantalla, joystick y botones.

- Programar la lógica del videojuego.

- Implementar lectura de entradas digitales y analógicas.

- Diseñar una PCB para organizar el hardware del sistema.

- Validar el funcionamiento estable del sistema.

- Documentar el proyecto conforme a estándares académicos.

# 3. Factibilidad del Proyecto
## 3.1 Factibilidad Técnica

El proyecto es técnicamente viable debido a que:

- El ESP32 cuenta con suficiente capacidad de procesamiento.

- Existen librerías disponibles para manejo de pantallas y entradas.

- El hardware necesario es de fácil adquisición.

- El sistema no requiere procesamiento intensivo ni hardware especializado.

- El entorno de desarrollo (Arduino IDE / PlatformIO) es accesible.

## 3.2 Factibilidad Económica

El costo del proyecto es reducido debido a que:

- Se utilizan componentes electrónicos comerciales.

- No se requiere fabricación compleja.

La PCB puede diseñarse en una sola tarjeta.

- El ESP32 es un microcontrolador económico y versátil.

## 3.3 Factibilidad Operativa

El sistema puede ser operado por cualquier usuario final de manera intuitiva, utilizando botones físicos y joystick como interfaz principal.

El sistema será documentado para facilitar su ensamblaje, programación y pruebas.

## 3.4 Riesgos Identificados

- Errores en la lectura de entradas analógicas.

- Problemas de compatibilidad con la pantalla.

- Fallos en el diseño de la PCB.

- Consumo energético elevado.

- Errores en la lógica del videojuego.

Se realizarán pruebas progresivas para mitigar riesgos antes de la integración final.


## 4. Arquitectura / SRS del Sistema

La arquitectura detallada del sistema y los requerimientos funcionales y no funcionales se encuentran documentados en la sección correspondiente del repositorio del proyecto.

En dicha sección se describen:

- Arquitectura general del sistema (Entradas → Procesamiento → Salida)

- Requerimientos funcionales

- Requerimientos no funcionales

- Restricciones técnicas

- Diagramas de bloques

- Consideraciones energéticas

- Diseño preliminar de la PCB


# --> [SRS](https://github.com/ZEROMTZ0/PROYECTO_ARCADE/blob/main/Overview/SRS.md)