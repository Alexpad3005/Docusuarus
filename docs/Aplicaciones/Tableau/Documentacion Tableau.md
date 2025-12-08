# Documentación: Cómo Usar Tableau

## 1. ¿Qué es Tableau?

Tableau es una herramienta de Business Intelligence (BI) enfocada en la visualización de datos. Permite:

Conectar múltiples fuentes de datos

Transformar datos sin código

Crear gráficos interactivos

Construir dashboards profesionales

Publicar informes en Tableau Server o Tableau Cloud

Su principal ventaja es la facilidad para analizar datos sin programación.

**Nota:** *La informacion presentada en este documento es para propositos educativos, no contiene la informacion real del processo al cual se creo este programa, por cuestion de privacidad y proteccion de la informacion.*

## 2. Versiones de Tableau
Producto	Uso
Tableau Desktop	Creación de dashboards y análisis.
Tableau Prep	Limpieza y transformación de datos.
Tableau Server	Publicación de dashboards dentro de la empresa.
Tableau Cloud	Versión en la nube administrada por Tableau.
Tableau Public	Versión gratuita para dashboards públicos.

## 3. Conectarse a Datos

Desde Tableau Desktop, al abrir la aplicación:

Selecciona la fuente de datos:

Excel / CSV

Google BigQuery

SQL Server

Snowflake

Amazon Redshift

Oracle

Tableau Extract (.hyper)

JSON, Parquet, etc.

Tableau mostrará una vista llamada Source o Data Source.

Selecciona:

Tablas

Uniones (JOIN)

Combinaciones (BLEND)

Uniones lógicas (relationships)

### Tipos de Conexión

Live Connection (en vivo): datos en tiempo real.

Extract (extracción): copia optimizada para análisis más rápido.

## 4. Crear tu Primer Dashboard
4.1 Terminología básica
Término	Significado
Dimensiones	Campos categóricos (categorías, fechas, nombres).
Medidas	Valores numéricos (ventas, costos, cantidades).
Shelves	Áreas donde arrastras campos (Rows, Columns, Filters).
Marks	Control de color, tamaño, etiquetas y nivel de detalle.
Worksheet	Hoja donde creas un gráfico.
Dashboard	Conjunto de gráficos y elementos interactivos.

## 4.2 Crear una visualización

Arrastra una Dimensión a Columns.

Arrastra una Medida a Rows.

Tableau generará un gráfico automáticamente.

Cambia el tipo de gráfico con el menú Show Me.

Tipos de gráficos comunes:

Barras

Líneas

Mapas geográficos

Gráficos de dispersión

Heatmaps

KPI cards

Árboles (treemaps)

## 5. Filtros, Parámetros y Acciones

### 5.1 Filtros

Puedes arrastrar cualquier campo a la sección Filters.

Tipos:

Filtros de dimensión (categorías)

Filtros de medida (rangos numéricos)

Filtros de fecha

Filtros contextuales

### 5.2 Parámetros

Un parámetro permite que el usuario seleccione un valor para cambiar:

Cálculos

Escalas

Campos usados en visualizaciones

Ejemplo: seleccionar región, escenario o umbral.

### 5.3 Acciones

Permiten crear interacción:

Acción de filtro

Acción de resaltar

Acción de navegación

Acción de URL

## 6. Cálculos en Tableau

Tableau permite crear campos calculados usando lógica similar a Excel.

Ejemplos:
```
IF [Ventas] > 10000 THEN "Alto" ELSE "Bajo" END`
```


Porcentaje del total:

```
[Sales] / TOTAL([Sales])
```

Cálculo por ventana (table calculation):

```
RUNNING_SUM(SUM([Ventas]))
```
Tipos de cálculos:

Básicos: IF, CASE, operadores — cálculo fila a fila

```
Nivel de detalle (LOD): { FIXED … }, { INCLUDE … }, { EXCLUDE …}

```

Table Calculations: cálculos sobre la visualización, no sobre los datos

Agregaciones: SUM, AVG, COUNT, MIN, MAX

Ejemplo LOD:

```
{ FIXED [País] : SUM([Ventas]) }

```

## 7. Construir un Dashboard

Haz clic en New Dashboard.

Arrastra tus Worksheets.

Organiza elementos:

Contenedores horizontales

Contenedores verticales

Imágenes

Texto

Filtros visibles

Buenas prácticas:

Mantén coherencia de colores.

Agrupa filtros.

Usa contenedores para mantener orden.

Evita usar demasiados gráficos.

Prueba en “Device Preview”.

## 8. Publicar en Tableau Server / Cloud

Archivo → Publish Workbook

Selecciona el proyecto de destino

Configura permisos (quién puede ver el dashboard)

Publica extractos si estás usando datos “Extract”

## 9. Roles de Usuario y Permisos (Tableau Server/Cloud)
Rol	Permiso
Viewer	Solo puede ver dashboards.
Explorer	Puede modificar vistas publicadas.
Author	Puede crear dashboards.
Site Admin	Administración completa.

## 10. Tableau Prep (limpieza y transformación)

Herramienta para ETL ligero:

Limpiar datos

Combinar fuentes

Remover duplicados

Crear columnas

Agregar lógica

Exportar a Tableau Hyper

Flujos típicos:
Input → Cleansing → Join → Aggregate → Output

## 11. Buenas Prácticas Generales

Mantener nombres limpios en campos y tablas.

Documentar fuentes de datos.

Usar extractos para mejorar velocidad.

Evitar cálculos pesados a nivel de fila.

Validar cifras antes de publicar.

Normalizar colores y formatos.

## 12. Recursos recomendados

(Estos son recursos generales, no enlaces directos)

Tutoriales oficiales de Tableau

Tableau Public Gallery (para inspiración)

Comunidad de Tableau

Cursos con casos reales (YouTube, Coursera, Udemy)