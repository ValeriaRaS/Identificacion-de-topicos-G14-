# Definición de los datos

## Origen de los datos

- Comentarios de los pedidos realizados a través de la aplicación y almacenados en una tabla cargada en el ambiente de Snowflake de la compañía DDV.

## Especificación de los scripts para la carga de datos

- scripts/data_acquisition/data_acquisition.ipynb

## Referencias a rutas o bases de datos origen y destino

- Snowflake / DDV / ecommerce / country / nps (Ruta de acceso a los datos es confidencial)

### Rutas de origen de datos

- Extracción de la tabla de datos en formato .csv con 208.191 comentarios asociados a pedidos realizados entre 2023-1 y 2024-9.

### Base de datos de destino

-  Snowflake / DDV / ecommerce / country / Modelo NLP 
