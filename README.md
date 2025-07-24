# 📦 Evolución del Top 10 de Exportaciones Colombianas (2015-2024)

Este repositorio contiene un análisis y visualización animada de cómo ha cambiado el Top 10 de productos exportados por Colombia entre 2015 y 2024, usando datos en bruto del comercio exterior.

Se compone de dos notebooks principales:

1. `01_limpieza_exportaciones.ipynb`: Procesamiento y limpieza de los datos.
2. `02_animacion_exportaciones.ipynb`: Visualización tipo "bar chart race" con imágenes por producto.

---

## 📁 Contenido del repositorio


<img width="491" height="139" alt="image" src="https://github.com/user-attachments/assets/37b45a44-c619-4118-9193-df41802a16ed" />


---

## 📘 Notebooks

### 1️⃣ `01_limpieza_exportaciones.ipynb`: Depuración de datos

**Objetivo**: Procesar y limpiar los datos de exportaciones colombianas entre 2015 y 2024 a partir de múltiples archivos CSV en bruto.

**Tareas principales que realiza:**

- Lectura de los datos originales desde carpetas anuales organizadas dentro de un directorio principal.
- Limpieza de columnas clave (por ejemplo: valores FOB, subpartidas arancelarias).
- Conversión de formatos numéricos (por ejemplo, reemplazo de comas y puntos decimales).
- Normalización de los códigos de productos (`POSAR6`), asegurando que tengan 10 dígitos (manteniendo ceros a la izquierda).
- Cálculo del total exportado por subpartida y año.
- Cálculo del porcentaje anual que representa cada producto respecto al total exportado ese año.
- Selección del **Top 10 productos por año**.

📁 **Sobre la estructura de los datos de entrada:**

En el notebook se detalla **de dónde provienen los datos**, cómo están organizadas las carpetas (`data/expo_2015`, `data/expo_2016`, etc.), y cómo se guardaron los archivos intermedios y finales.  
Estas rutas pueden verse directamente en las líneas de código donde se usan `pd.read_csv()` y otras operaciones con archivos, lo cual permite comprender el flujo de entrada y salida.

🔁 **Extensibilidad**  
Si más adelante se desean agregar nuevos años de datos (por ejemplo, 2025), es necesario **volver a ejecutar este notebook**, ya que en él se definen todas las reglas de limpieza, estructura y generación del archivo `top_10_por_año.csv`.

> 💡 Recomendado: revisar este notebook antes de hacer modificaciones, para entender completamente la lógica y las fuentes utilizadas.

---

### 2️⃣ `02_animacion_exportaciones.ipynb`: Visualización animada

**Objetivo**: Crear una animación del Top 10 de productos exportados por Colombia desde 2015 hasta 2024.

**Características:**

- Lectura del archivo limpio `top_10_por_año.csv` desde la carpeta `/data`.
- Pivot de los datos para representar la participación porcentual anual por producto.
- Carga de imágenes personalizadas para los productos, desde la carpeta `/imagenes`, en formato `.jpg`, para enriquecer la visualización.
- Generación de una animación tipo **"bar chart race"** usando `matplotlib.animation`.

> ⚠️ El archivo `.mp4` de la animación no se incluye en el repositorio, pero el notebook genera todo el contenido necesario para producirlo.

> 💡 Nota: Las imágenes deben estar en la carpeta imagenes/ con nombres idénticos a los productos (.jpg).

Previsualización

<img width="1365" height="653" alt="Captura de pantalla 2025-07-23 172139" src="https://github.com/user-attachments/assets/f61cd599-b4c4-442a-ae62-7bb339ed8bdb" />

---

## ✅ Requisitos

- Python 3.8+
- pandas
- matplotlib
- Jupyter Notebook


📌 Fuente de los datos
Los datos provienen del portal del DANE - Estadísticas de Comercio Exterior. La visualización y procesamiento posterior fueron realizados por Carlos Durán.
