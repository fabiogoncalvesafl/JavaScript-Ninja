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

- ++ (soma = soma + 1)
- --  (subtracao = subtracao - 1)
- += (soma = soma + soma) 
- -= (subtracao = subtracao - subtracao)
- *= (multiplicacao = multiplicacao * multiplicacao)
- /= (divisao = divisao / divisao)

## Operadores de igualdade / Relacionais

- == igual a  

- != diferente de  

- === igual a, e do mesmo tipo  

- !== diferente de, mas do mesmo tipo  

-  > Maior que  

-  < Menor que  

- >= Maior ou igual a  

- <= Menor ou igual a  

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

## Comentários

- De linha - //

- De bloco - /* */

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

qualquer carácter Unicode

## Palavras Reservadas

- break

- case

- catch

- if

- for

- typeof

- var 

...

## Instruções Condicionais

## if
```js
var a = 12;

var b = 10;

if(a > b){

    return "A variável " + a + " é maior!";

}     
```
## else 
```js
var a = 10;

var b = 12;



if(a > b){

    return "É maior!";

}else{

    return "É menor!";

}
```

## else if
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

var sexo = 'Masculino';

var sexo = sexo === 'Feminino' ? 'a' : 'o';

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

## Arrays - Propridade - length

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
