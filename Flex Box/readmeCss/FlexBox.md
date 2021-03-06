# Flex Box

Flex box e separado de 2 maneiras;

-   Flex container;
-   Flex item;

Para fazer o uso do __Flex Box__ deve-se identificar o elemento com o **display: flex** , assim que é colocado essa propriedade, o elemento ja é considerado como um **Flex Container** e tudo que estiver dentro do elemento é um **Flex item**.

<br>

## Usando somente a propriedade *displey: flex;*

Assim que é usado a propriedade display flex, todos os itens dentro do elemento, ficam um ao lado do outro, de acordo com seu tamanho do seu elemento **Pai**.

### Flex Container.

-   __flex-wrap: wrap;__ Não permite que os itens (  elementos filhos ) não fiquem fora dos elemento Pai.

-   __flex: 1;__ Faz com que os itens se ajuste de acordo com o tamanho do elemento pai.


## Exemplos:

Para que entenda melhor o exemplo, adicione mais um nome de classe listada abaixo:

-   flex
-   flex-wrap
-   flex-item-1

<br>

CSS:
```
/* Flex */
.flex {
	display: flex;
}

.flex-wrap {
	flex-wrap: wrap;
}

.flex-item-1 {
	flex: 1;
}

/* Flex Item */
.item {
	margin: 5px;
	background: tomato;
	text-align: center;
	font-size: 1.5em;
}

.container {
	max-width: 400px;
	margin: 0 auto;
	border: 1px solid #ccc;
}

h1 {
	text-align: center;
	margin: 20px 0 0 0;
	font-size: 1.25em;
	font-weight: normal;
}

body {
	font-family: monospace;
	color: #333;
}
```

HTML

```
<h1>display: flex;</h1>
<section class="container flex">
    <div class="item">Teste 1</div>
    <div class="item">Teste 2</div>
    <div class="item">Teste 3</div>
    <div class="item">Teste 4</div>
    <div class="item">Teste 5</div>
    <div class="item">Teste 6</div>
    <div class="item">Teste 7</div>
</section>

```
<hr>

## Flex-direction

Flex direction define direção e por padrão vem como **row(linha)**, tambem temos como valor o **column(coluna)**

-	flex-direction: row; (padrão)
-	flex-direction: column; (opção)
-	flex-direction: row-reverse; (opção)
-	flex-direction: column-reverse; (opção)

## Exemplo:

No exemplo substitua a classe *_row_* para umas das opções abaixo.

-	row-reverse
-	column
-	column-reverse

### CSS3

```
.row {
	flex-direction: row;
}
.row-reverse {
	flex-direction: row-reverse;
}
.column {
	flex-direction: column;
}
.column-reverse {
	flex-direction: column-reverse;
}

/* Flex Container */
.container {
	max-width: 400px;
	margin: 0 auto;
	display: flex;
	border: 1px solid #ccc;
}

/* Flex Item */
.item {
	flex: 1;
	margin: 5px;
	background: tomato;
	text-align: center;
	font-size: 1.5em;
}

h1 {
	text-align: center;
	margin: 20px 0 0 0;
	font-size: 1.25em;
	font-weight: normal;
}

body {
	font-family: monospace;
	color: #333;
}

```

### HTML

```
<h1>flex-direction: row;</h1>
<section class="container row">
	<div class="item">1</div>
	<div class="item">2</div>
	<div class="item">3</div>
</section>
```

<hr>

## Flex-wrap

Define se o itens do elemento devem quebrar ou não a linha quando chegar no limite definido do elemento.

valores usados:

-	flex-wrap: nowrap; => Valor padrão, não deve quebra a linha.
-	flex-wrap: wrap; => Quebra de linha ao chegar no limite do elemento.
-	flex-wrap: wrap-reverse; => Quebra de linha no limite do elemento, de modo reverso.


## Exemplos:

Para melhor entendimento adicionar as classes ou substitua a que esta no exemplo junto a classe container:

-	nowrap
-	wrap
-	wrap-reverse

### CSS3

```
.nowrap {
	flex-wrap: nowrap;
}
.wrap {
	flex-wrap: wrap;
}
.wrap-reverse {
	flex-wrap: wrap-reverse;
}

/* Flex Container */
.container {
	max-width: 360px;
	margin: 0 auto;
	display: flex;
	border: 1px solid #ccc;
}
/* Flex Item */
.item {
	flex: 1;
	margin: 5px;
	background: tomato;
	text-align: center;
	font-size: 1.5em;
}

h1 {
	text-align: center;
	margin: 20px 0 0 0;
	font-size: 1.25em;
	font-weight: normal;
}

body {
	font-family: monospace;
	color: #333;
}
```

### HTML

```
<h1>flex-wrap: wrap;</h1>
<section class="container wrap">
	<div class="item">TesteDoItem1</div>
	<div class="item">TesteDoItem2</div>
	<div class="item">TesteDoItem3</div>
</section>
```

## flex-flow

O flex-flow é um atalho para as propriedades flex-direction e flex-wrap.

-	flex-flow: row wrap;
-	flex-flow: column nowrap;

## justify-content

Ajuda a ajustar/alinha os itens no container, se os itens não ocupar o container inteiro.

como existe muitos valores, cabe pesquisar melhor sobre cada um que deseja usar para a situação que está. asim fazendo teste aderindo para o seu caso.

## Align items

>Alinha os itens flex no container de acordo com a direção. A propriedade só funciona se os itens atuais não ocuparem todo o container. Isso significa que ao definir flex: 1; ou algo similar nos itens, a propriedade não terá mais função

>Excelente propriedade para ser usada em casos que você deseja alinhar um item na ponta esquerda e outro na direita, como em um simples header com marca e navegação.

a o efeito muda de acordo com a direção de row para colunm. Ver no exemplo passado para fixa melhor como usar.

## Align-content
Propriedade que so funciona em caso que existão mais de 1 item dentro do container, e para isso tambem é usado o **flex-wrap**.

Está propriedade so funciona quando existe espaço dentro de container, caso o itens estejam ocupando todo o espaço vocã não vera a diferença.

<br><br>
# Flex Item

Filhos direto do flex container. um flex container é definido quando usado o **display: flex;**

## flex-grow
Em resumo, faz com que o elemente fique to tamanho do container, se usado "0" não ira ocupar todo o width, se usado "1" ira ocupar somente um parte dividindo espaço com outros elementos que tiver o mesmo tamanho e recebeu o **flex-grow: 1;**  ou até mesmo o tomanho maior.

>OBS: justify-content não funciona com em flex-grow;


## Flex Shrink

Define a capacidade de redução do tamanho item, com o valor padrão 1

"observe as mudanças no exemplo no site."

## Flex

Atalho para as propriedades flex-grow, flex-shrink e flex-basis.

## Order

Modifica a ordem dos flex itens. Sempre do menor para o maior.

## Align Self

defini o alinhamento específico de um único flex item dentro do nosso container.

# Dicas de Pratica:

Usado no image : display: block; e max-width:100%; para que a imagem almente com o determinado tamanho da container principal.

para usar o "em" sera feito um calculo de tamanho da font pela base, a formula é "tamanho_font / base"

o uso do **3n+1** com essa esprecao ela sempre vai usar a base de formatação contando 3x apartir de uma posição escolhida, serve para altomatizar cadas formatação de item por coluna.

```
.qualidade__item:nth-of-type(3n+1) h2::before{
    background: #ae81ff;
}

.qualidade__item:nth-of-type(3n+2) h2::before{
    background: #f9265e;
}

.qualidade__item:nth-of-type(3n+3) h2::before{
    background: #66d9eb;
}
```

<hr>

[Guia do README](https://medium.com/@raullesteves/github-como-fazer-um-readme-md-bonit%C3%A3o-c85c8f154f8)

[REFERÊNCIA 1 Flex Box](https://origamid.com/projetos/flexbox-guia-completo/)