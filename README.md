# Eloquent-JS
Repositorio para estudo do JavaScript

## Valores, Tipos e Operadores
Temos seis tipos básicos de valores no JavaScript: números, strings, booleans, objetos, funções e valores indefinidos.
Em inglês: [number, string, boolean, object, function, undefined]

### Números
Valores do tipo numbers são, previsivelmente, valor numéricos. Em um programa JavaScript, eles são escritos usualmente assim:

13

## Aritmética

### Operadores

Adição (+)
Subtração (-)
Multiplicação (*)
Divisão (/)
Resto (%) - Restante da operação

### Ordem de precedência

Quando operadores aparecem juntos sem parênteses, a ordem que eles vão ser aplicados é determinada pela precedência dos operadores. 
O exemplo mostra que a multiplicação vem antes da adição. / tem a mesma precedência de *. Igualmente para + e -. 
Quando múltiplos operadores com a mesma precedência estão próximos uns aos outros (como em 1 - 2 + 1), eles são aplicados da esquerda para a direita. A precedência deste operador (%) é igual a da multiplicação e divisão.

Estas regras de precedência não é algo que você deva se preocupar. Quando em dúvida, somente adicione parênteses.

## Números Especiais

Existem 3 valores especiais no JavaScript que são considerados números, mas não comportam-se como números normais.

Os dois primeiros são Infinity e -Infinity, que são usados para representar os infinitos positivo e negativo.
NaN significa “not a number” (não é um número).

## Strings

O próximo tipo básico de dado é a string. Strings são usadas para representar texto. 
Elas são escritas delimitando seu conteúdo entre aspas.

"Patch my boat with chewing gum"
'Monkeys wave goodbye'

Quase tudo pode ser colocado entre aspas, e o JavaScript vai fazer um valor de string com isso. Mas alguns caracteres são difíceis. 
Você pode imaginar como colocar aspas entre aspas deve ser difícil. Novas linhas, as coisas que você obtém quando pressiona enter, também não podem ser colocadas entre aspas - a string tem que estar em uma linha única.

Para ser capaz de ter estes caracteres em uma string, a convenção seguinte é usada: Sempre que um barra invertida \ é encontrada dentro do texto entre aspas, isto indica que o caracter depois desta tem um significado especial. 
Uma aspa precedida de uma barra invertida não vai findar a string, mas ser parte dela. Quando um caracter ‘n’ correr depois de uma barra invertida, será interpretado como uma nova linha. Similarmente, um ‘t’ depois da barra invertida significa o caracter tab. 
Veja a string seguinte:

"This is the first line\nAnd this is the second"
O verdadeiro texto contido é:

This is the first line
And this is the second

Existe, obviamente, situações onde você quer uma barra invertida em uma string apenas como uma barra invertida. não um código especial. Se duas barras invertidas estiverem seguidas uma da outra, elas se anulam, e somente uma vai ser deixada no valor da string resultante. Assim é como a string A newline character is written like "\n" can be written:

"A newline character is written like \"\\n\"."

Strings não podem ser divididas, multiplicadas ou subtraídas, mas o operador + pode ser usado nelas. Ele não adiciona, mas concatena - ele cola duas strings unindo-as. A linha seguinte vai produzir a string concatenate:

"con" + "cat" + "e" + "nate"

## Operadores Unários

Nem todos operadores são símbolos. Alguns são palavras escritas. Um exemplo é o operador typeof, que produz uma string com o valor do tipo dado para fornecido para avaliação.

console.log(typeof 4.5) // number
console.log(typeof "x") // string

