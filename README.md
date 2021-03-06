# JavaScript-Ninja
Repositório para estudo do JavaScript

## Variáveis e Tipos de Dados

## Variáveis 
- Nomes simbólicos de valores
- Palavra chave "var"
```js
var myvar;
myvar = 10;
```
## Tipos de Dados
- number
36
- string
'Fábio'
- boolean
true or false
- null
- undefined
- object {}
- array []

## Operadores Aritméticos

+ Adição
- Subtração
* Multiplicação
/ Divisão

## Operadores Aritméticos Abreviados
```
++ (soma = soma + 1)
--  (subtracao = subtracao - 1)
+= (soma = soma + soma) 
-= (subtracao = subtracao - subtracao)
*= (multiplicacao = multiplicacao * multiplicacao)
/= (divisao = divisao / divisao)
```
## Operadores de igualdade / Relacionais
```
== igual a  

!= diferente de  

=== igual a, e do mesmo tipo  

!== diferente de, mas do mesmo tipo  

> Maior que  

< Menor que  

>= Maior ou igual a  

<= Menor ou igual a  
```
## Funções
```js
function funcao(){}
```
- Blocos de código Javascript nomeados, que podem ser invocados usando o operador ()
```js
funcao();
```
- Criam escopo
```js
function soma(a, b){

    a + b;

} 
```
- Podem retornar valores
```js
function soma(a, b){

    return a + b;

}
```
- Podem receber argumentos (ou parâmetros)
```js
function soma (x ,y, z){

    return x + y +z;

}
```
- No literal de função, não é necessário utilizar o ';' no fechamento das chaves. 

## Operadores Lógicos

&& (AND)

- Se duas ou mais condições são verdadeiras

|| (OR)

- Se pelo menos uma condição for verdadeira

! (NOT)

- Inverte o valor



# Operadores Unários

- Quando você utiliza somente ele e outro valor

+ e -

Converte para um número ou NaN
```js
+'3' 

3

+'fabio'

NaN
```
Observação:

Serve para também concatenar (juntar)
```js
'Fá'+'bio'

Fabio

-'3'

-3
```

## Estrutura Léxica

- Case Sensitive

```js
var animal = 'cachorro';
var Animal = 'macaco';

animal //'cachorro'
Animal //'macaco'

animal !== Animal
true
```

## Comentários
```
De linha - //
De bloco - /* */
```
## Literais
```js
12

1.2

'ninja'

"ninja"

true

null

{a: 1}

[1, 2]
```
## Identificadores

_ ou $

letras de a a z

letras de A a Z

dígitos 0 a 9   


Pode utilizar qualquer carácter Unicode
- Mas NÃO deve !

## Palavras Reservadas

- break

- case

- catch

- class

- const 

- if

- for

- typeof

- var 

...  

<https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Lexical_grammar#Keywords>

## Instruções Condicionais

## if (Se)
```js
var a = 12;

var b = 10;

if(a > b){

    return "A variável " + a + " é maior!";

}     
```
## else (Senão)
```js
var a = 10;

var b = 12;



if(a > b){

    return "É maior!";

}else{

    return "É menor!";

}
```

## else if (Senão Se)
```js
var a = 10;

var b = 10;

if(a > b){

    return "É maior!";

}else if (a < b){

    return "É menor!";

}else if(a === b){

    return "É igual!";

}else{

    return null;

}
```

## Tipos

- Tipos Primitivos

- Tipos Objeto

## Tipos Primitivos

- number

- string

- boolean

- null e undefined

## Tipos Objeto

- Todos os outros

## Objeto

- Conjunto de Propriedades {nome: valor}
```js
var pessoa = {
    nome: 'Fábio',
    sobrenome: 'Gonçalves',
    sexo: 'Masculino',
    idade: 36,
    altura: 1.75,
    peso: 88,
    andando: false,
    caminhouQuantosMetros: 0
}
```
## Métodos de Objeto

- Sintaxe:
```js
var objeto = { propriedade: 'valor', metodo: function(){} };
```

- Recebe uma função
```js
pessoa.fazerAniversario = function(){
    pessoa.idade++;
}
```
- Invoca o metodo
```js
pessoa.fazerAniversario();
```
# Truthy e Falsy

- Testa se o retorno de um valor é booleano
```js
var teste;

if(1){ teste = true; } else { teste = false; }

true

if(1){ teste = true; } else { teste = false; }

false
```
## Falsy

- undefined

- null

- NaN

- 0

- -0

- ''

- ""
```js
if(undefined){ teste = true; } else { teste = false; }

if(null){ teste = true; } else { teste = false; }

if(NaN){ teste = true; } else { teste = false; }

if(0){ teste = true; } else { teste = false; }

if(-0){ teste = true; } else { teste = false; }

if(''){ teste = true; } else { teste = false; }

if(""){ teste = true; } else { teste = false; }
```

## Truthy

- Todos os outros valores

## Truthy e Falsy

### Descobrir a representação booleana: !!
```js
!!true

!!'fabio'

!!0

!!false

!!1

!!''

!!""

!!undefined

!!null

!!NaN
```

## Condicional Ternário
```js
condição ? true : false;

1 === 2 ? true : false;

var pessoa = { sexo: 'Masculino' };
var sexo;
var sexo = pessoa.sexo === 'Feminino' ? 'a' : 'o';

sexo

'o'
```

## Escopo de Variáveis

- Global (Quando é declarada fora da função) 

- Local (Quando é declarada dentro da função)

## function cria escopo local

- Quando é criado a variável dentro da função a mesma fica visível dentro da mesma

## Variável Global

- Fica visível para acessar dentro de funções e blocos de código.

### IMPORTANTE: Sempre utilize var para declarar uma variável.

Pois senão o Javascript interpreta como uma variável global. 

Exemplo:
```js
function newFunction(){

    newVar = 'Variável Global';

    return newVar;

}

newVar

undefined

newFunction(); // Quando chamar a função, ele irá criar a variável como Global porque não foi definido com a palavra var. 

'Variável Global'

newVar

'Variável Global'
```
### O garbage Colector não será capaz de excluir a variável Global, então isso pode consumir recurso da sua máquina. ##

#### Dicas para utilizar o Navegador e console do Node

#### No navegador: Em inspecionar na aba console.

- Quando escrever o código Javascript para testar, se precisar pular uma linha tem que pressionar o botão shift + enter.

#### No console do Node

- Quando precisar pular uma linha basta ter um bloco de código e pressionar enter que irá pular uma linha.

## Retorno de Funções com Arrays e Objetos
- Além dos tipos primitivos
- Pode retornar array []
- Pode retornar objeto {}

## Pode utilizar anotação de Arrays com Objetos
```js
var arr = [1, 2, 3];
var arr2 = {
    '0': 1,
    '1': 2,
    '2': 3
};

arr[0];
arr2['0'];

```
## Parâmetros de Funções como Arrays e Objetos 

```js
var myArray = ['Fábio', 36, true, {a: 1}, function(){}];

function myFunction(array){
	return array;
}

console.log(myFunction(myArray)[1]);

function twoParam(array, indice){
	return array[indice];
}

var array2 = ['Ninja', 1, true, [1,2,3], {a: NaN}];

console.log(twoParam(array2,0));
console.log(twoParam(array2,1));
console.log(twoParam(array2,2));
console.log(twoParam(array2,3));
console.log(twoParam(array2,4));

function book(bookName){
	var allBooks = {
		'Segredos do Ninja Javascript': {
			quantidadePaginas: 488,
			autor: 'John Resig & Bear Bibeault',
			editora: 'Novatec'
		},
		'Introdução ao HTML5': {
			quantidadePaginas: 220,
			autor: 'Bruce Lawson & Remy Sharp',
			editora: 'Alta Books'
		},
		'Smashing CSS': {
			quantidadePaginas: 283,
			autor: 'Erick A. Meyer',
			editora: 'Bookman'
		}
	};
	
	return !bookName ? allBooks : allBooks[bookName];
}

console.log(book());

var bookName = 'Smashing CSS';
console.log('O livro '+bookName+' tem '+book(bookName).quantidadePaginas+' páginas!');

console.log('O autor do livro '+bookName+' é '+book(bookName).autor+'.');

console.log('O livro '+bookName+' foi publicado pela editora '+book(bookName).editora+'.');
```
## Operador virgula
```js
var a, b = 2, c;

function myFunction(){
    var x = 0;
    return (x += 1, x);
    // return ++x
```

## Estrutura Condicional - Switch

```js
function convertToHex(color){
    var hexa;
    switch(color){
        case 'red':
            hexa = '#FF0000';
            break;
        case 'blue':
            hexa = '#0000FF';
            break;
        case 'yellow':
            hexa = '#FFFF00';
            break;
        case 'green':
            hexa = '#008000';
            break;
        case 'white':
            hexa = '#FFFFFF';
            break;
        default:
            return 'Não temos o equivalente hexadecimal para '+color+'.';
    }
    return 'O hexadecimal para a cor '+color+' é '+hexa+'.'
} 

/*
Tente mostrar o hexadecimal de 8 cores diferentes usando a função criada acima.
*/
console.log(convertToHex('red'));
console.log(convertToHex('blue'));
console.log(convertToHex('yellow'));
console.log(convertToHex('green'));
console.log(convertToHex('white'));
console.log(convertToHex('gray'));
console.log(convertToHex('black'));
console.log(convertToHex('orange'));
```

## Estrutura de Repetição (loop) - While

```js
/*
Utilizando a estrutura de repetição `while`, mostre no console todos os números
pares entre 10 e 20, inclusive esses 2.
*/
console.log( 'Números pares entre 10 e 20:' );
var num = 10;
while(num <= 20){
	num % 2 === 0 ? console.log(num) : '';
	num++;
}

/*
Na mesma ideia do exercício acima: mostre agora os números ímpares.
*/
console.log( 'Números ímpares entre 10 e 20:' );
while(num < 20){
	num % 2 === 1 ? console.log(num) : '';
	num++
}
```

## Operador Módulo %
- Resto de divisão (inteiro)

```js
10 % 2
0
15 % 2
1
```
## Arrays
```js
var arr = ['Fabio', null, true, {bola: 'azul'}];

console.log(arr[0]);
console.log(arr[1]);
console.log(arr[2]);
console.log(arr[3].bola);
```

## Arrays - Propridade - length

```js
var arr = ['Fabio', null, true, {bola: 'azul'}, function(){}];

var qtd = arr.length;

while(qtd > 0){
    console.log(arr[--qtd]);
}

var qtd = arr.length;

while(qtd > 0){
    console.log(arr[--qtd]);
    if(qtd === 3){
        console.log(arr[qtd].bola);
    }
}
```
### Exemplo 2

```js
var array = ['Fabio', 36, true, {cor: 'azul'}, function soma(x, y){return x + y;}];
array.length;

function addItem(param){
	array.push(param);
	return array;
}

addItem(['a', 'b', 'c']);

console.log('O segundo array tem '+array[5].length+' itens.');
```

## Arrays - Método - .push()
- push é empurrar (adicionar)

```js
array.push('Gonçalves');
//Vai adicionar na última posição do array a string 'Gonçalves'
```
### Exemplo:
```js
var arr2 = ['Fabio', null, true, {bola: 'azul'}];

arr2.push({carro: 'BMW'});//push - Empurra na última posição do array.

console.log(arr2);
```
## Estrutura de Repetição (Loop) - for
- for(init; condition; final-expression)

```js
console.log( 'Números pares entre 100 e 120:' );
for(var number = 100; number <= 120; number++){
	number % 2 === 0 ? console.log(number) : '';
}

console.log( 'Números ímpares entre 111 e 125:' );
for(var number = 111; number <= 125; number++){
	number % 2 === 1 ? console.log(number) : '';
}
```
## Funções - A Importância de nomear funções

- Sempre nomear
- Ao invés disso:
```js
var func = function(){   
};
```

- Prefira isso:
```js
var func = function func(){   
};
```
### Porque?
- Facilita o debug (Consegue obter o nome)

- Sem nomear:
```js
var func = function(){   
    return 'hi';
};

func(); //'hi'
func.name; //''
```
- Nomeando:
```js
var func = function func(){   
    return 'hi';
};

func(); //'hi'
func.name; //'func'

function myFunction(){
    return 'function';
}

myFunction(); //'function'
myFunction.name; //myFunction
```

## Indrodução ao Functional Programming

### Funções
- Objetos de primeira classe
- 'Cidadões' de primeira classe
{} <3 function(){}

- Como você usa objetos literais...
```js
var car = {
    brand: 'Chevrolet',
    model: 'Silverado'
};
```

- Você pode criar funções literais!
```js
function sum(x, y){
    return x + y;
}
```

- Como você atribui objetos à variáveis...
```js
var obj ={};
```

- Você pode atribuir funções:
```js
var func = function func(){};
```

- Como você retorna objetos em uma função...
```js
function person(){
    return {
        name: 'Fábio',
        lasName: 'Gonçalves'
    };
}

// ou numa segunda abordagem...

function person(){
    var info = {
        name: 'Fábio',
        lasName: 'Gonçalves'
    };
    return info;
}

console.log(person().name);
console.log(person().lasName);

```

- Você também pode retornar funções!
```js
function adder(x){
    return function(y){
        return x + y;
    };
}

// outra abordagem

function adder(x){
    function addOther(y){
        return x + y;
    }
    return addOther;
}

var add2 = adder(2);
console.log(add2(3)); 
5

console.log(adder(2)(3)); 
5
```

- Como você passa objetos por parâmetros...
```js
var car = {
    color: 'yellow'
};

function getCarColor(mycar){
    return mycar.color;
}

console.log(getCarColor(car));
'yellow'

function showOtherFunction(func){
    return func();
}

showOtherFunction(function(){
    return 'Function JS Ninja!';
});

'Function JS Ninja!'
```

## Função dentro de função é permitido.
- Mas, e o escopo?
```js
function myFunction(){
    function sum(){
        return 1 + 2;
    }
    return sum();
}

console.log(myFunction()); //3
console.log(sum()); // Irá apresentar um erro informando que sum não foi definido.
```

## HOISTING
- Içamento ou Elevação de funções literais

```js
function myFunction(){
    var number1 = 1;
    var number2 = 2;
    return sum(); // teoricamente finaliza aqui mas acontece um hoisting
    function sum(){
        return number1 + number2;
    }
}

console.log(myFunction());

// Acontece isso - um hoisting
function myFunction(){
    function sum(){ //vai elevar a função literal para executar primeiro
        return number1 + number2;
    }
    var number1 = 1;
    var number2 = 2;
    return sum(); 
}


console.log(myFunction());

```
- Içamento ou Elevação de variáveis 
```js
function myFunction(){
    console.log(number1);
    var number1 = 1;
    console.log(number1);
    return '';
}

console.log(myFunction());

// Acontece isso - um hoisting

function myFunction(){
    var number1;
    console.log(number1);
    number1 = 1;
    console.log(number1);
    return '';
}

console.log(myFunction());

```
- Dica: Sempre declarar variáveis no início das funções
- Depois as funções literais
- No final declarar o return

## IIFE - Immediately-invoked function expression

### Função auto-executável

- Execução por invocação

```js
function sum(){
    return 1 + 2;
}

console.log(sum());

var sum2 = function(){
    return 2 + 3;
};

console.log(sum2());

var sum3 = function otherSum(){
    return 5 + 8; 
};

console.log(sum3());
console.log(otherSum()); //otherSum is not defined

```
- Tornar uma expressão de uma função utilizando '()', então pode ser auto-executada 
- Assim cria um escopo local para função
```js
(function(){
    console.log(1 + 2);
})();

```

## Wrapper Objects

- Valores primitivos NÃO são objetos

```js
var name = 'Fábio';

name.length; 
5
```

-Então por que eles têm propriedades?

### Contrutores

- Criam novos objetos

```js
var name = new String('Fábio');
var age = new Number(36);
var ninja = new Boolean(true);
```
- Você não vai criar com os construtores e sim como literais
- O Javascript é uma linguagem de tipagem dinamica.
- O Javascript faz a conversão de tipo sem o new.

### Conversores - sem o new
- Convertem o tipo

```js
var name = String(30);//'30'
var age = Number('150');//150
var ninja = Boolean(0);//false
```

## Como testar tipos de valores?

typeof <operand>

```js
typeof undefined; //'undefined'
typeof function(){}; // 'function'
typeof true; // 'boolean'
typeof 10; //'number'
typeof 'JS Ninja'; //'string'

/* Qualquer outro objeto que não seja function => 'object' */

typeof {}; // 'object'
typeof []; // 'object'
typeof NaN; // 'number'
typeof null; // 'object' ??? - Erro de implementação no JS!
```
- Posso confiar no typeof?
- Somente para valores primitivos

```js
function subtract(num1, num2){
    if(typeof num1 === 'number' && typeof num2 === 'number'){
        return num1 - num2;
    }
    return 'Entre com dois numeros'
}
console.log( subtract(10, 2) );
console.log( subtract('JS', 2) );
console.log( subtract({}, []) );
```
## Laços (Loops) - do / while

```js
var counter = 1;

do {
    console.log( counter++ );
} while(counter < 10); //necessário o ";" no final

```

- Primeiro ele executa a instrução depois faz a verificação da condição, caso seja verdadeira ele volta a executar a instrução caso falso pula fora do bloco. 


## Laços (Loops) - for in
- Percorre propriedades de um objeto

```js
var car = {
    brand: 'WV',
    model: 'Gol',
    year: 2003
}

for( var prop in car){
    console.log( prop );
}
console.log('doors in car?', 'doors' in car);

for(var prop in car){
    console.log( car[prop] );
}
```

## Saltos

- É uma instrunção que você utiliza para pular partes do seu código.

### Saltos - return

- O return somente pode ser utilizado dentro de funções.

```js
function myFunction(){
    var number = 10;
    if( number === 10 ){
        return true;
    }
    var number2 = 5;
    var name = 'Fábio Gonçalves';
    return name + ' ' + number2;
}
console.log( myFunction() );
```

### Saltos - break

```js
var number = 10;
switch( number ){
    case 1: 
        console.log( '1' );
        break;
    case 2: 
        console.log( '2' );
        break;
    case 10: 
        console.log( '10' );
        break;
    default: 
        console.log( 'default' );
}
console.log( 'fim do switch' );
```

- Você pode utilizar o break também fora do switch

```js
for( var i = 0; i < 10; i++ ){
    if( i === 5  ){
        break;
    }
    console.log( i );
}
console.log( 'fim do for' );
```

```js
var arr = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10];
for( var i = 0; i < arr.length; i++ ){
    if( i === 5 ){
        break;
    }
    console.log( i );
}
console.log( 'fim do for' );
```

### Saltos - continue

```js
var arr = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10];
for( var i = 0; i < arr.length; i++ ){
    if( i === 5 ){
        continue;
    }
    console.log( i );
}
console.log( 'fim do for' );
```

```js
var arr = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10];
for( var i = 0; i < arr.length; i++ ){
    if( i % 2 === 0 ){
        continue;
    }
    console.log( i );
}
console.log( 'fim do for' );
```

```js
var arr = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10];
for( var i = 0; i < arr.length; i++ ){
    if( i % 2 === 1 ){
        continue;
    }
    console.log( i );
}
console.log( 'fim do for' );
```

## Objetos

- Mutáveis
- Manipulados por referência

```js
var obj = {
    prop1: 'prop1',
    prop2: 'prop2'
};

var obj2 = {
    prop1: 'prop1',
    prop2: 'prop2'
};

obj.prop1 = 'propriedade 1'

obj
{ prop1: 'propriedade 1', prop2: 'prop2' }

delete obj.prop1

obj
{ prop2: 'prop2' }

obj.prop1 = 'prop1'

obj
{ prop2: 'prop2', prop1: 'prop1' }

obj2
{ prop1: 'prop1', prop2: 'prop2' }

obj === obj2
false
var objCopy = obj;

objCopy
{ prop2: 'prop2', prop1: 'prop1' }

obj
{ prop2: 'prop2', prop1: 'prop1' }

objCopy === obj
true

objCopy.prop1 = 'propriedade do objeto copy'
objCopy
{ prop2: 'prop2', prop1: 'propriedade do objeto copy' }

obj
{ prop2: 'prop2', prop1: 'propriedade do objeto copy' }

```

### Criando Objetos

- Literais;
- Como construtor (new);
- Com Object.create();

```js
//Literal
var obj = {};
obj
{}

//Com construtor (new)
var newObj = new Object();
newObj
{}

//Com Object.create();
var obj2 = Object.create();
'Object prototype may only be an Object or null: undefined'

```

### Criando Objetos - Object.prototype

- Cada objeto criado em Javascript herda de Object.prototype 

```js
Object.prototype
//{}

```

### Criando Objetos - Object.create();

- Cria um novo objeto
- Esse objeto herda os valores do objeto referência 

### Herança

- Object.create();

```js
var obj = { x: 1, y: 2 };

var obj2 = Object.create(obj);

obj2
{}

obj2.prototype
undefined

obj2.x
1

obj2.y
2

obj.x = 2

obj2.x
2

obj2.x = 'lala'

obj2.x
'lala'

obj.x
2
```

- Como descobrir se as propriedades são do objeto ou foram herdadas
- .hasOwnProperty();

```js
var obj = { x:1, y: 2 };

var obj2 = Object.create( obj );

var obj3 = Object.create( obj2 );

obj
{ x:1, y: 2 }

obj2
{}

obj3
{}

obj2.x = 2

obj2
{ x:2 }

obj3.x
2

//Vamos verificar se as propriedades pertecem ao objeto

obj.hasOwnProperty('x')
true

obj.hasOwnProperty('y')
true

obj2.hasOwnProperty('x')
true

obj2.hasOwnProperty('y') 
false //Foi herdada por isso retornou false

obj3.hasOwnProperty('x')
false //Foi herdada por isso retornou false

obj2.hasOwnProperty('y')
false //Foi herdada por isso retornou false

//Vamos descobrir as propriedades que não são herdadas

for(var prop in obj){
    if( obj.hasOwnProperty( prop ) ){
        console.log(prop);
    }
}
x
y

for(var prop in obj2){
    if( obj2.hasOwnProperty( prop ) ){
        console.log(prop);
    }
}
x

for(var prop in obj3){
    if( obj3.hasOwnProperty( prop ) ){
        console.log(prop);
    }
}
undefined
```

### Criando Objetos - Object.keys(obj)

- Vai retornar um array com as propriedades do objeto

```js
obj
{ x:1, y: 2 }

obj2
{ x:1 }

obj3
{}

Object.keys(obj)
[ 'x', 'y' ]

Object.keys(obj).length
2

```

### Criando Objetos - obj.isPrototypeOf( otherObj )

- Verificar se aquele objeto ele é prototipo de algum outro

```js
obj
{ x:1, y: 2 }

obj2
{ x:1 }

obj3
{}

obj.isPrototypeOf( obj2 ) //obj é prototipo do obj2
true

obj.isPrototypeOf( obj3 ) //obj é prototipo do obj3
true

obj2.isPrototypeOf( obj3) //obj2 é prototipo do obj3
true
```

### Criando Objetos - JSON.stringify( obj )

- Tranforma o objeto no formato JSON
- JSON (Javascript Object Notation)

```js
obj
{ x:1, y: 2 }

JSON.stringify(obj)
'{"x":1,"y":2}'

var str = JSON.stringify(obj);
str
'{"x":1,"y":2}'
```

### Criando Objetos - JSON.parse( str )

- Tranforma o JSON no objeto novamente 
- <https://www.json.org/json-pt.html>

```js
str
'{"x":1,"y":2}'

JSON.parse(str)
{ x:1, y: 2 }

```

## Arrays

- Adiciona e remove itens
- push() e pop()

```js
var arr = [];

arr[0] = 10
arr[1] = 5
arr[2] = 'oito'
arr
[ 10, 5, 'oito' ]
arr[12] = 'doze'
arr
[ 10, 5, 'oito', , , , , , , , , , 'doze' ]

arr[11]
undefined

arr.push('treze') //adiciona no final do array

arr
[ 10, 5, 'oito', , , , , , , , , , 'doze', 'treze' ]

arr.pop() //remove do final do array
'treze'

arr
[ 10, 5, 'oito', , , , , , , , , , 'doze' ]

arr.pop()
'doze'

arr
[ 10, 5, 'oito', , , , , , , , , , ]

var arr = [];
arr.push('arroz');
arr.push('feijao');
arr.push('macarrao');

arr
['arroz', 'feijao', 'macarrao']

var last = arr.pop();
arr
['arroz', 'feijao']

last
'macarrao'

arr.length
2
```

### Arrays - Juntar: join()

```js
arr
['arroz', 'feijao', 'macarrao']

arr.join() //Ao juntar em uma unica string, o separador padrão é a virgula
'arroz,feijao,macarrao'

arr
['arroz', 'feijao', 'macarrao']

arr.join(' ')//Ao juntar o separador é um espaço em branco
'arroz feijao macarrao'

arr.join(', ')//Ao junta fica uma virgula e um espaço em branco
'arroz, feijao, macarrao'

console.log( 'Meu almoço hoje será ', arr.join( ', ' ) );
'Meu almoço hoje será  arroz, feijao, macarrao'
```

### Arrays - Inverter: reverse()

```js
arr
['arroz', 'feijao', 'macarrao']

arr[0]
'arroz'
arr[1]
'feijao'
arr[2]
'macarrao'

//modifica o array e inverte as posições do primeiro para o ultimo
arr.reverse() 
[ 'macarrao', 'feijao', 'arroz' ]

arr.reverse()
[ 'arroz', 'feijao', 'macarrao' ]

```

### Arrays - Ordem alfabetica: sort()

```js
arr
[ 'arroz', 'feijao', 'macarrao', 'lasanha' ]

//modifica o array e coloca em ordem alfabetica
arr.sort()
[ 'arroz', 'feijao', 'lasanha', 'macarrao' ]

arr
[ 'arroz', 'feijao', 'lasanha', 'macarrao' ]
```

### Arrays - Converter em string: toString()
- Converte no formato de string
- Separa os itens por ',' por padrão
- Não modifica o array

```js
var arr = [1, 2, 3, 4];
arr.toString()
'1,2,3,4'
arr
[1, 2, 3, 4]

```

### Arrays - Concatenar: concat()
- Vai concatenar qualquer item ao array
- Não modifica o array

```js
var arr = [1, 2, 3, 4];
arr.concat(5)
[1, 2, 3, 4, 5]
arr
[1, 2, 3, 4]

```

### Arrays - Inserir no inicio do array: unshift()
- Vai adicionar item no inicio do array
- Modifica o array
- Retorna o length do array

```js
var arr = [1, 2, 3, 4];
arr.unshift(0);
5
arr
[0, 1, 2, 3, 4]

```

### Arrays - Remove do inicio do array: shift()
- Vai remover item no inicio do array
- Modifica o array
- Retorna o item removido do array

```js
var arr = [0, 1, 2, 3, 4];
arr.shift()
0
arr
[1, 2, 3, 4]

```

### Arrays - Recorta um trecho do array: slice()
- Retorna um pedaço do array
- Possui dois parametros (origem, destino)
- Não modifica o array

```js
var arr = [1, 2, 3, 4, 5];
arr.slice(1)
[2, 3, 4, 5]
arr
[1, 2, 3, 4, 5]

arr.slice(0, 2)//quero o trecho do indice 0 ao 1 então o destino tem que ser sempre posterior
[1, 2]

arr.slice(1, 4)//quero o trecho do indice 1 ao 3 então o destino tem que ser sempre posterior
[2, 3, 4]

arr
[1, 2, 3, 4, 5]
```

### Arrays - adiciona e remove itens do array: splice()
- Pode adicionar quanto remover itens do array
- Possui três parametros (indice, adiciona/remove elemento, item)
- Modifica o array

```js
var arr = [1, 2, 3, 4, 5];
arr.splice(3)
[4, 5]
arr
[1, 2, 3]

var arr = [1, 2, 3, 4, 5, 6, 7];
arr.splice(1, 3) //apartir de qual indice quero remover '1' e quantos itens quero remover '3'
[2, 3, 4]

arr
[1, 5, 6, 7]

arr.splice(1, 0, 2, 3, 4) //apartir de qual indice quero adicionar '1', quantos itens quero remover '0' e os items (2, 3, 4)
[2, 3, 4]

arr
[1, 2, 3, 4, 5, 6, 7]

```

### Arrays - Laço de repetição: forEach()
- É um laço de repetição parecido com o for
- Recebe por parametro uma função
- Essa função recebe por parametro (item, index, array)
- Esse metodo é mais performático (mais rápido) que o for

```js
var arr = [1, 2, 3, 4, 5, 6, 7];

arr.forEach(function(item, index, array){
    console.log(item , index, array);
});

1 0 [ 1, 2, 3, 4, 5, 6, 7 ]
2 1 [ 1, 2, 3, 4, 5, 6, 7 ]
3 2 [ 1, 2, 3, 4, 5, 6, 7 ]
4 3 [ 1, 2, 3, 4, 5, 6, 7 ]
5 4 [ 1, 2, 3, 4, 5, 6, 7 ]
6 5 [ 1, 2, 3, 4, 5, 6, 7 ]
7 6 [ 1, 2, 3, 4, 5, 6, 7 ]

arr.forEach(function(item){
    console.log(item);
});

1 
2 
3 
4 
5 
6 
7 

var sum = 0;
arr.forEach( function( item ){
    sum += item;
});
console.log( sum );
28

```

### Arrays - : every()
- Ele é um predicado do array
- Ele retorna true ou false

```js
var arr = [ 1, 2, 3, 4, 5, 6, 7 ];
var every = arr.every(function(item){
    console.log( item );
    return item < 5;
});
console.log( every );
```

### Arrays - : some()
- Ele retorna true ou false
- Se pelo menos um item for true ele retorna true

```js
var arr = [ 1, 2, 3, 4, 5, 6, 7 ];
var some = arr.some(function(item){
    return item % 2 === 0;
});
console.log( some );
```

### Arrays - : map()
- Percorre o array e retorna um novo array
- Não modifica o array

```js
var arr = [ 1, 2, 3, 4, 5 ];
var map = arr.map(function(item, index, array){
    return item;
});
console.log( arr, map );

map = arr.map(function(item, index, array){
    return { 'index': index , 'item': item };
});
console.log( map );

// Construindo com forEach

var newArr = [];
arr.forEach(function(item, index, array){
    newArr.push( { index: index, item: item } );
});
console.log( 'newArr:' );
console.log( newArr );
```

### Arrays - : filter()
- Percorre o array e retorna um novo array
- Filtra os itens do array

```js
var arr = [ 1, 2, 3, 4, 5 ];
var filter = arr.filter(function(item, index, array){
    return item > 2;
});
console.log( filter );

//Utilizando map e filter

var arr = [ 1, 2, 3, 4, 5 ];
var map = arr.map(function(item){
    return item + 10;
}).filter(function(item){
    return item > 12;
});
console.log( map );
```