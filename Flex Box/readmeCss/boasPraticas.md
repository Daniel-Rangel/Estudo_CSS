<h1 align="center">Boas praticas com CSS3</h1>

> Com essa parter estudamos metodos de boas praticas para o css3, possibilitanto a manutenção mesmo com os projetos pequenos.

## BEM

Arquitetura que ajuda a ter regras que permite a reutilização e manuteção do CSS3 usando a nomeclatura para facilitar a reutilização, manuteção e organização.

*   facil de manuteção
*   torna o codigo modular (reutilizavel)
*   flexivel a mudança

<br>

## Descrição geral.

**Blocos** é tudo aquilo que tiver uma formatação padrão, onde poderá ser reaproveitado por outro bloco;

**Modifier** é inserido quando exite algo a ser modificado como exemplo a cor ou tamanho;

**"--"** usado para deixar modificadores e blocos separados de forma que entenda quem é quem, deixando *_nomeBloco--modifier_*... veja mais exemplos.

**"__"** usado para identificar que elemente faz parte de outro elemento *_"Pai__filho"_*... veja mais em exemplos.
## Regras gerais

Não fazer modificação direto no elemento;
Criar uma classe para os elementos;
sempre que criar um modifier adicionar "--" para identificar o modificador;

#### exemplo:

.nomeDoBloco--modifier {}</br>
Exemplo de uso quando se tem um nome.

.nomeDoBloco--big-modifier{} </br>
Exemplo de uso quando exite mais de um nome.

.Lista__item{} </br>
Uso simple de identidicação de pai e filho.


## Nomeclatura (1/2)

### *_Block :_*

-   Sem dependencia hierarquica, ele mesmo tem sua propria formatação.

-   Usar somente Class. (sem tag ou ID), o uso de classe faz com que ele poça ser usado em outras tegs.

### *_Element :_*

-   Nome é precedido do Block. sendo identificado com **"__"**, exemplo: form__input.

-   Não colocar forma hierarquica no css3, e sempre fomatar ele indepentende, exemplo: .form__input{}.

### *_Modifier :_*

-   identificado com "--" para adicionar o modifier, exemplo: somente block => form--novo-modificador, com elemente => form__input--novo-modificador.

- nunca colocar um modifier sem ter um precedente.

## Nomenclatura (2/2)

Usar somente a força do css3 quando se tratar de um modifier.

>Para notar a diferença retire "form--small"

*_exemplo:_*

HTML
```
<form class="form form--small">
    <input type="text" class="form_input">
    <input type="submit" value="Enviar" class="form_submit">
</form>
```

CSS3
```
.form{
    background: #ccc;
    padding: 15px;
    border: 1px solid #000;
    width: 300px;
    margin: 0 auto;
}

.form_input{
    border: 1px solid #ccc;
    font-size: 15px;
    padding: 10px;
    display: block;
    width: 100%;
    margin-bottom: 10px;
}

.form_submit{
    border: 1px solid #ccc;
    font-size: 15px;
    padding: 10px;
    display: block;
    width: 100%;
}

/* modificadores para  feito em cascata*/
.form--small{
    padding: 5px;
}

.form--small .form_input{
    padding: 5px;
    font-size: 12px;
    margin-bottom: 5px;
}

.form--small .form_submit{
    padding: 5px;
    font-size: 13px;
}
```
## Informações de ronnsivo:

meta tag usada para responsivo.
><meta name="viewport" content="width=device-width, initial-scale=1.0, shrink-to-fit=no">

## Posso criar modificadores globais?

Usando o bem, não é recomendavel fazer modificadores globais. essa estrutura trabalha com modificadores independentes. 

quando se deseja retirar um elemente usando modificadores globais usa-se até 3 tipos de valores para essa ação.

exemplo em css3:
```
.button--hidden{
    display: none; => modo 1
    visibility: hidden; => modo 2
    position: absolute; => modo 3
    left: -99999999;
}
```

