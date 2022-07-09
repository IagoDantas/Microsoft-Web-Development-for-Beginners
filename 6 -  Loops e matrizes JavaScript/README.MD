# Loops e matrizes JavaScript 

# Manipular Matrizes 

Para que os dados e informações em seus sites sejam interativos, você precisa de uma maneira de manipular e armazenar os dados em seu código. Felizmente, o JavaScript tem uma maneira de armazenar vários itens em uma matriz. O uso de matrizes ajudará a evitar que você declare muitas variáveis, entre outros benefícios.

## Sobre matrizes

Uma matriz é um tipo de estrutura de dados que contém mais de um elemento. Imagine uma ordem de compra que contém vários itens de pedido ou uma sorveteria com vários sabores para escolher. Em vez de armazenar, por exemplo, oito sabores de sorvete diferentes como oito variáveis diferentes, você pode usar uma única matriz para armazenar essas informações, conforme mostrado abaixo:

```
let iceCreamFlavors = ["Chocolate", "Strawberry", "Vanilla", "Pistachio", "Neapolitan"];

```
## Acessar um item

O conteúdo de uma matriz geralmente é conhecido como *elementos* ou *itens*. Geralmente, você precisa acessar um elemento específico para ler seu valor, atualizá-lo ou até mesmo removê-lo. Para acessar um elemento específico, use colchetes e a posição em que está interessado, desta forma:

````
array[<number>]
````

O primeiro item em uma matriz começa em 0 e o último item é seu comprimento (número de itens) menos 1. Ou seja, se uma matriz tiver três itens, 0 será a primeira posição e 2 sua última posição. Uma posição em uma matriz é conhecida como seu índice. Observando a matriz ````iceCreamFlavors````, vamos supor que você deseja pistache. Para ler seu valor, você pode escrever o seguinte código:

```
iceCreamFlavors[3] // Pistachio
```

## Alterar um valor

Para alterar um valor em uma matriz, você precisa selecionar o índice do item e atribuir a ele um novo valor usando o operador de atribuição de sinal de igual (```=```) e um valor à direita do operador. Sua sorveteria ficou sem “napolitano”, mas não se preocupe, você encontrou um pouco de “noz pecã”:

```
iceCreamFlavors[4] = "Butter Pecan"; //Changes "Neapolitan" to "Butter Pecan"
```

## Adicionar mais valores

Em algum momento, seu negócio de sorvete se expande e você deseja oferecer mais sabores. O que você faz? Você pode usar o método ```push()``` para adicionar mais sabores. O método ```push()``` aceita um item como entrada e adiciona o item à matriz original. Por exemplo, para adicionar “menta com chocolate” como sabor, você usaria o seguinte código:

```
iceCreamFlavors.push("Mint Chip");
```

## Usar o comprimento da matriz

Imagine que alguém pergunta: “Quantos sabores de sorvete você tem?”. Você olha nos fundos da loja, mas tudo o que você vê é um mar de sabores, o que levará algum tempo para contar. Mas espere, na matriz, há um campo length que você pode usar para contar todos os sabores:

```
iceCreamFlavors.length // 6 flavors, because you recently added "Mint Chip"
```
## Remover um valor

Para remover um valor de uma matriz, você pode usar ```delete```. Digamos que você acabou de ficar sem o "chips de menta". O balde ainda está lá, mas o sorvete "chips de menta" acabou. O código terá esta aparência:

````
let iceCreamFlavors = ["Chocolate", "Strawberry", "Vanilla", "Pistachio", "Neapolitan", "Mint Chip"];
delete iceCreamFlavors[iceCreamFlavors.length-1];
console.log(iceCreamFlavors[length-1]) // undefined
````

Todos os seus itens ainda estão lá, mas o balde, onde o “menta com chocolate” costumava estar, está desmarcado. Agora que você pode atribuir a ele um novo sabor:

```
iceCreamFlavor.splice(2,1); 
iceCreamFlavor // [ 'Chocolate', 'Strawberry', 'Pistachio', 'Neapolitan', 'Mint Chip' ]
```

## Iterar sobre itens em uma matriz usando loops

Então você tem uma matriz, e agora? Bem, você pode usar loops para executar iterações em cada item na matriz. Você pode executar operações como imprimir cada item, somar ou localizar itens específicos com uma condição determinada.

## Sobre loops

Os loops permitem tarefas repetitivas ou iterativas, e podem poupar muito tempo e código. Uma iteração pode variar em suas variáveis, valores e condições. Há diferentes tipos de loops no JavaScript, cada um com suas pequenas diferenças. Mas todos fazem praticamente a mesma coisa: eles executam um loop sobre os dados.

## Loops ````For````

Um loop for requer três partes para iterar:

- **Counter**: uma variável que é normalmente inicializada com um número que conta o número de iterações. Veja um exemplo:

```
let i = 0;
```

- **Condition**: uma expressão que usa operadores de comparação para fazer com que o loop pare quando ```true```. Aqui está um exemplo de uma condição que é interrompida quando a matriz está fora dos índices:

```
i < 10;
```
Neste exemplo, a expressão será falsa quando i for igual a arry.length. Se você estiver fazendo um loop em uma matriz, é esse o objetivo. Não é aconselhável resolver um índice fora dos limites da matriz.

- **Expressão de incremento**: uma expressão que é executada no final de cada iteração, normalmente para alterar o valor do contador. Você pode incrementar tanto quanto desejar por iteração, mas é comum aumentar em um, conforme mostrado neste exemplo:

```
i++;
i +=2; // this would work too and increases by 2
```

Quando as três partes são usadas juntas, um loop ```for``` pode ter esta aparência:

```
for (let i = 0; i < 10; i++ ) {
  console.log(i);
}
```

## Loops ````While````

Ao contrário do loop ````for````, um loop ````while```` requer uma condição que irá parar o loop somente quando a expressão no loop ````while```` for avaliada como ````true````.

As condições em loops geralmente dependem de outros valores, como contadores, e devem ser gerenciadas durante o loop.

Os valores iniciais para os contadores devem ser criados fora do loop e todas as expressões para atender a uma condição, incluindo a alteração do contador, devem ser mantidas dentro do loop. No exemplo a seguir, o loop ```while``` é executado para 10 iterações.

````
//Counting up to 10
let i = 0;
while (i < 10) {
 console.log(i);
 i++;
}
````
## Loops e matrizes

Vamos voltar à sua lista de deliciosos sabores de sorvete. Um cliente pediu para você dizer o nome de todos os sabores que está vendendo antes de decidir o que comprar. Felizmente, você conhece os loops for, portanto, vá em frente e use um.

Bem, sua matriz de sabores de sorvete tem um comprimento arbitrário, o que significa que você pode remover ou adicionar itens a ela a qualquer momento. Você sabe que tem seis tipos de sorvete, mas pode usar o campo ```length``` na matriz e depender disso:

```
let iceCreamFlavors = ["Chocolate", "Strawberry", "Vanilla", "Pistachio", "Neapolitan", "Mint Chip"];

for (let i = 0; i < iceCreamFlavors.length; i++) {
  console.log(iceCreamFlavors[i]);
} // Ends when all flavors are printed
```

## O loop ````forEach()````

O loop ```forEach()``` itera sobre os itens e oferece uma maneira simplificada de fazer loop, pois você não precisa de um contador se tudo o que você deseja fazer é um loop.

````
let numbers = [1, 2, 3, 4, 5];
numbers.forEach(number => console.log(number)); // 1 2 3 4 5
````

Além disso, se você quiser ter acesso ao índice atual, também poderá fazer isso, alterando ligeiramente o código anterior para o seguinte:

```
numbers.forEach((number, index) => console.log(`Number ${number} ${index}`));
```

## Quando usar qual constructo de loop

Os loops for e ````forEach()```` permitem que você faça um loop sobre os itens da matriz, mas a diferença entre eles é que o loop ````for```` permite que você saia se uma determinada condição for atendida.

```
let numbers = [1, 2, -1, 4, 5];
for(let i = 0; i< numbers.length; i++>) {
  if (numbers[i] < 0) {
    break;
  }
  console.log(numbers[i]);
}
```

Adicionar ````break```` faz o loop parar em um item negativo. O loop ````forEach()```` não pode fazer isso.

# Usar operações para consultar matrizes

Você percorreu um longo caminho, mas há mais sobre matrizes do que apenas iterar por elas ou remover e adicionar itens. Você também pode consultá-las ou executar operações nelas.

## Filtragem

Você pode executar muitas operações úteis em uma matriz. Localizar e filtrar o que você precisa são operações que você provavelmente vai fazer com frequência.

## Localizar um item usando ```find()```
 
Imagine que você tem seu sorvete e alguém pergunta: você tem “chocolate” e, se sim, posso pedir? Nesse momento, você pode usar o método ````find()```` na matriz, como mostrado aqui:

````
let iceCreamFlavors = ["Chocolate", "Strawberry", "Vanilla", "Pistachio", "Neapolitan", "Mint Chip"];
iceCreamFlavors.find(flavor => flavor === "Chocolate") // "Chocolate"
````

A operação ````find()```` executa a função que você forneceu como entrada para cada item. Se a operação encontrar o elemento pesquisado, ela retornará o elemento. Se ela não encontrar o elemento, ela retornará ````undefined````.

## Filtrar itens com uma propriedade comum usando ````filter()````

E se o cliente disser, quero um sorvete que contenha "chocolate", o que você tem? Agora, você precisa reorganizar um pouco sua sorveteria e começar a categorizar as coisas. Essa consulta de cliente deve retornar "Chocolate", "Napolitano" e "Menta com chocolate" como ofertas de sabor que contêm "Chocolate". Com isso em mente, você opta por armazenar a matriz da seguinte maneira:

````
let iceCreamFlavors = [
  { name: "Chocolate", type: "Chocolate" }, 
  { name: "Strawberry", type: "fruit"}, 
  { name: "Vanilla", type: "Vanilla"}, 
  { name: "Pistachio", type: "Nuts"}, 
  { name: "Neapolitan", type: "Chocolate"}, 
  { name: "Mint Chip", type: "Chocolate"}
];
````

Você agora reorganizou suas opções de sabores. O cliente solicitou qualquer sorvete contendo chocolate, e parece que quer uma bola de cada um dos três sabores retornados pela consulta. O melhor método a ser usado nesse caso é a operação filter(). Ele usa uma expressão de filtro (uma função) e retorna qualquer item que corresponda à expressão. Para ajudar o cliente a encontrar o que deseja, use o seguinte código:

````
iceCreamFlavors.filter(flavor => flavor.type === "Chocolate") // [{ name: "Chocolate", type: "Chocolate" }, { name: "Neapolitan", type: "Chocolate"}, { name: "Mint Chip", type: "Chocolate"}]
````

## Verificar uma condição usando ```some()```

Um de seus clientes é alérgico a "Nozes" e quer primeiro saber se algum dos seus sorvetes contém "Nozes". Você confira seu inventário usando o método some(). O método usa uma função que verifica se pelo menos um elemento atende a uma condição.

```
iceCreamFlavors.some(flavor => flavor.type === "Nuts") // true
```

Como o tipo “pistache” contém nozes, o método some() retorna com true. Agora, o cliente quer saber todos os sabores que ele pode ter com segurança, o que fará com que você execute este código:

````
iceCreamFlavors.filter(flavor => flavor.type !== "Nuts") // returns everything except for Pistachio.
````

## Mapa de projeções

Uma projeção é você tentar alterar sua matriz de alguma forma. Imagine, por exemplo, que você pega sua matriz original iceCreamFlavor e deseja adicionar uma propriedade price a cada sabor. Essa situação é um bom caso para um método de projeção chamado map(). Imagine que é um dia ensolarado e você decidiu que seu sorvete deve custar US$ 1 por bola. Você escreve o código para fazer isso acontecer, desta forma:

````
let iceCreamFlavors = [
  { name: "Chocolate", type: "Chocolate" }, 
  { name: "Strawberry", type: "fruit"}, 
  { name: "Vanilla", type: "Vanilla"}, 
  { name: "Pistachio", type: "Nuts"}, 
  { name: "Neapolitan", type: "Chocolate"}, 
  { name: "Mint Chip", type: "Chocolate"}
];
iceCreamFlavors.map(flavor => {
  flavor.price = 1;
  return flavor;
}) // every item now has a new property price: 1
````

## Agregações

Os negócios têm corrido bem. O clima está ensolarado hoje e você vendeu uma tonelada de sorvete. Os recibos da caixa registradora são armazenados em uma matriz longa, que se parece com o seguinte código:

```
let sales = [{
 date : '2021-05-01',
 amount: 2
},
{
 date : '2021-05-01',
 amount: 1
}
// and so on...
]
```

Você pode usar um loop ````for```` para somar todos juntos, desta forma:

```
let sum = 0;
for( let i =0; i< sales.length; i++) {
  sum += sales[i].amount; 
}
```

Esse código funciona, mas há uma abordagem mais elegante: ou seja, o método ````reduce()````. A ideia desse método é reduzir uma longa lista a um único item, que pode ser um objeto ou um número, por exemplo. Para usar ````reduce(),````, você precisa fornecê-lo com uma função que usa dois parâmetros, um valor acumulado e o valor atual no loop.

Dentro da função, você deve recalcular o valor acumulado usando o valor atual. O segundo argumento para ```reduce()``` é o valor inicial. Como você deseja usar ```reduce()``` nesse caso para calcular as vendas, sua função deve atualizar o valor acumulado com o valor do que está na propriedade ```amount``` para cada item. O valor inicial deve ser ```0```. Com isso em mente, veja como é o código

```
sales.reduce((acc, curr) => acc + curr.amount, 0);
```
Como você pode ver, não há necessidade de uma variável ```sum```. Agora, essa abordagem leva algum uso para, mas é eficiente e pode ser usada em muitas situações.