# Diccionario de datos

## Base de datos (Union de 3 bases dada la cantidad de comentarios)

**Agregar una descripción de la tabla o fuente de datos.

| Variable | Descripción | Tipo de dato | Rango/Valores posibles | Fuente de datos |
| --- | --- | --- | --- | --- |
| DATE_SPK | Especifica la fecha en la cual se hizo la valoracion del servicio | Fecha | 2023-1 y 2024-9 | snowflake |
| SCORE | Especifica el puntaje que se le asignó al servicio  | Entero | 1-10 | snowflake  |
| SCORE_CLASSIFICATION | Indica si la calificación es menor a 9 (detractor) o mayor o igual a 9 (promoter)  | Texto | Promoter / Detractor  | snowflake  |
| COMMENT | Comentario del cliente acerca del servicio (puede ser vacío) | Texto | Cadena de texto | snowflake  |
| COUPON_CODE | Indica si el cliente uso o no un cupón | Booleano | False /True | snowflake  |

- **Variable**: nombre de la variable.
- **Descripción**: breve descripción de la variable.
- **Tipo de dato**: tipo de dato que contiene la variable.
- **Rango/Valores posibles**: rango o valores que puede tomar la variable.
- **Fuente de datos**: fuente de los datos de la variable.
