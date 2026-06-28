1) ¿Por qué es mala práctica usar SELECT * en producción? 

Rendimiento: SELECT * trae todas las columnas aunque la app/report solo necesite algunas. Si hay columnas grandes (texto, JSON, blobs) o muchas filas, gastás más CPU, memoria y ancho de banda.
Mantenibilidad: si alguien agrega/elimina columnas en la tabla, las consultas pueden cambiar de comportamiento (o romperse) y también hacés más difícil entender qué usa realmente cada query.

2) ¿Por qué son importantes los alias para un stakeholder no técnico?
Porque el alias permite que el resultado tenga nombres de columnas “de negocio”, comprensibles para alguien que no sabe SQL ni el modelo de datos.

