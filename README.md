# Mini Proyecto – Medallion Architecture con Databricks

Este proyecto implementa un pipeline de datos utilizando Azure Databricks, Unity Catalog y la arquitectura Medallion (Bronze, Silver y Gold).

El flujo comienza con la carga de dos archivos CSV (clientes y detalles) almacenados en Azure Storage hacia la capa Bronze, donde los datos se guardan en su forma original.

En la capa Silver se realizan transformaciones y limpieza de datos para estructurar la información y prepararla para análisis.

Finalmente, en la capa Gold se genera una tabla analítica que calcula el ingreso total por cliente, realizando un JOIN entre las tablas de clientes y detalles y sumando el precio mensual de los servicios activos.

También se creó un Job en Databricks que ejecuta automáticamente la creación de las tablas en cada capa siguiendo el flujo Bronze → Silver → Gold.

Tecnologías usadas

Azure Databricks

Unity Catalog

Apache Spark SQL

Delta Lake

Arquitectura Medallion
