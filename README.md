# Descripción del Código de Códigos de Cadena

Este programa implementa varios algoritmos para generar códigos de cadena a partir de imágenes binarias, que son útiles para representar la forma de objetos en procesamiento de imágenes.

## Funcionalidades principales

El programa ofrece cinco métodos diferentes para generar códigos de cadena:

1. **F8**: Código de cadena en 8 direcciones (Freeman)
2. **F4**: Código de cadena en 4 direcciones (Freeman)
3. **VCC**: Vertex Chain Code (Código de Cadena de Vértices)
4. **3OT**: Three Orthogonal (Tres Ortogonal)
5. **AF8**: Código de cadena en 8 direcciones absoluto

## Estructura del código

### Funciones principales

1. **F8(imgArit)**:
   - Implementa el código de cadena en 8 direcciones
   - Sigue el contorno del objeto en la imagen binaria
   - Asigna valores del 0 al 7 para cada dirección de movimiento

2. **F4(imgArit)**:
   - Implementa el código de cadena en 4 direcciones
   - Similar a F8 pero con solo 4 direcciones posibles
   - Maneja casos especiales para transiciones entre direcciones

3. **VCC(vec)**:
   - Transforma un código de cadena F4 en Vertex Chain Code
   - Usa una matriz de identificación para determinar los cambios de dirección

4. **F3OT(vec)**:
   - Implementa el código Three Orthogonal basado en F4
   - Utiliza una matriz de identificación diferente a VCC

5. **AF8(imgArit)**:
   - Versión absoluta del código F8
   - Incluye función `direCe()` para manejar direcciones absolutas

### Flujo del programa

1. Carga una imagen binaria de un conjunto predefinido
2. Convierte la imagen a una matriz binaria (1 para objeto, 0 para fondo)
3. Solicita al usuario seleccionar el tipo de código de cadena
4. Genera el código correspondiente
5. Guarda el resultado en un archivo de texto con:
   - El código de cadena (dividido en líneas de 100 caracteres)
   - La longitud total del código

## Uso

1. Ejecutar el programa
2. Seleccionar una imagen (0-9)
3. Elegir el tipo de código de cadena (1-5)
4. El programa generará un archivo .txt con los resultados

## Requisitos

- Python 3.x
- Bibliotecas:
  - OpenCV (`cv2`)
  - NumPy (`numpy`)
  - Pathlib (`pathlib`)
