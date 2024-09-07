# **HTML (HYPERTEXT MARKUP LANGUAGE)**
HTML é uma linguagem de marcação. Ela representa o "Esqueleto" dum WebSite. Ela é onde o **Conteúdo** fica.
# **CRIANDO E FAZENDO AS PRIMEIRAS CONFIGURAÇÕES DOS ARQUIVOS HTML**

Quando criamos um `index.html`, ao digitar `!` e dar um `enter`, o VSCode automaticamente já cria e organiza a principal estrutura de todos os arquivos HTML, tendo o `<!DOCTYPE html>`, `<html lang>`, `<head>`, `<body>`, etc.

# **ELEMENTOS HTML**
Um elemento é uma tag de abertura, o texto dentro dela (Ou qualquer outra coisa) e a tag de fechamento. (Tags vazias também são elementos)
## Exemplo de elemento HTML:
`<h1>Olá!<h1>`
`<button>Clique aqui</button>`

# **TAGS DE CONTAINER HTML**
Uma tag de container é um tipo específico de elemento HTML cuja principal função é agrupar outros elementos dentro dela. Essas tags são usadas para estruturar e organizar o conteúdo da página em blocos, permitindo aplicar estilos CSS, manipular o layout e organizar a hierarquia do conteúdo.
Exemplo de uma tag de container (um elemento `<div>`):
```
<div class="container">
    <h1>Título</h1>
    <p>Este é um parágrafo dentro de um container.</p>
</div>
```
Aqui, o elemento `<div>` funciona como um container que agrupa um título (`<h1>`) e um parágrafo (`<p>`).

### **Principais Diferenças entre elementos e tags de container HTML:**
- **Função:**
    - **Elemento:** Qualquer parte individual de uma página HTML (como um parágrafo, imagem, link, etc.).
    - **Tag de Container:** Um tipo de elemento cuja principal função é agrupar outros elementos para organização e layout.
- **Uso:**
    - **Elemento:** Pode representar conteúdo específico, como texto, imagens, links, etc.
    - **Tag de Container:** Usada para criar seções lógicas ou blocos na página que contêm outros elementos.
- **Exemplos:**
    - **Elemento:** `<p>`, `<img>`, `<a>`, etc.
    - **Tag de Container:** `<div>`, `<section>`, `<article>`, etc.
Resumindo, todo elemento HTML (como `<div>`, `<p>`, `<img>`) é uma parte fundamental da estrutura de uma página web, enquanto uma tag de container é especificamente usada para agrupar e organizar outros elementos dentro dela.


# **IDENTAÇÃO HTML**
Em HTML, você pode identar todas as tags que quiser, o HTML simplesmente não liga para nenhuma delas. Isso facilita a leitura do seu código, deixando uam coisa dentro da outra por meio da identação. Procure sempre identar seu código.



# **PRINCIPAIS TAGS HTML**


## 1. **Estrutura Básica**



- `<!doctype html>`
##### 1. O que significa `<!doctype html>`?
`<!doctype html>` é a forma simplificada de declarar o tipo de documento para HTML5. Ele instrui o navegador a renderizar a página usando o modo de compatibilidade com os padrões do HTML5, que é a versão mais moderna do HTML.
- **`<!DOCTYPE>`**: Este é o começo da declaração e significa "Document Type Declaration" (Declaração de Tipo de Documento). Ele é necessário para que o navegador interprete o HTML corretamente.
- **`html`**: Isso especifica que o tipo de documento é HTML, e não XML, XHTML, ou outro tipo de linguagem de marcação.
##### 2. O `!` significa algo especial?
Sim, o `!` no início da declaração `<!DOCTYPE>` indica que essa linha é uma "declaração", não uma tag HTML comum. Ele serve como uma instrução ao navegador, e é por isso que se utiliza o `!` no começo. Não é algo específico do HTML5 ou HTML em geral, mas é uma convenção de linguagens SGML (a linguagem da qual o HTML deriva).
##### 3. Significa que o arquivo é da última versão do HTML?
Quando você usa `<!doctype html>`, está dizendo ao navegador que esse documento está usando a versão HTML5. Esta é a versão mais recente e recomendada, e essa declaração é a maneira mais simples de indicar isso. Em versões anteriores do HTML, as declarações de tipo de documento eram muito mais complexas, porque os navegadores precisavam de mais informações para processar o conteúdo corretamente.
**Vale lembrar que o `<!doctype html>` é no início do arquivo inteiro, nada vem antes dele.**

- `<html>`: Define o início de um documento HTML.
- `<head>`: Contém metadados, links para estilos e scripts, e o título da página.
- `<title>`: Define o título da página, que aparece na aba do navegador.
- `<body>`: Contém todo o conteúdo visível da página, como texto, imagens, vídeos, etc.




## 2. **Estrutura de Conteúdo**

- `<header>`: Define a seção de cabeçalho da página, geralmente contendo o título, logo, e navegação.

- `<nav>`: Define uma seção de navegação com links. Embora você possa criar navegações sem a tag `<nav>`, usá-la dá mais significado semântico ao código, o que é uma boa prática de desenvolvimento web. Ou seja, ela melhora tanto a organização quanto a experiência do usuário.

- `<main>`: Indica o conteúdo principal da página, é único por documento. Você pode, tecnicamente, criar um documento HTML sem o `<main>` e ele funcionará perfeitamente, porém, usar ela melhora a acessibilidade e o SEO do seu site. Fora que organiza mais ele.

- `<section>`: Seção temática de conteúdo.
- `<article>`: Define um conteúdo independente e autocontido, como um post de blog.
- `<aside>`: Conteúdo relacionado, mas separado do principal, como barras laterais.
- `<footer>`: Seção de rodapé da página, geralmente com informações de copyright ou links adicionais.
- `<details>`: Define uma seção expansível que o usuário pode abrir e fechar.
- `<summary>`: Define o título da seção expansível dentro de `<details>`.
#### Exemplo de `<details>` com `<summary>`:
```
<details>
  <summary>Mais informações</summary>
  <p>Este é o conteúdo adicional que pode ser expandido.</p>
</details>
```




## 3. **Texto e Formatação**

- `<h1>` a `<h6>`: Títulos/Cabeçalhos, sendo `<h1>` o mais importante e `<h6>` o menos. Detalhe: Isso não é "texto grande e pequeno", eles são títulos, onde cada um tem sua ordem de importância.
- `<p>`: Parágrafo de texto. Independente de quantos `enter` você aperte, o parágrafo vai ser escrito sempre na mesma linha, com exceção que você escreva `<br>` no meio, aí ele entende que é uma quebra de linha.
- `<strong>`: Dá ênfase forte ao texto (geralmente negrito).
- `<em>`: Dá ênfase ao texto (geralmente itálico).
- `<br>`: Quebra de linha em um texto.
- `<hr>`: Linha horizontal (divisória).
- `<del>`: Marca o texto com uma linha horizontal no meio, para indicar um texto que deve ser lido, mas não considerado. ~~Assim, por exemplo~~.
- `<ins>`: Sublinha um texto.
- `<sup>`: Eleva o número, como x²⁰+3.
- `<sub>`: Rebaixa o número, como H₂O.
- `<mark>`: Destaca texto (geralmente fundo amarelo).
- `<abbr>`: Define uma abreviação ou acrônimo, fornecendo um texto expandido ao usuário quando o cursor passa sobre a abreviação.
Exemplo de uso do `<abbr>`:
```
<p>O <abbr title="Cascading Style Sheets">CSS</abbr> é usado para estilizar páginas web.</p>
```
- `<bdo dir="ltr">`: Deixa o texto normal, da esquerda para a direita.
- `<bdo dir="rtl">`: Deixa o texto de forma invertida.




## 4. **Listas**

1. `<ul>`: Lista não ordenada (Unordered List) (com marcadores), tipo esse:
- 🠔 Símbolo de bolinha, seria equivalente ao "disc".
O uso da lista não ordenada é para listas onde você não precisa ordernar os itens dela, não tem uma ordem específica, como:
```
<ul>
	<li>Pão</li>
    <li>Leite</li>
    <li>Tomate</li>
    <li>Manteiga</li>
    <li>Arroz</li>
    <li>Feijão</li>
</ul>
```
Ela possui um atributo chamado `type`, ele indica qual o símbolo que vai ser exibido na lista. Ele tem 3 variantes: `disc`, `circle` e `square`:
1) O `disc` representa uma bolinha colorida por dentro, como os símbolos de listagem aqui no Obsidian também. **Símbolo:** • ou ●
2) O `circle` representa uma bolinha vazia por dentro. **Símbolo:** `○`.
3) O `square` representa um quadrado colorido por dentro. **Símbolo:** `■`, só que menor, e dentro do quadrado a cor é preta.
O que fica por padrão é o `disc`.
**Exemplo de uso dos atributos do `<ul>`:**
```
<ul type="square"> <!-- disc circle square -->
	<li>Pão</li>
	<li>Leite</li>
	<li>Tomate</li>
	<li>Manteiga</li>
	<li>Arroz</li>
	<li>Feijão</li>
</ul>
```
Aqui, a lista vai sair com os ícones em formato de quadrado, pois `type="square"`.

2. `<ol>`: Lista ordenada (Ordered List) (Numerada).
É equivalente ao símbolos de listas ordenadas do próprio Obsidian:
1. 🠔 Símbolo de número, seria equivalente ao "`type="1"`".
O uso da lista ordenada é para listas onde você precisa ordenar os itens dela, tem uma ordem específica, quando você adiciona um novo item, você não quer ter que ficar mudando o número deles toda vez, como:
```
<ol>
	<li>Acordar</li>
	<li>Ligar para o João</li>
	<li>Tomar café</li>
	<li>Escovar os dentes</li>
	<li>Ir para a faculdade</li>
	<li>Almoçar</li>
	<li>Ir para o trabalho</li>
	<li>Voltar para casa</li>
	<li>Jantar</li>
    <li>Dormir</li>
</ol>
```
Aqui, a lista vai ser ordenada por números, a saída vai ser:
1. Acordar
2. Ligar para o João
3. Tomar café
4. Escovar os dentes
5. Ir para a faculdade
6. Almoçar
7. Ir para o trabalho
8. Voltar para casa
9. Jantar
10. Dormir
Independente se você adiciona mais um item no ínicio, no meio ou no final da lista, ela sempre vai estar ordenada direitinho.
Ela possui um atributo chamado `type`, ele indica qual é o tipo de ordenação ele vai fazer. Ele tem 4 variantes: 1, A, a, I, i.
1) O `1` indica que a lista vai ser ordenada por números, exatamente como foi mostrado anteriormente.
2) O `A` indica que a lista vai ser ordenada por letras maiúsculas, como:
A. Acordar
B. Ligar para o João
C. Tomar café
etc...
3) O `a` indica que a lista vai ser ordenada por letras minúsculas, como:
a. Acordar
b. Ligar para o João
c. Tomar café
etc...
4) O `I` indica que a lista vai ser ordenada por números romanos em forma maiúscula, como:
I. Acordar
II. Ligar para o João
III. Tomar café
IV. Escovar os dentes
V. Ir para a faculdade
etc...
5) O `i`, por fim, indica que a lista vai ser ordenada por números romanos em forma minúscula, como:
i. Acordar
ii. Ligar para o João
iii. Tomar café
iv. Escovar os dentes
v. Ir para a faculdade
etc...

O padrão de exibição é o `1`.

**Exemplo do uso dos atributos do `<ol>`:**
```
<ol type="I"> <!-- 1 A a I i -->
	<li>Acordar</li>
	<li>Ligar para o João</li>
	<li>Tomar café</li>
	<li>Escovar os dentes</li>
	<li>Ir para a faculdade</li>
	<li>Almoçar</li>
	<li>Ir para o trabalho</li>
	<li>Voltar para casa</li>
	<li>Jantar</li>
	<li>Dormir</li>
</ol>
```
Aqui, a lista vai ser exibida e ordenada com números romanos em maiúsculo, pois `type="I"`.



#### `start=''`
Um outro atributo que as principais duas listas possuem é o `start`. Ele modifica em qual contagem ele vai começar. Se for de números, por exemplo, e eu colocar `start='4'`, o primeiro item da lista vai ter o número 4.
Vale lembrar que para letras, você não indica o `start` por letras também, como `start='c'`, isso é inválido; você deve indicar o `start` com um número, então, como c é a terceira letra do alfabeto, `start='3'`.
```
<ol type="a" start='5'>
            <li>PHP</li>
            <li>Python</li>
            <li>JavaScript</li>
            <li>Kotlin</li>
        </ol>
```
Aqui, PHP vai começar com e, pois é a quinta letra do alfabeto.

### Listas aninhadas
É quando colocamos uma lista dentro da outra. Para criar uma lista dentro da outra, é só você criar a tag da lista normalmente, como faria se não estivesse dentro de uma lista maior, mas agora estando numa lista maior.
**Exemplo:**
```
<h2>Linguagens de Programação Favoritas do Gustavo Guanabara</h2>
    <ol>
        <li>Antigas</li>
        <ol type="a">
            <li>Clipper</li>
            <li>Visual Basic</li>
            <li>Fortran</li>
            <li>Delphi</li>
        </ol>
        <li>Novas</li>
        <ol type="a" start='5'>
            <li>PHP</li>
            <li>Python</li>
            <li>JavaScript</li>
            <li>Kotlin</li>
        </ol>
    </ol>
```
Aqui, a lista maior é a de Linguagens de Programação Favoritas do Gustavo Guanabara, e as sub-listas são as linguagens Antigas e as linguagens Novas.
**Outro exemplo:**
```
<h2>Jogos favoritos do Gustavo Guanabara</h2>
    <ol>
        <li>NES</li>
        <ul type="square">
            <li>Mario Bros</li>
            <ul type="circle">
                <li>Mario Bros 3</li>
                <li>Mario: Lost Levels</li>
            </ul>
            <li>Ninja Gaiden</li>
        </ul>
        <li>SNES</li>
        <ul type="square">
            <li>Mario</li>
            <li>Donkey Kong</li>
        </ul>
        <li>PlayStation</li>
        <ul type="square">
            <li>Final Fantasy</li>
            <li>Castlevania</li>
        </ul>
    </ol>
```


3. `<li>`: Um item de lista. Independente do tipo da lista, todos vão ter o `<li>` nela.

4. `<dl>`: Lista de Definição. Indica um item e sua definição:
```
<dl>
    <dt>HTML</dt>
    <dd>Linguagem de marcação para a criação do conteúdo de um site.</dd>
    <dt>CSS</dt>
    <dd>Linguagem de marcação para a criação do design de um site.</dd>
    <dt>JavaScript</dt>
    <dd>Linguagem de programação para a criação de interatividade de um site.</dd>
</dl>
```
Nas Listas de Definição, os elementos não são indicados por `<li>`, e sim por `<dt>` e `<dd>`, sendo respectivamente, o nome da coisa e sua definição logo em seguida.
Saída da Lista de Definição:
```
HTML
	Linguagem de marcação para a criação do conteúdo de um site.
CSS
	Linguagem de marcação para a criação do design de um site.
JavaScript
	Linguagem de programação para a criação de interatividade de um site.
```




## 5. **Links e Mídia**

- `<a>`: Define um hyperlink (Link). É uma âncora à outro site.
- `href="github.com/queirozz8"`: É o principal atributo de `<a>`, define qual vai ser a URL.
## Caminhos absolutos e relativos
Usando o `href`, você pode fornecer o caminho de algo de forma absoluta, isso é, dizendo o caminho inteiro até chegar no que quer chegar, ou dizendo só a abreviação daquilo. Exemplos:
### Absolutos
- Com arquivos: `C:/Users/Rick/Downloads/Programação/HTML e CSS/coisa.extensao`
- Com links: `https://google.com`
### Relativos
- Com arquivos: `arquivo.extensao`
- Com links: Não dá para indicar um link externo por um caminho relativo.

A questão de um caminho relativo é: geralmente você vai linkar algo assim só quando você estiver em um diretório fixo, seu arquivo não vai mudar de diretório. Pois se você mudar e ainda estiver com o mesmo caminho relativo, o link não será feito. Geralmente você vai usar isso quando o arquivo está próximo do arquivo index.
### Atalhos para indicar arquivos
- `../`: Indicar o diretório pai
- `./`: Indicar o mesmo diretório
- `/diretorio/arquivo.extensao`: O `/diretorio/` é para indicar um subdiretório dentro do diretório onde o index está.



### Qual a linguagem do seu site? Usando o `hreflang`
- `<a href="site.com" hreflang="en">`: `hreflang` Define qual vai ser a língua do outro site em que seu link está associado.

### Você quer que o site do link substitua o site original, ou que ele seja aberto em uma nova guia? Usando o `target`
- `<a href="site.com" target="_self">`: `target="_self"` É o atributo padrão de todos os `href`. Quando o usuário clicar no seu link e ele carregar, ele vai SUBSTITUIR O SITE ANTIGO na mesma página que o usuário estava, ou seja, a página que estava antes é substituída pela que o link estava referenciando. Isso geralmente é bom de se fazer quando o link é um site seu, de sua autoria. Mas quando é um site de outros, você não quer que quando um usuário clique no seu link, ele entre no site, e seu site é esquecido, pois o que antes era seu site, agora foi substituído por o site do link, então o usuário vai fazer uma nova navegação, em um novo site, e o seu site cai em esquecimento por ele, não é isso que queremos. Quando o site em que seu link está referenciando é de outra pessoa, usamos o atributo `_blank`, mais detalhes abaixo.
Quando estamos levando o visitante à outra página dentro do nosso próprio site por meio do link, esse link se chama "Link local" ou "Link interno". Note que não é necessário nem indicar a URL completa nesses casos.

- `<a href="site.com" target="_blank">`: `target="_blank"` É quando o usuário clicar no seu link e ele carregar, ele vai ser exibido em uma GUIA DIFERENTE, ou seja, o site antigo não é substituído. Isso é bom quando o site em que o seu link está referenciando não é seu, e você não quer que quando o usuário clicar no seu link, ele for redirecionado para outro site, o seu "desaparecer" e ele esquecer da navegação antiga que ele estava fazendo (Consequentemente, esquecendo do seu site). Então, nós usamos esse atributo para fazer o link ser exibido em uma outra guia.
Se o link levar o visitante para outro site, o nome desse link é "Link externo". Nesses casos, devemos indicar a URL completa, incluindo o protocolo `http://` ou `https://` e o caminho que leve à uma página específica, se for necessário.

### Esse link é seu ou dos outros? Usando o `rel`:
- `<a href="site.com" rel="next">`: Indica que o link se refere à próxima parte do documento atual.
- `<a href="site.com" rel="prev">`: Indica que o link se refere à parte anterior do documento atual.
- `<a href="site.com" rel="author">`: Indica que é um link para o site do autor do artigo atual.
- `<a href="site.com" rel="external">`: Indica que é um link para outro site que não faz parte do site atual.
- `<a href="site.com" rel="nofollow">`: Indica para o mecanismo de busca, tipo o Google, que não é para ele entrarn esse link e continuar fazendo o trabalho dele no site que seu link referenciou. Isso geralmente é usado para sites patrocinados, você não tem envolvimento nenhum com o site, ele tem o link dele ali, porém não tem nada à ver com você, aí você coloca o `rel="nofollow"`

### Quer criar um link de download? Usando o `download` e o `type`
- `<a href="arquivos/meulivro.pdf" download type="application/pdf">Baixe aqui o PDF do meu livro</a>`: Aqui, `href` é o caminho local do diretório do arquivo HTML até o arquivo que você quer disponibilizar o download. `download` indica qual é a coisa que você quer disponibilizar para download.

`download`: O atributo `download`, resumidamente falando, força o download do arquivo. Ele indica ao navegador que ele deve baixar o arquivo em vez de abrir. Quando você adiciona esse atributo ao link, o arquivo especificado no `href` será baixado automaticamente quando o usuário clicar no link. O `download` pode ou não ter um valor. Se você quiser que o arquivo seja baixado com um nome específico diferente do nome original do arquivo no servidor, você pode especificar isso no atributo `download`, assim:
`<a href="arquivos/meulivro.pdf" download="Livro de Henrique" type="application/pdf">Baixe aqui o PDF do meu livro</a>`. Ao invés do arquivo ter o nome prévio na hora do download de "meulivro.pdf", ele tem o nome de "Livro de Henrique".
A maioria dos navegadores modernos suporta o atributo `download`, mas vale lembrar que ele não funciona em alguns casos específicos, como para links que apontam para recursos externos (diferentes domínios) ou para arquivos que o navegador pode renderizar diretamente (como imagens ou PDFs). Nesses casos, o navegador pode tentar abrir o arquivo em vez de baixá-lo.

O Atributo `application/pdf` e muitos outros podem ser usados em um link para fornecer ao navegador informações adicionais sobre o tipo de arquivo que o link está apontando. Isso é particularmente útil para ajudar o navegador a entender melhor como tratar o arquivo, especialmente em contextos onde o download automático não é obrigatório ou onde se deseja fornecer uma dica sobre o conteúdo do arquivo. O nome do atributo é `type`, mas o valor é chamado de `media type`. 
Lista de `media types` bem usados no dia-a-dia:
1. `application/zip`
2. `text/html`
3. `text/css`
4. `text/javascript`
5. `video/mp4`
6. `video/H264`
7. `video/JPEG`
8. `audio/aac`
9. `audio/mpeg`
10. `font/ttf`
11. `image/jpeg`
12. `image/png`



- `<img>`: Insere uma imagem.
#### Estrutura de imagens:
`<img src="" alt="">`
`img` é a tag. `src` é o conteúdo da imagem. É a URL da imagem, ou o caminho para uma imagem local, etc. `alt` é o texto alternativo que vai ser mostrado caso a imagem não seja exibida, ou o usuário estiver usando leitores de tela, etc.
#### Se você tiver uma imagem no mesmo diretório que o seu `index.html` (Local) e quer exibi-la, você faz assim:
`<img src="html-200.png" alt="Logo HTML5">`
Aqui, eu tinha na mesma pasta, a imagem, com o nome de "html-200.png", então só colocando o nome dela já funciona.
#### Se você tiver uma imagem em um diretório diferente em que o seu `index.html` está, e quer exibi-la, você faz assim:
`<img src="imagens/css-200.png" alt="Logo CSS3">`
Aqui, eu tinha uma pasta chamada "imagens", nela, tinha o arquivo "css-200.png", para eu selecionar um arquivo que não é do mesmo diretório que o `index.html`, eu não posso só digitar o nome dele, eu preciso digitar o caminho antes.
#### Se você quiser exibir uma imagem que está online, na internet, em um outro servidor, você faz assim:
`<img src="https://cdn.iconscout.com/icon/free/png-256/free-javascript-logo-icon-download-in-svg-png-gif-file-formats--html-programming-language-coding-logos-icons-1720087.png" alt="Logo JavaScript">`
Aqui, eu peguei uma imagem que está indexada em um outro servidor, se o servidor cair, essa imagem vai deixar de ser exibida. O que eu basicamente fiz foi copiar o endereço da imagem, ou, quando você abre a imagem em uma nova guia, você copia a URL dela e joga em `src`.

### Height (Altura) e Width (Largura)
As propriedades `height` e `width` em HTML são usadas para definir as dimensões de um elemento na página.

**height**: **A propriedade `height` define a ALTURA de um elemento.** Ela pode ser especificada em diferentes unidades de medida, como pixels (`px`), porcentagem (`%`) ou outras unidades. Por exemplo, `height: 200px;` define a altura do elemento como 200 pixels.

**width**: **A propriedade `width` define a LARGURA de um elemento.** Assim como a `height`, ela pode ser especificada em diferentes unidades de medida, como pixels (`px`), porcentagem (`%`) ou outras unidades. Por exemplo, `width: 50%;` define a largura do elemento como 50% do espaço disponível.

As principais diferenças entre elas são:
1. **Orientação**: A `height` define a dimensão vertical, enquanto a `width` define a dimensão horizontal do elemento.
2. **Aplicação**: Essas propriedades são comumente usadas em elementos como `<div>`, `<img>`, `<video>` e `<iframe>` para controlar suas dimensões.
3. **Comportamento**: Quando apenas uma das propriedades é definida, o elemento assumirá o tamanho padrão do seu conteúdo na outra dimensão. Por exemplo, se definir apenas `width: 100px;`, a altura do elemento será ajustada automaticamente de acordo com o conteúdo.
4. **Responsividade**: Ambas as propriedades podem ser usadas em conjunto com outras técnicas, como media queries, para criar layouts responsivos e adaptáveis a diferentes tamanhos de tela.
Em resumo, `height` e `width` são propriedades complementares que permitem controlar as dimensões de um elemento HTML, sendo a `height` responsável pela dimensão vertical e a `width` pela dimensão horizontal.




- `<picture>`: É uma tag de container que define diversos tamanhos de uma imagem, para cada tamanho de dispositivo, uma imagem diferente vai ser mostrada. 
Pense em uma loja de roupas que oferece diferentes tamanhos de uma mesma camiseta: pequeno, médio e grande. Quando um cliente chega, a loja não sabe qual tamanho será o melhor para ele, então tem que escolher um baseado nas características do cliente, como altura e peso.
Agora, imagine que, na web, o cliente é o dispositivo (computador, tablet, smartphone) e a camiseta é a imagem que você quer mostrar. O problema é que uma imagem grande demais pode demorar para carregar em um celular com conexão lenta, enquanto uma imagem pequena pode ficar borrada em uma tela de alta resolução.
### Estrutura da tag `<picture>`
Aqui está um exemplo básico de como usar a tag `<picture>`:
```
<picture>
  <source media="(min-width: 800px)" srcset="imagem-grande.jpg">
  <source media="(min-width: 400px)" srcset="imagem-media.jpg">
  <img src="imagem-pequena.jpg" alt="Descrição da imagem">
</picture>
```
- **`<picture>`**: Esta é a tag que agrupa todas as versões da imagem.
- **`<source>`**: Cada uma dessas tags define uma versão da imagem. O atributo `media` especifica a condição em que essa imagem deve ser usada. Por exemplo, se a largura da tela for de 800 pixels ou mais (`min-width: 800px`), o navegador usará a imagem `imagem-grande.jpg`.
- **`srcset`**: Este atributo especifica a URL da imagem que será carregada se a condição do `media` for atendida.
- **`<img>`**: Esta é a tag de fallback, que exibe uma imagem padrão (neste caso, `imagem-pequena.jpg`) se nenhuma das condições anteriores for atendida. O `alt` é importante para acessibilidade e SEO.
## Outro exemplo:
```
    <picture>
        <source media="(min-width: 1350px)" srcset="Imagens/Foto-G.png" type="image/png">
        <source media="(min-width: 800px)" srcset="Imagens/Foto-M.png" type="image/png">
        <img src="Imagens/Foto-P.png" alt="Imagem flexível">
    </picture>
```
- `<picture>` é a tag que define que vamos criar uma imagem que tem diversos tamanhos, e ela se adapta de acordo com o dispositivo.
- `<source>` é a tag que define uma versão da imagem. O atributo `media` especifica a condição em que essa imagem deve ser usada. Por exemplo, se a largura da tela for de 800 pixels ou mais (`min-width: 800px`), o navegador usará a imagem `imagem-grande.jpg`.
- `Foto-G`, `Foto-M` e `Foto-P` correspodem ao tamanho grande, médio e pequeno da imagem.

- Se a tela do dispositivo tiver no mínimo 1350px, a imagem exibida vai ser a `Foto-G`.
- Se a tela do dispositivo tiver menos que 1350px, então vamos para a segunda verificação, a linha de baixo, que é: Se a tela tiver no mínimo 800px (Porém tem menos que 1350, pois isso já foi verificado), a imagem exibida vai ser a `Foto-M`.
- E se a tela do dispositivo tiver menos que 800px, então vamos para a terceira opção, a linha de baixo dela, que é equivalente à um `else` da vida. O `else` vai ser sempre a tag `img`. Como a imagem tem menos que 800px e não tem nenhuma outra verificação, usamos o `else`, a imagem que está na tag `img`, não nas `source`. Que consequentemente, é a `Foto-P`.

- `srcset` especifica a URL da imagem que será carregada se a condição do `media` for atendida.

### Quando usar a tag `<picture>`
- **Imagens Responsivas**: Quando você precisa de diferentes versões de uma imagem para diferentes tamanhos de tela, como desktops, tablets e celulares.
- **Imagens Artísticas**: Quando você tem diferentes cortes ou proporções de uma imagem que devem ser exibidos dependendo do dispositivo. Por exemplo, uma imagem mais ampla para desktops e uma versão mais focada para celulares.
- **Compatibilidade com Formatos de Imagem**: Se você quer servir uma imagem em um formato moderno e eficiente, como o WebP, mas ainda oferecer suporte a navegadores que não o suportam, usando uma imagem no formato JPEG ou PNG como fallback.

### Benefícios
1. **Performance**: Carregar a imagem apropriada para o dispositivo reduz o tempo de carregamento e melhora a experiência do usuário.
2. **Flexibilidade**: Dá controle sobre como as imagens são exibidas em diferentes dispositivos, garantindo que a qualidade visual seja mantida.
3. **Acessibilidade e SEO**: Usar a tag `<picture>` corretamente, junto com textos alternativos (`alt`), melhora a acessibilidade do site e pode influenciar positivamente o SEO.




- `<video>`: Insere um vídeo.
## Estrutura básica da tag `<video>`
Aqui está um exemplo simples de como usar a tag `<video>`:
```
<video controls width="500">
    <source src="video.mp4" type="video/mp4">
    <source src="video.webm" type="video/webm">
    Seu navegador não suporta a reprodução de vídeos.
</video>
```
- **`<video controls width="500">`**: Esta é a tag principal que cria o reprodutor de vídeo na página. Vamos detalhar os atributos:
    - **`controls`**: Adiciona os controles de reprodução ao vídeo, como play, pause, volume, e botão de tela cheia. Sem esse atributo, o vídeo será reproduzido automaticamente (ou conforme o atributo `autoplay`), mas o usuário não terá controles visíveis.
    - **`width="500"`**: Define a largura do vídeo em pixels. É opcional, mas útil para controlar o tamanho do vídeo na página.

- **`<source src="video.mp4" type="video/mp4">`**: Define a fonte do vídeo e o tipo de arquivo. O navegador tentará carregar e reproduzir esse vídeo primeiro. Se ele suportar o formato MP4, usará esse arquivo.
- **`<source src="video.webm" type="video/webm">`**: Fornece uma alternativa no formato WebM, caso o navegador não suporte o formato MP4. Isso aumenta a compatibilidade com diferentes navegadores.

- **Texto de fallback**: "Seu navegador não suporta a reprodução de vídeos." Esse texto é exibido se o navegador não conseguir reproduzir nenhum dos formatos de vídeo fornecidos ou não suportar a tag `<video>`. É uma forma de garantir que o usuário entenda que deveria haver um vídeo ali.

## Outro exemplo, agora sem o `<source>`
```
<video src="video.mp4">Seu navegador não tem compatibilidade com reprodução de vídeos.</video>
```
- **`<video src="video.mp4">`**: Define a fonte do vídeo. Como não temos a tag `<source>`, que seria utilizada para disponibilizar diversas versões do arquivo, o único arquivo que é exibido é esse. Caso o navegador não consiga exibir, vai ser exibido "Seu navegador não tem compatibilidade com reprodução de vídeos.", que é o texto de fallback.



### Atributos Comuns da Tag `<video>`
Você usa um atributo assim: `<video src="video.mp4" atributo atributo atributo></video>`
Além dos atributos que vimos no exemplo acima, a tag `<video>` possui outros atributos úteis:

1. **`autoplay`**: Faz com que o vídeo comece a ser reproduzido automaticamente assim que a página é carregada. É importante notar que muitos navegadores modernos bloqueiam a reprodução automática, especialmente se o vídeo tiver som, para evitar experiências intrusivas.
2. **`loop`**: Faz com que o vídeo seja reproduzido em loop, ou seja, ele recomeçará automaticamente sempre que terminar.
3. **`muted`**: Inicia o vídeo sem som. Isso pode ser útil em conjunto com o `autoplay`, pois, como mencionei, muitos navegadores bloqueiam vídeos com som que se reproduzem automaticamente.
4. **`poster`**: Especifica uma imagem que será exibida antes do vídeo começar a ser reproduzido. Isso é útil como uma miniatura ou pré-visualização do vídeo. É a "Thumbnail" do vídeo.
5. **`preload`**: Controla o pré-carregamento do vídeo. Pode ser configurado como:
- **`auto`**: O navegador decide se deve carregar todo o vídeo quando a página é carregada.
- **`metadata`**: Apenas os metadados (como duração e dimensões) são carregados.
- **`none`**: O vídeo não é carregado até que o usuário o reproduza.





- `<audio>`: Insere um áudio.
## Estrutura básica da tag `<audio>`
```
<audio controls>
  <source src="musica.mp3" type="audio/mpeg">
  Seu navegador não suporta o elemento de áudio.
</audio>
```
- **`<audio controls>`**: Isso cria o reprodutor de áudio na página. A palavra `controls` adiciona os botões de play, pause, volume, etc., que o usuário pode usar. Sem essa palavra, o áudio ainda será reproduzido, mas não haverá controles visíveis para o usuário.
    
- **`<source src="musica.mp3" type="audio/mpeg">`**: Aqui, `src="musica.mp3"` define o caminho do arquivo de áudio que será reproduzido. O atributo `type="audio/mpeg"` especifica o formato do arquivo de áudio (neste caso, um MP3). A tag `<source>` permite que você inclua diferentes formatos de áudio para garantir que o som será reproduzido em diferentes navegadores, que podem ter suporte a diferentes formatos.
    
- **Texto entre `<audio>` e `</audio>`**: O texto "Seu navegador não suporta o elemento de áudio." é uma mensagem que será exibida se o navegador do usuário não suportar a tag `<audio>`. Isso é útil como um fallback/else, garantindo que o usuário saiba que deveria haver um áudio ali, mas ele não pode ser reproduzido.


## Outra estrutura, agora sem o `<source>`
```
<audio src="midia/happy-mistake.mp3" controls loop></audio>
```
1. **`<audio src="midia/happy-mistake.mp3">`**: Aqui, o atributo `src="midia/happy-mistake.mp3"` está sendo usado diretamente na tag `<audio>`. Isso significa que o navegador vai buscar e reproduzir o arquivo de áudio localizado no caminho especificado, que neste caso é `midia/happy-mistake.mp3`.
2. **`controls`**: Adiciona os controles de reprodução (play, pause, volume, etc.) ao player de áudio, permitindo que o usuário interaja com o som.
3. **`loop`**: Faz com que o áudio seja reproduzido continuamente em loop, ou seja, ele vai recomeçar automaticamente toda vez que terminar.


### Diferença entre usar `src` na tag `<audio>` e a tag `<source>`
Quando você usa o atributo `src` diretamente na tag `<audio>`, está especificando um único arquivo de áudio para ser reproduzido. Esse é o método mais simples e direto para adicionar som à página, mas ele tem uma limitação importante: se o navegador do usuário não suportar o formato do arquivo especificado (por exemplo, se for um navegador que não suporte o formato MP3), o áudio não será reproduzido.

Por outro lado, quando você usa a tag `<source>`, você pode fornecer várias fontes de áudio com diferentes formatos dentro da tag `<audio>`

### Quando usar cada abordagem?
- **Usar `src` diretamente na tag `<audio>`** é uma solução simples e funciona bem quando você tem certeza de que o formato de áudio escolhido é amplamente suportado pelos navegadores que os usuários do seu site utilizam.
- **Usar a tag `<source>`** é preferível quando você deseja garantir que o áudio será reproduzido no maior número possível de navegadores, especialmente quando você lida com diferentes tipos de dispositivos ou quando o público-alvo pode usar navegadores mais antigos ou menos comuns.


### Atributos da tag `<audio>`
Você usa um atributo assim: `<audio src="audio.mp3" atributo atributo atributo></audio>`
A tag `<audio>` tem vários outros atributos e opções que podem ser utilizados para customizar a experiência de áudio:
1) **`autoplay`**: Faz com que o áudio comece a tocar automaticamente assim que a página é carregada.
2) **`loop`**: Faz com que o áudio seja repetido indefinidamente.
3) **`muted`**: Inicia o áudio sem som.
4) **`preload`**: Controla o pré-carregamento do áudio. Pode ser configurado como:
- **`auto`**: O navegador decide se deve carregar todo o áudio quando a página é carregada.
- **`metadata`**: Apenas os metadados (como duração e dimensões) são carregados.
- **`none`**: O áudio não é carregado até que o usuário o reproduza.





- `<source>`: Especifica múltiplos recursos para elementos de mídia (`<video>` ou `<audio>`).
- `<iframe>`: Insere uma página HTML dentro de outra.




## 6. **Tabelas**

- `<table>`: Define uma tabela.
- `<tr>`: Linha de tabela.
- `<td>`: Célula de tabela.
- `<th>`: Cabeçalho de célula (geralmente negrito e centralizado).
- `<thead>`: Cabeçalho da tabela. É onde o `<th>` fica. Define as categorias da tabela; as colunas.
- `<tbody>`: Corpo da tabela. É onde o `<td>` geralmente fica. Indica o corpo da tabela, o conteúdo principal.
- `<tfoot>`: Rodapé da tabela. É onde o `<td>` fica também, indica o final da tabela; pode ter um total, qualquer coisa ali no fim.
- `<caption>`: Nome da tabela.
- `<colgroup>`: Uma tag container que muda as características das colunas da tabela
- `<rowgroup>`: Uma tag container que muda as características das linhas da tabela.
## Exemplo de tabela simples:
```
    <table>
        <thead>
            <tr>
                <th>Nome</th>
                <th>Idade</th>
            </tr>
        </thead>

  
        <tbody>
            <caption>Pessoas por idade</caption>

            <tr>
                <td>Mayk</td>
                <td>35</td>
            </tr>
            
            <tr>
                <td>Diego</td>
                <td>25</td>
            </tr>


        <tfoot>
            <tr>
                <td>Total:</td>
                <td>2 Pessoas</td>
            </tr>
        </tfoot>
    </table>
```
- Definimos as colunas da tabela com `<th>` dentro do `<thead>`. Suas categorias.
- Definimos o nome da tabela com o `<caption>` dentro do `<tbody>`, que é "Pessoas por idade".
- Definimos as células da tabela com o `<td>` dentro do primeiro `<tr>`. Que são os nomes das pessoas.
- Definimos as células da tabela com o `<td>` dentro do segundo `<tr>`. Que são as idades das pessoas.
- Definimos a última coisa na tabela com o `<td>` dentro de `<tfoot>`. Que são o total de pessoas.

## Exemplo de uma tabela mais complexa:
```
    <table>
        <caption>Produzidos x Vendidos por Loja</caption>


        <colgroup>
            <col>
            <col span="2" style="background-color: red;">
            <col span="2" style="background-color: blue;">
        </colgroup>

		<!-- colspan: Quantas linhas aquela coluna vai possuir -->
        <thead>
            <tr>
                <th rowspan="2"></th>
                <th colspan="2">Afonso Pena</th>
                <th colspan="2">Antônia Pereira</th>
            </tr>
            <tr>
                <th scope="col">Produzidos</th>
                <th scope="col">Vendidos</th>
                <th scope="col">Produzidos</th>
                <th scope="col">Vendidos</th>
            </tr>
        </thead>


        <tbody>
            <tr>
                <th scope="row">Vassouras</th>
                <td>50</td>
                <td>30</td>
                <td>20</td>
                <td>20</td>
            </tr>

            <tr>
                <th scope="row">Baldes</th>
                <td>10</td>
                <td>10</td>
                <td>30</td>
                <td>25</td>
            </tr>
        </tbody>

    </table>
```

- `rowspan` e `colspan`: São atributos que definem quanto espaço uma linha/coluna vai possuir. Sendo `rowspan` para linhas e `colspan` para colunas.



## 7. **Formulários**

- `<form>`: Define um formulário.
- `<input>`: Campo de entrada de dados (texto, senha, etc.).
- `<label>`: Rótulo para um elemento de formulário.
- `<textarea>`: Área de texto multilinhas.
- `<button>`: Botão clicável. Caso queira exibir um botão em baixo de outro, você precisa usar o `<br>`, se não, ele vai mostrar um do lado do outro.
- `<select>`: Menu suspenso.
- `<option>`: Opções dentro do menu suspenso.
- `<fieldset>`: Agrupa elementos de formulário.
- `<legend>`: Legenda para o `<fieldset>`.




## 8. **Semântica e Marcação**

- `<div>`: Container genérico de bloco.
- `<span>`: Container genérico em linha.
- `<code>`: Define um bloco de código, assim, a fonte fica Monoespaçada.
- `<pre>`: Define texto pré-formatado (Não desconsidera os espaços e quebras de linha do texto).
Exemplo de uso do `<pre>` junto com o `<code>`:
```
    <pre>
        <code>
    num = int(input('Digite um número: '))
    if num % 2 == 0:
        print(f'O número {num} é PAR')
    else:
        print(f'O número {num} é ÍMPAR')
    print('Fim do programa')
        </code>
    </pre>
```
- `<q>`: Citação em texto, deixa o texto que estiver dentro dessa tag com aspas duplas, quando você quer fazer algo como uma analogia, entre aspas, você usa as aspas normais, mas caso você queira fazer uma citação ao texto de outra pessoa, você usa o `<q>`.
- `<blockquote>`: Citação em bloco, deixa o texto com uma leve identação para a direita.
- `<cite>`: Referência uma obra (como título de livro ou site).




## 9. **Tags de Metadados**

- `<meta>`: Define metadados sobre a página, como o charset (codificação de caracteres).
1) `charset`: Define o conjunto de caracteres que os navegadores vão interpretar. Alguns navegadores não conseguem interpretar, por exemplo, caracteres japoneses, então nós sempre colocamos o `UTF-8` para que os navegadores que não conseguem adaptar, adaptem.
2) `name`: Especifica qual é esse metadado.
3) `content`: É onde fica a configuração desse metadado, o conteúdo dele.

- `<link>`: Define a relação entre o documento atual e um recurso externo (usado para vincular estilos CSS, por exemplo.).
- `<style>`: Define estilos CSS internos se estiver dentro do `<head>`. Se estiver como um atributo de uma tag, é considerado um CSS Inline.
- `<script>`: Define scripts JavaScript.
- `type`: Pode ser usado em diversas tags para fornecer ao navegador e ao serviço de busca de websites informações adicionais.
##### Como `type` Funciona
O atributo `type` especifica o tipo MIME (Multipurpose Internet Mail Extensions) do recurso apontado pelo link. O tipo MIME é uma forma padrão de indicar o formato do arquivo, o que permite ao navegador ou a outro software saber que tipo de conteúdo ele está lidando e como deve processá-lo.
##### Quando Usar o `type`
O `type` é mais uma dica do que uma obrigação para o navegador. Ele não força o navegador a fazer algo específico, mas pode melhorar a experiência do usuário e a compatibilidade com algumas ferramentas e scripts que possam estar processando o link. Por exemplo:
- **Melhorar a acessibilidade**: Alguns leitores de tela podem usar o `type` para anunciar o tipo de arquivo antes de o usuário clicar no link.
- **Otimização para scripts**: Se você estiver usando JavaScript para manipular links, o `type` pode ser útil para identificar o tipo de arquivo sem ter que analisar a URL.
Por exemplo, o tipo MIME `application/pdf` indica que o recurso é um arquivo PDF. Ao usar isso em um link, você está basicamente informando ao navegador que o arquivo apontado é um PDF.





# **MANIPULANDO ARQUIVOS EM HTML**

### Referenciando um arquivo no mesmo diretório
Se o arquivo se encontra no mesmo diretório em que o `index.html` está, você não precisa digitar o caminho inteiro, só o nome do arquivo.
- Para se referir à um arquivo do mesmo diretório: `<a href="arquivo.extensao">Link para Arquivo</a>`.
### Referenciando um arquivo em um subdiretório:[💀🧑🏼Bloco de Notas de HTML e CSS](💀🧑🏼Bloco%20de%20Notas%20de%20HTML%20e%20CSS.md)
Se o arquivo se encontra em um sub-diretório dentro do diretório em que o `index.html` está, você precisa digitar o sub-diretório e o arquivo que você quer pegar.
- Para se referir à um arquivo num sub-diretório dentro do diretório do arquivo: `<a href="sub-diretorio/arquivo.extensao">Link para Arquivo</a>`.
### Referenciando um arquivo em um diretório pai:
Para se referir à um arquivo em um diretório pai: `<a href="../arquivo.extensao">Link para Arquivo</a>`. Se o arquivo se encontra no diretório pai em que `index.html` está, você digita os `..`, que indica o diretório pai, e digita qual é o arquivo.
### Referenciando um arquivo em um diretório avô (ou mais níveis acima):
Se o arquivo está dois ou mais níveis acima do diretório onde o arquivo HTML está localizado, você usa `..` repetidamente, um para cada nível que você precisa subir.
**Exemplo:** Vamos considerar essa estrutura de diretórios:
```
arquivos/
  ├── arquivo001.txt
  └── arquivos-html/
      └── arquivo-principal/
          └── index.html
```
Aqui, o `index.html` está em `arquivo-principal`, que está dentro de `arquivos-html`, que por sua vez está dentro de `arquivos`. Para acessar o `arquivo001.txt` que está em `arquivos`, você precisaria subir dois níveis:
`<a href="../../arquivo.extensao">Link para Arquivo</a>`
Aqui, cada `..` representa subir um diretório: o primeiro `..` te leva de `arquivo-principal/` para `arquivos-html/`, e o segundo `..` te leva de `arquivos-html/` para `arquivos/`, onde `arquivo001.txt` está localizado.

### Referenciando um arquivo em um subdiretório de um diretório pai:
Se o arquivo está em um subdiretório de um diretório pai, você primeiro sobe para o diretório pai e depois desce no subdiretório desejado.
**Exemplo:** Vamos dizer que dentro do diretório `arquivos` exista um subdiretório chamado `docs`, e você queira acessar um arquivo chamado `arquivo002.txt` dentro de `docs`. A estrutura seria assim:
```
arquivos/
  ├── docs/
  │   └── arquivo002.txt
  └── arquivos-html/
      └── arquivo-principal/
          └── index.html
```
Para referenciar `arquivo002.txt` a partir de `index.html`, você faria: `<a href="../../docs/arquivo002.txt">Link para Arquivo</a>`


## Referenciando um arquivo a partir de um caminho absoluto:
### Caminho Absoluto no Sistema de Arquivos Local
Em um ambiente de sistema de arquivos local (como no Windows), um **caminho absoluto** refere-se ao caminho completo, desde a raiz do sistema de arquivos até o arquivo. No Windows, esse caminho normalmente começa com a letra da unidade (por exemplo, `C:\`). Por exemplo, se você tem um arquivo `arquivo001.txt` em `C:\Users\SeuNome\Documentos`, o caminho absoluto seria: `C:\Users\SeuNome\Documentos\arquivo001.txt`
### Caminho Absoluto no Contexto da Web
Em HTML, quando falamos de um **caminho absoluto**, geralmente nos referimos ao caminho completo a partir da raiz do servidor web, **não** do sistema de arquivos local. Esse caminho absoluto começa com uma barra (`/`), indicando a raiz do servidor, e continua pelo caminho da pasta no servidor.

Por exemplo, suponha que você tem um servidor web Apache, a estrutura dele é assim:
```
/var/www/html/
├── arquivo001.txt
└── arquivos principais/
    ├── arquivos html/
        └── index.html
    └── (Outros arquivos e diretórios)
```
Você, do `index.html`, quer referenciar pelo `href` o `arquivo001.txt`. Como faria isso com caminhos absolutos?
Para referenciar o `arquivo001.txt` a partir de `index.html` usando um caminho absoluto no contexto da web, você faria o seguinte: `<a href="/arquivo001.txt">Link para arquivo001</a>`
- **`/arquivo001.txt`**: Aqui, o `/` no início do caminho indica que o navegador deve começar a busca desde a raiz do servidor web, que é o diretório `/var/www/html/`.
- **`arquivo001.txt`**: Como `arquivo001.txt` está diretamente na raiz do diretório de documentos (`/var/www/html/`), você pode simplesmente colocar `/arquivo001.txt`.
Qual a vantagem de usar caminhos absolutos? Este link funcionará independentemente de onde o `index.html` esteja localizado dentro da estrutura de diretórios do servidor, pois ele usa o caminho absoluto da raiz do servidor.





# **HTML ENTITIES**

## Caracteres Especiais Comuns
- **&**: `&amp;` : E comercial
- **<**: `&lt;` : Menor que
- **>**: `&gt;` : Maior que
- **"**: `&quot;` : Aspas duplas
- **'**: `&apos;` : Aspas simples (Apóstrofo) (Não suportado em HTML4)


## Acentos e Letras Especiais
- **Á**: `&Aacute;` : Letra A com acento agudo
- **á**: `&aacute;` : Letra a com acento agudo
- **É**: `&Eacute;` : Letra E com acento agudo
- **é**: `&eacute;` : Letra e com acento agudo
- **Í**: `&Iacute;` : Letra I com acento agudo
- **í**: `&iacute;` : Letra i com acento agudo
- **Ó**: `&Oacute;` : Letra O com acento agudo
- **ó**: `&oacute;` : Letra o com acento agudo
- **Ú**: `&Uacute;` : Letra U com acento agudo
- **ú**: `&uacute;` : Letra u com acento agudo
- **Ç**: `&Ccedil;` : Letra C com cedilha
- **ç**: `&ccedil;` : Letra c com cedilha
- **Ñ**: `&Ntilde;` : Letra N com til
- **ñ**: `&ntilde;` : Letra n com til
- **Ü**: `&Uuml;` : Letra U com trema
- **ü**: `&uuml;` : Letra u com trema


## Símbolos Matemáticos
- **±**: `&plusmn;` : Mais ou menos
- **÷**: `&divide;` : Divisão
- **×**: `&times;` : Multiplicação
- **√**: `&radic;` : Raiz quadrada
- **≤**: `&le;` : Menor ou igual
- **≥**: `&ge;` : Maior ou igual
- **≠**: `&ne;` : Diferente de
- **≈**: `&asymp;` : Aproximadamente igual
- **Δ**: `&Delta;`: Delta (Triângulo, popularmente conhecido)
- **δ**: `&delta;`: Delta (Caractere grego)


## Moedas
- **$**: `&dollar;` : Dólar
- **€**: `&euro;` : Euro
- **£**: `&pound;` : Libra esterlina
- **¥**: `&yen;` : Iene
- **¢**: `&cent;` : Centavo


## Outros Símbolos Úteis
- **©**: `&copy;` : Copyright
- **®**: `&reg;` : Marca registrada
- **™**: `&trade;` : Marca registrada (trademark)
- **§**: `&sect;` : Símbolo de seção
- **°**: `&deg;` : Graus
- **¶**: `&para;` : Parágrafo
- **∞**: `&infin;` : Infinito
- **♥**: `&hearts;` : Coração
- **↑**: `&uparrow;` ou `&uarr;`: Seta para Cima
- **↓**: `&downarrow;` ou `&darr;`: Seta para Baixo
- **←**: `&leftarrow;` ou `&larr;`: Seta para Esquerda
- **→**: `&rightarrow;` ou `&rarr;`: Seta para Direita




# **ADICIONANDO EMOJIS EM HTML**

Quando for adicionar emojis, só copiar a imagem e jogar num texto HTML pode funcionar, mas nem sempre funciona para todos os navegadores, o mais correto a se fazer é usar os HTML Entities, assim:

1) Vá para `https://www.emojipedia.org`;
2) Pesquise o emoji que deseja adicionar;
3) Acesse a página dele, como por exemplo, o Nerd Face: `https://emojipedia.org/nerd-face#emoji`;
4) Entre nas informações técnicas dele: `https://emojipedia.org/nerd-face#technical`;
5) Em CodePoint, vai ter geralmente uma `letra+número`, ex: `u+1F913`, copie o hexadecimal do emoji, ou seja, todos os números que vem depois do `+`: `1F913`;
6) Vá no texto HTML, e escreva sempre `&#x`, depois, é só colar o número copiado, ficando assim: `&#x1F913`.




# **ESCREVENDO COMENTÁRIOS EM HTML**

Para escrever comentários em HTML, você digita:
1. `/*Comentário!*/`, você pode pular linhas no código, comentar qualquer coisa.
2. `<!--Comentário!-->`, você pode pular linhas no código, comentar qualquer coisa.







# **CSS (CASCADING STYLE SHEETS)**
CSS, ou **Cascading Style Sheets**, é uma linguagem de estilo usada para descrever a apresentação de um documento escrito em HTML ou XML. Pense no HTML como a estrutura básica de uma casa, enquanto o CSS é a pintura, decoração e design que tornam essa casa atraente e funcional.


# **ESTRUTURA DE UMA REGRA CSS**

Cada regra CSS é composta por duas partes principais:
1. **Seletor**: Identifica quais elementos HTML a regra vai estilizar.
2. **Declaração**: Define o estilo que será aplicado a esses elementos. A declaração, por sua vez, é dividida em:
    - **Propriedade**: Especifica a característica do elemento que você quer modificar (como cor, tamanho, etc.).
    - **Valor**: Define o que essa característica deve ser (por exemplo, azul, 16px, etc.).

Vamos olhar para um exemplo:
```
p {
    color: blue;
    font-size: 16px;
}
```
Aqui, temos uma regra CSS que estiliza todos os elementos `<p>` (parágrafos) de uma página.

- **Seletor**: `p`: este é o seletor, que indica que a regra se aplica a todos os elementos `<p>`.
- **Declarações**: Entre as chaves `{ }`, temos duas declarações:
    - `color: blue;`: Propriedade `color` com o valor `blue` (definindo a cor do texto como azul).
    - `font-size: 16px;`: Propriedade `font-size` com o valor `16px` (definindo o tamanho da fonte como 16 pixels).


# SELETOR
O seletor é como a "porta de entrada" para a regra CSS. Ele diz ao navegador onde aplicar as regras de estilo. Se compararmos uma página HTML a uma casa cheia de móveis, os seletores seriam como etiquetas nos móveis, dizendo o que deve ser pintado de azul, o que deve ser ampliado, etc.

Há vários tipos de seletores:
- **Seletores de Tipo**: Aplica estilos a todos os elementos de um determinado tipo. No exemplo acima, `p` é um seletor de tipo que seleciona todos os parágrafos.
- **Seletores de Classe**: Aplica estilos a elementos que possuem uma classe específica. Exemplo:
```
.botao {
    background-color: green;
}
```
Isso aplicaria um fundo verde a qualquer elemento com a classe `botao`.

- **Seletores de ID**: Aplica estilos a um único elemento com um ID específico. Exemplo:
```
#menu {
    border: 1px solid black;
}
```
Isso aplicaria uma borda preta ao elemento com o ID `menu`.

- **Seletores de Atributo**: Aplica estilos a elementos com um atributo específico. Exemplo:
```
input[type="text"] {
    border: 2px solid gray;
}
```
Isso aplicaria uma borda cinza a qualquer campo de entrada com o atributo `type="text"`.


# DECLARAÇÃO
Dentro da declaração, temos as propriedades e valores. Podemos pensar nas propriedades como "características" dos elementos que queremos alterar, como a cor, o tamanho da fonte, as margens, etc. O valor é simplesmente a nova definição para essa característica.

Por exemplo, se pensarmos em um elemento HTML como uma caixa de texto, a propriedade seria o rótulo que diz o que estamos alterando ("cor da caixa") e o valor seria a cor específica que queremos usar ("azul").


## Resumo com uma Analogia
Imagine que você é um designer de interiores e está encarregado de decorar uma casa inteira (a página HTML). As regras CSS são suas instruções:

- **Seletor**: Escolhe quais móveis (elementos) você vai decorar.
- **Propriedade**: Define o aspecto específico da decoração (cor, tamanho, etc.).
- **Valor**: Determina o que exatamente você vai fazer com esse aspecto (pintar de azul, aumentar para 16px, etc.).

Quando há várias instruções conflitantes, você decide qual seguir com base na especificidade e importância (quem fez a encomenda mais específica ou importante).





# **COMO O CSS É APLICADO**
Existem três maneiras principais de aplicar CSS a um documento HTML: **inline**, **interno** (ou embutido) e **externo**. Cada uma tem seus usos específicos.
## 1) Estilo Inline
O CSS inline é aplicado diretamente ao elemento HTML usando o atributo `style`. É como se você estivesse pintando uma parede de um cômodo específico na casa sem afetar outras paredes.
### Exemplos de Estilos Inline:
`<p style="color: blue; font-size: 14px;">Este texto é azul e tem 14px de tamanho.</p>`
`<h1 style="color: mediumblue; background-color: dodgerblue; font-size: 1.5em;"">Capítulo 2</h1>`

**Quando usar:** Estilos inline são úteis para alterações rápidas ou quando se deseja aplicar uma única regra de estilo a um único elemento. No entanto, não é ideal para manutenções grandes ou para garantir consistência em projetos maiores. Deixa o seu arquivo HTML todo poluído, e inviável para projetos minimamente maiores.



## 2) Estilo Interno (Embedded)
O CSS interno é colocado dentro da tag `<style>` no cabeçalho (`<head>`) do documento HTML. Isso é como aplicar um estilo a todas as paredes de um único cômodo da casa, sem afetar os outros cômodos.

Exemplo:
```
<head>
    <style>
        p {
            color: green;
            font-size: 16px;
        }
    </style>
</head>
```

**Quando usar:** Útil quando se deseja estilizar uma única página de maneira específica, sem a necessidade de reaproveitar os estilos em outras páginas. É ruim caso você tenha muitas páginas e queira ter a memsa configuração de cores em todas elas, pois você teria que copiar o `<style>` para todos os arquivos HTML. É ruim também quando o `<style>` é muito longo, que o desenvolvedor precisa ir lá para baixo no código para aí sim ver o código HTML de fato, pois o `<style>` é bem grande. Pàra resolver esses problemas, utilizamos o Estilo Externo.



## 3) Estilo Externo

O CSS externo é armazenado em um arquivo separado com a extensão `.css` e vinculado ao HTML usando a tag `<link>`. Isso é como ter um guia de design central para toda a casa, garantindo que todos os cômodos sigam a mesma estética.

Exemplo do arquivo HTML:
```
<head>
    <link rel="stylesheet" href="styles.css">
</head>
```
Exemplo do arquivo `styles.css`:
```
p {
    color: red;
    font-size: 18px;
}
```


**Quando usar:** Ideal para projetos grandes, onde a consistência é fundamental. Facilita a manutenção e reaproveitamento de estilos em múltiplas páginas.

### Casos de uso de cada CSS:
- **Todos os `<h1>` na página com a mesma cor**: Use CSS interno.
- **Vários `<h1>` com cores diferentes**: Use classes para definir estilos diferentes, e aplique essas classes aos `<h1>` conforme necessário.
- **Um `<h1>` específico com estilo único**: Use um ID se for o único elemento que precisa desse estilo na página.






# **PROPRIEDADES CSS**
CSS tem centenas de propriedades que podem ser usadas para alterar a aparência dos elementos.


## 1. **Cores e Fundos**

- `color`: Define a cor do texto. Exemplo: `color: #ff0000;` (vermelho)
- `background-color`: Define a cor de fundo de um elemento. Exemplo: `background-color: #f0f0f0;` (cinza claro)
- `background-image`: Define uma imagem como fundo de um elemento. Exemplo: `background-image: url('imagem.jpg');`
Você consegue colorir coisas em degradê com o `background-image` também. Usando funções do CSS:
### `Linear-Gradient` (Degradê Linear):
**O que é?** Imagine um pôr-do-sol, onde o céu muda suavemente de uma cor para outra em uma linha reta, de cima para baixo ou de lado a lado. No CSS, você pode definir essa transição de cores ao longo de uma linha (ou eixo) especificando um `linear-gradient`.
**Exemplo:**
`background-image: linear-gradient(to right, red, yellow);`
Isso cria um degradê que começa com a cor vermelha à esquerda e muda suavemente para amarelo à direita.
Você pode indicar a direção por grau também, como:
`background-image: linear-gradient(90deg, red, yellow);`
### `Radial-Gradient` (Degradê Radial):
 **O que é?**
 Agora, imagine que você está olhando para uma luz em uma sala escura, onde o brilho se espalha em todas as direções a partir do centro. Um degradê radial funciona assim: as cores mudam suavemente do centro para as bordas.
**Exemplo:**
`background-image: radial-gradient(circle, red, yellow);`
Aqui, o degradê começa com a cor vermelha no centro e se transforma em amarelo nas bordas, em um formato circular.



- `background-repeat`: Controla como a imagem de fundo é repetida. Valores: `repeat`, `repeat-x`, `repeat-y`, `no-repeat` Exemplo: `background-repeat: no-repeat;`
- `background-position`: Define a posição inicial da imagem de fundo. Exemplo: `background-position: center top;`
- `background-attachment`: Controla como o plano de fundo se comporta ao rolar a página.
Imagine que você colou um grande pôster na parede de um quarto. O `background-attachment` controla o comportamento desse "pôster" (ou seja, o plano de fundo) quando você rola a página (ou anda pelo quarto).
Existem três valores principais para `background-attachment`:
1. **scroll:**
    - **O que é?** Pense nisso como um pôster colado na parede que se move junto com você quando você anda pela sala. Quando você rola a página, o plano de fundo se move junto com o conteúdo.
    - **Exemplo:**
`background-attachment: scroll;`
Isso é o comportamento padrão. À medida que você rola a página, o plano de fundo se move junto.

- **fixed:**  
    - **O que é?** Agora, imagine que o pôster está colado à janela. Quando você anda pelo quarto, o pôster não se move – ele permanece fixo na janela. Em CSS, `background-attachment: fixed;` faz com que o plano de fundo fique "preso" à janela do navegador. Ele não se move quando você rola a página.
    - **Exemplo:**
`background-attachment: fixed;`
Aqui, o plano de fundo fica parado enquanto o conteúdo da página rola sobre ele.

- **local:**   
    - **O que é?** Imagine que o pôster está colado ao chão e você coloca um tapete transparente sobre ele. Quando você rola o tapete, o pôster se move junto. Esse é o comportamento de `background-attachment: local;`. O plano de fundo se move apenas dentro da área de rolagem do elemento ao qual está aplicado.
    - **Exemplo:**
`background-attachment: local;`
O plano de fundo se moverá junto com o conteúdo do elemento, mas apenas dentro da área de rolagem do próprio elemento.



- `opacity`: Define a opacidade de um elemento (0 a 1). Exemplo: `opacity: 0.5;` (50% opaco)




## 2. **Texto e Fontes**

- `font-family`: Define a família da fonte. Exemplo: `font-family: Arial, Helvetica, sans-serif;`
Quando você coloca uma fonte na `font-family`, algum dispositivo que está acessando o seu site pode não ter aquela fonte disponível, então nós colocamos mais de uma fonte na `font-family` por questões de segurança. Primeiro, o HTML tenta com a primeira fonte da esquerda para a direita; depois a seguinte, até chegar na última (é bom você colocar algo genérico na última, tipo "sans-serif", "serif" ou "monospace").
- `font-size`: Define o tamanho da fonte. Exemplo: `font-size: 16px;`
- `font-weight`: Define a espessura da fonte. Valores: `lighter`, `normal`, `bold`, `bolder`, `100` a `900` Exemplo: `font-weight: bold;`. 
`lighter` é o menor valor, `bolder` é o maior. Nem todas as fontes possuem todas essas variantes, geralmente é o `normal` e o `bold` que a maioria tem.

- `font-style`: Define o estilo da fonte. Valores: `normal`, `italic`, `oblique` Exemplo: `font-style: italic;`. Essa propriedade geralmente é utilizada quando não queremos dar um significado semântico para um determinado texto, só queremos modificar como eles ficam. Eles são diferentes do `<em>`, `<strong>` ou `<ins>`, que além de deixar o texto com uma aparência diferente, também dão um significado semântico ao texto.

- `text-align`: Alinha o texto horizontalmente. Valores: `left`, `right`, `center`, `justify` (Ocupe toda a largura disponível do contêiner, distribuindo os espaços entre as palavras de forma que o texto fique alinhado tanto à esquerda quanto à direita.) Exemplo: `text-align: center;`

- `text-decoration`: Define decorações no texto. Valores: `none`, `underline`, `overline`, `line-through` Exemplo: `text-decoration: underline;`.
- `line-height`: Define a altura da linha. Exemplo: `line-height: 1.5;`
- `font`: É usada para definir as propriedades da fonte de forma abreviada, com o shorthand. Exemplo: `font: italic bolder 3em 'Work Sans', sans-serif;`. Vale lembrar que a ordem é sempre: 
font-style -> font-weight -> font-size -> font-family




## 3. **Layout e Posicionamento**

- `display`: Define como um elemento deve ser exibido. Valores comuns: `block`, `inline`, `inline-block`, `flex`, `grid`, `none` Exemplo: `display: flex;`
- `position`: Define o método de posicionamento de um elemento. Valores: `static`, `relative`, `absolute`, `fixed`, `sticky` Exemplo: `position: absolute;`
- `top`, `right`, `bottom`, `left`: Define a posição de elementos posicionados. Exemplo: `top: 10px; left: 20px;`
- `float`: Posiciona um elemento à esquerda ou direita de seu container. Valores: `left`, `right`, `none` Exemplo: `float: left;`
- `clear`: Controla o comportamento de elementos ao lado de elementos flutuantes. Valores: `left`, `right`, `both`, `none` Exemplo: `clear: both;`




## 4. **Dimensões**

- `width`: Define a largura de um elemento. Exemplo: `width: 300px;` ou `width: 50%;`
- `height`: Define a altura de um elemento. Exemplo: `height: 200px;`
### Aspect Ratio calculado pelos navegadores
O _aspect ratio_ é simplesmente a proporção entre a largura (width) e a altura (height) de uma imagem ou de qualquer outro elemento retangular. Imagine que você tem uma foto e quer ampliá-la ou reduzi-la. Para garantir que ela não fique distorcida, é importante manter a mesma proporção entre a largura e a altura. Esse relacionamento é o que chamamos de _aspect ratio_.

Por exemplo, se você tem uma imagem com 800 pixels de largura e 400 pixels de altura, o _aspect ratio_ dessa imagem seria 800:400 ou, simplificando, 2:1. Isso significa que a largura é o dobro da altura.

### Como o Aspect Ratio Funciona em HTML?
Quando você define apenas uma dimensão (largura ou altura) de uma imagem em HTML, o navegador automaticamente calcula a outra dimensão para manter o _aspect ratio_ original da imagem. Isso é importante para evitar que a imagem fique distorcida.

Imagine que você tenha uma imagem com 600 pixels de largura e 300 pixels de altura (um _aspect ratio_ de 2:1). Se você definir a largura dessa imagem em 300 pixels no HTML e não definir a altura, o navegador calculará automaticamente a altura como 150 pixels. Isso mantém o _aspect ratio_ original (2:1), já que 300 pixels de largura ainda são o dobro da altura (150 pixels).

### Exemplo Prático
`<img src="imagem.jpg" width="300">`
Nesse caso, o HTML sabe a largura, mas não a altura. Então, ele vai calcular a altura usando o _aspect ratio_ da imagem original. Se a imagem original for 600x400 pixels (um _aspect ratio_ de 3:2), a altura calculada seria 200 pixels. Isso acontece porque, para manter a proporção de 3:2, se a largura foi reduzida para 300 pixels (metade da original), a altura também precisa ser reduzida para metade, resultando em 200 pixels.

### Como Calcular Aspect Ratio
Quando sabemos o Aspect Ratio de uma imagem, e queremos calcular a outra parte dela (Por exemplo: Tenho o tamanho do Width e quero saber o Height num aspect ratio de 4:3), temos 2 fórmulas:

1. Descobrir o Height (Altura): 
Fórmula: Altura = Largura / (Aspect Ratio X / Aspect Ratio Y)

- Aspect Ratio(X) / Aspect Ratio(Y) = num. Pegue esse num.
- Width / num = Height
Ex: Aspect Ratio de 16:9, Width de 800px:
- 16 / 9 = 1.777...8
- 800 / 1.7778 = 450
O Width já era 800px, o Height é 450px com um Aspect Ratio de 16:9.


2. Descobrir o Width (Largura):
Fórmula: Largura = Altura * (Aspect Ratio(X) / Aspect Ratio(Y))

- Aspect Ratio(X) / Aspect Ratio(Y) = num. Pegue esse num.
- Height * num = Width
Ex: Aspect Ratio de 4:3, Height de 800px:
- 4 / 3 = 1.333...
- 800 * 1.333 = 1066
O Height já era 800px, o Width é 1066px com um Aspect Ratio de 4:3


### Por que isso é importante?
Manter o _aspect ratio_ garante que a imagem não seja distorcida. Se você alterar a largura e a altura de uma imagem de forma independente, sem manter a proporção correta, a imagem pode parecer achatada ou esticada, o que geralmente não é desejável.



- `max-width`, `max-height`: Define a largura/altura máxima. Exemplo: `max-width: 1000px;`
- `min-width`, `min-height`: Define a largura/altura mínima. Exemplo: `min-height: 100px;`
- `aspect-ratio`: Define explicitamente qual será o Aspect Ratio de qualquer elemento HTML.
### Aspect Ratio manual por CSS
1. Definição básica:
`aspect-ratio` define a proporção preferida entre a largura e a altura de um elemento.

2. Sintaxe: `aspect-ratio: width / height;`

3. Funcionalidade principal:
- Mantém uma proporção consistente do elemento enquanto uma de suas dimensões muda.
- Útil para criar layouts responsivos sem distorção.

4. Comportamento:
- Se a largura é definida, a altura é automaticamente calculada (e vice-versa).
- Se ambas as dimensões são definidas, `aspect-ratio` age como uma sugestão, mas não sobrescreve dimensões explícitas.

5. Casos de uso comuns:
- Vídeos e players de mídia responsivos
- Imagens de fundo que mantêm proporção
- Cards ou contêineres de conteúdo uniformes
- Layouts de grade com células proporcionais

**Exemplo prático:**
```
.video-container {
  width: 100%;
  aspect-ratio: 16 / 9;
}
```
Isso criará um contêiner que sempre manterá uma proporção de 16:9, independente da largura da tela.

6. Flexibilidade:
- Pode ser usado com valores fracionários ou decimais.
- Suporta a palavra-chave `auto` para usar as dimensões intrínsecas do elemento.

7. Compatibilidade:
- É uma propriedade relativamente nova, então é importante verificar o suporte do navegador.
- Existem fallbacks e polyfills para navegadores mais antigos.

8. Diferença do cálculo automático de imagens:
- Enquanto navegadores calculam automaticamente o aspect ratio para imagens `<img>`, `aspect-ratio` permite controlar explicitamente as proporções de qualquer elemento HTML.

9. Combinação com outras propriedades:
- Frequentemente usado em conjunto com `object-fit` para controlar como o conteúdo se ajusta dentro do elemento.

`aspect-ratio` é particularmente útil para criar layouts responsivos e consistentes, especialmente em designs que requerem proporções específicas em diferentes tamanhos de tela.

### Diferenças entre o Cálculo automático do navegador e a propriedade CSS `aspect-ratio`
1. Cálculo automático do navegador:
- Aplica-se principalmente a elementos `<img>` e `<video>`.
- Baseia-se nas dimensões intrínsecas do conteúdo (por exemplo, o tamanho real da imagem).
- Ocorre automaticamente quando apenas uma dimensão (largura ou altura) é especificada.
- Mantém a proporção original do conteúdo.

2. Propriedade `aspect-ratio`:
- Pode ser aplicada a qualquer elemento HTML.
- Define uma proporção desejada, independente do conteúdo.
- Oferece controle explícito sobre a proporção do elemento.
- Funciona mesmo quando o elemento não tem conteúdo intrínseco.

Vantagens do `aspect-ratio`:
1. Flexibilidade: Permite definir proporções para elementos que não têm dimensões intrínsecas, como `<div>s` ou outros contêineres.
2. Consistência de layout: Ajuda a manter proporções consistentes em todo o design, mesmo para elementos não-mídia.
3. Prevenção de layout shift: Pode reservar espaço para conteúdo antes que ele carregue, reduzindo mudanças bruscas no layout.
4. Responsividade avançada: Facilita a criação de layouts complexos que mantêm proporções específicas em diferentes tamanhos de tela.
5. Performance: Pode melhorar o desempenho ao evitar recálculos de layout durante o carregamento da página.
6. Controle preciso: Permite especificar proporções exatas que podem não corresponder às dimensões originais do conteúdo.
7. Aplicação a elementos gerados: Útil para elementos criados dinamicamente via JavaScript ou para componentes de UI.
8. Combinação com outras propriedades CSS: Trabalha bem com `object-fit`, `min-height`, `max-width`, etc., para layouts mais sofisticados.

Exemplo prático da diferença:
```
<!-- Cálculo automático do navegador -->
<img src="imagem.jpg" width="300">

<!-- Usando aspect-ratio -->
<div style="width: 300px; aspect-ratio: 16 / 9; background: url('imagem.jpg') center/cover;">
</div>
```
- No primeiro caso, a altura da imagem será calculada automaticamente com base na largura especificada e nas dimensões originais da imagem.
- No segundo caso, o `<div>` terá sempre uma proporção de 16:9, independentemente das dimensões da imagem de fundo.

Em resumo, enquanto o cálculo automático do navegador é conveniente para imagens e vídeos simples, `aspect-ratio` oferece um controle mais fino e versátil sobre as proporções dos elementos, sendo especialmente útil para layouts complexos e responsivos.




## 5. **Margens, Preenchimento e Bordas**

- `margin`: Define a margem externa de um elemento. Exemplo: `margin: 10px;` ou `margin: 10px 20px 30px 40px;` (top, right, bottom, left)
- `padding`: Define o preenchimento interno de um elemento. Exemplo: `padding: 15px;` ou `padding: 5px 10px;` (vertical, horizontal)
- `border`: Define a borda de um elemento. Exemplo: `border: 1px solid black;`
- `border-radius`: Arredonda os cantos de um elemento. Exemplo: `border-radius: 5px;`




## 6. **Flexbox**

- `flex-direction`: Define a direção dos itens flex. Valores: `row`, `row-reverse`, `column`, `column-reverse` Exemplo: `flex-direction: column;`
- `justify-content`: Alinha itens flex ao longo do eixo principal. Valores: `flex-start`, `flex-end`, `center`, `space-between`, `space-around` Exemplo: `justify-content: space-between;`
- `align-items`: Alinha itens flex ao longo do eixo transversal. Valores: `flex-start`, `flex-end`, `center`, `baseline`, `stretch` Exemplo: `align-items: center;`
- `flex-wrap`: Controla se os itens flex devem quebrar linha. Valores: `nowrap`, `wrap`, `wrap-reverse` Exemplo: `flex-wrap: wrap;`




## 7. **Grid**

- `grid-template-columns`: Define as colunas de um grid. Exemplo: `grid-template-columns: 1fr 1fr 1fr;` (três colunas iguais)
- `grid-template-rows`: Define as linhas de um grid. Exemplo: `grid-template-rows: 100px auto;`
- `grid-gap`: Define o espaçamento entre células do grid. Exemplo: `grid-gap: 10px;`
- `grid-column`, `grid-row`: Posiciona um item em uma célula específica do grid. Exemplo: `grid-column: 1 / 3;` (ocupa da coluna 1 à 3)




## 8. **Transições e Animações**

- `transition`: Define uma transição suave entre estados de um elemento. Exemplo: `transition: all 0.3s ease;`
- `animation`: Define uma animação para um elemento. Exemplo: `animation: slidein 3s ease-in-out infinite;`




## 9. **Visibilidade e Overflow**

- `visibility`: Controla se um elemento é visível ou não. Valores: `visible`, `hidden` Exemplo: `visibility: hidden;`
- `overflow`: Define o que acontece quando o conteúdo é maior que o container. Valores: `visible`, `hidden`, `scroll`, `auto` Exemplo: `overflow: auto;`




## 10. **Outros**

- `cursor`: Define o tipo de cursor do mouse. Valores: `default`, `pointer`, `text`, `not-allowed`, etc. Exemplo: `cursor: pointer;`
- `z-index`: Controla a ordem de empilhamento de elementos posicionados. Exemplo: `z-index: 100;`
- `box-shadow`: Adiciona sombra a um elemento. Exemplo: `box-shadow: 2px 2px 5px rgba(0,0,0,0.3);`
- `transform`: Aplica transformações 2D ou 3D a um elemento. Exemplo: `transform: rotate(45deg);`






# **AT-RULES**
As regras at-rules (`@rules`) em CSS são comandos especiais que controlam como as folhas de estilo devem ser processadas.

## 1. **Importação e Encapsulamento**

- **`@import`**: Importa uma folha de estilo externa. Exemplo: `@import url('styles.css');`
- **`@namespace`**: Define um namespace para seletores XML, usado principalmente com SVG. Exemplo: `@namespace svg url('http://www.w3.org/2000/svg');`


## 2. **Consultas de Mídia**

- **`@media`**: Aplica estilos condicionais com base nas características do dispositivo (tamanho da tela, resolução, etc.). Exemplo: `@media (max-width: 768px) { ... }`
- **`@supports`**: Aplica estilos condicionais baseados no suporte do navegador para uma propriedade CSS específica. Exemplo: `@supports (display: grid) { ... }`


## 3. **Fontes**

- **`@font-face`**: Define uma fonte personalizada para uso na página, mesmo que não esteja instalada no dispositivo do usuário. Exemplo:
```
@font-face {
    font-family: 'MinhaFonte';
    src: url('minha-fonte.woff2') format('woff2');
}
```


## 4. **Animações**

- **`@keyframes`**: Define uma animação CSS, especificando as etapas da animação. Exemplo:
```
@keyframes nomeAnimacao {
    from { opacity: 0; }
    to { opacity: 1; }
}
```


## 5. **Páginas e Impressão**

- **`@page`**: Controla a aparência de documentos impressos, como margens e tamanho da página. Exemplo:
```
@page {
    margin: 1cm;
}
```

- **`@media print`**: Aplica estilos específicos quando um documento está sendo impresso. Exemplo:
```
@media print {
    body {
        color: black;
        background: white;
    }
}
```


## 6. **Regras de Documentos e Componentes**

- **`@document`**: Aplica estilos a documentos baseados em sua URL ou outras características (não amplamente suportado). Exemplo:
```
@document url("https://example.com/") {
    h1 {
        color: red;
    }
}
```

- **`@layer`**: Controla a ordem de aplicação de camadas de estilos, garantindo que as regras CSS se sobreponham da maneira desejada (CSS Cascade Layers). Exemplo:
```
@layer base {
    body {
        margin: 0;
    }
}
```


## 7. **Suporte para Condições de Propriedades**

- **`@supports not`**: Aplica estilos se uma propriedade **não** for suportada. Exemplo:
```
@supports not (display: grid) {
    .container {
        float: left;
    }
}
```


## 8. **Condições de Idioma**

- **`@lang`**: (Ainda experimental) Permite definir regras específicas com base no idioma do conteúdo.


## 9. **Estilização de Componentes Web**

- **`@container`**: (Experimental) Aplica estilos baseados nas dimensões de um contêiner específico, útil para layouts responsivos de componentes. Exemplo:
```
@container (max-width: 600px) {
    .item {
        font-size: 14px;
    }
}
```


## 10. **Outras At-Rules**

- **`@counter-style`**: Define estilos personalizados para listas numeradas. Exemplo:
```
@counter-style minha-contagem {
    system: cyclic;
    symbols: "A" "B" "C";
    suffix: ". ";
}
```

- **`@viewport`**: Define configurações para a viewport em dispositivos móveis (pouco utilizado). Exemplo:
```
@viewport {
    width: device-width;
    zoom: 1;
}
```






# **CLASSES E IDS**
# CLASSES
**Classe** é uma forma de agrupar elementos HTML para que todos eles compartilhem o mesmo estilo. Pense em uma classe como um "apelido" que você dá a um grupo de elementos que devem parecer iguais.

#### Analogia: Uniformes na Escola
Imagine que todos os alunos de uma escola que estão no mesmo time esportivo usem camisetas da mesma cor. Essa cor da camiseta representa a classe. Quando você diz que alguém pertence a essa classe (ou time), todos sabem que essa pessoa veste aquela camiseta específica.

No código, as classes são definidas no CSS e aplicadas aos elementos HTML usando o atributo `class`.

#### Exemplo Prático:
Suponha que você queira que todos os títulos `<h1>` em uma página tenham cor vermelha e um certo tamanho de fonte. Você faria o seguinte:

No HTML:
```
<h1 class="titulo-vermelho">Título 1</h1>
<h1 class="titulo-vermelho">Título 2</h1>
<h1 class="titulo-vermelho">Título 3</h1>
```
No CSS:
```
.titulo-vermelho {
    color: red;
    font-size: 24px;
}
```
- **`.titulo-vermelho`** é o nome da classe (note o ponto `.` antes do nome no CSS).
- Qualquer elemento com a classe `titulo-vermelho` receberá as propriedades de estilo definidas: cor vermelha e tamanho de fonte 24px.




# IDS
**ID** é uma forma de identificar **um único** elemento de maneira única na página. Enquanto uma classe pode ser usada em vários elementos, um ID é exclusivo para um único elemento, como um CPF (ou documento de identidade) para pessoas.

#### Analogia: Identidade Única
Imagine que em uma escola, cada aluno tem seu próprio número de matrícula. Esse número é único e identifica apenas aquele aluno. No HTML, o ID faz o mesmo para um elemento específico.

IDs são usados quando você quer aplicar um estilo único a um elemento específico, sem compartilhar esse estilo com outros elementos.

#### Exemplo Prático:
Suponha que você tenha um título na página que quer destacar com uma cor e tamanho únicos.

No HTML:
```
<h1 id="titulo-unico">Título Único</h1>
```
No CSS:
```
#titulo-unico {
    color: blue;
    font-size: 30px;
}
```
- **`#titulo-unico`** é o ID do elemento (note o `#` antes do nome no CSS).
- Esse estilo só será aplicado ao `<h1>` que tem o ID `titulo-unico`.

### Diferenças Principais entre Classes e IDs

1. **Quantidade de Usos:**
    - **Classe**: Pode ser usada em vários elementos. Você pode ter muitos elementos com a mesma classe.
    - **ID**: Deve ser único por página. Um ID só pode ser atribuído a um único elemento na página.
2. **Especificidade (Prioridade):**
    - **ID** tem maior prioridade que uma classe. Se um elemento tiver tanto uma classe quanto um ID que definem estilos conflitantes, o estilo do ID prevalece.
3. **Sintaxe:**
    - **Classe no CSS**: Começa com um ponto (`.`). Ex: `.minha-classe`.
    - **ID no CSS**: Começa com uma cerquilha ou hash (`#`). Ex: `#meu-id`.

### Quando Usar o Que?
- **Classes**: Use quando você quiser que múltiplos elementos compartilhem o mesmo estilo.
- **IDs**: Use quando precisar estilizar um único elemento de maneira única. Também são usados em situações onde é necessário um identificador exclusivo, como em links de âncoras ou ao interagir com JavaScript.

### Resumindo:
- **Classes**: Ideais para estilos reutilizáveis em vários elementos.
- **IDs**: Ideais para estilos únicos e exclusivos para um elemento específico.






# **CASCATA E ESPECIFICIDADE**
O nome "Cascading Style Sheets" não é por acaso. Em CSS, "cascata" se refere à maneira como as regras são aplicadas e combinadas.

- **Especificidade**: É uma maneira de determinar qual regra deve prevalecer quando múltiplas regras se aplicam ao mesmo elemento. Regras mais específicas têm precedência. Por exemplo, um seletor de ID (`#menu`) é mais específico que um seletor de classe (`.botao`), que por sua vez é mais específico que um seletor de tipo (`p`).
- **Importância**: Regras com a palavra-chave `!important` sobrescrevem outras regras, independentemente da especificidade.
- **Herança**: Algumas propriedades em CSS são herdadas automaticamente dos elementos pai para os filhos, como `font-family` e `color`.


A "cascata" no CSS refere-se a como os estilos são aplicados de cima para baixo, e a "especificidade" determina qual estilo é aplicado quando múltiplos seletores atingem o mesmo elemento.

- **Cascata:** Se dois estilos conflitantes são aplicados, o último na ordem do código geralmente prevalece.
```
p {
    color: black;
}
p {
    color: blue;
}
```
Neste exemplo, o texto será azul porque o segundo estilo é o último.

- **Especificidade:** Seletores mais específicos (como IDs) têm prioridade sobre seletores mais genéricos (como elementos).
```
p {
    color: red;
}
#especial {
    color: green;
}
```
Se um parágrafo tiver o ID `especial`, ele será verde, não vermelho.





# **SELETORES CSS**
Os seletores são usados para "alcançar" os elementos HTML e aplicar estilos a eles. Eles são como endereços que você usa para encontrar o cômodo certo para decorar.

- **Seletores de Elemento:** Aplicam estilos a todas as instâncias de um determinado tipo de elemento. Você consegue selecionar mais de um elemento por vez, só colocar uma vírgula e o nome do outro elemento. Os elementos colocados irão receber as mesmas configurações que ficarem dentro das chaves.
```
p {
    color: blue;
}
```
- **Seletores de Classe:** Aplicam estilos a elementos que possuem uma determinada classe. Classes são como etiquetas que você pode colar em diferentes móveis (elementos).
```
.destaque {
    color: orange;
    font-weight: bold;
}
```
Aplicação:
```
<p class="destaque">Texto destacado.</p>
```
- **Seletores de ID:** Aplicam estilos a um único elemento que possui um ID específico. Como um número de série único para um móvel.
```
#cabecalho {
    background-color: lightgrey;
}
```
Aplicação:
```
<div id="cabecalho">Cabeçalho do site</div>
```





# **MEDIA QUERIES E RESPONSIVIDADE**
CSS também permite criar designs responsivos que se adaptam a diferentes tamanhos de tela usando media queries. Pense nisso como ajustar a decoração da sua casa de acordo com o tamanho do cômodo.

Exemplo:
```
@media (max-width: 600px) {
    p {
        font-size: 12px;
    }
}
```
Este código reduz o tamanho da fonte dos parágrafos para 12px em telas menores que 600px de largura.



# **BOAS PRÁTICAS EM CSS**

- **Manter o CSS organizado e bem comentado.**
- **Reutilizar classes e evitar repetição de código.**
- **Usar um arquivo externo para facilitar a manutenção.**
- **Evitar estilos inline para maior consistência e facilidade de modificação.**





# **PEGANDO IMAGENS SEM DIREITOS AUTORAIS**
# Melhores sites para pegar imagens sem direitos autorais:
- Unsplash
- Pexels
- Freepik
- Rawpixel
- Pixabay
- Libreshot
- Wikimedia Commons




# **CORES**
Procure sempre ter uma paleta de 3 à 5 cores. Não ultrapasse, nem tenha menos que 3 cores (Preto e Branco não contam).

# REPRESENTAÇÃO DE CORES
Para representar cores em CSS, temos 5 representações:
1. Nome
- Exemplo: `<h2 style="background-color: blue; color: white;">Exemplo de Cores</h2>`
- É a forma mais fácil de representar as cores, mas é um pouco limitado aos nomes, se você quiser algo mais detalhado, precisará ir para os outros métodos.

2. RGB (Red, Green, Blue)
- Exemplo: `<h2 style="background-color: rgb(0, 0, 255); color: rgb(255, 255, 255);">Exemplo de Cores</h2>`
- Outro exemplo, com o Alpha: `<h2 style="background-color: rgba(22, 68, 49, 0.562); color: #ffffff;">Exemplo de Cores</h2>`
- É o jeito mais convencional, o mais fácil de memorizar para o ser humano.

3. Hexadecimal
Hexadecimal é representado por os algarismos 0, 1, 2, 3, 4, 5, 6, 7, 8, 9, A, B, C, D, E, F. Totalizando 16 algarismos. Diferente do sistema Decimal, que vai de 0 até 9 (10 Algarismos, por isso "decimal").
- Exemplo: `<h2 style="background-color: #0000ff; color: #ffffff;">Exemplo de Cores</h2>`
- É um dos jeitos mais difíceis de se entender. Basicamente, 0 é o menor valor possível, e F é o maior. Você precisa dar uma estudada em bases numéricas se quiser usar o modelo Hexadecimal.

4. HSL (Hue, Saturation, Luminosity)
- Exemplo: `<h2 style="background-color: hsl(240, 100%, 50%); color: hsl(0, 0%, 100%);">Exemplo de Cores</h2>`
- É o jeito mais exótico, eu não gosto muito.

5. E todas as outras opções, só que agora com transparência, que adiciona o Alpha (Transparência)
Com a transparência, as outras formas recebem um novo valor, o Alpha.

1) Em RGB, fica RGBA (Red Green Blue Alpha)
- Ex: `rgba(22, 68, 49, 0.562)`. O último "bloco" de números é o do Alpha. No caso, `0.562`.

2) Em Hexadecimal, fica com outros 2 dígitos no final, que é responsável pela transparência.
- Ex: `#0000ffbe`. Os últimos 2 algarismos é o do Alpha. No caso, `be`.

3) Em HSL, fica HSLA (Hue Saturation Luminosity Alpha)
- Ex: `hsla(240, 100%, 50%, 0.699)`. O último "bloco" de números é o do Alpha, no caso, `0.699`.




# QUAL A MELHOR FORMA DE ESCREVER AS CORES NO VSCODE, BASEADO NOS 5 TIPOS QUE EXISTEM

Se você não tem o código expecífico da cor que queira representar, e quer representar ela, a melhor forma de você conseguir dizer cores específicas, sem ser limitado pelos nomes das cores, é usando o RGB/RGBA.

O segredo é:
1. Primeiro escrever o nome da cor que você quer. Geralmente o nome não vai ser exatamente da mesma cor que você quer, então é só uma aproximação. 
2. Depois, você clica no quadradinho que fica do lado do código de cor. Vai abrir um painel de cores.
3. Agora você vai se deparar com algo mais ou menos assim:
![](Painel%20de%20cores%20para%20o%20Bloco%20de%20notas%20de%20HTML%20e%20CSS.png)
- O quadrado maior representa a TONALIDADE DA COR que você quer.
- O retângulo vertical da direita representa a COR que você quer.
- O retângulo vertical da esquerda representa a TRANSPARÊNCIA DA COR que você quer. Caso mude o seletor para algo que não seja a transparência máxima (Seletor no topo do retângulo), o seu código de cor vai receber uma parte nova, que é a de transparência (Alpha). Se o seletor estiver no topo do retângulo, o código extra é retirado.

4. Modifique como queira, até encontrar a cor que deseja. Após fazer as modificações, o que antes era um nome de cor, agora é um código RGB. Clicando em cima, no retângulo horizontal acima, você consegue mudar o tipo de representação que você quer. Pode ser os 3 tipos principais, RGB, Hexadecimal e HSL. 
5. Após as mudanças, você conseguiu colocar a cor complexa que queria, de forma simples, o único trabalho que teve foi de colocar o nome da cor para se aproximar, e depois ir arrastando os seletores de cor para achar a cor que deseja. Você não precisou decorar um código de cor complexo. Esse é o segredo.




# MELHORES SITES DE CORES 

1. https://coolors.co/: Uma ferramenta popular que permite gerar paletas de cores rapidamente. Você pode explorar paletas criadas por outros usuários, ajustar cores, e bloquear ou desbloquear cores individuais enquanto ajusta as outras.
2. https://color.adobe.com/: Oferece diversas formas de criar paletas de cores, como usando a roda de cores, explorando esquemas monocromáticos, complementares, análogos, e mais. Você também pode explorar paletas populares e salvar suas próprias.
3. https://colorhunt.co/: Um repositório de paletas de cores curadas por uma comunidade de designers. Você pode navegar pelas paletas mais populares ou procurar por temas específicos.
4. https://colorsinspo.com/: Uma ferramenta completa que oferece paletas de cores, gradientes, e até mesmo exemplos de tipografia que combinam com certas cores.
5. http://colormind.io/: Gera paletas de cores baseadas em inteligência artificial. Você pode carregar uma imagem e o Colormind criará uma paleta que combina com as cores da imagem, ou você pode simplesmente explorar as paletas sugeridas.
6. https://www.happyhues.co/: Um site que mostra exemplos de paletas de cores em uso real em layouts de sites, permitindo que você veja como as cores funcionam em contexto.





# PSICOLOGIA DAS CORES

| Cor      | Associada a                                    | Usar em                                                            | Evitar                                      |
| -------- | ---------------------------------------------- | ------------------------------------------------------------------ | ------------------------------------------- |
| vermelho | amor, emoção, energia, raiva, perigo           | comida, moda, entretenimento, serviços de emergência e saúde       | luxo, natureza, serviços em geral           |
| Amarelo  | felicidade, alegria, otimismo, covardia        | dar luz, dar calma e felicidade, chamar atenção                    | pode indicar que algo é barato ou spam      |
| laranja  | divertimento, ambição, calor, cautela          | comércio eletrônico, entretenimento, call-to-action                | pode se tornar cansativo se muito explorado |
| verde    | saúde, natureza, dinheiro, sorte, inveja       | relaxamento, turismo, financeiros, meio ambiente                   | luxo, tecnologia, meninas adolescentes      |
| azul     | competência, sabedoria, calma, frio            | tecnologia, medicina, ciências, governo                            | comida (reduz apetite)                      |
| roxo     | criatividade, poder, sabedoria, mistério       | produtos de beleza, astrologia, ioga, espiritualidade, adolescente | não prende muito a atenção, indiferente     |
| marrom   | terra, robustez, estabilidade, amizade         | alimentação, imobiliária, animais, finanças                        | cor considerada conservadora                |
| preto    | elegância, autoridade, mistério, morte         | luxo, moda, marketing, cosméticos                                  | desconforto e medo                          |
| branco   | pureza, limpeza, felicidade, segurança         | medicina, saúde, tecnologia, luxo (com preto, ouro, cinza)         | não chama atenção, deve ser combinado       |
| cinza    | formalidade, sofisticação, frieza, indiferença | bens de luxo, efeito calmante                                      | dá a sensação de frieza                     |
| rosa     | amor, romance, sinceridade, cuidados           | produtos femininos e cosméticos                                    | pode tornar muito sentimental e doce        |





# **FONTES**
Sites de fontes: 
- https://fonts.google.com/
- https://www.dafont.com/pt/
- https://www.fontsquirrel.com/

Sites para descobrir uma fonte de uma imagem:
- https://www.whatfontis.com/
- https://www.fontsquirrel.com/
- https://www.myfonts.com/
Para importar uma fonte de outro lugar, você precisa do código embedado dela. Pode ser tanto um `<link>` (HTML) quanto um `@import`(CSS) (Preferível).

Existem diversos tipos de fonte, mas os principais são:
- Serifada: Fonte que tem "frufru", é um pouco mais detalhada. Indicada para papéis;
- Sans-Serif (Sem serifa): Fonte um pouco mais simples. Indicada para qualquer conteúdo.
- Monoespaçada: Fonte que todas as letras possuem o mesmo tamanho horizontal. Indicada para escrever códigos.


# SAFE COMBINATIONS
Safe Combinations são quando você escolhe uma fonte para o seu site, porém o dispositivo que está acessando o site não tem essa fonte. O que você vai fazer é adicionar outras opções de fontes, em sites como o https://www.w3schools.com/cssref/css_websafe_fonts.php, essas combinações de opções de fontes são listadas, listando quais são as melhores variantes da fonte principal que você quer.


# TAMANHO DAS FONTES
Com o `font-size`, podemos aumentar e diminuir o tamanho das fontes, temos formas de representar os tamanhos das fontes, segue abaixo:
1. Medidas Absolutas
- px (Pixels)
- cm (Centímetros)
- mm (Milímetros)
- in (Polegadas)
- pt
- pc

2. Medidas Relativas
- em (Baseada no tamanho do "M" da fonte)
- ex (Baseada no tamanho do "x" da fonte)
- rem (Baseada no tamanho do "M" da fonte, só que no root)
- vw
- vh (Baseada no tamanho do dispositivo)
- %

**A W3 recomenda a utilização SOMENTE do px e do em.**
16px é o tamanho padrão das fontes, geralmente.
16px geralmente = 1em

**Exemplos:**
`font-size: 2em;`
`font-size: 20px;`



# FONTES EXTERNAS, COMO USAR

Quando a fonte é geralmente famosa e existe em um site que disponibilize o código para você utilizar, é preferível.
```
@import url('https://fonts.googleapis.com/css2?family=Work+Sans:ital,wght@0,100..900;1,100..900&display=swap');
```

Mas quando a fonte não está num site como o Google Fonts, você vai precisar baixar ela, tendo o arquivo `.ttf` ou `.otf`, você utiliza o `@font-face`:
```
@font-face {
	font-family: 'Love';
	src: url('fonts/love larry.ttf') format('truetype');
	font-weight: normal;
	font-style: normal;
}
```
Caso queira usar uma fonte externa com mais de uma extensão de arquivo, você adiciona um outro `url` do lado, assim:

```
@font-face {
	font-family: 'Love';
	src: url('fonts/love larry.ttf') format('truetype'), url('fonts/love larry.otf') format(opentype);
	font-weight: normal;
	font-style: normal;
}
```

## Formatos de arquivos de fonte
1. opentype (otf)
2. truetype (ttf)
3. embedded-opentype
4. truetype-aat (Apple Advanced Typography)
5. svg
Os melhores são o truetype e opentype.




# **FAVICONS (ÍCONES DE FAVORITO, SÃO OS ÍCONES QUE APARECEM ANTES DO TÍTULO DA ABA DO SITE)

Recomendação: Sempre nomeie seu FavIcon de `favicon.ico`, a maioria dos favicons são nomeados assim.

Para adicionar um favicon em seu site, você vai na tag `head` do seu arquivo HTML, escreve `link:favicon` e dá enter, a estrutura vai se sair mais ou menos assim:
`<link rel="shortcut icon" href="nerd face.ico" type="image/x-icon">`
Aqui, a única coisa que eu precisei mudar para mostrar o favicon foi ter modificado para `"nerd face.ico"` o parâmetro href.

# Melhores sites para pegar favicons
- www.favicon.io (Transformar PNG em ícones, texto em ícones, emoji, etc.)
- www.iconarchive.com (Pesquisa de ícones por nome)
- www.favicon.cc (Desenhar o FavIcon por Pixel)





# **ATALHOS DO VISUAL STUDIO CODE PARA PROGRAMAR WEBSITES**

- Caso tenha escrito um texto, e queira formatar ele, colocar em negrito, itálico, sublinhado, etc, porém você já escreveu, e não quer ter que ficar escrevendo a tag inteira no início e no final do texto, você pode usar o atalho: Ctrl + Shift + P e escrever `Emmet: Wrap with Abbreviation`. Você escreve a tag que quer colocar no texto (Sem os `<>` e `</>`), e aperta enter.