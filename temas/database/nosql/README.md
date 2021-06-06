# MONGODB
MongoDB es una base de datos distribuida, basada en documentos y de uso general que ha sido diseñada para desarrolladores de aplicaciones modernas y para la era de la nube. Ninguna otra ofrece un nivel de productividad de uso tan alto.

![SQL](https://bit.ly/3uSNmFl)

## Instalacion en local

[MongoDB Community Server](https://www.mongodb.com/try/download/community) Descargala e instalar.

Se instalara la consola (Shell) , Compas que es la interfaz grafica .
Crear carpetas “data\db” en la raíz C:\

```javascript
C:\data\db
```

[Agregar al Path ](https://www.youtube.com/watch?v=2KMQdqDk9e8) En configuracion avanzada del sistema

## Iniciar el servidor de Mongo DB
```javascript
C:\ >  mongod  
t":{"$date":"2021-06-05T18:58:15.621-05:00"},"s":"I",  "c":"CONTROL",

```
Mongo shell se conecta automáticamente con la instancia de Mongo DB ejecutada en el host y
 el puerto local 27017
## Iniciar Shell de mongo
```javascript
C:\ >  mongo
  ---
    > show dbs

```

## Crear una base de datos
```javascript

    > use mydb

```
## Crear collection
```javascript

    > db.createCollection("users" )

```
## Agregar documentos

```javascript

    > db.users.insertOne( { name: "luis", age: 33, occupation: "engineer"})

```
## Listar 

```javascript

    > db.users.find()
    { "name": "luis", "age": 33, "occupation": "engineer"}

    > db.users.find().pretty()

```

```javascript

    >

```

### Documentos JSON



```javascript
{
  "_id": "5cf0029caff5056591b0ce7d",
  "firstname": "Luis",
  "lastname": "Mr Castro",
  "address": {
    "street": "130  Boston",
    "city": "Las Vegas",
  },
  "hobbies": ["running", "coding", "traveling"]
}
```