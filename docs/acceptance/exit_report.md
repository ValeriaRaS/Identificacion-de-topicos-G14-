# Informe de salida

## Resumen Ejecutivo

Este informe describe los resultados del proyecto de machine learning implementado para analizar los comentarios de los clientes de DDV sobre su experiencia con el e-commerce. A través de técnicas de procesamiento de lenguaje natural y modelado de tópicos, se identificaron factores que impulsan las calificaciones altas y las áreas de mejora asociadas con las calificaciones bajas. Además, se proporcionan recomendaciones basadas en estos insights para mejorar la experiencia del cliente y optimizar el servicio de e-commerce.

## Resultados del Proyecto

- **Entregables y logros alcanzados:**
  - **Entendimiento del negocio y carga de datos:** Se completó la carga y comprensión de los datos de comentarios de clientes, con 208.191 comentarios entre enero de 2023 y septiembre de 2024.
  - **Preprocesamiento y análisis exploratorio:** Se limpiaron y analizaron los datos, destacando las características más relevantes para el análisis de los comentarios.
  - **Modelado y extracción de características:** Se implementó y ajustó un modelo de **Latent Dirichlet Allocation (LDA)** para identificar los temas subyacentes en los comentarios según las calificaciones.
  - **Despliegue y evaluación:** Se entregó una herramienta operativa que permite a los equipos interesados cargar nuevos comentarios y realizar un análisis automático de tópicos.
  
- **Evaluación del modelo final:**  
  El modelo mostró una precisión superior al 60%, con buen rendimiento en todos los puntajes de calificación. Aunque los resultados para comentarios con calificaciones bajas fueron más desafiantes debido a su diversidad y longitud, se lograron identificar los principales temas asociados a estos comentarios.
  
- **Relevancia para el negocio:**  
  Los resultados proporcionan insights clave para la mejora continua del servicio de e-commerce, permitiendo a los equipos de marketing y comercial identificar áreas de mejora en la experiencia del cliente y tomar decisiones informadas sobre cómo optimizar la plataforma.

## Lecciones Aprendidas

- **Desafíos y obstáculos:**
  - Los comentarios con calificaciones bajas presentaron una mayor variabilidad en términos de longitud y terminología, lo que dificultó la identificación precisa de los temas.
  - Hubo que ajustar los parámetros del modelo LDA varias veces para lograr resultados satisfactorios en los comentarios negativos.
  
- **Lecciones aprendidas en el manejo de datos, modelamiento e implementación:**
  - La separación de los comentarios en función de las calificaciones (altas, medias y bajas) facilitó el análisis y mejoró la calidad de los resultados.
  - La elección de LDA como modelo no supervisado fue adecuada, pero se requería una iteración cuidadosa de parámetros para obtener tópicos claros, especialmente en los comentarios negativos.
  
- **Recomendaciones para futuros proyectos de machine learning:**
  - Considerar el uso de algoritmos alternativos como **BERTopic**, que se enfocan mejor en documentos cortos y voluminosos, para mejorar el análisis de comentarios más largos y específicos.
  - Implementar un proceso continuo de refinamiento y ajuste de modelos para asegurar que el sistema evolucione con el tiempo.

## Impacto del Proyecto

- **Impacto en el negocio:**  
  Este proyecto ha permitido a DDV obtener una visión clara y procesable de la percepción del consumidor sobre el servicio de e-commerce. Los insights obtenidos son valiosos para la optimización de la plataforma, el fortalecimiento de la competitividad en el mercado y la mejora continua de la experiencia del cliente.

- **Áreas de mejora y oportunidades futuras:**  
  - Expandir el análisis a comentarios en otros idiomas, ampliando la cobertura geográfica y mejorando la comprensión global del servicio.
  - Desarrollar nuevos modelos de predicción basados en los tópicos identificados, como sistemas de recomendación o segmentación de clientes, para mejorar la personalización del servicio.

## Conclusiones

- **Resumen de resultados y logros:**  
  El proyecto permitió identificar los temas clave asociados con calificaciones altas y bajas, proporcionando una herramienta útil para que los equipos de DDV analicen los comentarios de los clientes de manera eficiente y automatizada.
  
- **Conclusiones finales y recomendaciones para futuros proyectos:**  
  La metodología de modelado de tópicos LDA ha demostrado ser efectiva para extraer insights de grandes volúmenes de datos no estructurados. Sin embargo, se recomienda continuar iterando y mejorando el modelo, probando otros algoritmos y abordando posibles limitaciones como la variabilidad en los comentarios negativos.

## Agradecimientos

- Agradecimientos al **equipo de trabajo** compuesto por:
  - **Valeria Ramírez Sánchez** (líder del proyecto),
  - **Daniel Felipe Hernández Montoya** (Data scientist senior),
  - **Diego Alejandro Sandoval Skinner** (Data scientist junior), quienes contribuyeron al éxito del proyecto con su dedicación y habilidades.

- Agradecimientos especiales a los **patrocinadores** y **financiadores** del proyecto, cuyo apoyo fue fundamental para llevar a cabo esta iniciativa.
- Otros agradeciemientos al profesor Jorge Eliecer Camargo Mendoza y al profesor Oscar Alberto Bustos.
