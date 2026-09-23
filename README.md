## ¿Cuántas filas devuelve cada consulta y por qué son distintas?

La primera consulta, utilizando `UNION`, devuelve **10 registros**, ya que elimina los registros duplicados del resultado. En este caso, como se seleccionó únicamente `nombre_producto`, los nombres repetidos aparecen una sola vez.

La segunda consulta, utilizando `UNION ALL`, devuelve **14 registros**, ya que combina los resultados de ambas consultas y conserva los registros duplicados.

### ¿Por qué `UNION ALL` es más eficiente que `UNION`?

`UNION ALL` es más eficiente porque no necesita realizar el proceso adicional de identificar y eliminar registros duplicados.

En cambio, `UNION` debe comparar los resultados de ambas consultas para determinar qué registros están repetidos. Este proceso puede tener un mayor impacto en el rendimiento cuando se trabaja con grandes cantidades de datos.

### ¿En qué casos de negocio usarías cada uno?

**`UNION`:** lo utilizaría cuando se necesite obtener resultados únicos de diferentes consultas, por ejemplo, para obtener una lista sin duplicados de nombres de productos, ciudades, países, etc.

**`UNION ALL`:** lo utilizaría cuando se necesite consolidar información proveniente de diferentes consultas o tablas y sea necesario conservar todos los registros, incluidos los duplicados.

### ¿Qué pasa si las columnas de ambas consultas no coinciden en número o tipo?

Las consultas utilizadas con `UNION` o `UNION ALL` deben tener el mismo número de columnas y tipos de datos compatibles.

Si no se cumple esta condición, SQL Server genera un error y la consulta no puede ejecutarse correctamente.
