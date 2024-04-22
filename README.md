### Sergio Daniel Lopez Vargas

# AREP_Taller7


## Introducción
En un mundo cada vez más interconectado y digitalizado, la capacidad de desarrollar sistemas inteligentes capaces de comprender y responder a consultas complejas es fundamental. En este contexto, el uso de tecnologías como Lang Chain, Pinecone y OpenAI se vuelve crucial para crear soluciones eficientes en el procesamiento del lenguaje natural y la recuperación de información.

En este proyecto, exploramos el potencial de estas tecnologías a través de diversos desafíos orientados a desarrollar sistemas de pregunta-respuesta inteligentes. Utilizando Python como lenguaje de programación principal, nos enfocamos en tres áreas específicas: la interacción con modelos de lenguaje como ChatGPT de OpenAI, la creación de sistemas de recuperación de respuestas utilizando bases de datos vectoriales en memoria y servicios como Pinecone, y la implementación de un sistema de respuesta basado en la comprensión de texto mediante RAG (Answer Generation and Retrieval).

Cada desafío representa un paso hacia la creación de sistemas inteligentes capaces de comprender preguntas complejas y proporcionar respuestas precisas y relevantes. A lo largo de este informe, describiremos detalladamente las técnicas utilizadas, los resultados obtenidos y las lecciones aprendidas en cada etapa del proyecto.

Este trabajo no solo tiene como objetivo desarrollar soluciones técnicas, sino también fomentar la comprensión y el uso eficiente de estas tecnologías en aplicaciones del mundo real. Con ello, buscamos contribuir al avance en el campo del procesamiento del lenguaje natural y la inteligencia artificial aplicada a la recuperación de información.

## 
### Desafío 1: Uso de Lang Chain y OpenAI para enviar y recibir respuestas de ChatGPT

1. **LLMChain:** Esta clase se utiliza para crear una cadena de procesamiento de lenguaje (LLM) que conecta diferentes etapas del procesamiento de texto. En este caso, se conecta un prompt con el modelo de OpenAI para generar respuestas basadas en las consultas.

2. **OpenAI:** Representa la instancia de la API de OpenAI utilizada para enviar consultas y recibir respuestas del modelo de lenguaje de OpenAI, como ChatGPT en este caso.

3. **PromptTemplate:** Es una plantilla que define cómo se estructuran las consultas que se enviarán al modelo. En este contexto, se utiliza para crear consultas que contienen preguntas específicas.

### Desafío 2: Creación de un RAG utilizando una base de datos vectorial en memoria

1. **WebBaseLoader:** Clase utilizada para cargar documentos desde recursos web, como páginas HTML en este caso. Permite obtener texto de páginas web para su posterior procesamiento.

2. **RecursiveCharacterTextSplitter:** Se utiliza para dividir documentos de texto en fragmentos más pequeños para su procesamiento eficiente. En este caso, se divide el texto de los documentos obtenidos de las páginas web.

3. **Chroma:** Representa la base de datos vectorial en memoria que se utiliza para almacenar los vectores de embeddings de los fragmentos de texto. Permite realizar búsquedas de similitud para recuperar documentos relevantes.

4. **ChatOpenAI:** Es la clase que se utiliza para interactuar con el modelo de lenguaje de OpenAI, como ChatGPT, para generar respuestas basadas en consultas.

### Desafío 3: Creación de un RAG utilizando Pinecone

1. **TextLoader:** Similar a WebBaseLoader pero específico para cargar texto desde archivos locales. En este caso, se utiliza para cargar documentos desde un archivo de texto.

2. **OpenAIEmbeddings:** Clase que proporciona funcionalidad para generar embeddings utilizando el modelo de OpenAI. Se utiliza para convertir el texto en vectores que pueden ser utilizados por Pinecone para búsquedas de similitud.

3. **PineconeVectorStore:** Representa la conexión con la base de datos vectorial en Pinecone. Permite almacenar vectores de embeddings y realizar búsquedas de similitud.

## Instrucciones de Ejecución
* Clone el repositorio desde GitHub:

```
git clone https://github.com/sergiolopezzl/AREP_Taller9.git
```

* Navegue al directorio del proyecto: 

```
cd AREP_Taller9
```

* Entorno virtual: 

```
python -m venv venv
```
```
venv\Scripts\activate
```
* Instalar las dependencias: 

```
pip install -r requirements.txt
```

* Configurar las variables de entorno:

```
os.environ["OPENAI_API_KEY"] = <OpenAI API Key>
```
```
os.environ["PINECONE_API_KEY"] = <Pinecone API Key>
```

* Ejecutar los scripts:

```
python 1.py
```
```
python 3.py
```
```
python 2.py
```

---

### Experimentos y Resultados

#### Desafío 1: Uso de Lang Chain y OpenAI para enviar y recibir respuestas de ChatGPT

**Descripción del Experimento:**
- Se utilizó Python junto con Lang Chain y la API de OpenAI para enviar consultas a ChatGPT y obtener respuestas.

**Instrucciones de Ejecución:**
1. Instalar las dependencias utilizando `pip install -r requirements.txt`.
2. Configurar la clave de la API de OpenAI en el entorno.
3. Ejecutar el script `challenge1.py`.

**Resultado Esperado:**
- Obtención de una respuesta de ChatGPT a partir de la consulta enviada.

---

#### Desafío 2: Creación de un RAG utilizando una base de datos vectorial en memoria

**Descripción del Experimento:**
- Se utilizó Lang Chain para crear un RAG (Retrieve and Generate) utilizando una base de datos vectorial en memoria.

**Instrucciones de Ejecución:**
1. Instalar las dependencias utilizando `pip install -r requirements.txt`.
2. Configurar las claves de API de OpenAI y Pinecone en el entorno.
3. Ejecutar el script `challenge2.py`.

**Resultado Esperado:**
- Generación de una respuesta utilizando el modelo RAG para una pregunta dada.

---

#### Desafío 3: Creación de un RAG utilizando Pinecone

**Descripción del Experimento:**
- Se utilizó Lang Chain junto con Pinecone para crear un RAG (Retrieve and Generate) para responder preguntas utilizando un vectorstore en Pinecone.

**Instrucciones de Ejecución:**
1. Instalar las dependencias utilizando `pip install -r requirements.txt`.
2. Configurar las claves de API de OpenAI y Pinecone en el entorno.
3. Ejecutar el script `challenge3.py`.

**Resultado Esperado:**
- Obtención de una respuesta utilizando el modelo RAG y Pinecone para una pregunta específica.

---

En la sección de "Resultados", puedes incluir capturas de pantalla de las respuestas generadas por los scripts o cualquier otro tipo de salida relevante que demuestre el funcionamiento de cada experimento.

Recuerda también incluir cualquier observación importante, como configuraciones adicionales necesarias o problemas conocidos.

---

### Experimentos y Resultados

#### Desafío 1: Uso de Lang Chain y OpenAI para enviar y recibir respuestas de ChatGPT

**Descripción del Experimento:**
- Se utilizó Python junto con Lang Chain y la API de OpenAI para enviar consultas a ChatGPT y obtener respuestas.

**Instrucciones de Ejecución:**
1. Instalar las dependencias utilizando `pip install -r requirements.txt`.
2. Configurar la clave de la API de OpenAI en el entorno.
3. Ejecutar el script `challenge1.py`.

**Resultado Esperado:**
- Obtención de una respuesta de ChatGPT a partir de la consulta enviada.

---

#### Desafío 2: Creación de un RAG utilizando una base de datos vectorial en memoria

**Descripción del Experimento:**
- Se utilizó Lang Chain para crear un RAG (Retrieve and Generate) utilizando una base de datos vectorial en memoria.

**Instrucciones de Ejecución:**
1. Instalar las dependencias utilizando `pip install -r requirements.txt`.
2. Configurar las claves de API de OpenAI y Pinecone en el entorno.
3. Ejecutar el script `challenge2.py`.

**Resultado Esperado:**
- Generación de una respuesta utilizando el modelo RAG para una pregunta dada.

---

#### Desafío 3: Creación de un RAG utilizando Pinecone

**Descripción del Experimento:**
- Se utilizó Lang Chain junto con Pinecone para crear un RAG (Retrieve and Generate) para responder preguntas utilizando un vectorstore en Pinecone.

**Instrucciones de Ejecución:**
1. Instalar las dependencias utilizando `pip install -r requirements.txt`.
2. Configurar las claves de API de OpenAI y Pinecone en el entorno.
3. Ejecutar el script `challenge3.py`.

**Resultado Esperado:**
- Obtención de una respuesta utilizando el modelo RAG y Pinecone para una pregunta específica.

---

#### Desafío 4 (Opcional): Creación de un RAG para comprensión de código

**Descripción del Experimento:**
- Se utilizó Lang Chain para crear un RAG que pueda comprender código y responder preguntas relacionadas.

**Instrucciones de Ejecución:**
1. Instalar las dependencias utilizando `pip install -r requirements.txt`.
2. Configurar las claves de API de OpenAI en el entorno.
3. Ejecutar el script `challenge4.py` (Opcional).

**Resultado Esperado:**
- Generación de respuestas comprensivas a preguntas sobre código utilizando el modelo RAG.

---

En la sección de "Resultados", puedes incluir capturas de pantalla de las respuestas generadas por los scripts o cualquier otro tipo de salida relevante que demuestre el funcionamiento de cada experimento.

Recuerda también incluir cualquier observación importante, como configuraciones adicionales necesarias o problemas conocidos.

---

¿Te gustaría agregar más detalles o ajustar algo en la descripción de los experimentos y resultados?


# Imagenes
### Login 1
![prueba1.png](src/main/resources/public/img/prueba1.png)
### Login 2
![prueba2.png](src/main/resources/public/img/prueba2.png)
### Login Incorrecto
![prueba3.png](src/main/resources/public/img/prueba3.png)
### Pruebas unitarias
![prueba4.png](src/main/resources/public/img/prueba4.png)







