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
* `>=` maior ou igual a;<br>
* `<=` menor ou igual a;<br>

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
## Estruturas condicionais
São instruções para realizar determinadas tarefas a partir de uma condição, seja de decisão ou repetição;

Ex.: Um jogo precisa mudar o placar toda vez que um jogador
marca pontuação;

### Estruturas de decisão
Podemos usar as palavras reservadas “if” para estabelecer uma
condição:
Ex.: 
```
var jogador1 = 0;
var jogador2 = 0;

if (jogador1 > 0) {
    console.log(‘jogador1 marcou ponto’);
}
```
como ler: se o jogador1 tiver valor maior que 0
ele marcou ponto.

No caso de a condição não ser atendida podemos usar o “else” :

Ex.: 
```
var jogador1 = 1;
var jogador2 = 0;

if (jogador1 > 0) {
    console.log(‘jogador1 marcou ponto’);
} else {
    console.log(‘ninguem marcou ponto’);
}
```

Caso haja mais de uma condição usamos o “else if“.

Ex.: 
```
var jogador1 = 1;
var jogador2 = 0;

if (jogador1 > 0) {
    console.log(‘jogador1 marcou ponto’);
} else if (jogador2 > 0) {
    console.log(‘jogador2 marcou ponto’);
} else {
    console.log(‘ninguém marcou ponto);
}
```

Podemos também usar o “if” dentro de um outro “if”, chamamos isso de aninhamento de if’s ou ninho de if’s.
Ex.: 
```
if (jogador1 = -1) {
    if (jogador1 > 0) {
        console.log(‘jogador 1 marcou ponto’);
    } else {
        console.log(‘ninguém marcou ponto’);
    }
} else {
    console.log(‘jogador inválido’);
}
```

Podemos também fazer uma verificação em uma única linha
usando o “if” ternário:

Ex.: 

[condição] ? [instrução1] : [instrução2];

jogador1 > 0 ? console.log(‘marcou ponto’) : console.log(‘não
marcou ponto”);

// lembre de usar a interrogação “?” e dois pontos “:”

```
var jogador1 = 0;
var jogador2 = 0;
var placar; 

jogador1 != -1 && jogador2 != -1 ? console.log("Jogadores validos") : console.log("Jogadores invalido");
```
O “switch/case” funciona como uma estrutura condicional também;

Ex.:
```
switch (${expressao}) {
    case 1:
        ${instrucao};
        break;
    case 2:
        ${instrução};
        break;
    default:
        ${instrução};
}

```
### Laços de repetição
São estruturas condicionais que repetem uma instrução até atingir determinada condição:

* For;
* For/in;
* For/of;
* While;
* Do/while;

#### Laços de repetição For
for ([expressaoInicial]; [condicao]; [incremento]) {
declaracao }

Ex.: 
```
var array = [‘valor1’, ‘valor2’, ‘valor3’, ‘valor4’]

for (let i = 0; i < array.length; i++) {
    console.log(i);
}
```

for ([indice] in [objeto ou array]) {declaracao }

Ex.:
```
var array = [‘valor1’, ‘valor2’, ‘valor3’, ‘valor4’]

for (i in array) {
    console.log(i);
}
```

for ([indice] of [array]) {declaracao}

Ex.:
```
var array = [‘valor1’, ‘valor2’, ‘valor3’, ‘valor4’]

for (i of array) {
    console.log(i);
}
```
#### Laços de repetição While

Ex.: 
```
var a = 0;
while (a < 10) {
    a++;
    console.log(a);
}
```
// como ler: enquanto a variável a for menor que 10 ela
vai receber mais um e imprimir no console.

#### Laços de repetição Do/while
Ex.: 
```
var a = 0;
do {
    a++;
    console.log(a);
} while (a < 10)
```
// como ler: a variável a vai receber mais um e imprimir
no console até que seu valor chegue a 10

## Funções
São blocos de comandos e instruções para a execução de determinadas tarefas:

() – indica que é um objeto do tipo function;
{} – indica que é um bloco de instrução;

Ex.: 
```
function nomeDaFuncao() {
    ${instrucao};
}
nomeDaFuncao();
```
### Funções com parâmetros
As funções podem receber em sua declaração, parâmetros, que servem como variáveis, onde sua atribuição pode ser feita durante a chamada da função:

Ex.: 
```
function nomeDaFuncao(parametro) {
    ${instrucao};
}
nomeDaFuncao(valorDoParametro);
```
### Expressões de Funções
São funções atribuídas à expressões. A nomeação das funções por expressão é opcional:
```
Ex. 1: 
var funcao = function nomeDaFuncao() {
    ${instrucao};
}
```
Ex. 2: 
```
var funcao = function() {

    ${instrucao};
};
```

### Arrow Function
São funções de expressão de sintaxe curta. Arrow functions sempre serão anônimas, e portanto não podem ser nomeadas.
deve ser declarada com parênteses "()", seguido de "=>" e depois chaves "{}"

Ex.
``` 
var funcao = () => {
    ${instrucao};
}
```