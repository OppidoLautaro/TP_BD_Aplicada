README – TP Base de Datos Aplicada
Data Warehouse – Wide World Importers (DW_WideWorldImporters)

1. Objetivo del trabajo
El propósito del trabajo práctico es diseñar, construir y cargar un Data Warehouse basado en la base transaccional WideWorldImporters. 
Se debe implementar un modelo en estrella, construir un ETL para poblar las tablas dimensionales y de hechos, y crear un cubo OLAP para análisis multidimensional.


2. Diseño del Modelo en Estrella
Tabla de Hechos:
- FactSales

Tablas Dimensionales:
- DimProduct
- DimCustomer
- DimEmployee
- DimDate
- DimPaymentMethod

3. Creación de Tablas del DW
Se configuraron PK con IDENTITY en cada dimensión y FactSales. Se definieron tipos de datos adecuados y FKs correspondientes.

4. Preparación de la Capa ETL (SSIS)
En Visual Studio 2022:
- Se creó un proyecto SSIS.
- Se configuraron conexiones a WideWorldImporters (origen) y DW_WideWorldImporters (destino).
- Se implementaron Data Flows para cargar cada dimensión y FactSales.
- Se ejecutó el ETL sin errores.

5. Carga de Datos en el DW
Tras ejecutar el ETL, se verificaron los datos con consultas para asegurar la correcta carga.


6. Creación del Cubo OLAP (SSAS Multidimensional)
- Se creó un proyecto Multidimensional.
- Se añadió un Data Source.
- Se armó el cubo con FactSales como tabla de hechos.
- Se generaron dimensiones automáticamente.

7. Uso en Power BI
Power BI puede conectarse directamente al DW:
Servidor: .
Base: DW_WideWorldImporters

