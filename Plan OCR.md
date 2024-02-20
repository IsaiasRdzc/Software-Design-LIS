# Extracción de datos para documentos mexicanos


## Requerimientos funcionales

- **RF1. Procesamiento de Imágenes:**

Importar imágenes de documentos en diferentes formatos (JPG, PNG, PDF, etc.).
Preprocesamiento de imágenes para mejorar la calidad y facilitar el reconocimiento de caracteres.

- **RF2. Identificación de formas:** 
    - El sistema debe ser capaz de reconocer una variedad de documentos oficiales, como pasaporte, INE, diferentes comprobantes de domicilio, CURP, acta de nacimiento, etc.
    - Deber tener la capacidad de diferenciar cada tipo de documento oficial.

- **RF4. Extracción de información:**
    - El sistema debe ser capaz de extraer información específica de cada tipo de documento
    - La información debe ser precisa y completa


## Requerimientos no funcionales

### Restricciones:

- **RNF1. Precisión:**
   - El sistema puede carecer de precición al momento del escaneo e identificación de la forma, es decir, puede no reconocer algún documento que tenga una baja calidad
   - El sistema puede dar salidas errones, esto debido a un mal reconocimiento de caracteres.

- **RNF2. Privacidad y Seguridad:**
   - Garantizar la privacidad y seguridad de los datos sensibles extraídos de los documentos oficiales.


### Atributos de Calidad:

- **RNF3. Exactitud:**
   - La información extraída debe ser precisa y estar libre de errores para evitar problemas legales o administrativos.

- **RNF4. Escalabilidad:**
   - El sistema debe ser capaz de manejar grandes volúmenes de documentos y estar preparado para futuras expansiones.

- **RNF5. Robustez:**
   - Capacidad para manejar diferentes tipos de documentos, independientemente de su calidad de imagen o formato.

- **RNF6. Mantenibilidad:**
   - Diseño modular y código bien estructurado que facilite la incorporación de nuevas funcionalidades y la corrección de errores.

## Plan de desarrollo

### Tecnologías y Herramientas:
- Lenguaje de Programación:
Para este proyecto podemos optar por usar Python debido a su amplia variedad de bibliotecas de visión por computadora y procesamiento de imágenes, como OpenCV y Tesseract OCR, que son fundamentales para el desarrollo del sistema.

- Bibliotecas de Procesamiento de Imágenes:
Después de una investigación, se encontraron algunas bibliotecas relacionadas al proyecto como OpenCV para el preprocesamiento de imágenes, que incluye operaciones como el ajuste de contraste, binarización y eliminación de ruido para mejorar la calidad de las imágenes antes del reconocimiento de caracteres.

- Reconocimiento de Caracteres (OCR):
Tesseract OCR es la mejor opción el reconocimiento óptico de caracteres. Permite la extracción de texto apartir de imágenes.

### Estructura básica del sistema

- Ya con esto, podemos hacernos una temprana idea de como puede estar compuesto el sistema, que incluye dos procesos principales, el procesamiento de imágenes (reconocimiento de formas, ajuste y mejora de cada documento para la extracción de la información), y el OCR.

[![imagen-2024-02-19-234049861.png](https://i.postimg.cc/G3Bf5SJB/imagen-2024-02-19-234049861.png)](https://postimg.cc/V584Sgh1)