### CÓDIGOS DEL EJERCICIO 01
---
 1. `!head files/sales_data.csv` Este código funciona de la siguiente manera: el `!head` es un comando de Unix que se usa para mostrar las primeras lineas de un archivo. En Jupyter el símbolo (!) significa que debe ejecutar un comando del sistema. Mientras que el `files/sales_data.csv` es la ruta del archivo que se mostrará.
   
 1. `sales = pd.read_csv("files/sales_data.csv", parse_dates=["Date"])`

    - `pd.read_csv()` Esto es un método de Pandas para leer archivos csv y convertirlos a DataFrames (estructura similar a la hoja de cálculos).
    - `files/sales_data.csv` Este argumento es para indicar la ruta del archivo que se leerá.
    - `pase_dates=["Date"]` Este segundo argumento (opcional) convierte la columna Date a un tipo de date datetime.

 1. `sales.head()` Muestra las primeras 5 líneas de un dataframe (en este caso "sales"). Permite una inspección rápida, además que ya se trabaja con datos procesados y convertidos.

 1. `sales.shape` Devuelve una tupla (#filas, #columnas).

 1. `sales.info()` Devuelve información sobre el dataframa, tipos de datos, valores no nulos, presencia de valores nulos.

 1. `sales.describe()` Muestra estadísticas descriptivas para un dataframe (media, desviación estándar, percentiles, valores min y max)

    - `sales.describe(percentiles=[.10, .25, .50, .75, .90])` Especifica los percentiles
    - `sales.describe(include=[np.number])` Especifica que columnas debes incluir
    - `sales.describe(exclude=[np.object])` Especifica que columnas debes excluir
 1. `sales['Unit_Cost'].describe()` Aplica estadistica descriptiva a una sola columna del datafram.

 1. `sales['Unit_Cost'].mean()` Devuelve el promedio de la columna indicada

    - `.mean()`
    - `.sum()`
    - `.median()`
    - `.min()`
    - `.max()`
    - `.std()`
    - `.var()`
    - `.quantile(0.25)`

 1. `sales['Unit_Cost'].plot(kind='box', vert=False, figsize=(14,6))`

    -`kind='box'` Indica que queremos una gráfica de cajas.
    -`vert=False` Indica que la gráfica será horizontal.
    -`figsize=(14,6)` Controla el tamaño del diagrama de caja.
