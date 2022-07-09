# Visão geral das funções

As funções são blocos de construção principais para escrever código. Uma função é uma coleção reutilizável de linhas de código que faz algo acontecer no seu programa.

As funções são perfeitas para cenários em que você precisa executar a mesma tarefa várias vezes. Em vez de duplicar a lógica em várias localizações, o que dificultaria a atualização do código posteriormente, você pode centralizá-la em apenas uma localização. Dessa forma, você pode chamá-la sempre que precisar que a operação seja executada novamente. Você pode até mesmo chamar funções por meio de outras funções!

Tão importante quanto isso é a capacidade de dar nome a uma função. Embora dar nome para uma função possa parecer trivial, o nome representa uma forma rápida de documentar uma seção de código. Você pode pensar nos nomes como em um rótulo de botão. Por exemplo, se você selecionar um botão com o texto "Cancelar temporizador", ele interromperá a execução do relógio.

## Criar e chamar uma função

Uma função recebe uma entrada e retorna uma saída que, de alguma forma, transforma a entrada. Por exemplo, uma função de adição pode usar dois inteiros recebidos e retornar a soma de seus valores.

As funções são feitas de três componentes distintos:

- O corpo da função é o bloco de código que é executado quando a função é chamada.
- Parâmetro é outro nome dado à entrada passada para uma função.
- Por fim, há um valor retornado ou a saída da função.

A sintaxe de uma função é mostrada no seguinte código:

```
function nameOfFunction(parameter) {
// corpo da função
}
```

Parâmetros e valores retornados são opcionais ao escrever uma função. Para começar, vamos conferir algumas funções básicas que não recebem entradas e nem retornam valores. Se você quisesse criar uma função para exibir uma saudação no console de depuração do editor de código, ela ficaria assim:

```
function displayGreeting() {
  console.log('Hello, world!');
}
```

Essa função é chamada de displayGreeting. Ao ser chamada ela irá executar o texto "Olá, mundo!" e será impresso no console.

Sempre que você quiser chamar a função, use o nome da função seguido por um par de parênteses _(())_.

```displayGreeting();

```

## Práticas recomendadas

Ao criar funções, lembre-se sempre de algumas melhores práticas:

- Use nomes descritivos que revelem a que se destinam as funções. Por exemplo, o nome displayGreeting deixa claro que a finalidade da função é exibir uma saudação. O nome greet para uma função que executa a mesma tarefa é um pouco ambíguo.

- Como os nomes de funções e de variáveis não podem conter espaços, a adoção do modelo camelCasing facilita a leitura das palavras no código. Por exemplo, displayGreeting é mais fácil de ler do que displaygreeting.

- Mantenha suas funções focadas em uma tarefa específica. Isso não apenas facilita a reutilização de uma função no programa, mas também ajuda na depuração do código. Se ocorrer um problema com a função que a impeça de executar a tarefa pretendida, você saberá que a falha está nessa função específica.

- Use comentários para fazer anotações no código e descrever o que as funções fazem. Para aprimorar a leitura do código, inclua nos comentários uma breve descrição da tarefa de cada função.

# Parâmtros de função

Para tornar uma função mais reutilizável, geralmente você passa mais informações a ela. Esse tipo é chamado de _parâmetro_. Às vezes também chamado de argumento, ele representa uma informação adicional a enviada a uma função.

Digamos que você deseje alterar sua função displayGreeting para poder saudar uma pessoa específica, em vez de imprimir simplesmente "Olá, mundo!" cada vez que chamar a função. Você pode usar um parâmetro para especificar o nome da pessoa.

Os parâmetros são listados na definição da função e são envoltos por parênteses (()). Você pode ter vários parâmetros separados por vírgulas.

```
function name(param, param2, param3) {
}
```

Você pode atualizar sua função displayGreeting para usar o nome de uma pessoa como entrada e imprimir uma mensagem personalizada no console.

```
// função com um parâmetro chamado nome.
function displayGreeting(name) {
    // cria uma nova variável local que insere o nome em uma string.
    const message = `Hello, ${name}!`;
    // printando a variável no console.
    console.log(message);
}
```

Quando quiser chamar a função e passar o parâmetro para ela, basta especificá-lo dentro dos parênteses, da seguinte maneira:

```
displayGreeting('Christopher');
```

## Valores padrão

Você pode tornar sua função ainda mais flexível adicionando novos parâmetros. Mas e se você não quiser exigir que todos os valores sejam especificados? Seguindo em nosso exemplo de saudação, você pode deixar `name` como obrigatório (ou seja, é necessário saber quem está sendo saudado), mas permitir que a saudação em si seja personalizável. E se alguém não quiser personalizá-la, você poderá fornecer um valor padrão. Para fazer isso, você definirá o valor da mesma forma que define o valor de uma variável: `parameterName = 'defaultValue'`. Por exemplo:

```
function displayGreeting(name, salutation='Hello') {
  console.log(`${salutation}, ${name}`);
}
```

Ao chamar a função, você poderá decidir se deseja ou não especificar o valor da saudação:

```
displayGreeting('Christopher');
// mostra "Hello, Christopher"

displayGreeting('Christopher', 'Hi');
// mostra "Hi, Christopher"
```

## Valores retornados

Até esse ponto, todas as funções que criamos imprimiram a saída no console. Isso pode ser exatamente o que procuramos ao criar funções que chamam outros serviços. Mas e se quisermos criar uma função auxiliar para executar um cálculo e fornecer um valor que pode ser usado em outro lugar?

Isso pode ser feito usando um valor retornado. O valor retornado é produzido pela função e pode ser armazenado em uma variável, assim como se faz com um valor literal, como uma cadeia de caracteres ou um número.

Se a função precisar retornar algo, use a palavra-chave `return`, geralmente seguida por um valor ou uma referência àquilo que está sendo retornado. No entanto, você também pode usar `return` de maneira independente para sair de uma função.

Aqui está um exemplo de uma instrução `return` que retorna um valor:

```
return myVariable;
```

E aqui está como você usaria return de maneira independente:

```
return;

```

Continuando nosso exemplo anterior, você pode escrever uma função para criar uma mensagem de saudação e retornar o valor ao chamador. Observe que a palavra-chave `return` interrompe a execução da função e retorna o valor especificado se aplicável. Portanto, em geral você deve usar `return` ao final da função, desta forma:

```
function createGreetingMessage(name) {
  const message = `Hello, ${name}`;
  return message;
}
```

Ao chamar essa função, você armazenará o valor em uma variável. Você faz isso da mesma forma que definiria uma variável com um valor estático (por exemplo, `let name = 'Christopher'`), desta forma:

```
let greetingMessage = createGreetingMessage('Christopher');
```

Os valores retornados ajudam a demonstrar outro motivo pelo qual as funções são uma parte tão importante do JavaScript. Você pode reutilizar a mesma função com diferentes argumentos a fim de produzir valores retornados distintos.

# Funções Anônimas

Como você viu, é possível chamar uma função sob demanda usando o nome dela e passando os parâmetros apropriados. Porém, algumas vezes, você pode querer permitir que outros processos executem as funções que você criou.

## Introdução aos retornos de chamada(callback)

Em essência, o retorno de chamada é uma forma de passar uma função como parâmetro para outra função. Esse parâmetro se comporta da mesma forma que qualquer outro, como cadeias de caracteres ou números, exceto pelo fato de que ele pode ser chamado, já que é uma função.

Os retornos de chamada são frequentemente usados em uma série de estruturas e bibliotecas para indicar o código que deseja executar quando algo acontece ou chega ao fim. Você usará um retorno de chamada para indicar o que deve acontecer quando, por exemplo, um usuário selecionar um botão, uma operação de execução longa chegar ao fim ou um temporizador expirar.

## Usar um retorno de chamada

Um retorno de chamada é uma função normal, que pode ser criada da mesma forma que qualquer outra função já escrita no passado. No exemplo `displayDone` a seguir, você observará que é uma função normal sem parâmetros.

```
function displayDone() {
    console.log('Done!');
}
```

Você poderá passá-la para uma função que aceite um retorno de chamada, como `setTimeout`. O retorno de chamada `setTimeout` é uma função interna que lhe permite criar um temporizador. Quando o temporizador chega ao fim, ele chama a função passada como primeiro parâmetro. O segundo parâmetro indica o número de milissegundos a aguardar até chamar a função.

Se você quiser definir um tempo limite de três segundos e fazer com que o código mostre "Concluído!" quando terminar a execução, você poderá usar `setTimeout`, desta forma:

```
// o valor do timer é em milissegundos
setTimeout(displayDone, 3000);
```

## Funções anônimas

Embora o código anterior seja válido, ele pode criar o que alguns desenvolvedores chamam de "poluição do namespace". Ou seja, quando você escreve código com muitas variáveis, funções e outras entidades com nomes, pode se tornar confuso saber a finalidade de cada uma delas e, às vezes, os bons nomes podem acabar. Em nosso exemplo, se o único lugar e que `displayDone` será usado for com `setTimeout`, então não será necessário dar um nome a ele. Você pode criar uma função anônima.

Uma função anônima é uma função sem nome. As funções anônimas se comportam da mesma forma que as funções regulares e são como os desenvolvedores normalmente configuram os retornos de chamada.

É possível criar uma função anônima usando a mesma sintaxe que você usaria para criar uma função normal, exceto pelo fato de omitir o nome.

```
setTimeout(
    function() { // função anônima
        console.log('Done!');
    },
    3000 // 3000 milissegundos (3 segundos)
)
```

Esse código executa exatamente a mesma tarefa que o código anterior da função displayDone. A principal diferença é que você cria sua função embutida (ou seja, dentro da chamada à setTimeout), sem um nome. Ao fazer isso, você deixa o código um pouco mais limpo.

## Funções de seta (Arrow Functions)

As funções Arrow (ou Fat Arrow) são uma forma ligeiramente diferente de criar funções anônimas. As funções Arrow usam o operador `=>` para indicar o início do corpo da função. Você pode reescrever o exemplo de função anônima anterior usando a sintaxe Fat Arrow:

```setTimeout(
    () => { // função anônima
        console.log('Done!');
    },
    3000 // 3000 milissegundos (3 seconds)
)
```

Esse código faz exatamente a mesma coisa que o anterior. A única diferença é o uso do operador ````=>````. Você descobrirá que muitos desenvolvedores preferem a sintaxe concisa oferecida pelas funções Arrow.
