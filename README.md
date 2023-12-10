Instructivo Detallado para Ejecutar el Código
Paso 1: Descarga del Código Fuente
Descarga el Código:

Asegúrate de tener el código fuente descargado en tu máquina local. Puede estar en un archivo comprimido (zip) o en una carpeta.
Descomprime el Archivo:

Si descargaste un archivo comprimido, descomprímelo en una ubicación de tu elección. Esto te dará acceso a los archivos del proyecto.
Paso 2: Instalación de Dependencias
Abre una Terminal o Símbolo del Sistema:

Para hacer esto, puedes buscar "Símbolo del sistema" o "Terminal" en el menú de inicio (en Windows) o utilizar el terminal de tu sistema operativo.
Navega al Directorio del Proyecto:

Usa el comando cd para cambiar al directorio donde descomprimiste el código fuente. Por ejemplo:
bash
Copy code
cd ruta/del/proyecto
Instala las Dependencias con PIP:

Ejecuta los siguientes comandos para instalar Flask y descargar el modelo de lenguaje de Spacy en español:
bash
Copy code
pip install Flask spacy
python -m spacy download es_core_news_md
Paso 3: Ejecución de la Aplicación Flask
Navega al Directorio del Proyecto (si no lo has hecho aún):

bash
Copy code
cd ruta/del/proyecto
Ejecuta la Aplicación Flask:

Utiliza el siguiente comando para iniciar la aplicación Flask:
bash
Copy code
python app.py
Verás mensajes en la terminal indicando que el servidor Flask ha iniciado.
Paso 4: Enviar una Pregunta a la API
Abre una Nueva Terminal o Usa Herramientas como cURL:

Abre otra terminal o usa herramientas como cURL para enviar una solicitud POST a la API de la aplicación Flask.
bash
Copy code
curl -X POST -H "Content-Type: application/json" -d '{"pregunta": "¿Dónde puedo consultar mi kardex?"}' http://127.0.0.1:5000/pregunta
Si estás en Windows y no tienes cURL instalado, considera usar Postman o PowerShell.
Observa la Respuesta en la Terminal de la Aplicación Flask:

En la terminal donde ejecutaste app.py, deberías ver la respuesta generada por la aplicación.
Personalización de Preguntas y Respuestas
Abre el Archivo pregunta_responder_lib.py:

Utiliza un editor de código para abrir el archivo pregunta_responder_lib.py. Puedes usar Visual Studio Code, Atom, o cualquier editor de tu elección.
Personaliza Preguntas y Respuestas:

En el archivo pregunta_responder_lib.py, encuentra el diccionario respuestas y personaliza las preguntas y respuestas según tus necesidades.
Guarda los Cambios y Vuelve a Ejecutar la Aplicación:

Guarda los cambios en pregunta_responder_lib.py.
Vuelve a ejecutar la aplicación Flask utilizando el comando python app.py.
