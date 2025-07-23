### Evolución de las Exportaciones Colombianas (2015–2024)

Este proyecto tiene como objetivo visualizar la evolución del top 10 de productos exportados por Colombia entre los años 2015 y 2024, con base en su participación porcentual sobre el valor FOB total exportado cada año.

La animación generada permite observar cómo cambian las participaciones de los principales productos a lo largo del tiempo, mostrando dinámicas que pueden estar influenciadas por factores como el precio internacional, el volumen exportado o la aparición de nuevos productos.

Estructura del proyecto
📁 1. 01_preparacion_datos.ipynb
Este notebook realiza la depuración y transformación de los datos originales de exportaciones, hasta obtener el archivo final top_10_por_año.csv. Este archivo contiene el top 10 de productos exportados por año con su respectiva participación porcentual.

📁 02_animacion.ipynb
Este notebook toma como insumo top_10_por_año.csv y genera una animación estilo bar chart race que muestra la evolución anual del top 10 de exportaciones colombianas. Las barras están acompañadas por imágenes ilustrativas de cada producto.

🔧 Requisitos
Asegúrate de tener instalado:

Python 3.8+

Jupyter Notebook

Las siguientes librerías:

pip install pandas matplotlib pillow numpy



📌 Fuente de los datos
Los datos provienen del portal del DANE - Estadísticas de Comercio Exterior. La visualización y procesamiento posterior fueron realizados por Carlos Durán.
