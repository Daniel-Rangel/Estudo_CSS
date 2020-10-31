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


