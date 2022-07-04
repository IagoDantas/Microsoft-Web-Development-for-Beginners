# Garantir que as páginas estejam acessíveis para todos

É fundamental garantir que sua página da Web esteja **acessível** a todos os usuários e a todos os clientes. 

Como desenvolvedor Web em crescimento, você acredita que é importante aprender a garantir que suas páginas estejam acessíveis no início. É sempre mais fácil criar uma página para ser acessível do que readaptar-se posteriormente.


# Navegar na Web com mais de um navegador

Provavelmente, você ja está familiarizado com o uso de um navegador como cliente para navegar na Web. Quando você pensa em crirar páginas da Web, poderá analisar a experiência do usuário com esse cliente porque tem experiência pessoal com ele. Mas nem todos os usuários usam um navegador da mesma forma ou usam um navegador. Para criar experiências para todos os usuários, você deverá compreender as várias ferramentas que as pessoas podem usar ao navegar na Web.


## Leitores de tela

Uma das ferramentas mais conhecidas é um **leitor de tela**. Os leitores de tela são geralmente usados para pessoas com deficiências visuais. Eles são incorporados a maioria dos sistemas operacionais. À medida que gastamos tempo garantindo que um navegador transmita corretamente as informações que desejamos compartilhar, também devemos garantir que um leitor de tela faça o mesmo.

Em seu mais básico, um leitor de tela lê uma página de cima para baixo de forma audível. Se a sua página for todo o texto, o leitor transmitirá as informações de forma semelhante a um navegador.

## Zoom

Outra ferramenta que as pessoas com deficiências visuais geralmente usam é o zoom. O tipo mais básico de zoom é o estático, que é controlado pelo atalho de teclado 'CTRL + Sinal de adição(+)'. Esse tipo de zoom redimensiona a página inteira. Usando o design responsivo, onde os itens mudam com base no visor, é importante fornecer uma boa experiência de usuário em níveis de zoom maiores.

O sistema operacional provavelmente tem recursos de zoom internos que permitem a você ampliar partes da tela, muito parecido com o uso de uma lupa real.

# Garantir a acessibilidade com ferramentas de desenvolvedor

Testar sua página da Web em vários clientes e exibições é tão importante quanto testar em vários navegadores. Esse teste pode não ser prático em todos os cenários e pode perder situações em que os usuários usam um navegador, mas podem ter outra deficiência. Felizmente, há ferramentas que você pode usar como desenvolvedor para medir a acessibilidade da sua página.

## Verificador de contraste

Alguém que seja daltônico pode não ser capaz de diferenciar as cores ou pode ter dificuldade para trabalhar com cores semelhantes uma da outra. O World Wide Web Consortium (W3C), a organização de padrões da Web, estabeleceu um sistema de classificação para contraste de cores.

Pode ser difícil escolher manualmente as cores certas para garantir que sua página seja acessível a todos. Você pode usar as seguintes ferramentas para gerar as cores apropriadas e testar seu site para garantir a conformidade:

- Ferramentas de geração de paleta:
 - Adobe Color, uma ferramenta interativa para testar combinações de cores
 - Color Safe, uma ferramenta para gerar cores de texto com base em uma cor de tela de fundo selecionada

- Verificador de conformidade: 
 -Extensões de navegador para testar uma página:
  - Edge: verificador de contraste de cores WCAG
  - Firefox: verificador de contraste WCAG 
  - Chrome: verificador de contraste de cores (Colour Contrast Checker)

- Aplicativos: 
 - CCA(Colour Contrast Analyser)

# Lighthouse

O Lighthouse é uma ferramenta criada pelo Google para analisar sites. Ele se tornou tão popular que está incluido em muitas ferramentas de desenvolvedor de navegadores. O Lighthouse pode examinar a SEO(otimização do mecanismo de pesquisa) de uma página, o desempenho de carga e outras práticas recomendadas. O Lighthouse também pode analisar uma página e fornecer uma pontuação para sua acessibilidade atual.

# Garantir que os links e as imagens estejam acessíveis

Dois componentes mais comuns em qualquer página da Web são links e imagens. Esses itens têm um impacto profundo na acessibilidade. Garantir um bom texto de link e texto ALT é uma das primeiras etapas que você pode executar para aprimorar suas páginas para todos os usuários.

## Texto do link

Os hiperlinks são fundamentais para navegar na Web. Garantir que um leitor de tela possa ler os links corretamente permite que todos os usuários naveguem pelo site.

Precisamos sempre usar um texto de link significativo. Um bom texto de link descreve brevemente o que há no outro lado do link. No exemplo anterior sobre pequenos pinguins, o link vai para a página da Wikipédia sobre a espécie. A frase **pequeno pinguim** seria um texto de link perfeito, pois ele esclarece o que alguém aprenderá se selecionar o link:

"O [pequeno pinguim](https://en.wikipedia.org/wiki/Little_penguin), às vezes conhecido como pinguim-azul, é o menor pinguim do mundo".

## Atributos do ARIA

O HTML é compatível com um conjunto de atributos conhecidos como ARIA (Aplicativos de Internet Avançados Acessíveis). Você pode usar esses atributos para fornecer mais informações para os leitores de tela.

Por exemplo, você pode usar aria-label para descrever um link quando o formato da página não permitir. A descrição do widget pode ser definida como:

```
<a href="#" aria-label="Widget description">description</a>
```

O ARIA tem vários usos além de adicionar texto para que os leitores de tela leiam links. Você pode usá-lo para descrever as funções que determinados elementos desempenham quando o HTML semântico não está disponível. Por exemplo, ao criar uma árvore, você poderá usar funções do ARIA para descrever a interface para um leitor de tela:

``` 
<h2 id="tree-label">File Viewer</h2>
<div role="tree" aria-labelledby="tree-label">
<div role="treeitem" aria-expanded="false" tabindex="0">Uploads</div>
</div>
```

## Texto Alt para imagens

Como regra geral, os leitores de tela não podem ler o conteúdo de uma imagem. Embora alguns possam usar inteligência artificial, os resultados gerados podem não ser contextualmente precisos. Felizmente, garantir que as imagens sejam acessíveis não dá muito trabalho é para isso que se trata o atributo 'alt'. Todas as imagens significativas devem ter um atributo 'alt' (conhecido de forma casual como texto alt) para descrever o que elas são ou as informações que estão tentando transmitir.

As imagens que são apenas decorativas devem ter seu atributo alt definido como uma cadeia de caracteres vazia: 'alt=""'. Essa configuração impede que os leitores de tela anunciem desnecessariamente a imagem decorativa.


# Criação voltada à acessibilidade.

A criação de uma página acessível desde o início é sempre mais fácil do que voltar a uma página existente para torná-la acessível.

## Use HTML da maneira como ele foi projetado

O HTML fornece muitos elementos que você pode usar para criar uma página, incluindo botões, links e controles de formulário. Cada um desses elementos tem um conjunto de funcionalidades internas, como ser clicável, ser vinculável ou aceitar o foco.

Com CSS e JavaScript, é possível fazer com que qualquer elemento pareça qualquer tipo de controle. Por exemplo, você pode usar '<span>' para criar um elemento ```<button>``` e '<b>' pode se tornar '<a>'. Embora esse recurso forneça alguns atalhos para estilizar ou dispor sua página, ele remove a funcionalidade interna. Ferramentas como um leitor de tela não conseguirão entender que '<span>' está sendo usado como '<a>'. Alguém navegando com um teclado não será capaz de definir o foco em um elemento '<div>', que tenha sido programado para simular um elemento '<button>'.

Outro elemento HTML que muitas vezes é ignorado são os cabeçalhos ('h1' a 'h6'). De um ponto de vista visual, as marcas de cabeçalho começam do maior para o menor tamanho de texto. Essa convenção leva muitos desenvolvedores a abrir mão de elementos de cabeçalho e estilizar 'div' ou outros elementos genéricos.

## Usar boas indicações visuais

Os desenvolvedores geralmente consideram os leitores de tela como a única ferramenta de acessibilidade. No entanto, os usuários podem usar várias outras ferramentas ou podem não usar ferramentas.

Um dos ótimos recursos do CSS é que ele fornece controle completo sobre como exibir uma página, incluindo a remoção de determinados elementos de exibição. Por exemplo, você pode remover o contorno de uma caixa de texto ou remover o sublinhado de um hiperlink. Infelizmente, a remoção desses tipos de indicações pode torná-lo mais desafiador para alguém que dependa deles para reconhecer o tipo de controle.

## Considere o teclado

Alguns usuários não podem usar um mouse ou trackpad/touchpad. Em vez disso, esses usuários dependem de interações do teclado para tabulação de um elemento para o próximo. É importante que suas páginas apresentem o conteúdo em ordem lógica, de modo que um usuário de teclado possa acessar cada elemento interativo à medida que eles se moverem para baixo.

Quando um usuário passa por uma página alternando, o foco passa de um controle para o outro com base na ordem em que os controles são listados na fonte HTML. Os controles da sua página devem ser listados na fonte HTML na ordem em que você espera que a página seja navegada, enquanto dependem do CSS para dispor a página visualmente para os usuários.

Por exemplo, imagine criar um formulário com duas colunas. Você precisará considerar qual é o fluxo natural para alguém preenchendo o formulário e listar os controles nessa ordem. Você pode usar o CSS para criar as colunas e exibir os controles em seus locais apropriados.

A navegação por teclado depende muito do HTML semântico. Determinados controles (como botões) aceitam o foco, enquanto os elementos div não. Se você estiver recriando controles que já existem no HTML, estará tornando mais difícil para a pessoa usar sua página com um teclado.