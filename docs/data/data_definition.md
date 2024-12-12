# Definición de los datos

## Origen de los datos
- Comentarios de los pedidos realizados a través de la aplicación y almacenados en una tabla cargada en el ambiente de Snowflake de la compañía DDV.

### Descripción del origen de los datos
- Usuario realiza una orden en la aplicación
- Usuario recibe la orden en su ubicación
- En la aplicación se le solicita al usuario una clasificación del servicio, con un rango de 1 a 10 (Score_clasification)
- Usuario tiene la opción voluntaria de escribir un comentario (Comment)
- Esta información se almacena en la base de datos
- La base se consolida en snowflake para la consulta del data scientist (formato csv)

## Especificación de los scripts para la carga de datos

- scripts/data_acquisition/data_acquisition.ipynb

## Referencias a rutas o bases de datos origen y destino

- Snowflake / DDV / ecommerce / country / nps (Ruta de acceso a los datos es confidencial)

### Rutas de origen de datos

- Extracción de la tabla de datos en formato .csv con 208.191 comentarios asociados a pedidos realizados entre 2023-1 y 2024-9.

### Base de datos de destino

-  Snowflake / DDV / ecommerce / country / Modelo NLP 
