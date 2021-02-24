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

### Modificar Nombre de una tabla

FALTA



### Actualizar Registros
Vamos agregar un registro a la columna description.
```sql
-- 
UPDATE products 
SET description = 'nueva descripcion'
WHERE prodId = 1;
```

### Borrar Base de Datos

```sql
DROP DATABASE prueba;
```
### Borrar Tabla 

```sql
DROP TABLE tablaPrueba;
```

```sql

```
