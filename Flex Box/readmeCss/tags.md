# HTML semântico

HTML semântico é aquele que usa as tags a partir do significado dos documentos 
## Tag's usadas para layout (corpo)

-   \<header>
-   \<nav>
-   \<main>
-   \<section>
    -   \<article>
    -   \<h1> a \<h6>
    -   \<figure>
    -   \<img>
    -   \<p>
-   \<aside>
-   \<footer>

### \<header>

Usado para representar o cabeçalho, ou seção do html. Nele podemos usar:

- \<h1> ao \<h6> para definir titulos;
- \<img> representando o banner do site;
- \<p> paragragos de um conteúdo;
- \<nav> lista de navegação.

```
<header>
    <h1>Aqui um titulo principal</h1>
    <p>Texto de apresentação</p>
    <nav>
        <ul>
            <li>link 1</li>
            <li>link 2</li>
            <li>link 3</li>
        </ul>
    </nav>
</header>
```

### \<nav>

Usamos quando precisamos representar um grupo de links, listados atravez do **\<ul>**, **\<li>**, **\<a>**.

-   \<ul> lista não ordenada;
-   \<li> item de lista não ordenada;
-   \<a> link e direciona para outro sites ou documentos;

```
<nav>
    <ul>
        <li><a href="#">link 1</a></li>
        <li><a href="#">link 2</a></li>
        <li><a href="#">link 3</a></li>
    </ul>
</nav>
```


### \<main>
Elemento principal, indicado o item de maior relevancia dentro da  pagina. sendo aconselhado ter somente um dentro da pagina. 

```
<main>
  <h2>Titulo</h2>

  <p>Lorem ipsum dolor sit amet, consectetur adipisicing ...</p>

  <article>
     <h3>Subtítulo</h3>
        <p>Duis aute irure dolor in reprehenderit...</p>
   </article>
</main>
```

### \<article>

É utilizado para quanto precisamos declarar um conteúdo que não presiza de outro para fazer sentido, como por exmplo um artigo de um blog. usado com titulos de **\<h2>** a **\<h3>**, e paragrafos **\<p>**.

```
<article>
    <h3>Título do artigo</h3>
      <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod ...</p>
</article>
```

### \<figure>

O elemento de uso especifico, usado quando adicionado uma imagem **\<img>** que pode a ter uma descrição **\<figcaption>**.

```
<figure>
   <img src=”#” alt=”Imagem”>

   <figcaption>Figura 1. Imagem</figcaption>
</figure>
```

### \<section>

Elemento que representa um seção de um documento,contém um titulo de **\<h2>** a **\<h6>**, podendo utilisar o **\<p>**, **\<img>**, **\<article>**, entre outras tags. O **\<section>** descreve as seções e topicos de um documento. 

```
<section>
    <img src="#">
    <article>
        <h3>Título do artigo</h3>
        <p>
            Lorem ipsum dolor sit amet, consectetur
            adipisicing elit, sed do eiusmod ...
        </p>
    </article>
</section>
```
### aside
Elemento usado quando é necessario criar um conteúdo de apoio/adicional ao conteúdo principal. como por exemplo, usado ele para indicar mais leiturar complementar sobre o assunto do documento.

```
<aside>
    <nav>
        <ul>
            <li><a href="#">link 1</a></li>
            <li><a href="#">link 2</a></li>
            <li><a href="#">link 3</a></li>
        </ul>
    </nav>
</aside>
```

### footer

rodape do documento, usado como area que representa o fim da pagina, onde contem informações de autoria, parcerias e contato do autor.

```
<footer>
     <p>Escrito por Estevão Dias</p>
     <p>Publicado em 25/03/2017 </p>
</footer>
```

Exemplo final:

```
<body>
    <header>
        <nav>
            <ul>
                <li><a href=""></a></li>
            </ul>
        </nav>
    </header>
    <main>
        <h1>flex-direction: row;</h1>
        <section class="container column-reverse">
            <h2>Teste de titulo</h2>
            <article>Lorem ipsum dolor sit amet consectetur... </article>
            <figure>
                <img src="#" alt="uma imagem">
                <figcaption>texto do img</figcaption>  
            </figure>
        </section>
    </main>
    <aside>
        <nav>
            <ul>
                <li><a href="#"></a></li>
                <li><a href="#"></a></li>
            </ul>
        </nav>
    </aside>
    <footer>
        <h3>feito por Daniel Rangel</h3>
    </footer>
</body>
```
