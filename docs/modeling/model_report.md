# Reporte del Modelo Final

## Resumen Ejecutivo
Los tópicos identificados en los comentarios bajos son:
- Tópico 0: precio, envio y cobrar
- Tópico 1: cancelar y pedido
- Tópico 2: producto, mejorara, servicio y tiempo
- Tópico 3: cerveza, caliente y fria
- Tópico 4: tardar, pedido, cupon y entregar
- Tópico 5: llegar, cervaeza y traer
- Tópico 6: repartifor, malo, horario y promocion
  
Los tópicos identificados en los comentarios altos son:
- Tópico 0: servivio, excelente y promocion
- Tópico 1: tiempo, entrega, cerveza y oferta
- Tópico 2: frio, producto y cerveza
- Tópico 3: fria, llegar y rapido
- Tópico 4: servicio, gracias, rapido  y precio
- Tópico 5: cupon, gustar, envio y descuento
- Tópico 6: encantar, atencion, calidad, rapidez y precio

## Descripción del Problema

DDV, una empresa de bienes de consumo masivo, lanzó en 2023 una plataforma de e-commerce para la venta de alimentos y bebidas, ofreciendo a los consumidores la comodidad de comprar en línea y recibir sus productos directamente en casa. Sin embargo, buscan comprender mejor la percepción del consumidor sobre este nuevo servicio para optimizar la experiencia del cliente y aumentar su competitividad en el mercado. El desafío principal radica en la gran cantidad de datos no estructurados generados por la plataforma, como reseñas de clientes y comentarios en redes sociales, lo que dificulta el análisis manual y la extracción de insights valiosos. Para abordar esto, se propone el uso de un modelo que procese y analice estos datos de manera automatizada, permitiendo identificar áreas de mejora, descubrir fortalezas, comprender las necesidades del cliente, y tomar decisiones estratégicas basadas en datos para fortalecer la posición de DDV en el mercado del comercio electrónico.


## Descripción del Modelo

Se implementó un modelo de tópicos Latent Dirichlet Allocation (LDA) para analizar la percepción del consumidor sobre el servicio de e-commerce de DDV. Este modelo no supervisado identifica los temas principales presentes en los comentarios de los clientes y su asociación con las calificaciones (altas, medias y bajas). La elección de LDA se basa en su capacidad para descubrir patrones ocultos en texto no estructurado, asumiendo que cada comentario es una mezcla de diferentes temas, cada uno representado por una distribución de palabras. Esto permite identificar áreas de mejora, fortalezas y comprender las necesidades del cliente en relación a la satisfacción con la plataforma.

## Evaluación del Modelo

### Métricas de evaluación

Utilizamos nubes de palabras para encontrar el top 15 de los términos mas comunes dentro de cada tópico. Esto se hizo reiterativamente hasta encontrar los parametros que nos mostraran los temas con mas sentido para el negocio.

### Resultados y Análisis de los resultados

* Nube de palabras ponderada con la importancia de cada término en un tópico, para visualizar mejor los temas de todos los comentarios:
![comentarios](https://github.com/ValeriaRaS/Identificacion-de-topicos-G14-/blob/master/docs/modeling/Images/todos_comentarios.png)
Número de comentarios por tópico de todas las reviews
![comentarios](https://github.com/ValeriaRaS/Identificacion-de-topicos-G14-/blob/master/docs/modeling/Images/barra_todos.png)

* Nube de palabras ponderada con la importancia de cada término en un tópico, para visualizar mejor los temas de los comentarios bajos:
![bajos](https://github.com/ValeriaRaS/Identificacion-de-topicos-G14-/blob/master/docs/modeling/Images/comentarios_bajos.png)
Los tópicos identificados en los comentarios bajos son:
- Tópico 0: precio, envio y cobrar
- Tópico 1: cancelar y pedido
- Tópico 2: producto, mejorara, servicio y tiempo
- Tópico 3: cerveza, caliente y fria
- Tópico 4: tardar, pedido, cupon y entregar
- Tópico 5: llegar, cervaeza y traer
- Tópico 6: repartifor, malo, horario y promocion
  
  Número de comentarios por tópico de las reviews bajas
  ![bajos](https://github.com/ValeriaRaS/Identificacion-de-topicos-G14-/blob/master/docs/modeling/Images/barra_bajos.png)

  
* Nube de palabras ponderada con la importancia de cada término en un tópico, para visualizar mejor los temas de los comentarios altos:
![altos](https://github.com/ValeriaRaS/Identificacion-de-topicos-G14-/blob/master/docs/modeling/Images/comentarios_altos.png)
Los tópicos identificados en los comentarios altos son:
- Tópico 0: servivio, excelente y promocion
- Tópico 1: tiempo, entrega, cerveza y oferta
- Tópico 2: frio, producto y cerveza
- Tópico 3: fria, llegar y rapido
- Tópico 4: servicio, gracias, rapido  y precio
- Tópico 5: cupon, gustar, envio y descuento
- Tópico 6: encantar, atencion, calidad, rapidez y precio

   Número de comentarios por tópico de las reviews altas
  ![bajos](https://github.com/ValeriaRaS/Identificacion-de-topicos-G14-/blob/master/docs/modeling/Images/barra_altos.png)

   
## Conclusiones y Recomendaciones
*   Logramos analizar los comentarios de los clientes sobre su experiencia con los pedidos realizados a través del e-commerce, utilizando técnicas de procesamiento de lenguaje natural. Este análisis nos permitio identificar los factores que impulsan calificaciones altas y las áreas de mejora asociadas con calificaciones bajas. Lo que permitirá extraer insights estratégicos para la optimización del servicio de e-commerce y la mejora continua de la experiencia del cliente.

*   En terminos mas tecnicos, entrenamos un modelado de identificacion de tópicos, encontrando los temas asociados con calificaciones altas (9 a 10) versus aquellas con calificaciones medias (7 a 8) y bajas (0 a 6). Entregamos una herramienta que le permite a los equipos interesados, cargar los comentarios asociados con ciertas ordenes de su interés y realice un proceso de identificación de temas y/o clasificación de los comentarios por tópicos, de manera eficiente y automatica.

> **Principales aprendizajes:**

*   Identificamos que era util tomar la informacion del score como variable auxiliar para realizar el analisis de topicos, separando el embedding y el modelo entre comentarios de puntajes altos y de puntajes bajos. Esto fue util pues, primero, los comentarios negativos y positivos tenian tendencias diferentes en: Cantidad de documentos, Cantidad de palabras dentro de cada documento y especificidad de terminos (En los puntajes bajos solian encontrarse palabras mas variadas y ser mas largos, en los puntajes altos habia menor variedad de terminos y comentarios mucho mas concisos). Segundo, al separar los comentarios podiamos entender las diferencias en topicos entre cada uno de ellos, ademas el score ya nos daba informacion del sentimiento positivo o negativo hacia los topicos que encontrabamos.

*   El modelo LDA mostro rapidamente muy buenos resultados identificando los topicos en los comentarios con puntajes mas altos. Sin embargo, con los de puntajes bajos tuvimos un reto mas grande, creemos que esto se debe a que eran menor cantidad de comentarios, tambien eran comentarios con un numero de palabras bastante mayor y diverso, e incluso contenian terminos mas especificos, por ello tuvimos que ajustar e iterar bastantes veces los parametros hasta lograr el resultado final.

> **Next Steps:**

*   Seria interesante llevar a cabo una comparación de los temas clave emergentes en los comentarios entre los años 2023 y 2024. Pueden haber temas que ya no son tan comunes en 2024, asi como otros que sean prioritarios actualmente.
*   Creemos que el modelo tiene bastante potencial de seguir siendo mejorado, optimizando quiza el numero de topicos disponibles. Tambien probar otros algoritmos mas enfocados en documentos que son cortos y voluminosos, como BERTopic.
