# Reporte del Modelo Baseline

Este documento contiene los resultados del modelo baseline.

## Descripción del modelo

Tipo de modelo seleccionado: **Modelos de Tópicos**

Elegimos este tipo de modelo no supervisado dado que esta aproximación nos ayuda a identificar los temas principales que se discuten en los comentarios buenos, medios y bajos (principal objetivo del proyecto). Esto nos da información sobre qué aspectos del servicio son los más importantes para los usuarios y como estos estan asociados con cada nivel de calificacion.

Modelo: **LDA**

Utilizamos el modelo LDA dado que asume que los documentos (comentarios) son una mezcla de temas, y cada tema es una distribución de palabras, de esta manera se pueden calcular las probabilidades de las palabras en cada tópico y en cada documento. Generando temas más claramente diferenciados, que a su vez facilita la interpretación de los resultados. Ademas, como los comentarios tienden a centrarse en varios temas concretos y no tanto en el significado más profundo de las palabras, LDA puede ser más eficaz.

## Variables de entrada

Los modelos de tópicos, en especial el LDA, se aplica sobre representaciones basadas en bolsas de palabras. Asi que comenzamos por entrenar vectorizadores para conteo de palabras, siendo asi nuestra unica variable de entrada cada comentario.

## Variable objetivo

Topico o tema principal de los comentarios con puntajes 9 y 10 (altos), con puntajes de 8 o menos (bajos). Y de todos los comentarios, sin importar su calificacion.

## Evaluación del modelo

### Métricas de evaluación

Utilizamos nubes de palabras para encontrar el top 15 de los términos mas comunes dentro de cada tópico. Esto se hizo reiterativamente hasta encontrar los parametros que nos mostraran los temas con mas sentido para el negocio.

### Resultados y Análisis de los resultados

- Nube de palabras ponderada con la importancia de cada término en un tópico para visualizar mejor los tópicos de todos los comentarios:


## Conclusiones

Conclusiones generales sobre el rendimiento del modelo baseline y posibles áreas de mejora.

