# Multiple choice corrector & Image processing toolkit

> Procesamiento de Imágenes - TP 1  
> Tecnicatura Universitaria en Inteligencia Artificial (Universidad Nacional de Rosario)  
> Facundo Geuna, Pedro Casado, Máximo Alva  
> 2024

---

## Sobre el proyecto
Este repositorio contiene la resolución del primer trabajo práctico de la materia **Procesamiento de Imágenes**. El proyecto combina técnicas de visión por computadora y manipulación de matrices para resolver dos problemas distintos.

---

## Problemas

### 1. Ecualización local de histogramas
* **Objetivo:** Revelar detalles y objetos ocultos dentro de áreas de baja visibilidad aplicando ecualización local de histogramas.
* **Implementación:** Se desarrolló una función con ventanas deslizantes de tamaño variable (`size`) utilizando bordes espejados (`cv2.BORDER_REPLICATE`)

### 2. Corrector automático de exámenes multiple choice
* **Objetivo:** Automatizar la corrección de exámenes multiple choice y la validación de sus datos de cabecera.
* **Implementación:** 
  * Se diseñaron funciones para la detección de líneas horizontales y verticales que permiten aislar la grilla y las celdas de las preguntas.
  * Se implementó el análisis de componentes conectados (`cv2.connectedComponentsWithStats`) para evaluar los recuadros de respuesta y diferenciar letras manuscritas (A, B, C, D) según sus contornos y áreas.
  * Se automatizó la validación de restricciones en los campos de cabecera (*Name*, *Date*, *Class*) y se generó un reporte gráfico resumen con códigos de color para alumnos aprobados y desaprobados.

---

## Stack tecnológico
* Python
* OpenCV
* NumPy
* Matplotlib

---

## Cómo ejecutarlo
1. Cloná el repositorio.
	```bash
   git clone https://github.com/maximoalva/opencv-multiple-choice-corrector.git
   ```
2. Asegurate de tener instaladas las librerías necesarias:
   ```bash
   pip install opencv-contrib-Python numpy matplotlib
   ```
3. ¡Ahora sí está todo listo para correr el código!
   ```bash
   python main.py
   ```
