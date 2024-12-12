# Reporte del Modelo Baseline

Este documento contiene los resultados del modelo baseline.

## Descripción del modelo

Tipo de modelo seleccionado: **Modelos de Tópicos**

Elegimos este tipo de modelo no supervisado dado que esta aproximación nos ayuda a identificar los temas principales que se discuten en los comentarios buenos, medios y bajos (principal objetivo del proyecto). Esto nos da información sobre qué aspectos del servicio son los más importantes para los usuarios y como estos estan asociados con cada nivel de calificacion.

Modelo: **LDA**

Utilizamos el modelo LDA dado que asume que los documentos (comentarios) son una mezcla de temas, y cada tema es una distribución de palabras, de esta manera se pueden calcular las probabilidades de las palabras en cada tópico y en cada documento. Generando temas más claramente diferenciados, que a su vez facilita la interpretación de los resultados. Ademas, como los comentarios tienden a centrarse en varios temas concretos y no tanto en el significado más profundo de las palabras, LDA puede ser más eficaz.

## Otros modelos
Para este proyecto aparte del modelo baseline se busco desarrollar, para encontrar mas resultados y mayor informacion, un modelo Bertopic, usando como base el embedding FastText. Sin embargo, debido a limitantes de tiempo, no logramos completarlo/revisarlo completamente. 

## Variables de entrada

Los modelos de tópicos, en especial el LDA, se aplica sobre representaciones basadas en bolsas de palabras. Asi que comenzamos por entrenar vectorizadores para conteo de palabras, siendo asi nuestra unica variable de entrada cada comentario.

## Variable objetivo

Topico o tema principal de los comentarios con puntajes 9 y 10 (altos), con puntajes de 8 o menos (bajos). Y de todos los comentarios, sin importar su calificacion.

## Evaluación del modelo

### Métricas de evaluación

Utilizamos nubes de palabras para encontrar el top 15 de los términos mas comunes dentro de cada tópico. Esto se hizo reiterativamente hasta encontrar los parametros que nos mostraran los temas con mas sentido para el negocio.

### Resultados y Análisis de los resultados

- Nube de palabras ponderada con la importancia de cada término en un tópico, para visualizar mejor los temas de todos los comentarios:
![comentarios](https://github.com/ValeriaRaS/Identificacion-de-topicos-G14-/blob/master/docs/modeling/Images/todos_comentarios.png)

- Nube de palabras ponderada con la importancia de cada término en un tópico, para visualizar mejor los temas de los comentarios bajos:
![bajos](https://github.com/ValeriaRaS/Identificacion-de-topicos-G14-/blob/master/docs/modeling/Images/comentarios_bajos.png)

- Nube de palabras ponderada con la importancia de cada término en un tópico, para visualizar mejor los temas de los comentarios altos:
![altos](https://github.com/ValeriaRaS/Identificacion-de-topicos-G14-/blob/master/docs/modeling/Images/comentarios_altos.png)

## Conclusiones

*   Logramos analizar los comentarios de los clientes sobre su experiencia con los pedidos realizados a través del e-commerce, utilizando técnicas de procesamiento de lenguaje natural. Este análisis nos permitio identificar los factores que impulsan calificaciones altas y las áreas de mejora asociadas con calificaciones bajas. Lo que permitirá extraer insights estratégicos para la optimización del servicio de e-commerce y la mejora continua de la experiencia del cliente.
  
*   Identificamos que era util tomar la informacion del score como variable auxiliar para realizar el analisis de topicos, separando el embedding y el modelo entre comentarios de puntajes altos y de puntajes bajos. Esto fue util pues, primero, los comentarios negativos y positivos tenian tendencias diferentes en: Cantidad de documentos, Cantidad de palabras dentro de cada documento y especificidad de terminos (En los puntajes bajos solian encontrarse palabras mas variadas y ser mas largos, en los puntajes altos habia menor variedad de terminos y comentarios mucho mas concisos). Segundo, al separar los comentarios podiamos entender las diferencias en topicos entre cada uno de ellos, ademas el score ya nos daba informacion del sentimiento positivo o negativo hacia los topicos que encontrabamos.

