# Variáveis e tipos de dados JavaScript

# Visão geral de variáveis

Para entender corretamente o JavaScript (a linguagem que fornece interatividade na Web), você primeiro precisa entender os tipos de dados e variáveis dessa linguagem e a maneira de criá-los. E, mais importante, você precisa entender quando, onde e como usá-los.

## Interatividade

Quando você usa variáveis, você pode acompanhar estados. Pode ser que você precise se lembrar do valor da seleção de um usuário, ou salvar o resultado de um cálculo. Situações como essas pedem o uso de variáveis.

Tipos de dados aprimoram o uso de variáveis ao permitirem que você especifique a forma e o tamanho dos dados que você precisa armazenar. Os tipos de dados podem ser expressos como números, cadeias de caracteres ou até mesmo estruturas mais complexas.

# Usar variáveis para lembrar valores

Saber usar variáveis e tipos de dados adequadamente é essencial para escrever código em JavaScript. As variáveis armazenam valores que podem ser usados e alterados em todo o código, e os tipos de dados ajudam a descrever quais tipos de dados são armazenados nessas variáveis.

## Variáveis

Suponha que, em seu código, você tenha um valor que deseje lembrar para uso futuro. Ao armazenar o valor, você pode consultá-lo posteriormente em seu código.

Você pode criar e declarar uma variável usando a seguinte sintaxe: ```[keyword]``` ```[name]```. Aqui está um exemplo de uma declaração de variável:

```
var aVariable;
```

A palavra-chave ```var``` indica que você deseja declarar uma variável, sendo ```aVariable``` o nome da variável. É você quem define o nome de uma variável, e ele deve refletir o uso.

## Palavra-chave para trabalhar com variáveis

A palavra-chave ```let``` foi introduzida no JavaScript padrão ECMAScript 6 (ES6). Ao usar ```let```, você obtém o escopo de bloco da sua variável. Recomendamos que você use ```let``` em vez de ```var``` para gerenciar melhor o escopo em seu aplicativo.


O JavaScript usa diferentes tipos de escopo, como escopo global e escopo de função, para determinar quais variáveis estão disponíveis em cada parte do código. Por exemplo, uma variável global está disponível dentro de uma função porque ela pertence ao escopo global, ou escopo "externo". As variáveis designadas com a palavra-chave ```var``` têm o escopo definido (seus valores são visíveis) no corpo da função, e as variáveis ```let``` têm seu escopo definido no respectivo bloco delimitador entre chaves. Isso significa que se você usar ```var``` em um loop for, ele ficará visível fora do loop for, o que pode ter resultados inesperados. Usar o ```let``` é uma melhor opção, porque ele está disponível apenas no bloco delimitador (ou seja, o loop for), e, portanto, é mais provável que tenha essa disponibilidade.

Para declarar uma variável usando ```let```, use a seguinte sintaxe:

```
let myVariable;
```


```myVariable``` foi declarado por meio da palavra-chave ```let```. Ele não tem um valor no momento, mas você pode atribuí-lo.

## Atribuir um valor

Para armazenar um valor em uma variável, use o operador de atribuição (```=```) seguido do valor esperado:

```
myVariable = 123;
```

```myVariable``` teve atribuído o valor 123.

## Inicialização explícita

Uma *inicialização* difere de uma atribuição porque você declara o valor e também atribui um valor. Aqui está um exemplo de uma inicialização:

```
let myVariable = 123;
```

O motivo para usar uma inicialização explícita em vez de uma atribuição é que você deseja que uma variável contenha um valor inicial. Imagine, por exemplo, que você deseja que todos os jogadores de um jogo de cartas tenham 100 pontos em fichas de pôquer ao iniciarem um jogo. Para representar esse estado, você pode declará-lo da seguinte forma:

```
let pokerChips = 100;
```

## Alterar variáveis

Talvez você queira armazenar temporariamente um valor em uma variável. Um exemplo disso é a soma de um cálculo.

O código a seguir mostra como usar o operador de atribuição (```=```) e como atribuir um valor no lado direito do operador:

```
myVariable = 321;
```
Algumas vezes, você pode não querer que os valores de variáveis mudem. Essa situação pode ocorrer quando você depende de uma constante matemática, como o valor de pi. Para atender a essa necessidade, o JavaScript permite que você crie constantes.

### Constantes

A declaração e a inicialização de uma constante seguem os mesmos conceitos de uma variável, com a diferença de que é usada a palavra-chave ```const```:

```
const MY_VARIABLE = 123;
```

As constantes são semelhantes às variáveis, com duas exceções:

-Elas precisam ter um valor. As constantes precisam ser inicializadas, ou você obterá um erro ao executar o código.
-A referência não pode ser alterada. Se a referência de uma constante mudar depois de inicializada, você obterá um erro ao executar o código.

Veja alguns exemplos:

- A sintaxe de código a seguir para um valor simples não é permitida:
```
const PI = 3;
PI = 4; // not allowed
```
- A sintaxe a seguir tem uma referência de objeto protegido e não é permitida:

```
const obj = { a: 3 };
obj = { b: 5 } // not allowed
```
- A sintaxe a seguir tem um valor de objeto que não está protegido. Ela é permitida, porque você está alterando o valor do objeto, mas não a própria referência.

```
const obj = { a: 3 };
obj.a = 5;  // allowed
```
*A presença de const significa que a referência está protegida contra reatribuições. Mas o valor não é imutável e pode ser alterado, principalmente se for um constructo complexo como um objeto.*

# Tipos de dados


As variáveis podem armazenar diversos tipos de valores, como números e texto. Esses valores são chamados de tipos de dados.

Os tipos de dados são uma parte importante do desenvolvimento de software, porque os desenvolvedores os usam para tomar decisões sobre como o código deve ser escrito e como o software deve ser executado. Alguns tipos de dados têm recursos exclusivos que ajudam a transformar ou extrair informações adicionais de um valor.

Os tipos de dados também são chamados de primitivos de dados do JavaScript, pois são os tipos de dados de nível mais baixo que a linguagem fornece. Há seis tipos de dados primitivos: ````string````, ````number````, ````bigint````, ````boolean````, ````undefined```` e ````symbol````.

# Números

As variáveis podem armazenar todos os tipos de números, incluindo decimais ou números negativos. Os números também podem ser usados com operadores aritméticos.

Aqui estão alguns tipos de operadores que você pode usar ao executar funções aritméticas:

image.png

# Cadeias de caracteres

Strings são conjuntos de caracteres situados entre aspas simples ou duplas.

As cadeias de caracteres são textuais e exigem formatação de tempos em tempos.

Para concatenar duas ou mais cadeias de caracteres ou associá-las, use o operador +:

```
let myString1 = "Hello";
let myString2 = "World";

myString1 + myString2 + "!"; //HelloWorld!
myString1 + " " + myString2 + "!"; //Hello World!
myString1 + ", " + myString2 + "!"; //Hello, World!
```

Os literais de modelo são outra maneira de formatar cadeias de caracteres, exceto que, em vez de aspas, você usa o acento grave. Tudo o que não for texto sem formatação deve ser colocado dentro de espaços reservados ````${ }````, incluindo qualquer variável que possa ser uma cadeia de caracteres.

```
let myString1 = "Hello";
let myString2 = "World";

`${myString1} ${myString2}!` //Hello World!
`${myString1}, ${myString2}!` //Hello, World!
```

# Boolianos

Boolianos podem ter apenas dois valores: ````true```` ou ````false````. Os boolianos podem ajudar a tomar decisões sobre quais linhas de código devem ser executadas quando determinadas condições são atendidas. Em muitos casos, os operadores auxiliam na definição do valor de um booliano. Muitas vezes, você observará que as variáveis são inicializadas ou têm seus valores atualizados com um operador. Veja um exemplo:

```
let myTrueBool = true
let myFalseBool = false
```

