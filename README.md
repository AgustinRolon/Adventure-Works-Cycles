# 🚴 Visualizando el Rendimiento de AWC en Power BI

## 📌 Introducción

Este proyecto, llamado **“Visualizando el Rendimiento de AWC en Power BI”**, tiene como objetivo realizar un análisis sistematizado de las ventas de **Adventure Works Cycles (AWC)**, una empresa multinacional de fabricación que produce y distribuye bicicletas, piezas y accesorios en Norteamérica, Europa y Asia. Actualmente, la empresa carece de indicadores adecuados para la toma de decisiones eficiente.

Para satisfacer esta necesidad, se desarrolló un informe integral en Power BI que proporciona un análisis detallado y visualizaciones interactivas sobre el rendimiento de ventas de AWC. Este análisis permite a los usuarios comprender los factores que afectan las ventas, los costos y la rentabilidad, facilitando la toma de decisiones estratégicas basadas en datos.

## 🛠 Desarrollo del Proyecto

1. **Preparación de la Base de Datos:**
   - Se descargó el archivo `adventure works dw 2019.bak` y se restauró la base de datos en SQL Server.
   - Se conectó la base de datos restaurada en SQL Server a Power BI, incluyendo las siguientes tablas:
     - Dimensiones: `DimProduct`, `DimProductCategory`, `DimProductSubcategory`, `DimDate`, `DimPromotion`, `DimSalesTerritory`, `DimGeography`.
     - Hechos: `FactInternetSales`.

2. **Transformación de Datos:**
   - La tabla `DimCustomer` fue conectada desde un archivo Excel y transformada en Power Query:
     - Eliminación de filas nulas y columnas irrelevantes (`Title`, `Middle Name`, `Name Style`, `Suffix`, etc.).
     - Combinación de columnas (`CountryRegionCode`) en una única columna renombrada como `País`.
   - Combinación de tablas:
     - `DimCustomer` con `DimGeography` para agregar información de ciudad y provincia.
     - `DimProduct` con `DimProductCategory` y `DimProductSubCategory` para mostrar categorías y subcategorías de productos.
   - Adición de columnas personalizadas (`Mes Corto` y `Trimestre`) y deshabilitación de la carga de tablas redundantes.
   - Marcado de `DimDate` como tabla de fechas con `FullDateAlternateKey` como columna de fecha.

3. **Creación de Medidas y Parámetros:**
   - Medidas para responder consultas del cliente, tales como ingresos totales, cantidad vendida, utilidades, COGS, entre otras.
   - Desarrollo de medidas adicionales como ratios de costos operacionales y márgenes de utilidad.
   - Agrupación de medidas en carpetas: Ganancias, Costos, Inteligencia de Tiempo y Otras Medidas.
   - Creación de parámetros de campo y grupos de cálculo para visualizaciones específicas.

4. **Visualización y Dashboard:**
   - Configuración del lienzo con tamaño personalizado (1080x1920).
   - Creación de 3 páginas: portada, reporte financiero general, y detalle del mercado de Estados Unidos.
   - Inclusión de tarjetas informativas, segmentadores de datos (año, categoría, subcategoría) y gráficos para visualizar métricas clave como ingresos, COGS y utilidades.

## 📊 Análisis General del Tablero

El tablero proporciona una visualización clara y concisa de los principales indicadores de rendimiento de AWC, permitiendo a los usuarios segmentar información por año, categoría de producto, y ubicación geográfica.

### 🔍 Detalles del Tablero:

- **Portada:**
  - Logo de la empresa y botones de navegación.
- **Reporte Financiero:**
  - Tarjetas de métricas clave: Ingresos Totales, Clientes, COGS, Órdenes Totales.
  - Gráficos para analizar ingresos, costos y utilidades por diferentes segmentos.
- **Detalle del Mercado de Estados Unidos:**
  - Tabla detallada con métricas por provincia y ciudad, incluyendo márgenes y costos.
  - Gráficos comparativos de COGS y márgenes de utilidad por ciudad.

## 🔍 Insight del Análisis

- Los ingresos aumentaron en 7 millones desde 2011 hasta 2013. Existe un crecimiento constante en las ventas, siendo que de 2012 a 2013 el crecimiento en ventas fue de un 174%.
- Los costos se mantuvieron estables en torno a 3-4 millones durante los 3 años.
- El margen bruto en términos generales es de 41,12%, indicando que la empresa está generando ganancias antes de considerar los gastos adicionales.
- El margen neto expresa que el 30% de los ingresos se destinan como ganancias netas después de considerar todos los gastos.
- El Ratio Costo Operacional es del 61%, siendo que por cada dólar generado se gastan 0.60 en gastos operativos.
- La categoría más vendida y más rentable es la de Bikes, ya que es la única categoría que se vende desde 2011.
- La subcategoría más vendida y más rentable es la Road Bikes, ya que es la única subcategoría que se vende desde 2011.
- Estados Unidos es el país con mayores clientes, ventas y ganancias.
- Desde 2011 al 2013 los clientes aumentaron un 466%, siendo el año 2013 el de mayor crecimiento de clientes.
- En Estados Unidos, California es el Estado con mayores ventas y Bellflower es la ciudad con mayores ventas y ganancias.

## 📈 Conclusión

Este proyecto facilita la toma de decisiones estratégicas basada en datos para Adventure Works Cycles, proporcionando insights clave sobre ventas, costos y rentabilidad a través de un dashboard interactivo en Power BI. El análisis detallado de métricas financieras y la capacidad de segmentación avanzada permiten a los usuarios explorar y entender mejor el rendimiento de la empresa.

## 🛠 Tecnologías Utilizadas

- **Power BI** para visualización y creación de dashboards.
- **SQL Server** para la gestión de la base de datos.
- **Power Query** para la transformación de datos.

<p align="left">
  <a href="https://powerbi.microsoft.com/en-us/" target="_blank">
    <img src="https://profilinator.rishav.dev/skills-assets/powerbi.png" alt="Power Bi" height="50" style="margin: 10px"/>
  </a>
  <a href="https://www.microsoft.com/en-us/sql-server" target="_blank" rel="noreferrer">
    <img src="https://www.svgrepo.com/show/303229/microsoft-sql-server-logo.svg" alt="mssql" width="40" height="40" style="margin: 10px"/>
  </a>
</p>


## 🚀 Cómo Empezar

1. Restaurar la base de datos `AdventureWorksDW2019.bak` en SQL Server. (https://learn.microsoft.com/es-es/sql/samples/adventureworks-install-configure?view=sql-server-ver16&tabs=ssms)
2. Conectar SQL Server y el archivo Excel a Power BI.
3. Aplicar las transformaciones y medidas descritas en este README.
4. Configurar el lienzo y construir el dashboard como se detalla en la sección de Desarrollo del Proyecto.

## 👤 Autor

[Agustin Rolon](https://github.com/AgustinRolon)

---

# 💛 Agradecimiento Especial

[![Henry](https://github.com/user-attachments/assets/00eeb5c8-4dcf-4124-ac29-d4ba7b113e6f)](https://www.soyhenry.com)  
[Henry](https://www.soyhenry.com)

