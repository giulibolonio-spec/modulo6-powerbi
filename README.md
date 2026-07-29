# Módulo 6 - Conectividad y Transformación de Datos en Power BI

## Objetivo

Preparar un conjunto de datos para su posterior análisis en Power BI mediante el uso de Power Query, aplicando procesos de limpieza, transformación y normalización.

---

## Transformaciones realizadas

Las transformaciones se realizaron en el siguiente orden:

1. Importación del archivo Excel en Power BI Desktop.
2. Renombrado de columnas utilizando nombres descriptivos.
3. Corrección de los tipos de datos.
4. Reemplazo de valores nulos.
5. Eliminación de registros duplicados.
6. Normalización del conjunto de datos mediante la creación de tablas independientes.

---

## Tipos de datos

Se asignaron los siguientes tipos de datos según el contenido de cada columna:

- IDs → Número entero.
- Fechas → Fecha.
- Costos y precios → Moneda.
- Texto descriptivo → Texto.

Esta configuración permite realizar filtros, cálculos y relaciones correctamente dentro del modelo de datos.

---

## Tratamiento de valores nulos

Se aplicaron los siguientes criterios:

- Color → "Sin color".
- Categoría → "Sin categoría".
- Subcategoría → "Sin subcategoría".
- Ubicación → "Sin ubicación".

La columna **fecha_fin_venta** se mantuvo con valores nulos, ya que representan la ausencia de una fecha de finalización de venta y reemplazarlos por un valor ficticio modificaría el significado original de los datos.

---

## Eliminación de duplicados

Se eliminaron registros duplicados utilizando las claves correspondientes de cada entidad:

- Productos → product_id.
- Ubicaciones → combinación de id_ubicacion y ubicacion.
- Categorías → combinación de categoria y subcategoria.

---

## Normalización

Se reorganizó la información en cuatro consultas:

### F_productos

Tabla principal que contiene las claves necesarias para relacionar la información.

Campos:

- product_id
- id_ubicacion
- categoria
- subcategoria

### D_Productos

Contiene la información descriptiva de cada producto.

### D_Ubicaciones

Contiene la información de las ubicaciones disponibles.

### D_Categorias

Contiene la clasificación de categorías y subcategorías.

La normalización reduce la redundancia de información y facilita la construcción del modelo de datos dentro de Power BI.

---

## Herramientas utilizadas

## Autor

Giuliana Bolonio
Curso Data Analytics - Coderhouse
- Power BI Desktop
- Power Query
- Microsoft Excel
