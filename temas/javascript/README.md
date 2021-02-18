# JAVASCRIPT

Es el lenguaje de programación con el cual podras ser el rey , un full stack. 
![Javascript](https://bit.ly/2LM4xbe)

## OBJETOS 
Un objeto es una colección de propiedades, y una propiedad es una asociación entre un nombre (o clave) y un valor.

## Sintaxis
```javascript
// object literal 
const ecommerce = {
    name: 'woocommerce',
    opcion: 'free'
}

// otra forma de crear un objeto
const obj = new Object();
obj.name = 'shopify';
obj.opcion = 'paga';
console.log(obj); // {name: "shopify", opcion: "paga"}
```
## Acceder a los valores de un objeto
```javascript
 const startup = {
     name: 'airbnb',
     industry: 'commerce'
 };

 // 1ra forma con la opcion de .
  console.log(startup.name); // --> airbnb

  // 2da forma con []
   console.log(startup['industry']); // --> commerce
```
## Agregar nuevas propiedades al objeto
```javascript
    startup.imagen = "imagen.jpg";
    console.log(startup) 
    // {name: "airbnb", industry: "commerce", imagen: "imagen.jpg"}

```

## borrar propiedades del objeto

```javascript
    delete startup.name;
    console.log(startup);  // {industry: "commerce", imagen: "imagen.jpg"}

```

```javascript

```



--- 

## ARREGLOS (array)
Un array es una lista ordenada de valores a los que te refieres con un nombre y un índice.

```javascript

const fruits = ['mango', 'banana'];
const arr = new Array(1, 2, 3);
```
## Acceder a valores de un array
```javascript

const friends = ['paolo', 'gustavo', 'jhosep'];
const numbers = [33, 22 , [3,4,5]];

console.log(friends[0]) // paolo
console.log(numbers[2][0]) // 3
```
## Agregar y eliminar nuevos valores a un array

```javascript
const products = ['tablet', 'laptop', 'printer'];
// agregar al final del arreglo
products.push('camera');
console.log(products); // --> (4) ["tablet", "laptop", "printer", "camera"]

// agregar al inicio del arreglo
products.unshift('tv'); // --> (5) ["tv", "tablet", "laptop", "printer", "camera"]

// elimina el ultimo  elemento el arreglo
products.pop();
console.log(products); // --> 4) ["tv", "tablet", "laptop", "printer"]

// elimina el 1er elmento del arreglo
products.shift();
console.log(products); // --> (3) ["tablet", "laptop", "printer"]

// eliminar cualquier elemento
products.splice(1, 1);
console.log(products); // ["tablet", "printer"]

```
## Recorrer un array

```javascript
const spirits = ['pisco', 'wisky', 'vodka'];
for(let i = 0; i < spirits.length ; i ++) {
    console.log(spirits[i]);
};
// pisco
// wisky
// vodka
```

## Spread Operator ( ES6 ) 
El operador de propagación  permite que una expresión sea expandida en situaciones donde se 
esperan múltiples argumentos (llamadas a funciones) o múltiples elementos (arrays literales).
```javascript
// array literals
const arr = [1,2,3];
const spred = [...arr, 4, 5];
console.log(spred); // --> [1, 2, 3, 4, 5]
```
## Destructuring de arrays
La sintaxis de desestructuración es una expresión de JavaScript que permite desempacar valores de arreglos
o propiedades de objetos en distintas variables.
```javascript
const numbers = [10,20,30,40];
const [first, second, ,fourth ]= numbers;
console.log(first); // --> 10
console.log(fourth); // --> 40

```
## foreach() --  array methods
El método forEach() ejecuta la función indicada una vez por cada elemento del array.

```javascript
const startups = [
    {name: 'airbnb', industry: 'commerce'},
    {name: 'wish', industry: 'consumer '},
    {name: 'spaceX', industry: 'science'}
];
startups.forEach(startup => {
    console.log(`${startup.name} - Industry: ${startup.industry}`)
    
});
// airbnb - Industry: commerce
// wish - Industry: consumer 
// spaceX - Industry: science

const numbers = [30,50];
numbers.forEach(function(n) {
    console.log(n * 2)
});
// 60
// 100


```
## map()
El método map() crea un nuevo array con los resultados de la llamada a la función indicada aplicados 
a cada uno de sus elementos.

```javascript
// tomamos como referencia el array de startups anterior
const nuevoArreglo = startups.map(st => {
    return `${st.name} - ${st.industry}`;
})

console.log(nuevoArreglo);
// ["airbnb - commerce", "wish - consumer ", "spaceX - science"]

const numbers = [11,80];
const nuevoArr = numbers.map(function(n) {
    return n * 3;
});
console.log(nuevoArr); // [33, 240]



```


```javascript

```