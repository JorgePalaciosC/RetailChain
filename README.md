### ¿Cuántas filas devuelve cada consulta y por qué son distintas?
La primera consulta `UNION` devuelve 10 registros ya se filtro por nombre_producto y existían valores repetidos eliminando el resto de columnas
La segunda consulta UNION ALL`` devuelve solo 14 registro por que se realizo la suma de todo las filas de ambas tablas

### ¿Por qué UNION ALL es más eficiente que UNION?
UNION ALL es más eficiente por que no realiza el proceso interno que hace UNION de buscar que filas son duplicadas y esto puede afectar en una base de datos que contenga muchos registros haciendo el proceso de respuesta más lento.

### ¿En qué casos de negocio usarías cada uno? 
UNION: lo utilizaría en caso que se requiera saber nombres únicos de productos, ciudades, países, etc.
UNION ALL: lo utilizaría para consolidar información dispersa.

### ¿Qué pasa si las columnas de ambas consultas no coinciden en número o tipo?
La base de datos detiene la ejecución inmediatamente y genera un error de sintaxis o de tipado.
