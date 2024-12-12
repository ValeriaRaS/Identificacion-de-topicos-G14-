# Project Charter - Entendimiento del Negocio

## Nombre del Proyecto

Modelo de Tópicos para Clasificación de Comentarios de DDV

## Objetivo del Proyecto

Analizar los comentarios de los clientes sobre su experiencia con los pedidos realizados a través del e-commerce, utilizando técnicas de procesamiento de lenguaje natural. Este análisis busca identificar los factores que impulsan calificaciones altas y las áreas de mejora asociadas con calificaciones bajas. Adicionalmente, se llevará a cabo una comparación de los temas clave emergentes en los comentarios entre los años 2023 y 2024, lo que permitirá extraer insights estratégicos para la optimización del servicio de e-commerce y la mejora continua de la experiencia del cliente.

## Alcance del Proyecto

### Incluye:

- Descripción de los datos disponibles: Comentarios de los pedidos realizados a través de la aplicación y almacenados en una tabla cargada en el ambiente de Snowflake de la compañía DDV (llamada asi dado que son datos sensibles), lo cuales se extraen en una tabla de datos en formato .csv con 208.191 comentarios asociados a pedidos realizados entre 2023-1 y 2024-9.
  
- Descripción de los resultados esperados: Resultados que nos permitan identificar los factores que impulsan calificaciones altas y las áreas de mejora asociadas con calificaciones bajas. Para asi poder extraer insights estratégicos a favor de la optimización del servicio de e-commerce y la mejora continua de la experiencia del cliente.
  
- Criterios de éxito del proyecto: El primer criterio sería que la precisión del modelo (accuracy) sea superior al 60%, que el modelo tenga un buen rendimiento en todos los puntajes 8sean bajos o altos) y que el modelo represente correctamente las palabras y sus relaciones semánticas.

### Excluye:

Para este proyecto se tuvo en cuenta las limitaciones mencionadas a continuación:
- Enfoque limitado en los datos dado que el modelo desarrollado no considerará reseñas en idiomas distintos al español ni caracteres especiales.
- Alcance limitado en el preprocesamiento de texto puesto que este proyecto no incluye la detección ni corrección de errores gramaticales o de sintaxis de las reseñas.
-  Limitación en la cobertura temporal ya que el proyecto no incluirá el análisis de reseñas que cubran un período más allá de los años 2023 y 2024.

## Metodología

La metodología que se utilizará para llevar a cabo este proyecto es Modelado de tópicos "LDA", que asume que los documentos (comentarios) son una mezcla de temas, y cada tema es una distribución de palabras, de esta manera se pueden calcular las probabilidades de las palabras en cada tópico y en cada documento. Generando temas más claramente diferenciados, que a su vez facilita la interpretación de los resultados e identifica los temas asociados con calificaciones altas (9 a 10) versus aquellas con calificaciones medias (7 a 8) y bajas (0 a 6).

## Cronograma

| Etapa | Duración Estimada | Fechas |
|------|---------|-------|
| Entendimiento del negocio y carga de datos | 1 semanaa | del 21 de noviembre al 28 de noviembre |
| Preprocesamiento, análisis exploratorio | 1 semana | del 28 de noviembre al 5 de diciembre |
| Modelamiento y extracción de características | 1 semana  | del 5 de diciembre al 12 de diciembre |
| Despliegue | 1 semana  | del 12 de diciembre al 19 de diciembre |
| Evaluación y entrega final | 1 semana  | del 19 de diciembre al 21 de diciembre |


## Equipo del Proyecto

- Valeria Ramírez Sánchez (líder del proyecto)
- Daniel Felipe Hernández Montoya (Data scientist senior)
- Diego Alejandro Sandoval Skinner (Data scientist junior)

## Presupuesto

- Presupuesto temporal: 1 mes (duración del módulo).
- Presupuesto de recursos: Servios de internet y energía.
- Presupuesto computacuional: GPU de Google Collab.

## Stakeholders
Los Stakeholders de este proyecto son los equipos de marketing y comercial de la empresa DDV, los cuales buscan obtener una comprensión más profunda de la percepción de los consumidores sobre el servicio de e-commerce. Para así identificar y analizar insights clave que revelen tanto oportunidades de mejora como fortalezas de la plataforma, permitiendo una optimización continua de la experiencia del cliente y fortaleciendo la competitividad de la aplicación en el mercado, ya que no han tenido la capacidad de realizar este análisis debido al gran volumen de información no estructurada que representan estos datos, lo que dificulta su procesamiento y extracción de valor.

## Aprobaciones

Nombre y cargo del aprobador del proyecto:  
- Profesor Jorge Eliecer Camargo Mendoza
- Profesor Oscar Alberto Bustos
