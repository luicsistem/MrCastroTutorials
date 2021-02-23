# JAVASCRIPT

Es el lenguaje de programación con el cual podras ser el rey , un full stack. 
![Javascript](https://bit.ly/2LM4xbe)

## FUNCIONES
Es  un conjunto de instrucciones que realiza una tarea o calcula un valor

### Sintaxis

```javascript
function functionName(parameters) {
    // codigo a ejecutar
}

```
## Function Declaration
Las funciones declaradas no se ejecutan inmediatamente. Se "guardan para un uso posterior" 

y se ejecutarán más tarde, cuando se invoquen .

```javascript
function sumar(a, b) {
    return a + b;
}
```
## Function Expression
la función se crea y se asigna a la variable de forma explícita, como cualquier otro valor.

La función  es en realidad una función anónima. Siempre se invocan (se llaman) utilizando

 el nombre de la variable.

```javascript
const restar =function (a, b) {
    return a - b;
};
// Invocar
restar(10,4)  // --> 6

```


## OBJETOS 
Un objeto es una colección de propiedades, y una propiedad es una asociación entre un nombre (o clave) y un valor.

## Sintaxis
```javascript
// object literal 
const ecommerce = {
    name: 'woocommerce',
    option: 'free'
}

// otra forma de crear un objeto
const obj = new Object();
obj.name = 'shopify';
obj.option = 'paid';
console.log(obj); // {name: "shopify", option : "paid"}
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
## Destructuring de objetos
Podemos extraer aquella propiedad del objeto que queramos y asiganarlas a las varaibles que definamos.

```javascript
const user = {
    name: 'mr castro',
    age: 33
}

// desestructurando
const {name, age } = user;
console.log(name); // mr castro
console.log(age); // 33
```

## Destructuring de objetos anidados

```javascript
const product = {
    name: 'laptop',
    price: 3200,
    available: true,
    dataSheet : {
        model: '15-cw108la',
        weight: '1,8 kg'
         }
}

const {name, dataSheet: { model, weight }} = product;
console.log(model); // 15-cw108la

// forma antigua de acceder
console.log(product.dataSheet.model); // 15-cw108la

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

console.log(friends[0]) // -->  paolo
console.log(numbers[2][0]) // -->  3
```
## Agregar nuevos valores a un array

```javascript
const products = ['tablet', 'laptop', 'printer'];
// agregar al final del arreglo
products.push('camera');
console.log(products); // -->  ["tablet", "laptop", "printer", "camera"]

// agregar al inicio del arreglo
products.unshift('tv'); // -->  ["tv", "tablet", "laptop", "printer", "camera"]

// otra forma 
products[0] = 'nuevo producto';
console.log(products);  
 // ["nuevo producto", "tablet", "laptop", "printer", "camera"]

products[5] = 'radio'; 
console.log(products);  
// ["nuevo producto", "tablet", "laptop", "printer", "camera", "radio"]
```
## Eliminar valores de un array
```javascript
const products = ["tv", "tablet", "laptop", "printer", "camera"];

// elimina el ultimo  elemento del arreglo
products.pop();
console.log(products); // -->  ["tv", "tablet", "laptop", "printer"]

// elimina el 1er elmento del arreglo
products.shift();
console.log(products); // -->  ["tablet", "laptop", "printer"]

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
La sintaxis de desestructuración es una expresión de JavaScript que permite desempacar valores de 
arreglos o propiedades de objetos en distintas variables.
```javascript
const numbers = [10,20,30,40];
const [first, second, ,fourth ]= numbers;
console.log(first); // --> 10
console.log(fourth); // --> 40

```

## foreach() 
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
El método map() crea un nuevo array con los resultados de la llamada a la función 

indicada aplicados a cada uno de sus elementos.

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
## ARRAY METHODS

## filter()

El método filter() crea un nuevo array con todos los elementos que cumplan 

la condición implementada por la función dada.

```javascript
const cart = [
    {name: 'short' , price: 40},
    {name: 'jean' , price: 70},
    {name: 'shoes' , price: 120},
    {name: 'watch' , price: 150}
]
// traer los productos que cuesten mas de 100
const result = cart.filter( prod => prod.price > 100);
console.log(result);
/*
 [
    {name: 'shoes' , price: 120},
    {name: 'watch' , price: 150}
]
*/
```
## find()
El método find() devuelve el valor del primer elemento del array que cumple

la función de prueba proporcionada.


```javascript
// trae el producto jean del array de cart 
const result = cart.find( prod => prod.name === 'jean');
console.log(result);
//  {name: 'jean' , price: 70}

```
## reduce()

El método reduce() ejecuta una función reductora sobre cada elemento de un array,

devolviendo como resultado un único valor.


```javascript
const carrito = [
    {name: 'pisco' , price: 50},
    {name: 'wisky' , price: 60},
    {name: 'vodka' , price: 40} 
]
// cuanto es el total a pagar del carrito de compras
const resultado = carrito.reduce((acum, prod) => acum + prod.price, 0);
console.log(`El total es : ${resultado} dolares`);
//   El total es : 150 dolares

```

```javascript

```