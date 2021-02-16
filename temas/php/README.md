# PHP

* PHP es un lenguaje de programacion, de codigo abierto.

* 80%  de los sitios web del mundo están hechos en PHP.

![PHP](https://bit.ly/2LOuGGw)

## Herramientas

* [Laragon](https://laragon.org/download/ ) ó  [Xammp](https://www.apachefriends.org/es/download.html) 
Entornos de desarrollo , stack necesario para trabajar con PHP (Apache + PHP + Mysql).
* [Composer](https://getcomposer.org/) Es un gestor de dependencias para PHP.
* [Visual Studio Code](https://code.visualstudio.com/) Editor de codigo.

## Sintaxis
```php
<?php

echo "Hola emprendedor";
echo "<br>";
var_dump("Hello Brother"); // nos da mayor información.

```
## Variables

```php
<?php
$name = "Mr Castro";
echo $name;
```
## Tipos de datos

```php
<?php
// enteros
$number = 300;
echo "<pre>";
var_dump($number);
echo "</pre>";

// floats
$float = 99.99;

// string
$name = "Luis";

// Boolean
$single = true;

// arreglos
$array = [];

```
## Numeros y Operadores

```php
<?php
$number1 = 80;
$number2 = 20;
// suma
echo $number1 + $number2;     // -->  100

// resta
echo $number1 - $number2;     // -->  60

// multiplicar
echo $number1 * $number2;     // -->  1600

// dividir
echo $number1 + $number2;     // -->  4
```
## Operadores
```php
<?php
// mayor >  , menor <
$num1 = 10;
$num2 = 20;
$num3 = '10';

//igualdad 
var_dump($num1 == $num3);    // --> true

// igualdad estricta
var_dump($num1 === $num3);    // --> false


```
## Incrementos 
```php
<?php
$number1 = 7 ;
$number1++;
echo $number1; // --> 8

$number2 = 10;
$number2 += 5;
echo $number2;  // --> 15

```

## Funciones para Strings
```php
<?php
$name = "Mr Castro";

// extension de un string
echo strlen($name);  // --> 9

// eliminar espacios en blanco
$email = 'mail@mail.com  ';
$text = trim($email);

// convertir a mayusculas
echo strtoupper($name);

// convertir a minusculas
echo strtolower($name);

// donde se podria usar estas funciones
$mail1 = "correo@correo.com";
$mail2 = "Correo@correo.com";

var_dump(strtolower($mail1) === strtolower($mail2));  // --> bool(true)

// reemplazar
$name = 'Luis alfredo';
echo str_replace('Luis', 'L', $name);  // --> L alfredo

// concatenar

$lenguaje = 'PHP';
echo $lenguaje." es un lenguaje interpretado"; //  --> PHP es un lenguaje interpretado

echo "{$lenguaje} es de codigo abierto"; // --> PHP es de codigo abierto
```

## Arreglos

```php
<?php
$carrito = ['monitor', 'teclado', 'mouse'];
// util para ver los contenidos de un array
echo "<pre>";
var_dump($carrito);
echo "</pre>";

// acceder a un elemento de un array
echo $carrito[1]; // --> teclado

// añadir un elemento al array
array_push($carrito, 'microfono');

// añadir al inicio
array_unshift($carrito, 'smartTv');

// otra forma de crear arreglos
$skills = array('proactivo', 'resilente', 'creativo');
var_dump($skills);





```
## Arreglo asociativo

```php 
<?php

$product = [
    'name' => 'labtop',
    'precio' => 2300,
    'informacion' => [
        'hecho' => 'china'
    ]
];
var_dump($product);

echo $product['name']; // --> labtop
echo $product['informacion']['hecho']; // --> china

// insertar un nuevo valor
$product['id'] = 33;

```

## Funciones de manejo de array
**empty** — Determina si un array está vacío
```php
<?php
$countries = [];
$countries2 = array();
$countries3 = ['Perú', 'Brazil', 'USA'];
var_dump(empty($countries)); // --> bool(true)
var_dump(empty($countries2)); // --> bool(true)
var_dump(empty($countries3)); // --> bool(false)


```
**isset** — Determina si un array esta creado o definido 
```php
<?php
$countries = [];
$countries2 = ['Perú', 'Brazil', 'USA'];
var_dump(isset($countries)); // --> bool(true)
var_dump(isset($countries5)); // --> bool(false)

// tambien reviza si una propiedad existe
$cliente = [
    'name' => 'luis',
    'saldo' => 300
];
var_dump(isset($cliente['id'])); // --> bool(false)
var_dump(isset($cliente['name']));// --> bool(true)

```
**in_array** — Comprueba si un valor existe en un array
```php
<?php

$os = array("Mac", "Windows", "Linux");
var_dump(in_array('Mac', $os)); // --> bool(true)
var_dump(in_array('NT', $os)); // --> bool(false)


```

**sort** — Ordena un array
```php
<?php

$fruits = ['orange',  'banana', 'mango'];
sort($fruits);
var_dump($fruits);

$cliente = array(
    'saldo' => 500,
    'tipo' => 'Premiun',
    'name' => 'Luis'
);

asort($cliente); // ordena por valores (alfabetico)
ksort($cliente); // ordena por llaves
```
[ksort](https://www.php.net/manual/es/function.ksort.php)  — Ordena un array por clave

[asort](https://www.php.net/manual/es/function.asort.php) - Ordena un array por sus valores