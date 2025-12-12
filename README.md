# 🛠️ Herramienta de Transferencia para Módulo Lorenzo (vía RP2040)

Este repositorio aloja el ecosistema completo de software y firmware diseñado para transferir archivos de código ensamblador desde un PC hacia un **Módulo Lorenzo**, utilizando una **Raspberry Pi Pico (RP2040)** como interfaz de comunicación.

## 📋 Contenido del Repositorio

El proyecto se divide en 4 componentes principales, disponibles en los siguientes archivos comprimidos y de texto:

| Archivo | Tipo | Descripción |
| :--- | :--- | :--- |
| **`version1.1.rar`** | 🖥️ Ejecutable | Aplicación de escritorio lista para usar. Permite al usuario seleccionar el archivo ensamblador y enviarlo. |
| **`pythonproject2.rar`** | 🐍 Código Fuente (PC) | Proyecto completo en Python. Descarga este archivo si deseas optimizar el software de PC o agregar nuevas funciones. |
| **`transESPaLorenzo.rar`** | 🍓 Firmware (RP2040) | Código necesario para la Raspberry Pi Pico (RP2040). Se encarga de recibir los datos del PC y enviarlos al módulo. |
| **`instrucciones_drivers.txt`** | 📄 Documentación | Guía paso a paso para instalar los drivers necesarios para que el computador reconozca la RP2040. |

---

## 🚀 Guía de Inicio Rápido (Para Usuarios)

Si solo deseas utilizar la herramienta para transferir archivos, sigue estos pasos:

### 1. Configuración de Hardware

1. Conecta tu **Raspberry Pi Pico (RP2040)** al computador mediante USB.
2. Abre el archivo `instrucciones_drivers.txt` y sigue los pasos para asegurar que tu PC reconoce la placa correctamente.
3. Descomprime `transESPaLorenzo.rar` y carga el código en tu RP2040 (usando Thonny u otro IDE compatible).

### 2. Ejecución del Software
1. Descarga y descomprime el archivo `version1.1.rar`.
2. Ejecuta el archivo principal (generalmente `.exe` o script de arranque).
3. Selecciona tu archivo de código ensamblador y presiona el botón de transferencia.

---

## 💻 Guía para Desarrolladores

Si deseas contribuir al código, mejorar la interfaz o realizar optimizaciones, esta sección es para ti.

### Requisitos Previos
* Python 3.x instalado.
* Librerías necesarias (verificar si hay un `requirements.txt` dentro del rar, de lo contrario instalar las dependencias estándar de comunicación serial).
* IDE recomendado: VS Code o PyCharm.

### Cómo trabajar con el código fuente
1. Descomprime `pythonproject2.rar`.
2. Abre el proyecto en tu editor de código.
3. Realiza tus mejoras (ej. optimización de velocidad de transferencia, validación de sintaxis ensamblador, UI).
4. Para generar un nuevo ejecutable, se recomienda usar herramientas como `PyInstaller`.

---

## 🔧 Arquitectura del Sistema

El flujo de datos funciona de la siguiente manera:

1.  **PC (Python):** Lee el archivo `.asm` y lo envía por puerto Serial (COM).
2.  **RP2040:** Recibe los paquetes de datos, los procesa y los reenvía a través de sus pines GPIO.
3.  **Módulo Lorenzo:** Recibe las instrucciones finales para su ejecución.

---

## 🤝 Contribuciones

Las contribuciones son bienvenidas. Por favor, asegúrate de probar el código tanto en la parte de Python como en la integración con la RP2040 antes de hacer un *commit*.

## 📄 Licencia

Este proyecto es de uso libre para fines educativos y de desarrollo.
