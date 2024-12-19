# Despliegue de modelos

## Infraestructura

- **Nombre del modelo:** Identificador de topicos 
- **Plataforma de despliegue:**
   - Piloto: Ngrok
   - Producción: Google Cloud Platform
     
- **Requisitos técnicos:** 
  - Python 3.10.12
  - FastAPI 0.115.6
  - pyngrok 7.2.2
  - mlflow 2.19.0
  - joblib 1.4.2
  - numpy 1.26.4
  - uvicorn 0.34.0
  - sklearn 1.6.0
  - requests 2.32.3
  
- **Requisitos de seguridad:**
  Autenticación a través del SSO de los empleados de la compañia DDV.
   
- **Diagrama de arquitectura:** 
![estructura](https://github.com/ValeriaRaS/Identificacion-de-topicos-G14-/blob/master/docs/deployment/Images/Diagrama_deployment.jpeg)

*¿Cómo funciona?*

Usuario → ngrok → FastAPI Server:

El usuario envía una solicitud, que pasa a través de ngrok y llega al servidor FastAPI.

FastAPI Server → MLFlow:

FastAPI solicita a MLFlow el modelo correspondiente, basándose en los parámetros de la solicitud.

MLFlow → FastAPI Server:

MLFlow responde con el modelo solicitado (o lanza un error si no está disponible).

FastAPI Server → ngrok → Usuario:

FastAPI utiliza el modelo cargado para procesar la entrada del usuario, genera una predicción y la devuelve al usuario a través de ngrok.

## Código de despliegue

- **Archivo principal:** deployment_U6
- **Rutas de acceso a los archivos:**
   - scripts/deployment/deployment_U6.ipynb
   - scripts/deployment/ejemplo_api.ipynb
- **Variables de entorno:**
   - NGROK_AUTHTOKEN
   - MLFLOW_TRACKING_URI: sqlite:///mlruns.db
   - MLFLOW_TRACKING_URI: sqlite:///mlruns.db
   - MLFLOW_ARTIFACT_URI: file:///path/to/artifacts
   - API_PORT: 8000
   - API_HOST: 0.0.0.0
   - DEBUG_MODE=True
   - MODEL_SELECTION_PARAM: todos, altos, bajos
   - DB_HOST=localhost
   - DB_USER=admin
   - DB_PASSWORD=password123
   - DB_NAME=mlflow_db

## Documentación del despliegue

- **Instrucciones de instalación:**
  - Instalar dependencias: Asegúrate de tener Python instalado y las bibliotecas necesarias como FastAPI, Uvicorn, MLFlow, joblib, y 
    scikit-learn.
  - Registrar los modelos: Guarda los modelos LDA y los vectorizadores en MLFlow y archivos locales.
  - Configurar el entorno: Define las variables necesarias, como la URI de MLFlow y los puertos para FastAPI.
- **Instrucciones de configuración:** (instrucciones detalladas para configurar el modelo en la plataforma de despliegue)
  - Configurar el servidor FastAPI: Asegúrate de que el servidor esté configurado para cargar modelos desde MLFlow y vectorizadores desde 
    archivos locales.
  - Habilitar ngrok: Usa ngrok para exponer el servidor local y obtener una URL pública para acceso remoto.
  - Asegurar el entorno: Protege las rutas públicas y utiliza autenticación para ngrok si es necesario.
- **Instrucciones de uso:** 
  - Acceder al API: Visita la URL pública generada por ngrok seguida de /docs para interactuar con el API usando Swagger.
  - Enviar solicitudes: Envía un JSON al endpoint /predict_topic/ con la estructura:
      - texto: El texto a analizar.
      - modelo: El modelo a utilizar (todos, altos, bajos).
  - Interpretar la respuesta: El API devolverá el tópico dominante y la distribución de probabilidades entre tópicos.
  - Ver script con ejemplos (scripts/deployment/ejemplo_api.ipynb)
- **Instrucciones de mantenimiento:**
  - Actualizar modelos: Reentrena y sube nuevos modelos a MLFlow según sea necesario.
  - Verificar dependencias: Asegúrate de que las bibliotecas y versiones estén actualizadas.
  - Monitorear uso: Supervisa el rendimiento del API y ajusta el sistema para manejar más solicitudes si es necesario.
  - Resguardar archivos: Mantén copias de seguridad de los vectorizadores y modelos almacenados.
