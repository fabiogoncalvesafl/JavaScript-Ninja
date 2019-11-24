# JavaScript-Ninja
Repositorio para estudo do JavaScript

## Dicas e orientações sobre JavaScript - Ninja

## Variáveis e Tipos de Dados

### Variáveis 
- Nomes simbólicos de valores
- Palavra chave "var"
```js
var myvar;
myvar = 10;
```
### Tipos de Dados
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

### Operadores Aritméticos

 + Adição
 - Subtração
 * Multiplicação
 / Divisão

### Operadores Aritméticos Abreviados

 ++ (soma = soma + 1)
 --  (subtracao = subtracao - 1)
 += (soma = soma + soma) 
 -= (subtracao = subtracao - subtracao)
 *= (multiplicacao = multiplicacao * multiplicacao)
 /= (divisao = divisao / divisao)

### Operadores de igualdade / Relacionais

 == igual a

 != diferente de

 === igual a, e do mesmo tipo

 !== diferente de, mas do mesmo tipo



 > Maior que

 < Menor que

 >= Maior ou igual a

 <= Menor ou igual a



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

### Operadores Lógicos



 && (AND)

- Se duas ou mais condições são verdadeiras

 || (OR)

- Se pelo menos uma condição for verdadeira

 ! (NOT)

- Inverte o valor



### Operadores Unários

- Quando você utiliza somente ele e outro valor

 + e -

- Converte para um número ou NaN
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

### if
```js
var a = 12;

var b = 10;

if(a > b){

    return "A variável " + a + " é maior!";

}     
```
### else 
```js
var a = 10;

var b = 12;

if(a > b){

    return "É maior!";

}else{

    return "É menor!";

}
```

### else if
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

## Truthy e Falsy

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
### O garbage Colector não será capaz de excluir a variável Global, então isso pode consumir recurso da sua máquina.

### Dicas para utilizar o Navegador e console do Node ###

#### No navegador: Em inspecionar na aba console.

- Quando escrever o código Javascript para testar, se precisar pular uma linha tem que pressionar o botão shift + enter.

#### No console do Node

- Quando precisar pular uma linha basta ter um bloco de código e pressionar enter que irá pular uma linha.
