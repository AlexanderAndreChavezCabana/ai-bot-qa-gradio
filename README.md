# QA Bot using WatsonX AI

Un chatbot de preguntas y respuestas construido con IBM WatsonX AI, LangChain y Gradio. Este proyecto implementa un sistema RAG (Retrieval-Augmented Generation) que permite hacer preguntas sobre documentos PDF.

## Descripción

Este proyecto implementa un asistente de IA conversacional que puede:
- Procesar documentos PDF
- Responder preguntas basadas en el contenido de los documentos
- Utilizar modelos de lenguaje avanzados de IBM WatsonX AI
- Proporcionar una interfaz web amigable con Gradio

## Requisitos

- Python 3.11 o superior
- Conexión a Internet (para acceder a IBM WatsonX AI)

## Librerías Requeridas

- **gradio** (4.44.0) - Para crear la interfaz web
- **ibm-watsonx-ai** (1.1.2) - Acceso a los modelos de IBM WatsonX
- **langchain** (0.2.11) - Framework para orquestar modelos de IA
- **langchain-community** (0.2.10) - Integraciones comunitarias de LangChain
- **langchain-ibm** (0.1.11) - Integración específica con IBM WatsonX
- **chromadb** (0.4.24) - Base de datos vectorial para almacenar embeddings
- **pypdf** (4.3.1) - Para cargar y procesar documentos PDF
- **pydantic** (2.9.1) - Validación de datos

## Instalación

1. **Actualizar el sistema** (si es necesario):
```bash
sudo apt-get update -y
sudo apt-get install python3.11
python3.11 -m ensurepip
python3.11 -m pip install --upgrade pip
```

2. **Instalar las dependencias**:
```bash
python3.11 -m pip install \
    gradio==4.44.0 \
    ibm-watsonx-ai==1.1.2 \
    langchain==0.2.11 \
    langchain-community==0.2.10 \
    langchain-ibm==0.1.11 \
    chromadb==0.4.24 \
    pypdf==4.3.1 \
    pydantic==2.9.1
```

## Estructura del Proyecto

El notebook `Chatbot_qa_ibm.ipynb` contiene:

1. **Inicialización del Entorno** - Instalación de dependencias
2. **Importación de Librerías** - Imports necesarios de Gradio, IBM WatsonX, LangChain
3. **Configuración del Modelo LLM** - Inicialización de WatsonxLLM con Mixtral 8x7B
4. **Cargador de PDF** - Integración con PyPDFLoader
5. **Vector Store** - Almacenamiento de embeddings con ChromaDB
6. **Cadena de Recuperación** - RetrievalQA para responder preguntas
7. **Interfaz Gradio** - Interfaz web interactiva

## Componentes Principales

### Modelo LLM
- **Modelo Base**: Mixtral 8x7B (mistralai/mixtral-8x7b-instruct-v01)
- **Temperatura**: 0.5
- **Max Tokens**: 256
- **Plataforma**: IBM WatsonX AI

### Procesamiento de Documentos
- Carga de archivos PDF
- División de texto en chunks
- Generación de embeddings
- Almacenamiento en base de datos vectorial

### Interfaz de Usuario
- Interfaz web con Gradio
- Entrada de texto para preguntas
- Respuestas generadas en tiempo real

## Configuración de Credenciales

Para usar IBM WatsonX AI, necesitarás configurar tus credenciales. Consulta la [documentación oficial de IBM WatsonX](https://www.ibm.com/products/watsonx-ai) para obtener tu API key y project ID.

## Uso

1. Abre el notebook `Chatbot_qa_ibm.ipynb` en Jupyter
2. Ejecuta las celdas en orden
3. Proporciona tus credenciales de IBM WatsonX
4. Carga un documento PDF
5. Formula preguntas sobre el contenido del documento

## Características

✅ RAG (Retrieval-Augmented Generation)  
✅ Modelos LLM avanzados de IBM WatsonX  
✅ Procesamiento de documentos PDF  
✅ Interfaz web interactiva  
✅ Búsqueda semántica con vectores  
✅ Respuestas contextuales  

## Notas

- El proyecto suprime advertencias automáticamente para mantener la salida limpia
- Los modelos se configuran con parámetros optimizados para balance entre calidad y velocidad
- La interfaz Gradio se lanza en modo compartido para acceso remoto

## Autor

Proyecto del curso IBM Coursera - RAG (Retrieval-Augmented Generation)

## Licencia

MIT
