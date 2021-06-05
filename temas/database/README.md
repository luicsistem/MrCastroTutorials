# BASE DE DATOS (DATABASE)
Es un conjunto de información almacenado y consultado sistematicamente.


![SQL](https://bit.ly/3aO4xRD)

## Sistemas Gestores de Base de Datos (SGBD)
En inglés DataBase Management System (DBMS).
Son programas que permiten almacenar y posteriormente acceder a los datos
de forma rápida y estructurada.

## TIPOS DE BASE DE DATOS
## Relacionales - SQL
Como MySQL, SQL Server, PostgreSQL/ Oracle.
Su composición está hecha con bases de datos llenas de tablas con filas que 
contienen campos estructurados

## No Relacionales - NO-SQL
Como MongoDB, Redis, Cassandra.

NO-SQL (Not Only SQL). Estas son más flexibles en cuanto a consistencia 
de datos.Son escalables.

***
## SQL
SQL son las siglas de Structured Query Language , lenguaje de 
consulta estructurada.
SQL es un lenguaje de dominio específico utilizado en programación, 
diseñado para administrar, y recuperar información de sistemas de 
gestión de bases de datos relacionales

## BASE DE DATOS SQL

### CREATE DATABASE
La siguiente sentencia SQL crea una base de datos llamada "ecommerce":

```sql
-- En Sql Server y MySQL
CREATE DATABASE ecommerce;
USE ecommerce;

```

### CREATE TABLE
La instrucción CREATE TABLE se utiliza para crear una tabla en una base de datos.

```sql
-- En Sql Server 
CREATE TABLE products (
 prodId int IDENTITY(1,1) PRIMARY KEY,
 prodName varchar(100) NOT NULL,
 price decimal(5,2)  -- no superará los 999.99
);

-- En MySQL
CREATE TABLE produts (
 prodId int AUTO_INCREMENT PRIMARY KEY,
 prodName varchar(100) NOT NULL,
 price decimal(5,2) NOT NULL
);
-- Para el incremento automatico se utiliza la palabra clave
--En  Sql Server IDENTITY  | -- En MySQL AUTO_INCREMENT

| prodId | prodName | price |
----------------------------
|        |          |       |    
```
### Insertando datos
Para insertar un nuevo registro en la tabla "products", NO tendremos que especificar 

un valor para la columna "prodId" (se agregará un valor único automáticamente)
```sql
-- En Sql Server y MySQL
INSERT INTO products (prodName, price) 
VALUES ('Tablet', 300.99);

```
### Agregar Columna nueva  

```sql
-- 
ALTER TABLE products
ADD description TEXT;

| prodId | prodName | price      | description |
---------------------------------------------  
|        |          |            |             |
```
### Modificar Columna de una tabla
Para cambiar el tipo de datos de una columna en una tabla, use la siguiente sintaxis:

```sql
-- En Sql Server
ALTER TABLE products
ALTER COLUMN price int;

-- En MySQL
ALTER TABLE products
MODIFY COLUMN price INT ;
```

### Modificar nombre de la columna de una tabla

```sql
-- En Sql Server , se utiliza un procedimiento almacenado
EXEC sp_rename 'products.price', 'modificado';

-- En MySQL
ALTER TABLE products
CHANGE price  modificado  INT ;


| prodId | prodName | modificado | description |
---------------------------------------------  
|        |          |            |             |

```

### Modificar nombre a una  tabla

```sql
-- En Sql Server , se utiliza un procedimiento almacenado
EXEC sp_rename 'products', 'modiNameTable';

-- En MySQL
RENAME TABLE products 
TO modiNameTable;

-- lo volvemos a modificar el nombre quedando (productos)

```

### Actualizar Registros
Vamos agregar un registro a la columna description.
```sql
-- 
UPDATE productos 
SET description = 'nueva descripcion'
WHERE prodId = 1;
```

### Borrar columna de una Tabla 

```sql
-- 
ALTER TABLE productos 
DROP COLUMN description;

| prodId | prodName | modificado | 
--------------------------------
|        |          |            |            

```
### Borrar todos los registros de una Tabla 

```sql
--
TRUNCATE TABLE productos;
```

### Borrar Tabla 

```sql
--
DROP TABLE productos;
```


### Borrar Base de Datos

```sql
--
DROP DATABASE ecommerce;
```

***

# UN DIA DE TRABAJO DE UN DBA (SQL SERVER) 

![DBA](https://bit.ly/3aSRmz2)

## Herramientas
* Microsoft SQL Server
* Microsoft excel
* Visual Studio Code
* SQL Server Integration Services (SISS)
* SQL Server Reporting Services (SSRS)
* Power BI
* Remoto : VPN como FortiClient

## Tareas del dia
* Restauracion - Backups
* Crear Usuarios , dar permisos.
* Atender Tickes.
* Correr scripts.
* Realizar reportes, etc.

***
## Para los Reportes
lo solicitado los (id) los pasa a un excel que esta concatenado 

con insert.Luego crea una tabla temporal x , para luego realizar 

inner join con las tablas correspondientes.

## SENTENCIAS CONSULTADAS
* GROUP BY, ORDER BY.
* COUNT , SUM, MAX , AVG().
* INNER JOIN.
* LIKE, UPDATE, IN .
* DATEDIFF().
* SELECT TOP(1).
* CASE WHEN - THEN ELSE, etc.

*** 

```sql

```
