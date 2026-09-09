Encabezados promovidos: la primera fila pasa a ser el nombre de columnas.
Tipo cambiado: se asigna un tipo de dato inicial a las 20 columnas originales (texto, fecha, entero, número, etc.).
Columnas con nombre cambiado: se traducen los códigos crípticos del legado (COD_OP, COD_CLI, etc.) a nombres legibles en español (ID_Operacion, ID_Cliente, etc.).
Tipo cambiado1: se corrige Fecha_Venta, que había quedado como datetime, a date puro.
Columnas con nombre cambiado1: segundo ajuste de nombres — corrige Punto_Venta a Precio_Unitario (nombre mal puesto en el paso 4) y SEG_CLI a Segmento (columna que no se había renombrado antes).
Columnas quitadas: se eliminan los atributos descriptivos del cliente (Nombre, Mail, Teléfono, Ciudad, Provincia, Segmento, Activo, Fecha de alta).
Columnas reordenadas: se ordenan las columnas restantes en una secuencia lógica (operación → cliente → producto → fecha → detalle de venta).
Columnas quitadas1: se eliminan los atributos descriptivos del producto (Descripción, Rubro).
Poner en mayúsculas cada palabra: se estandariza Canal con Text.Proper (evita "online"/"Online"/"ONLINE" como valores distintos).
Duplicados quitados: Table.Distinct sobre toda la fila.
Filas en blanco eliminadas: se descartan filas donde absolutamente todos los campos están vacíos o nulos.
Filas filtradas: filtro final que descarta las filas donde Total_Venta es nulo.
