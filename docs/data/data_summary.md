# Reporte de Datos

Este documento contiene los resultados del análisis exploratorio de datos.

## Resumen general de los datos

**Composición del corpus:** El corpus esta constituido por un total de 206.268 documentos con un peso aproximado de 41 MB

**Idioma:** Los documentos en su gran mayoría estan escritos en Español. Algunos unicamente tienen caracteres especiales o incluso emojis. Estos se trabajaran posteriormente en la limpieza del corpus.

**Relación entre los documentos:** Los documentos del corpus se relacionan entre si, ya que todos son valoraciónes, comentarios y opiniones sobre el mismo e-commerce de la compañia DDV.

## Resumen de calidad de los datos

**Documentos vacíos:** Debido a que incluir un comentario dentro de la review es opcional, el corpus cuenta con varios documentos vacios. En total son 121.338 (59%) las reviews que no cuentan con algun comentario entre el 2023 y 2024.

**Documentos ilegibles:** Debido a que los usuarios realizan los comentarios por medio de un dispositivo movil, este le permite ingresar caracteres especiales como los emojis, dando asi problemas en la codificacion de los documentos. En total, se tienen 1.472 comentarios con alguno de estos caracteres.

**Mezcla de idiomas:** Se espera que el corpus este completamente en español debido al contexto del proyecto.

## Variable objetivo

**Variable objetivo:** Ya que el problema que se quiere solucionar, es de análisis no supervizado, el corpus no tiene una variable objetivo a estimar.

## Variables individuales

Como variables utilizaremos el score (variable cuantitativa discreta), el cupon (variable cuantitativa discreta) y la fecha en formato MM-yyyy de la review.

![Histograma](https://github.com/ValeriaRaS/Identificacion-de-topicos-G14-/blob/master/Images/Histogram_scoresbycategory.png)
![Histograma](https://github.com/ValeriaRaS/Identificacion-de-topicos-G14-/blob/master/Images/Graficopastel_cupones.png)
![Histograma](https://github.com/ValeriaRaS/Identificacion-de-topicos-G14-/blob/master/Images/TimeSeries_Fecha.png)

## Ranking de variables
Dado que no hay una variable objetivo, se procedió a analizar la relación entre variables individuales.

## Relación entre variables explicativas y variable objetivo

Exploramos si hay algun favoritismo dentro de cada score con estar relacionado o no con un cupon. Sin embargo, encontramos que la distribución dentro de cada score de reviews con y sin cupon no tiene diferencias siginificativas.

Hasta el momento no se han encontrado redundancias entre las variables que nos interesan para el análisis de identificacion de tópicos.

![Histograma](https://github.com/ValeriaRaS/Identificacion-de-topicos-G14-/blob/master/Images/TablaContingencia.png)
