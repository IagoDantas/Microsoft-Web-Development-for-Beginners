# Tomar decisões com JavaScript

## Operadores boolianos


Quando você deseja definir caminhos diferentes por meio de seu código, você usa operadores e variáveis Boolianos para fazer isso. Primeiro, vamos examinar variáveis Boolianos, como declará-los e como atribuir valores a eles.

# Operadores de comparação e Boolianos

image.png

Para usar um operador, você pode usá-lo como parte de uma atribuição ou parte de uma comparação em um constructo ````if/else.```` Você verá mais sobre ````if/else```` posteriormente no módulo. O código a seguir mostra como você pode usar um operador como parte de uma atribuição.

```
let timeOfDay = 8;
let timeToWakeUp = timeOfDay >= 8;// O valor de `timeToWakeUp` vai ser true 
```

# Instruções if...else

## Instrução if`

A instrução ```if``` executará o código entre seus blocos se a condição for true. A condição dentro da cláusula if pode ser um valor que contém um valor verdadeiro ou uma instrução condicional que é avaliada como true. O código a seguir mostra como você expressa uma cláusula ````if````.

```
if (condition){
    //Se a condição for verdadeira, esse bloco de cógido será executado
}
```

## Comparar um valor

Você pode passar uma variável ou um valor booliano para uma cláusula ````if```` como esta:


```
let isTrue = true;
if (isTrue) {
  // run code if true
}

if (true) {
  // run code if true
}
```

## Usar um operador lógico

Os operadores lógicos geralmente são usados para formar a condição. Você precisa de três coisas: um valor, um operador de comparação que mostra como você deseja comparar e um valor para comparar. A sintaxe é semelhante ao seguinte código:

```
if (value operator compareToThisValue) {
  // run code
}
```

## Operadores lógicos e Boolianos

Há operadores específicos que nos permitem conectar muitas instruções boolianas. O resultado é uma instrução mais complexa que ainda é avaliada como ````true```` ou ````false````. Você pode usar o seguinte conjunto de operadores para construir essas comparações mais complexas:

image.png

## Condições e decisões com operadores lógicos

Você pode usar esses operadores complexos com ambas as atribuições, mas também com as cláusulas ````if```` e ````else````.

## Em atribuições

Como parte da atribuição de um valor a uma variável, você pode usar um operador OR (````||````).

```
let isHoliday = true;
let isMember = true;
let hasDiscount = isHoliday || isMember;
```

Com o código anterior, você expressa se um cliente pode ter um desconto ou não. Somente uma das variáveis, ````isMember```` ou ````hasDiscount````, precisa ter um valor verdadeiro para que a variável ````hasDiscount```` seja atribuída como true.

## Em if...else

Você também pode usar esse tipo de operador lógico em uma instrução ````if/else````. No exemplo de código a seguir, você tem uma situação em que há dois laptops, um com desconto e um vendido pelo preço cheio. Usando um operador ````||````, você é capaz de construir uma cláusula ````if```` com aparência mais complexa.

```
let currentMoney= 800;
let laptopPrice = 1000;
let laptopDiscountPrice = laptopPrice - (laptopPrice * .20) //Laptop price at 20 percent off

if (currentMoney >= laptopPrice || currentMoney >= laptopDiscountPrice){
    //Condition was true. Code in this block will run.
    console.log("Getting a new laptop!");
}
else {
    //Condition was true. Code in this block will run.
    console.log("Can't afford a new laptop, yet!");
}
```
## Operador de negação

Tudo o que entra em um ````if```` precisa ser avaliado como verdadeiro ou falso. Usando o operador ````!````, você pode negar a expressão. Ele deve ter esta aparência:

````
if (!condition) {
  // runs if condition is false
} else {
  // runs if condition is true
}
````

## Expressões ternárias

Usar o ````if...else```` não é a única maneira de expressar a lógica de decisão. Você também pode usar algo chamado de operador ternário.

```
let variable = condition ? <return this if true> : <return this if false>
```


```
let firstNumber = 20;
let secondNumber = 10
let biggestNumber = firstNumber > secondNumber ? firstNumber: secondNumber;
```

O código declara que:

se ````firstNumber```` for maior que ````secondNumber````, atribua ````firstNumber```` a ````biggestNumber````, caso contrário, atribua ````secondNumber````.