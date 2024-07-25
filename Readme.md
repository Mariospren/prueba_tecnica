# Prueba Técnica para Operador de Inteligencia Artificial

Antes de empezar, me gustaría agradecer a Onestic por la oportundiad de esta prueba técnica. He podido aprender muchísimo, pues francamente esta semana por mi parte ha sido más estudiar que trabajar en sí. Conocí mucho más sobre los LLM, llegué a probar al menos otros tres más (como Llava,  de ollama) e incluso llegué a frustrarme un poco porque sentía que no estaba avanzando. Con todo, he hecho lo mejor que he podido en el tiempo estalecido.
Siento que he podido crecer un poco más profesionalmente, y estoy seguro de que teniendo la base que acabo de ganar, podría profundizar muchísimo más en este campo y hacer mejores cosas en menos tiempo. Gracias, de verdad

## Resumen

Este documento muestra cómo automatizar el enriquecimiento de información utilizando IA generativa, apoyándose en un LLM como Gemini. El notebook contiene varios scripts y uso de librerías que facilitan el uso y acceso a algoritmos, así como la comunicación con APIs. Cada paso está documentado para facilitar su implementación y utilización.


## Contenido

1. **Análisis Exploratorio de Datos**
   - Importación de librerías necesarias.
   - Lectura y visualización de archivos CSV.
   - Limpieza y preparación de datos.
   - Fusión de dataframes.

2. **Descarga de Imágenes**
   - Iteración sobre URLs y nombres de archivos.
   - Función para descargar imágenes con encabezados HTTP.
   - Creación de carpetas y aplicación de la función de descarga.

3. **Configuración del LLM**
   - Uso del LLM de Gemini de Google.
   - Autenticación en la API de Gemini.
   - Generación de contenido y descripciones a partir de imágenes.

4. **Generación de Descripciones**
   - Alimentación del modelo con imágenes.
   - Ajuste de prompts para obtener descripciones precisas.
   - Generación de descripciones para todas las imágenes del dataframe.
   - Limpieza de texto generado.

5. **Guardado de Resultados**
   - Agregación de descripciones al dataframe.
   - Guardado del dataframe como archivo CSV.

## Instrucciones de Uso

### Requisitos Previos

1. **Registro en Google Cloud:**
   - Es necesario registrarse en [Google Cloud](https://cloud.google.com/) para obtener una API key de Google.

2. **Archivo `config.py`:**
   - Crear un archivo `config.py` en el mismo directorio que el notebook.
   - Añadir la siguiente línea al archivo `config.py` con tu API key de Google:
     ```python
     Google_api_key = 'TU_API_KEY_AQUÍ'
     ```

### Instalación

1. **Instalar Anaconda:**
   - Descargar e instalar [Anaconda](https://www.anaconda.com/products/distribution).

2. **Crear un Entorno Virtual:**
   - Abrir Anaconda  y crear un entorno virtual:
     ```bash
     conda create -n prueba_tecnica python=3.8
     conda activate prueba_tecnica
     ```

3. **Instalar Librerías Necesarias:**
   - Instalar las librerías necesarias ejecutando el siguiente comando:
     ```bash
     pip install pandas requests pillow google-generativeai textwrap ipython
     ```

### Ejecución del Notebook

1. **Abrir Jupyter Notebook:**
   - En Anaconda, activar el entorno virtual y abrir Jupyter Notebook:
     ```bash
     conda activate prueba_tecnica
     jupyter notebook
     ```

2. **Abrir el Archivo `prueba.ipynb`:**
   - Navegar hasta el directorio donde se encuentra el archivo `prueba.ipynb` y abrirlo.

3. **Ejecutar el Notebook:**
   - Ejecutar cada celda del notebook para seguir el flujo de trabajo y generar las descripciones de los productos.

### Alternativa: Visual Studio Code

1. **Instalar Visual Studio Code:**
   - Descargar e instalar [Visual Studio Code](https://code.visualstudio.com/).

2. **Instalar la Extensión de Jupyter:**
   - Abrir Visual Studio Code y buscar la extensión "Jupyter" en el marketplace de extensiones e instalarla.

3. **Abrir el Notebook en Visual Studio Code:**
   - Abrir el archivo `prueba.ipynb` en Visual Studio Code y ejecutar las celdas.

   ## Fuentes

- [Gemini API Developer Docs and API Reference](https://platform.openai.com/docs/api-reference/introduction)
- [OpenAI API Reference](https://platform.openai.com/docs/api-reference/introduction)
- [LLaVA: Large Language-and-Vision Assistant](https://llava-vl.github.io/)
