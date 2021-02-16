# Javascript

Es el lenguaje de programación con el cual podras ser el rey , un full stack. 
![Javascript](https://bit.ly/2LM4xbe)

## Arreglos (array)
Un array es una lista ordenada de valores a los que te refieres con un nombre y un índice.

```javascript

const fruits = ['mango', 'banana'];
const arr = new Array(1, 2, 3);

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
console.log(products);
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

```


```javascript

```