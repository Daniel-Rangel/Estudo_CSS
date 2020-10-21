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

<hr>

[Guia do README](https://medium.com/@raullesteves/github-como-fazer-um-readme-md-bonit%C3%A3o-c85c8f154f8)

[REFERÊNCIA 1 Flex Box](https://origamid.com/projetos/flexbox-guia-completo/)