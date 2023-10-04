# Informações Básica Sobre JavaScript

## Variaveis e Tipagem

Variável é um espaço reservado pelo sistema para guardar um valor do tipo: Booleano, String, Number, Null, Underfined, Arrey, Object ou Function.
No JavaScript as variáveis são de tipagem dinâmica, isso significa que, ao declarar uma variável não precisa indicar o tipo.

Ex. `var variavel = "valor";` tipo String<br>
Ex. `const variavel = 5;` tipo Number<br>
Ex. `let variavel = false;` tipo booleano<br>

`typeoff()` é um parametro para mostrar o tipo de variavel<br>
Ex.: 
```
console.log(typeof(variavel))
```

Existem 3 modos de declarar as variáveis em JavaScript:

`var` – escopo global e local, pode ter seu valor alterado, se não
tiver um valor inicial será tratada como null;

`let` – escopo local de bloco, pode ter seu valor alterado, se não
tiver um valor inicial será tratada como null;

`const` – escopo local de bloco, somente leitura, o valor inicial é
obrigatório e não pode ser alterado.

## Sinal de Igual

O sinal de igualdade “=“ em JavaScript, significa atribuição.<br>
Ex: 
```
var nome = "meunome"
```
como ler: variável nome recebe o valor meunome;

Para fazermos uma comparação de valores em JavaScript usamos
“==“.<br>
Ex.:como declarar: "0" == 0; <br>
como ler: “0” tem o valor igual a 0? Nesse caso retorna true.

Para fazermos uma comparação de valores e tipos em JavaScript
usamos “===“.<br>
Ex.:como declarar: "0" === 0; <br>
como ler: “0” tem o valor e o tipo idêntico a 0? Nesse caso retorna false

## Operadores aritméticos, relacionais e lógicos
### São tipos de operadores matemáticos com valor numérico:

* `+` adição;<br>
* `-` subtração;<br>
* `*` multiplicação;<br>
* `/` divisão real;<br>
* `%` divisão inteira;<br>
* `**` potenciação;<br>

### São tipos de operadores que consultam a relação entre valores:

* `>` maior que;<br>
* `<` menor que;<br>
* `>`= maior ou igual a;<br>
* `<`= menor ou igual a;<br>

### São tipos de operadores que consultam valores lógicos:

* `&` - “e” – considera que todos os valores sejam true;
* `||` - “ou” – considera que qualquer valor seja true;
* `!` - “não” – inverte o valor de true para false ou vice-versa;

## Vetores e Objetos
Arrays são um tipo de lista, ou matriz de variáveis, onde cada variável possui um índice. Os valores podem ser de vários tipos.

Ex.:
```
let array = [‘string’, 1, true]
```

O array deve ser declarado entre colchetes “[]”, e podem guardar qualquer valor dentro de seus índices: inclusive outros arrays.

Ex.:
```
let array = ['string', 1, true, false, [‘array1], [‘array2’]]
```

### Manipulando Arrays
Ao ser declarado, o Array traz consigo uma série de métodos para
manipulá-lo.

* `forEach()` – itera um array;
* `push()` – add item no final do array;
* `pop()` – remove item no final do array;
* `shift()` – remove item no início do array;
* `unshift()` – add item no início do array;
* `indexOf()` – retorna o índice de um valor;
* `splice()` – remove ou substitui um item pelo índice;
* `slice()` – retorna uma parte de um array existente;

### O que são objetos?
Dados que possuem propriedades e valores que definem suas características. Deve ser declarado entre chaves “{}”.

Ex.: imagine uma xícara azul. Ela tem cor, pode ter vários
tamanhos e funções(quero cafééé). Pode ser declarada assim:<br>

```
var xicara = {
    cor: ‘azul’,
    tamanho: ‘p’,
    funcao: tomarCafe()
}
```
### Manipulando objetos
As propriedades de ojbetos podem ser atribuídas à variáveis, facilitando a manipulação do objeto. Chamamos isso de desestruturação.

Ex.: 
```
var xicara = {cor: ‘azul’, tamanho: ‘p’, funcao: tomarCafe()}
```
Ex. de como acessar o objeto:
```
var cor = xicara.cor;
var tamanho = xicara.tamanho;
var funcao = tomarCafe();
```