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
```html
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
#### 1. O que significa `<!doctype html>`?
`<!doctype html>` é a forma simplificada de declarar o tipo de documento para HTML5. Ele instrui o navegador a renderizar a página usando o modo de compatibilidade com os padrões do HTML5, que é a versão mais moderna do HTML.
- **`<!DOCTYPE>`**: Este é o começo da declaração e significa "Document Type Declaration" (Declaração de Tipo de Documento). Ele é necessário para que o navegador interprete o HTML corretamente.
- **`html`**: Isso especifica que o tipo de documento é HTML, e não XML, XHTML, ou outro tipo de linguagem de marcação.
#### 2. O `!` significa algo especial?
Sim, o `!` no início da declaração `<!DOCTYPE>` indica que essa linha é uma "declaração", não uma tag HTML comum. Ele serve como uma instrução ao navegador, e é por isso que se utiliza o `!` no começo. Não é algo específico do HTML5 ou HTML em geral, mas é uma convenção de linguagens SGML (a linguagem da qual o HTML deriva).
#### 3. Significa que o arquivo é da última versão do HTML?
Quando você usa `<!doctype html>`, está dizendo ao navegador que esse documento está usando a versão HTML5. Esta é a versão mais recente e recomendada, e essa declaração é a maneira mais simples de indicar isso. Em versões anteriores do HTML, as declarações de tipo de documento eram muito mais complexas, porque os navegadores precisavam de mais informações para processar o conteúdo corretamente.
**Vale lembrar que o `<!doctype html>` é no início do arquivo inteiro, nada vem antes dele.**

- `<html>`: Define o início de um documento HTML.
- `<head>`: Contém metadados, links para estilos e scripts, e o título da página.
- `<title>`: Define o título da página, que aparece na aba do navegador.
- `<body>`: Contém todo o conteúdo visível da página, como texto, imagens, vídeos, etc.




## 2. **Estrutura de Conteúdo**

- `<header>`: Define a seção de cabeçalho da página, geralmente contendo o título, logo, e navegação.
- `<nav>`: Define uma seção de navegação com links. Embora você possa criar navegações sem a tag `<nav>`, usá-la dá mais significado semântico ao código, o que é uma boa prática de desenvolvimento web. Ou seja, ela melhora tanto a organização quanto a experiência do usuário. Geralmente fica dentro do `<header>`, mas pode ficar em outros lugares também. Pode ter mais de um `<nav>` por página.

- `<main>`: Indica o conteúdo principal da página, é único por documento. Você pode, tecnicamente, criar um documento HTML sem o `<main>` e ele funcionará perfeitamente, porém, usar ela melhora a acessibilidade e o SEO do seu site. Fora que organiza mais ele. Use sempre um `<main>` por página. Geralmente não é nele que colocamos o `<nav>`, ou outros elementos. **Ele fica sempre com o conteúdo principal da página.**

- `<aside>`: Conteúdo relacionado, mas separado do principal, algo não muito importante. Conteúdos levemente relacionados ao conteúdo principal, como explicações do conteúdo, glossários, links extras, biografia do autor, informações de perfil e etc.

- `<footer>`: Seção de rodapé da página, geralmente com informações de copyright ou links adicionais.

- `<section>`: Seção temática de conteúdo. Geralmente você usa ele junto com um título logo em seguida. Quando existem muitos deles que são iguais, e estão no mesmo lugar, é mais recomendado que se use um `<article>`.

- `<article>`: Cria blocos de conteúdo que são relacionados, como um post de blog. Imagine que você está lendo uma revista física. Cada artigo que você lê dentro da revista faz sentido independentemente do restante da revista, certo? Pode ser um texto sobre tecnologia, um review de filme, ou uma receita. Esses artigos são entidades independentes que poderiam ser recortados e colados em outro lugar (como em um blog ou outro jornal) e ainda fariam sentido. O conteúdo dentro desse `<article>` pode ser reutilizado em outros contextos ou plataformas e ainda faria sentido, mesmo fora do site original. O `<article>` deve ser usado quando você está trabalhando com um **bloco de conteúdo independente** que pode ser compreendido por si só.

**Uma regra básica: se eu extrair esse elemento do seu contexto, ele continuará fazendo sentido? Se sim, tudo indica que é um `<article>`, se não, é possível que seja um `<section>`. Um capítulo de um livro, por exemplo, perderia o sentido, pois está fortemente associado ao contexto do resto da história - ele seria um `<section>`; já um post em um blog costuma ser independente de outros posts e fazer sentido mesmo fora do contexto do site - ele seria um `<article>`.
Por exemplo:
- **Sim para uma notícia, porque você pode ler a notícia em qualquer lugar e ela continua a ser relevante.**
- **Sim para um post de blog, porque você pode compartilhar o texto em redes sociais ou outro site.**
- **Não para um item de menu de navegação, porque um item de menu sozinho não faz sentido fora do contexto de sua página original.**


### Diferença entre `<article>` e `<section>` e melhor explicação sobre os 2 elementos
- **Section**: quando vários conteúdos estão relacionados, mas se estivessem num lugar qualquer, sem ser naquele lugar em específico aonde ele está, não faria tanto sentido.
- **Article**: quando um conteúdo faz sentido por si só. O título que ele tem, e o conteúdo dentro dele em si já explica o que ele é, e se estivesse em qualquer outro lugar, as pessoas entenderiam o que é aquilo.



- `<details>`: Define uma seção expansível que o usuário pode abrir e fechar.
- `<summary>`: Define o título da seção expansível dentro de `<details>`.
#### Exemplo de `<details>` com `<summary>`:
```html
<details>
  <summary>Mais informações</summary>
  <p>Este é o conteúdo adicional que pode ser expandido.</p>
</details>
```
Exemplo de uso das tags semânticas:
![](Exemplo%20de%20uso%20das%20tags%20semânticas.png)



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
```html
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
```html
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
```html
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
```html
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
```html
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
```html
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
```html
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
```html
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


## Atributos da tag `<img>`:

- `src`: Define a URL da imagem.
- `alt`: Define o texto alternativo que vai ser exibido caso o navegador não consiga exibir a imagem.
- `title`: Define a caixinha que é exibida quando você "descansa o mouse" em cima da imagem, mostrando o título dela.
- `width`: Define a largura da imagem.
- `height`: Define a altura da imagem.

## Título externo das imagens com `<figure>`:

- `<figure>`: Cria uma tag de container, onde a imagem fica dentro dela, e no fim, colocamos o `<figcaption>`, que é o título da imagem.
- `<figcaption>`: Cria o título da imagem, ele é exibido por padrão em baixo da imagem.
**Exemplo de uso do `<figure>`:**
```html
    <a href="https://google.com" target="_blank">
        <figure>
            <img src="images/Computer.jpeg" alt="Computador de um programador" title="Computador de um programador" width="500px" height="723px">
            <figcaption>Computador de um programador.</figcaption>
        </figure>
    </a>
```
Colocamos a tag dentro de um link, para que assim, qualquer área que o usuário clicar, ele for redirecionado para o Google. O grande diferencial do `<figure>` é o título que ele tem, o `<figcaption>`. É o título da imagem.




- `<picture>`: É uma tag de container que define diversos tamanhos de uma imagem, para cada tamanho de dispositivo, uma imagem diferente vai ser mostrada. 
Pense em uma loja de roupas que oferece diferentes tamanhos de uma mesma camiseta: pequeno, médio e grande. Quando um cliente chega, a loja não sabe qual tamanho será o melhor para ele, então tem que escolher um baseado nas características do cliente, como altura e peso.
Agora, imagine que, na web, o cliente é o dispositivo (computador, tablet, smartphone) e a camiseta é a imagem que você quer mostrar. O problema é que uma imagem grande demais pode demorar para carregar em um celular com conexão lenta, enquanto uma imagem pequena pode ficar borrada em uma tela de alta resolução.
### Estrutura da tag `<picture>`
Aqui está um exemplo básico de como usar a tag `<picture>`:
```html
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
```html
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
```html
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
```html
<video src="video.mp4">Seu navegador não tem compatibilidade com reprodução de vídeos.</video>
```
- **`<video src="video.mp4">`**: Define a fonte do vídeo. Como não temos a tag `<source>`, que seria utilizada para disponibilizar diversas versões do arquivo, o único arquivo que é exibido é esse. Caso o navegador não consiga exibir, vai ser exibido "Seu navegador não tem compatibilidade com reprodução de vídeos.", que é o texto de fallback.



### Atributos Comuns da Tag `<video>`
Você usa um atributo assim: `<video src="video.mp4" atributo atributo atributo></video>`
Além dos atributos que vimos no exemplo acima, a tag `<video>` possui outros atributos úteis:

1. **`autoplay`**: Faz com que o vídeo comece a ser reproduzido automaticamente assim que a página é carregada. É importante notar que muitos navegadores modernos bloqueiam a reprodução automática, especialmente se o vídeo tiver som, para evitar experiências intrusivas.
2. **`loop`**: Faz com que o vídeo seja reproduzido em loop, ou seja, ele recomeçará automaticamente sempre que terminar.
3. **`muted`**: Inicia o vídeo sem som. Isso pode ser útil em conjunto com o `autoplay`, pois os navegadores que não permitem o `autoplay`, permitem ele, caso ele estiver com o `muted` junto.
4. **`poster`**: Especifica uma imagem que será exibida antes do vídeo começar a ser reproduzido. Isso é útil como uma miniatura ou pré-visualização do vídeo. É a "Thumbnail" do vídeo.
5. **`preload`**: Controla o pré-carregamento do vídeo. Pode ser configurado como:
- **`auto`**: O navegador decide se deve carregar todo o vídeo quando a página é carregada.
- **`metadata`**: Apenas os metadados (como duração e dimensões) são carregados.
- **`none`**: O vídeo não é carregado até que o usuário o reproduza.





- `<audio>`: Insere um áudio.
## Estrutura básica da tag `<audio>`
```html
<audio controls>
  <source src="musica.mp3" type="audio/mpeg">
  Seu navegador não suporta o elemento de áudio.
</audio>
```
- **`<audio controls>`**: Isso cria o reprodutor de áudio na página. A palavra `controls` adiciona os botões de play, pause, volume, etc., que o usuário pode usar. Sem essa palavra, o áudio ainda será reproduzido, mas não haverá controles visíveis para o usuário.
    
- **`<source src="musica.mp3" type="audio/mpeg">`**: Aqui, `src="musica.mp3"` define o caminho do arquivo de áudio que será reproduzido. O atributo `type="audio/mpeg"` especifica o formato do arquivo de áudio (neste caso, um MP3). A tag `<source>` permite que você inclua diferentes formatos de áudio para garantir que o som será reproduzido em diferentes navegadores, que podem ter suporte a diferentes formatos.
    
- **Texto entre `<audio>` e `</audio>`**: O texto "Seu navegador não suporta o elemento de áudio." é uma mensagem que será exibida se o navegador do usuário não suportar a tag `<audio>`. Isso é útil como um fallback/else, garantindo que o usuário saiba que deveria haver um áudio ali, mas ele não pode ser reproduzido.


## Outra estrutura, agora sem o `<source>`
```html
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
3) **`muted`**: Inicia o áudio sem som. Isso **não** garante que o áudio consiga ficar com o `autoplay` em navegadores que proíbem isso.
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
```html
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
``` html
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
- `action`: Define para onde os dados do formulário devem ser enviados quando você clica no botão de "enviar" (ou "submit"). 
1) **Redirecionamento natural**: Quando o formulário é submetido, o navegador envia os dados para o URL definido no `action`. Se essa URL aponta para outra página HTML estática, o navegador simplesmente navega até essa página após o envio do formulário. Isso acontece porque, no caso de uma página HTML estática, não há um backend processando os dados, então o navegador apenas carrega a nova página.
    
2. **Envio de dados**: O `action` normalmente envia dados para um script no backend (PHP, Python, etc.) que processa os dados e retorna uma resposta. Mas, se o `action` aponta para um arquivo HTML, como no seu caso, o navegador não processa os dados, apenas redireciona o usuário para a página especificada.

- `method`: Define o método HTTP que esse formulário vai estar fazendo. Qualquer método pode ser colocado nesse atributo. Os métodos mais comuns são:
1) **`POST`**: Para enviar dados de forma mais segura (como em cadastros, login, etc.).
2) **`GET`**: Para enviar dados na URL (geralmente usado para buscar ou consultar algo).


- `fieldset`: Define um agrupamento de campos de mesmo propósito dentro do seu formulário. É usado para deixar seu HTML mais semântico e mais acessível para leitores de tela.
Imagine que você está preenchendo um formulário físico para fazer uma inscrição em um evento. O formulário é longo e inclui várias seções: informações pessoais, detalhes de contato, e preferências do evento. Se essas seções fossem apenas uma longa lista de perguntas sem separação, ficaria confuso. No entanto, se o formulário estiver dividido em blocos bem definidos, com títulos que indicam o que cada seção significa, será muito mais fácil de entender e preencher.

O **`fieldset`** faz exatamente isso em formulários HTML.


1) É o nome do agrupamento que vai aparecer na tela, ele é o primeiro elemento dentro do fieldset.
2) `form`: o id de um formulário ao qual esse fieldset pertence. Você usa ele quando ele não está dentro da tag do formulário. Exemplo abaixo:
```html
<form id="contato" action="">
	<input type="text">Input
</form>


<fieldset form="contato" name="input Qualquer">
	<legend>Contato</legend>

	<label for="">Nome</label>
	<input type="text">
</fieldset>
```

3) `name`: Nome do grupo do fieldset. É só para deixar um pouco melhor escrito e mais semântico o seu HTML.
4) `disabled`: Desabilita todos os elementos dentro do fieldset. Eles não serão enviados ao submeter o formulário.



- `<input>`: Campo de entrada de dados (texto, senha, etc.).
1) `type`: Define o tipo de input. Existem diversos tipos de input existentes. 
Para verificar a disponibilidade de um tipo de input com os navegadores, use o site https://caniuse.com. Os principais tipossão:

1. `text`: Cria um campo de entrada de texto em uma única linha. Feito para capturar informações simples, como nome, e-mail, etc.  
Exemplo:
```html
<label for="nome">Nome:</label>
<input type="text" id="nome" name="nome">
```

2. `password`: Um campo de texto em que os caracteres digitados são mascarados. Feito para capturar senhas e dados sensíveis.  
Exemplo:
```HTML
<label for="senha">Senha:</label>
<input type="password" id="senha" name="senha">
```

1) `minlength` e `maxlength`: Definem o mínimo e o máximo de caracteres que uma senha precisa ter.
2) `size`: Define o tamanho do input, geralmente é bom você colocar o mesmo número que está no `maxlength`.
3) `pattern`: Define um padrão à ser seguido na senha. Por exemplo: `pattern="[0-9a-fA-F]{4,8}"`. Aqui, estamos dizendo que a senha só aceita caracteres hexadecimais, tem no mínimo 4 caracteres e no máximo 8 caracteres.
4) `inputmode`: Altera o teclado em smartphones, tipo abrir o teclado numérico (`numeric`) ao invés de abrir o teclado inteiro.
5) `title`: Define o título à ser mostrado na mensagem de erro, caso o usuário digite uma senha inválida.
6) `autocomplete="new-password"`: É uma das opções de `autocomplete` que você pode definir. Ela define se o navegador vai sugerir uma senha feita por ele mesmo, para auxiliar o usuário. Existem navegadores que fazem isso por padrão, então caso você queira que isso não aconteça no seu input, você deixa o `autocomplete="off"`.


3. `email`: Um campo de texto que valida se o valor inserido é um endereço de e-mail válido.  
Exemplo:
``` HTML
<label for="email">E-mail:</label>
<input type="email" id="email" name="email">
```
1) `multiple`: O campo irá receber 1 ou mais e-mails, separado por vírgulas.
2) `minlength` e `maxlength`: Definem o mínimo e o máximo de caracteres que o campo terá.


4. `number`: Cria um campo que permite a entrada de números inteiros ou decimais.  
Exemplo:
``` HTML
<label for="quantidade">Quantidade:</label>
<input type="number" id="quantidade" name="quantidade" min="1" max="10">
```
1) `min` e `max`: Definem o menor e o maior número que o usuário pode colocar no input.
2) `step`: Define de quanto em quanto a setinha do input vai pular.


3. `date`: Campo de seleção de data. A formatação no código é `yyyy-mm-dd`. A formatação no ouput vai depender da região que está o seu navegador. 
Exemplo:
``` HTML
<label for="nascimento">Data de nascimento:</label>
<input type="date" id="nascimento" name="nascimento">
```
1) `value`: Define o valor prévio em que aquele campo está. Lembre-se da formatação de código padrão.


6. `datetime-local`: Permite a entrada de data e hora no formato local.  
Exemplo:
``` HTML
<label for="agendamento">Agendamento:</label>
<input type="datetime-local" id="agendamento" name="agendamento">
```

7. `time`: Campo para escolher uma hora (sem data).  
Exemplo:
```html
<label for="horario">Horário:</label>
<input type="time" id="horario" name="horario">
```

8. `month`, `week`, `year`: Usados para definir suas respectivas datas em um input. Tome cuidado com eles, pode ser que eles não sejam aceitos por todos os navegadores.

9. `tel`: Campo para números de telefone. Não realiza validação automática, mas é formatado para esse propósito.  
Exemplo:
```html
<label for="telefone">Telefone:</label>
<input type="tel" id="telefone" name="telefone">
```

10. `checkbox`: Cria uma caixa de seleção que pode ser marcada ou desmarcada. Se o usuário marcar a caixa, o valor definido pelo desenvolvedor é enviado ao Backend. Se o usuário não marcar a caixa, nenhum dado vai ser enviado ao Backend.
Exemplo:
```html
<label for="aceito">Aceito os termos e condições</label>
<input type="checkbox" id="aceito" name="aceito">
```

1) `value`: Indica o valor que o formulário vai enviar para o Backend caso o usuário selecione a checkbox e envie o formulário. Se colocarmos algo como:
```html
<p>Selecione seus interesses:</p>

<input type="checkbox" 
id="coding"
value="Programação"
name="interesse">
<label for="coding">Programação</label>
```
Se o usuário marcar essa checkbox, o que vai ser enviado para o Backend vai ser algo como:
`interesse=Programação`
Se o desenvolvedor não especificar qual o `value`, o padrão, caso o usuário marque a caixa, é `on`.
então ficaria `interesse=on`

2) `checked`: Define a checkbox para estar pré-marcada.
3) `name`: Usada para definir múltiplos campos que estejam relacionados. Como:
```html
<p>Selecione seus interesses:</p>

<input type="checkbox" 
id="coding"
value="Programação"
name="interesse">
<label for="coding">Programação</label>
 
<input type="checkbox" 
id="musica"
value="Música" 
name="interesse">
<label for="musica">Música</label>

<input type="checkbox"
id="xadrez"
value="Xadrez"
name="interesse">
<label for="xadrez">Jogar Xadrez</label>

<input type="checkbox"
id="ler"
value="Ler"
name="interesse">
<label for="ler">Ler</label>
```
Aqui, todos os checkboxes estão relacionados, eles fazem parte dos interesses que o usuário pode ter. Caso o usuário marque mais de uma caixa, e os checkboxes não estejam relacionados, o HTML vai enviar separadamente os dados para o Backend. Isso é ruim. Caso queremos que ele mande tudo de uma vez, pois são coisas que estão relacionadas, utilizamos o atributo `name`. Se mais de um input tem o mesmo `name`, o HTML automaticamente entende que eles estão relacionados, meio que são "farinha do mesmo saco".

Caso o usuário marcassse por exemplo, Programação, Xadrez e Ler, o que seria mandado para o Backend seria:
`interesse=Programação&interesse=Xadrez&interesse=Ler`.


10. `radio`: Um grupo de botões de opção, onde apenas uma opção pode ser selecionada por vez.  
Exemplo:
```html
<label for="genero">Masculino</label>
<input type="radio" id="masculino" name="genero" value="masculino">
<label for="genero">Feminino</label>
<input type="radio" id="feminino" name="genero" value="feminino">
```
1) `name`: Define o nome daquele grupo de opções. Sem ele, cada opção é tratada como independente, e você não vai conseguir selecionar só uma por vez. Os nomes precisam ser os mesmos para que funcione corretamente. É o nome que vai ser enviado ao Backend.
2) `value`: Define o valor que vai ser enviado ao Backend caso o usuário marque aquele campo e envie o formulário.
3) `checked`: Define para que uma opção já fique previamente marcada.


11. `search`: Um campo de texto semelhante ao campo `text`, mas otimizado para pesquisas. Quando o usuário insere texto, esse tipo de campo pode sugerir correções ou ter o botão de limpar automaticamente, dependendo do navegador. A ideia é facilitar a entrada de dados em situações onde se espera que o usuário faça buscas, como em barras de pesquisa de sites.
Exemplo:
```html
<label for="busca">Buscar:</label>
<input type="search" id="busca" name="busca">
```
Ele é utilizado principalmente em formulários ou interfaces de busca, onde você quer que o navegador aplique algumas melhorias visuais e funcionais automaticamente. Ao contrário do campo `text`, o `search` pode incluir uma opção para limpar o texto digitado, ajudando na experiência de pesquisa.
1) `aria-label`É como se fosse um `<label>`, porém, se utilizássemos um `<label>` aqui, isso ficaria meio redundante para pessoas que enxergam, pois elas já sabem que ali é um campo de busca. Mas pessoas que usam leitores de tela não conseguem saber isso, então só deixar no `placeholder`, ou até mesmo não deixar nada é algo não muito semântico, os mecanismos de busca podem acabar te limitando. Então fazemos com que os leitores de tela possam ler que aquilo é um campo de busca, mas para usuários que enxergam, aquilo não é visível.
Existe uma forma alternativa e ainda mais semântica de se fazer a mesma coisa. Que seria utilizando um `<label>` mesmo, porém ocultando ele com CSS. Dessa forma:

HTML:
```
<label for="pesquisa" class="visually-hidden">Pesquisa:</label>
<input type="search" id="pesquisa" name="q" list="searchterms" placeholder="Digite seu termo de busca" size="29">
```
CSS:
```css
.visually-hidden {
    position: absolute;
    width: 1px;
    height: 1px;
    margin: -1px;
    padding: 0;
    overflow: hidden;
    clip: rect(0, 0, 0, 0);
    border: 0;
}
```
Essa forma supostamente é melhor aceita por mecanismos de busca, e é uma forma mais semântica.

2) `pattern`: Define um padrão que precisa ser seguido pelo usuário ao digitar alguma coisa no campo de busca. Exemplo: `pattern="[0-9]{2}"` (Aceita números de 0 até 9, e apenas dezenas.)


12. `file`: Permite a seleção de arquivos do sistema do usuário para upload.  
Exemplo:
```html
<label for="arquivo">Envie um arquivo:</label>
<input type="file" id="arquivo" name="arquivo">
```
1) Sempre quando você for mexer com inputs de `type="file"`, você precisa colocar ele dentro de um `<form method="post" enctype="multipart/form-data">`. Se o seu formulário não irá mexer com inputs de tipo file, você não precisa disso.
2) `accept`: Filtra quais arquivos ele vai aceitar. Se você quiser que o usuário mande uma imagem, você colocaria algo como: `accept="image/*"`, ou `accept=".png"` (Todos os arquivos pngs vão ser mostrados, qualquer outro arquivo que não tenha essa extensão não poderá ser interagido.). Se fosse para aceitar todos os vídeos, seria `accept="video/*`, áudios: `accept="audio/*`.
3) `multiple`: Permite que o usuário possa selecionar mais de um arquivo e mande tudo de uma vez.


13. `range`: Cria um controle deslizante para selecionar um valor dentro de uma faixa numérica.  
Exemplo:
```html
<label for="volume">Volume:</label>
<input type="range" id="volume" name="volume" min="0" max="100">
```
1) `min` e `max`: Definem os menores e os maiores valores que vão ser aceitos por esse input.
2) `step`: Define de quanto em quanto o controle deslizante vai pular. Quanto maior o número, maior é o pulo que ele dá e consequentemente, menos preciso é.


14. `color`: Um seletor de cores, permitindo ao usuário escolher uma cor específica.  
Exemplo:
```html
<label for="cor">Escolha uma cor:</label>
<input type="color" id="cor" name="cor">
```

15. `submit`: Cria um botão que envia os dados do formulário ao servidor.  
Exemplo:
`<input type="submit" value="Enviar">`

16. `reset`: Cria um botão que redefine todos os campos do formulário para seus valores iniciais.  
Exemplo:
`<input type="reset" value="Redefinir">`

17. `url`: Valida se a entrada é um URL válido.  
Exemplo:
```html
<label for="website">Website:</label>
<input type="url" id="website" name="website">
```
1) `spellcheck="true"`: Habilita a verificação ortográfica para este input.


18. `hidden`: Campo invisível ao usuário, útil para enviar dados ocultos, como IDs ou informações de sessão.  
Exemplo:
`<input type="hidden" name="id" value="12345">`


## Atributos usados na maioria dos inputs:
1) `id`: Define a indentificação daquele input, é o atributo que vai ser utilizado para o `<label>` e o `<input>` se comunicarem. 
2) `value`: Define o valor prévio daquela entrada de dados, algo que já está previamente ali. Esse valor não consegue ser apagado por um botão que tenha o `type="reset"` (na verdade, qualquer outra coisa que o usuário digitar e esse botão for ativado, o valor dentro da caixa de entrada de dados vai se transformar no que estiver dentro de `value`), ele só consegue ser apagado se for apagado manualmente pelo usuário. 
3) `placeholder`: Define o texto que vai estar com pouca opacidade no input, geralmente tem algo escrito como "Digite aqui", algo do tipo
4) `autocomplete`: Faz com que quando o usuário vá digitar algum dado no input, o próprio navegador vai pegar as informações que ele tem guardadas para oferecer sugestões de dados comuns para ele colocar no input, porque o usuário sempre usa aqueles dados na maioria dos sites. Se o navegador não tiver nenhum tipo de dado sobre aquilo, a sugestão não será exibida. Existem diversos tipos de dados que podemos indicar para o navegador buscar sobre o usuário, como `email`, `bday`, `adress`, `country`, `new-password`, etc.
5) `autofocus`: Faz com que o input fique automaticamente com o cursor nele quando o usuário acessar o site. Sem que ele precise clicar no input para aí sim começar à escrever. Você só consegue determinar um `autofocus` por página.
6) `disabled`: Desabilita o input, ele fica meio transparente e você não consegue interagir de nenhuma forma com ele. Geralmente é utilizado junto com JavaScript para reabilitar ele novamente.
7) `readonly`: É como se fosse um primo de segundo-grau do `disabled`, ao invés de você não conseguir interagir de nenhuma forma com o input, agora você pode ler ele, pelo menos. O input fica com a coloração normal, sem ficar transparente igual ao `disabled`.
8) `form`: Indica o formulário que aquele input está relacionado. Um input pode não estar dentro de um formulário, mas você pode interligar os 2 da mesma forma. Por meio do `form`. O formulário precisa ter o `id` dele para isso funcionar.
9) `name`: Fornece o nome do input, é para o Backend saber aonde direcionar cada dado recebido no Banco de Dados.
10) `required`: Faz um input se tornar obrigatório.
11) `list`: É usado para associar o campo de entrada a um elemento `<datalist>`, que define uma lista de opções sugeridas para o usuário. Isso permite que o usuário veja sugestões enquanto digita no campo, mas sem limitar a entrada apenas às opções da lista, como faria um `<select>`.



- `<label>`: Rótulo para um elemento de formulário. Serve para associar e indentificar uma (ou mais) tag de entrada de dados. Ela melhora a acessibilidade, e o usuário pode clicar no texto do rótulo para focar o campo de entrada automaticamente. Isso facilita o preenchimento, especialmente em dispositivos móveis, onde clicar diretamente em um campo pequeno pode ser mais difícil. O uso de `<label>` é recomendado porque ele deixa o código mais semântico.

Existe duas formas de se utilizar o `<label>` com o `<input>`:
1. De forma separada (que é a forma mais comum). Onde o `<label>` tem o seu `for`, e o `<input>` tem o seu `id`. Um separado do outro, pode estar um na linha seguinte do outro ou não.
Exemplo:
```html
<label for="cidade">Digite o nome da cidade onde mora:</label>
<input id="cidade" type="text" placeholder="Digite o nome da cidade aqui">
```
Aqui, os 2 elementos estão separados, com o `for` e o `id`, fica mais explícito o que cada coisa é.

2. De forma junta (não é muito comum, mas é válido). Onde o `<input>` fica dentro do `<label>`. `for` e `id` não são utilizados aqui, até porque um já está dentro do outro, não tem porque indentificar eles.
Exemplo:
```html
<label>Digite o nome da cidade onde mora: <input type="text" placeholder="Digite o nome da cidade aqui"></label>
```
Aqui, os 2 elementos estão juntos, isso deixa o código menos verboso e simples, porém menos legível e menos "Clean Code".


1) `for`: Define a conexão entre este label e a tag de entrada de dados. Quando uma tag de entrada de dados não está dentro de um label, mas queremos que eles estejam relacionados (Como se um estivesse dentro do outro), nós fazemos isso pelo `id` e o `for`.
2) `id`: Indentificação que vai ser agregada à tag de entrada de dados.
Exemplo de uso de um label:
```html
<label for="nome">Nome Completo</label>
<!--Resto do código HTML-->
<input id="nome" type="text">
```
Aqui, as 2 tags parecem não estar relacionadas, mas pelo `for` e `id`, elas estão. Um código com um label e as tags de entrada de dados dentro dele é considerado um código menos legível, desorganizado. Um código com o `for` e o `id` para todos os elementos de entrada de dados é considerado mais organizado e legível para o desenvolvedor.

Vale notar que esse atributo `for` só funciona com elementos específicos, como `<button>`, `<input>` (Not hidden), `<meter>`, `<output>`, `<progress>`, `<select>`, `<textarea>`, etc.


- `<button>`: Define um botão clicável
1) `type`: Define o tipo de botão que aquele botão é. Existem 3 tipos de botões: 
1. `submit` (padrão), que é usado para enviar o formulário
2. `reset`, que serve para resetar algum elemento, alguma coisa
3. `button`, que é apenas um botão comum que não realiza ações de formulário, geralmente usado para scripts.

2) `name`: Define o nome do botão, útil para quando você precisa identificar o botão no back-end ao enviar um formulário.
3) `formtarget`: Define onde o resultado da submissão do formulário será exibido. Pode ter valores como `_self` (padrão), `_blank` (nova aba), `_parent`, ou `_top`.
4) `value`: Especifica o valor do botão, que é enviado junto ao nome quando o formulário é submetido.
5) `disabled`: Este atributo desabilita o botão, tornando-o não clicável. Não precisa de valor, apenas a presença do atributo já faz o botão ser desativado.
6) `autofocus`: Define que o botão deve receber foco automaticamente quando a página é carregada.
7) `form`: Permite associar o botão a um formulário específico na página, usando o `id` do formulário. Isso é útil quando o botão está fora do `<form>`.
8) `formaction`: Especifica uma URL diferente para onde os dados do formulário devem ser enviados, apenas para aquele botão.
9) `formenctype`: Define como os dados do formulário devem ser codificados ao serem enviados. Comumente usado com upload de arquivos.
- **Valores principais**:
    - `application/x-www-form-urlencoded` (padrão)
    - `multipart/form-data` (para envio de arquivos)
    - `text/plain`
Exemplo de uso: `<button type="submit" formenctype="multipart/form-data">Enviar Arquivos</button>`

9) `formmethod`: Especifica qual método HTTP deve ser usado ao enviar o formulário (GET ou POST).
10) `formnovalidate`: Ignora a validação dos campos do formulário ao enviar. Por exemplo, mesmo que algum campo obrigatório não esteja preenchido, o formulário será enviado.



- `<datalist>`: Define uma lista de opções que o usuário pode escolher num input. É aquele clássico tipo de input de setinha, onde você clica na setinha, e aparece diversas opções para você escolher. Você não é naturalmente forçado à escolher uma daquelas opções, por padrão, você pode digitar o que quiser ali, as opções do `<datalist>` são só sugestões, por padrão. Ela não pode estar relacionada com um `<label>` para funcionar corretamente, se estiver, ela vira uma entrada de texto padrão. Exemplo de uso:
```html
<label for="cidade">Escolha uma cidade:</label>
<input type="text" id="cidade" name="cidade" list="cidades">

<datalist id="cidades">
  <option value="São Paulo">
  <option value="Rio de Janeiro">
  <option value="Belo Horizonte">
  <option value="Curitiba">
  <option value="Porto Alegre">
</datalist>
```
Aqui, a `<datalist>` tem o mesmo id que é utilizado pelo input, e tem as opções que o usuário pode escolher.

```html
<input type="color" list="lista_de_cores" placeholder="Escolha uma cor">
	<datalist id="lista_de_cores">
		<option>#ff0000</option>
		<option>#00ff00</option>
		<option>#0000ff</option>
		<option>#ffffff</option>
	</datalist>
```
Aqui, é uma lista com códigos de cores, o layout exibido é diferente. Sempre faça uma lista só com cores, nunca com texto normal misturado.



- `<select>`: Menu com diversas opções. Se parece com o `datalist`, porém o usuário só consegue selecionar as opções que são mostradas à ele. Ele não pode digitar uma outra opção que ele queira.
Exemplo de uso do `<select>`:
```html
<label for="carselect">Qual o modelo do carro?</label>
<select name="carmodel" id="carselect">
    <option value="" disabled selected>Selecione o modelo</option>
    <option value="fiat">Fiat Uno</option>
    <option value="audi">Audi A3</option>
    <option value="bmw">BMW X6</option>
</select>
```
Você geralmente, utilizando o `<select>`, vai colocar a primeira opção com um "Selecione a opção", algo do tipo. Porém, se você deixar ele como se fosse uma opção normal, o usuárop vai poder não escolher nada e mandar o formulário, sem ter marcado nada. Por isso, colocamos o atributo `disabled`, para que a mensagem de escolher uma opção seja mostrada, porém não será possível escolher ela e mandar o formulário.

1) `multiple`: Permite que o usuário possa escolher mais de uma opção.



- `<option>`: Opções dentro do menu suspenso. É o que define as opções do `<datalist>` e do `<select>`. Vale lembrar que se o que estiver dentro da opção for um código de cor (independente do tipo, hexadecimal, rgb, etc.), o layout exibido para o usuário é diferente, agora, com uma lista de cores. Só tome cuidado: Nunca misture códigos de cores com listas de texto normal, ao invés de sair a cor para o usuário escolher, vai sair o código de cor, sem a cor em si, só o código dela.


- `<textarea>`: Área de texto grande para o usuário digitar. Tem tamanho adaptável pelo usuário, mas essa opção pode ser desabilitada com CSS.
1) Quando usamos o `<textarea>`, espaços, quebras de linha, e qualquer outra coisa que usamos para deixar o código mais limpo é contado no output. Então, quando for utilizar o `<textarea>`, não faça assim caso não queira que o `<textarea>` fique com 4 espaços no início:
```html
<textarea>
	conteúdo
</textarea>
```
Faça assim:
```html
<textarea>conteúdo</textarea>
```

2) `rows`e `cols`: Define a quantidade de linhas (`rows`) (Altura) e colunas (`cols`) (Largura) que aquele `<textarea>` vai ter. Isso altera o tamanho dele.
3) `minlength` e `maxlength`: Define o mínimo e o máximo de caracteres que o usuário pode digitar naquele `<textarea>`.
4) `wrap`: Define se o texto vai se "embrulhar" dentro do `<textarea>`. Exemplo:
```
Esse é um texto 
que está com o
wrap.
```

```
Esse é um texto que não está com o wrap.
```
Por padrão, ele vem com o `wrap="soft"`, porém podemos desabilitar ele com `wrap="off"` e a quebra de linha automática para que o texto caiba corretamente dentro do `<textarea>` não vai acontecer.


- `<optgroup>`: Define uma lista de opções que são separadas por um título. É útil quando as opções de um select são muitas, então separando por títulos fica algo mais organizado e legível para o usuário.
Todo `<optgroup>` precisa estar dentro de um `<select>`.

1) `label`: Define o que vai ser mostrado para o usuário. Faz o papel de um label normal.
Exemplo de uso do `<optgroup>`:
```html
<label>Selecione um ou mais pets: 
	<br>
    <select name="pets" multiple size="8">
        <optgroup label="Pets de 4 patas">
            <option value="cao">Cachorro</option>
            <option value="gato">Gato</option>
            <option value="hamster">Hamster</option>
        </optgroup>
        <optgroup label="Pets que voam">
            <option value="pombo">Pombo</option>
            <option value="arara">Arara</option>
            <option value="aguia">Águia</option>
        </optgroup>
    </select>
</label>
```
Aqui, o ATRIBUTO `label` do `<optgroup>` representa o que vai ser mostrado para o usuário, para ele entender o que ele precisa fazer.




## 8. **Semântica e Marcação**

- `<div>`: É uma tag genérica, é usada quando não se encontra uma tag semântica para um conteúdo em bloco, então utilizamos a `<div>`.
## Partes que compõem uma div
1. **O conteúdo** (a parte de dentro, como o texto ou imagens que você colocou ali).
2. **O padding** (espaço entre o conteúdo e a borda da caixa, como um “colchão” que envolve o conteúdo).
3. **A borda** (um contorno em volta da caixa, como se fosse uma moldura).
4. **A margem** (espaço externo ao redor da caixa, que a separa de outros elementos).


## Divs externas e internas
1. **Div externa**: É a `<div>` que contém outras `<divs>` ou elementos dentro dela. Ela age como um contêiner maior. Por exemplo:
```css
<div class="externa">
    <!-- Conteúdo ou divs internas aqui -->
</div>
```

2. **Div interna**: É a `<div>` que está dentro de outra `<div>` (a externa). Ela pode ser usada para organizar melhor o conteúdo ou para aplicar estilos específicos. Exemplo:
```css
<div class="externa">
    <div class="interna">Conteúdo 1</div>
    <div class="interna">Conteúdo 2</div>
</div>
```
Nesse exemplo, as `divs` com classe `interna` estão dentro da `div` com classe `externa`. Isso cria uma relação de "div interna" e "div externa". Essa estrutura permite que você aplique diferentes estilos, posições e funcionalidades tanto para as divisões internas quanto para a externa, facilitando o layout da página.

Essas divisões também são essenciais para aplicar CSS, onde você pode, por exemplo, estilizar a `div externa` de forma diferente da `div interna` e organizar o layout de maneira mais eficiente.




## Box Sizing
A propriedade `box-sizing` controla como o navegador deve calcular o **tamanho da caixa** quando você define a sua largura e altura.
Existem dois valores principais para `box-sizing`: **`content-box`** e **`border-box`**. Vamos ver a diferença entre eles.

### 1. **`content-box` (Padrão)**
Aqui, o tamanho que você define para a largura e a altura refere-se **somente ao conteúdo** da caixa, sem incluir o padding e a borda. Ou seja, o navegador **soma** o padding e a borda ao tamanho total da caixa.

#### Analogia:
Pense no conteúdo da sua caixa como um **livro**. Se você disser que a largura do seu "livro" é 300px, isso **não inclui** a capa dura (borda) ou o espaço extra para proteção (padding). O livro por si só tem 300px de largura, mas se você adicionar padding ou uma borda grossa, o tamanho total do livro (com capa e tudo) vai aumentar.

#### Exemplo:
```css
div {
  width: 300px;
  padding: 20px;
  border: 10px solid black;
  box-sizing: content-box; /* Padrão */
}
```
- **Conteúdo:** 300px de largura.
- **Padding:** 20px em cada lado (esquerda e direita).
- **Borda:** 10px em cada lado (esquerda e direita).

Então, o **tamanho total da caixa** seria:  
300px (conteúdo) + 20px (padding esquerdo) + 20px (padding direito) + 10px (borda esquerda) + 10px (borda direita) = **360px** de largura total.

O que acontece aqui é que o tamanho da caixa acaba sendo **maior do que você esperava** porque o padding e a borda são adicionados **além** da largura e altura especificadas.

### 2. **`border-box`**
Neste caso, o valor de largura e altura que você define já inclui o conteúdo, o padding e a borda. Isso significa que o navegador ajusta o conteúdo para que a caixa completa (com borda e padding) tenha o tamanho que você especificou.

#### Analogia:
Imagine que você tem uma mala de viagem e diz que ela tem que caber no compartimento do avião, que tem 300px de largura. Aqui, você inclui **tudo**: o conteúdo dentro da mala, o forro interno (padding), e a capa externa da mala (borda). A mala toda tem que caber nos 300px, então, se a capa ou o forro forem muito grandes, o espaço para o conteúdo vai ser menor.

#### Exemplo:
```css
div {
  width: 300px;
  padding: 20px;
  border: 10px solid black;
  box-sizing: border-box;
}
```
- A **largura total** da caixa será sempre **300px**, mesmo que você adicione padding e bordas.
- O navegador ajusta o conteúdo para caber nos 300px, então o espaço real disponível para o conteúdo será menor.

Aqui, o cálculo seria:
- **Largura total:** 300px (fixo).
- **Padding:** 20px (ocupando parte dessa largura).
- **Borda:** 10px (ocupando parte dessa largura).

O **espaço real para o conteúdo** será:  
300px (largura total) - 20px (padding esquerdo e direito) - 10px (borda esquerda e direita) = **240px** de espaço para o conteúdo.


### Resumo das diferenças:
- **`content-box`:** A largura e a altura referem-se apenas ao conteúdo. O padding e a borda são **somados** à largura e à altura, tornando o tamanho total da caixa maior do que o especificado.
- **`border-box`:** A largura e a altura incluem o conteúdo, o padding e a borda. O conteúdo é ajustado para garantir que o tamanho total da caixa seja **igual** ao especificado.

### Para que usar cada um?
- **`content-box`** é bom quando você quer ter controle direto sobre o tamanho do conteúdo sem se preocupar com o padding e a borda.
- **`border-box`** é mais útil quando você quer garantir que a caixa sempre tenha um tamanho total exato, independente do padding ou da borda.




## Tipos de Display das Divs
Em CSS, a propriedade `display` controla como os elementos HTML (como `divs`) se comportam visualmente e como são colocados no layout da página. Aqui estão os principais valores que podem ser aplicados ao `display` de uma `div`, e como cada um funciona:

### 1. **`block`**
- **Explicação**: Define o elemento como um "bloco". Ele ocupa toda a largura disponível, começando em uma nova linha, e empurra outros elementos para a linha seguinte.
- **Exemplo**: A `div` se comporta como um parágrafo ou um título (`<p>`, `<h1>`).
- **Uso comum**: Para criar seções de página, caixas, containers de conteúdo.
- **Limitações**: Só consegue ser usada isoladamente numa linha, não tem como exibir mais de um elemento em uma linha só.
```css
div {
  display: block;
}
```

### 2. **`inline`**
- **Explicação**: Faz o elemento se comportar como um elemento "em linha", ocupando apenas a largura do seu conteúdo. Ele não quebra a linha, então pode ficar lado a lado com outros elementos.
- **Exemplo**: Similar a como uma tag `<span>` ou `<a>` se comporta.
- **Uso comum**: Para aplicar estilos sem quebrar o fluxo do texto.
- **Limitações**: Você não consegue alterar a altura do seu elemento. Só alterações horizontais, como `width`, porém `height`, não.
```css
div {
  display: inline;
}
```

### 3. **`inline-block`**
- **Explicação**: Combina comportamentos de `block` e `inline`. O elemento não quebra a linha, mas pode ter largura e altura definidas, diferente de `inline`.
- **Exemplo**: Elementos ficam lado a lado, mas você pode controlar suas dimensões.
- **Uso comum**: Para criar botões ou pequenos blocos que ficam lado a lado.
```css
div {
  display: inline-block;
}
```

### 4. **`flex`**
- **Explicação**: Ativa o **Flexbox**, um modo de layout que distribui os elementos filhos de uma maneira flexível. Ele oferece um controle avançado sobre o alinhamento e o espaço entre os elementos internos.
- **Exemplo**: Útil para layouts dinâmicos onde você deseja que os elementos se ajustem ao espaço disponível.
- **Uso comum**: Para layouts responsivos, como menus, galerias de imagens ou grids flexíveis.
```css
div {
  display: flex;
}
```

### 5. **`grid`**
- **Explicação**: Ativa o **Grid Layout**, que permite organizar os elementos filhos em linhas e colunas. Oferece controle mais preciso que o `flex` em alguns casos.
- **Exemplo**: Ótimo para layouts mais complexos de página, como layouts de revistas ou dashboards.
- **Uso comum**: Para criar layouts com múltiplas colunas e linhas.
```css
div {
  display: grid;
}
```

### 6. **`inline-flex`**
- **Explicação**: Comporta-se como `flex`, mas o container flexível é tratado como um elemento "em linha", ou seja, não quebra a linha.
- **Exemplo**: Útil quando você deseja um layout flexível, mas precisa que ele esteja no fluxo de texto, sem quebrar a linha.
- **Uso comum**: Botões com ícones e textos ou pequenos layouts responsivos embutidos.
```css
div {
  display: inline-flex;
}
```

### 7. **`none`**
- **Explicação**: Remove o elemento completamente do layout visual e da acessibilidade. Ele não ocupa espaço, nem é renderizado.
- **Exemplo**: Ótimo para esconder temporariamente elementos da página.
- **Uso comum**: Para esconder modais ou conteúdos dinâmicos que podem aparecer sob certas condições.
```css
div {
  display: none;
}
```

### 8. **`table`**
- **Explicação**: Faz com que o elemento se comporte como uma tabela. Ele cria um contexto de tabela, onde os filhos podem ser tratados como linhas e células.
- **Exemplo**: A `div` se comporta como uma tag `<table>`.
- **Uso comum**: Quando você precisa de um layout semelhante a uma tabela sem usar tags `<table>`.
```css
div {
  display: table;
}
```

### 9. **`table-row`**
- **Explicação**: Faz com que o elemento se comporte como uma linha de tabela.
- **Exemplo**: A `div` age como uma `<tr>`.
- **Uso comum**: Para criar layouts de tabela com flexibilidade usando apenas `divs`.'
```css
div {
  display: table-row;
}
```

### 10. **`table-cell`**
- **Explicação**: Faz com que o elemento se comporte como uma célula de tabela.
- **Exemplo**: A `div` age como uma `<td>`.
- **Uso comum**: Para criar estruturas de tabela usando apenas `divs`, onde você tem controle mais direto do layout.
```css
div {
  display: table-cell;
}
```

### 11. **`contents`**
- **Explicação**: Faz com que o elemento não seja renderizado, mas seus filhos ainda sejam exibidos e façam parte do fluxo de layout como se fossem filhos diretos do pai do elemento.
- **Exemplo**: O `div` some, mas seus elementos internos continuam no layout.
- **Uso comum**: Quando você precisa de uma div para organização sem ela interferir no layout.
```css
div {
  display: contents;
}
```

### 12. **`list-item`**
- **Explicação**: Faz o elemento se comportar como um item de lista (`<li>`), permitindo que ele tenha marcadores (bullets).
- **Exemplo**: O `div` age como um `<li>`.
- **Uso comum**: Para criar listas personalizadas sem usar tags de lista.
```css
div {
  display: list-item;
}
```




- `<span>`: É uma tag genérica, é usada quando não se encontra uma tag semântica para um conteúdo de texto, então utilizamos o `<span>`.
- `<code>`: Define um bloco de código, assim, a fonte fica Monoespaçada.
- `<pre>`: Define texto pré-formatado (Não desconsidera os espaços e quebras de linha do texto).
Exemplo de uso do `<pre>` junto com o `<code>`:
```html
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
- `<cite>`: Referência uma obra (como título de livro ou site, ou o nome do autor).




## 9. **Tags de Metadados**

- `<meta>`: Define metadados sobre a página, como o charset (codificação de caracteres).
1) `charset`: Define o conjunto de caracteres que os navegadores vão interpretar. Alguns navegadores não conseguem interpretar, por exemplo, caracteres japoneses, então nós sempre colocamos o `UTF-8` para que os navegadores que não conseguem adaptar, adaptem.
2) `name`: Especifica qual é esse metadado.
3) `content`: É onde fica a configuração desse metadado, o conteúdo dele.

- `<link>`: Define a relação entre o documento atual e um recurso externo (usado para vincular estilos CSS, por exemplo.).
- `<style>`: Define estilos CSS internos se estiver dentro do `<head>`. Se estiver como um atributo de uma tag, é considerado um CSS Inline.
- `<script>`: Define scripts JavaScript.
- `type`: Pode ser usado em diversas tags para fornecer ao navegador e ao serviço de busca de websites informações adicionais.
#### Como `type` Funciona
O atributo `type` especifica o tipo MIME (Multipurpose Internet Mail Extensions) do recurso apontado pelo link. O tipo MIME é uma forma padrão de indicar o formato do arquivo, o que permite ao navegador ou a outro software saber que tipo de conteúdo ele está lidando e como deve processá-lo.
#### Quando Usar o `type`
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
```css
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
```css
.botao {
    background-color: green;
}
```
Isso aplicaria um fundo verde a qualquer elemento com a classe `botao`.

- **Seletores de ID**: Aplica estilos a um único elemento com um ID específico. Exemplo:
```css
#menu {
    border: 1px solid black;
}
```
Isso aplicaria uma borda preta ao elemento com o ID `menu`.

- **Seletores de Atributo**: Aplica estilos a elementos com um atributo específico. Exemplo:
```css
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





# FUNÇÕES CSS
Funções no CSS são **mecanismos que permitem realizar cálculos ou transformar valores** para estilizar os elementos de uma página de forma dinâmica e flexível. Pense nelas como pequenas "ferramentas" que você pode usar para ajustar valores de estilo, como cor, tamanho ou posição, de forma mais precisa e até automatizada.

#### Analogia
Imagine que você está construindo uma casa. As funções no CSS seriam como ferramentas (martelo, régua, serra) que você usa para moldar os materiais de acordo com o que você precisa, seja cortar uma madeira (ajustar um tamanho) ou medir uma parede (calcular uma posição). Essas ferramentas facilitam o trabalho ao invés de você ter que fazer tudo "na mão".


## 1. Funções de Cálculo

- `calc()`
A função `calc()` permite fazer cálculos matemáticos diretamente dentro do CSS. Você pode somar, subtrair, multiplicar e dividir diferentes unidades.

#### Analogia:
É como usar uma calculadora enquanto você projeta um móvel. Ao invés de adivinhar as medidas, você pode calcular a altura ideal de uma mesa somando as pernas à espessura do tampo.

#### Exemplo:
```css
.elemento {
    width: calc(100% - 20px);
}
```

Aqui, estamos dizendo que a largura do elemento deve ser 100% da largura do contêiner, mas subtraindo 20px. Isso é útil quando você precisa de um ajuste fino em um layout responsivo, por exemplo.



## 2. Funções de Manipulação de Cores

- `rgb()` e `rgba()`
Essas funções definem cores no formato RGB, onde você controla os níveis de vermelho (R), verde (G) e azul (B). A função `rgba()` adiciona um quarto parâmetro: a opacidade (alpha).

#### Analogia:
É como misturar tintas. Você tem três latas de tinta (vermelho, verde e azul) e pode misturá-las em diferentes proporções. No caso da função `rgba()`, você também pode adicionar mais ou menos água para deixar a tinta mais transparente (opacidade).

#### Exemplo:
```css
.elemento {
    background-color: rgba(255, 0, 0, 0.5); /* Vermelho com 50% de opacidade */
}
```


- `hsl()` e `hsla()`
Outra forma de definir cores é usando o **matiz (hue), saturação e luminosidade**. Aqui, você define a cor base pelo ângulo de matiz (de 0 a 360), a saturação (quanto de cor pura) e a luminosidade (quão clara ou escura a cor é). O `hsla()` também permite controlar a opacidade.

#### Analogia:
É como ajustar as cores de uma lâmpada LED inteligente, onde você controla o tom da luz (matiz), o quão forte ou fraca a cor aparece (saturação) e o brilho (luminosidade).

#### Exemplo:
```css
.elemento {
    color: hsl(120, 100%, 50%); /* Um verde vibrante */
}
```



## 3. Funções de Transformação

- `rotate()`
Essa função gira um elemento pelo número de graus que você especificar.

#### Analogia:
Imagine que você está segurando uma foto em suas mãos. Você pode girar essa foto em diferentes ângulos, como se fosse uma moldura na parede que você ajusta para ficar reta ou inclinada.

#### Exemplo:
```css
.elemento {
    transform: rotate(45deg); /* Gira o elemento 45 graus */
}
```

- `scale()`
Essa função aumenta ou diminui o tamanho de um elemento de acordo com um fator de escala.

#### Analogia:
Pense em uma lupa. Você pode usá-la para aumentar ou diminuir o tamanho daquilo que você está olhando, mas sem mudar a proporção.

#### Exemplo:
```css
.elemento {
    transform: scale(1.5); /* Aumenta o tamanho em 150% */
}
```



## 4. Funções de Posicionamento

- `translate()`
Essa função move um elemento de um lugar para outro, usando valores de deslocamento no eixo X (horizontal) e Y (vertical).

#### Analogia:
Imagine uma peça de xadrez em um tabuleiro. A função `translate()` é como pegar a peça e movê-la para outra posição, sem mudar o seu tamanho ou forma.

#### Exemplo:
```css
.elemento {
    transform: translate(50px, 100px); /* Move o elemento 50px à direita e 100px para baixo */
}
```



## 5. Funções de Desfoque e Filtros

-  `blur()`
Essa função aplica um efeito de desfoque em um elemento, semelhante ao que acontece quando você olha algo através de um vidro fosco.

#### Analogia:
Imagine que você está olhando uma foto através de um vidro embaçado. A função `blur()` cria exatamente esse efeito, tornando o conteúdo menos nítido.

#### Exemplo:
```css
.elemento {
    filter: blur(5px); /* Aplica um desfoque de 5px */
}
```

- `brightness()`
Ajusta o brilho de um elemento.

#### Analogia:
Pense em ajustar o brilho de uma TV. Quando você aumenta o brilho, a imagem fica mais clara; quando diminui, fica mais escura.

#### Exemplo:
```css
.elemento {
    filter: brightness(0.8); /* Reduz o brilho em 80% */
}
```



## 6. Funções de Gradientes

- `linear-gradient()`
Essa função cria uma transição suave entre duas ou mais cores ao longo de uma linha reta.

#### Analogia:
É como pintar uma parede com duas cores que vão se misturando conforme você sobe ou desce o pincel.

#### Exemplo:
```css
.elemento {
    background-image: linear-gradient(to right, red, yellow);
}
```
Aqui, a cor muda suavemente do vermelho para o amarelo, ao longo de uma linha horizontal (da esquerda para a direita).



## 7. Funções de Conteúdo

-  `attr()`
Essa função permite inserir o valor de um atributo HTML no conteúdo CSS.

#### Analogia:
É como preencher um campo de formulário automaticamente com base em uma informação já existente, sem que você precise digitar novamente.

#### Exemplo:
```css
a::before {
	content: attr(href); /* Mostra o valor do atributo href antes do link */

}
```





# USO DO `!IMPORTANT`
É usado para atribuir à um elemento HTML algum tipo de estilo, porém sobreescrevendo qualquer regra de cascata ou especificidade. É perigoso usá-lo, use com cuidado.
**Exemplo com cascata:**
```css
body {
	background-color: blue;
}

body {
	background-color: white !important;
}

body {
	background-color: red;
}

```
Seguindo a cascata do CSS, era pro fundo da página ficar vermelho, mas como a segunda declaração tem o `!important`, o fundo fica branco ao invés de vermelho.

**Exemplo com especificidade:**
```css
#exemplo {
	font-family: Verdana;
}

.exemplo_2 {
	width: 100px;
}

#exemplo {
	font-family: "Work Sans" !important;
}

.exemplo2 {
	width: 150px !important;
}

.exemplo2 {
	width: 200px;
}

#exemplo {
	font-family: Arial;
}
```
- Aqui, inicialmente, o elemento que tem o id `exemplo` tem a fonte Verdana. E os elementos que possuem a classe `exemplo_2` tem a largura de 100px.
- Porém, modificamos a fonte do `exemplo` para a Work Sans. E a largura do `exemplo_2` para 150px. Estes agora, com o `!important`.
- Modificamos de novo os elementos, agora, `exemplo` possui a fonte Arial, e `exemplo_2` possui 200px de largura.

Qual vai ser o resultado exibido? O `exemplo` com a Work Sans e o `exemplo_2` com 150px de largura. Pois estes detinham o `!important`. **Então independente da cascata, especificidade ou qualquer outra coisa, o resultado exibido vai ser o que estiver com o `!important`.**




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
```html
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
```html
<head>
    <link rel="stylesheet" href="styles.css">
</head>
```
Exemplo do arquivo `styles.css`:
```css
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

### PROPRIEDADES HERDÁVEIS E NÃO HERDÁVEIS
Propriedades **herdáveis** e **não herdáveis** em CSS definem como certos estilos são aplicados de elementos pais para seus elementos filhos.
### Propriedades Herdáveis:
Essas propriedades, por padrão, são transmitidas de um elemento pai para seus filhos, ou seja, os filhos herdam os valores definidos no pai. Isso ocorre para propriedades que fazem sentido serem consistentes ao longo de uma hierarquia de elementos.

#### Exemplos de propriedades herdáveis:
- **`color`**: A cor do texto.
- **`font-family`**: A família de fontes.
- **`font-size`**: O tamanho da fonte.
- **`line-height`**: A altura da linha.
- **`text-align`**: O alinhamento do texto.
- **`visibility`**: A visibilidade do conteúdo (visível ou oculto).

#### Por que são herdáveis?
Essas propriedades afetam o conteúdo textual e a aparência geral de elementos em uma árvore de elementos HTML. Por exemplo, se você definir uma cor de texto em um `div`, você provavelmente quer que todos os textos dentro dessa `div` tenham a mesma cor, a menos que especifique algo diferente em um nível mais baixo.


### Propriedades Não Herdáveis:
Essas propriedades **não são herdadas** automaticamente pelos elementos filhos. Elas precisam ser definidas especificamente para cada elemento, ou, por padrão, esses elementos usarão os valores iniciais ou padrões fornecidos pelo navegador.

#### Exemplos de propriedades não herdáveis:
- **`margin`**: A margem ao redor de um elemento.
- **`padding`**: O preenchimento dentro de um elemento.
- **`width` / `height`**: A largura e altura de um elemento.
- **`border`**: A borda de um elemento.
- **`background-color`**: A cor de fundo de um elemento.
- **`display`**: O tipo de exibição do elemento (por exemplo, `block`, `inline`, etc.).

#### Por que não são herdáveis?
Essas propriedades afetam a estrutura ou layout de elementos específicos, e não faz sentido que elas sejam herdadas. Por exemplo, se você define um `margin` em um elemento pai, não significa que você quer que todos os elementos filhos também tenham a mesma margem.

### Como controlar a herança:
- Você pode forçar a herança de uma propriedade não herdável usando **`inherit`**:
```css
div {
  background-color: inherit; /* Força a herança do background do pai */
}
```

Ou você pode evitar a herança de uma propriedade herdável usando **valores explícitos** como `initial` ou definir seu próprio valor:
```css
p {
  color: initial; /* Força o retorno ao valor padrão (normalmente preto) */
}
```

- **Propriedades herdáveis** são aquelas que fazem sentido se aplicarem de maneira consistente em um grupo de elementos filhos (como `color`, `font-family`).
- **Propriedades não herdáveis** são aquelas que afetam o layout ou características específicas de um elemento individual, e não têm um comportamento natural de herança (como `margin`, `width`).





## 1. **Cores e Fundos**

- `color`: Define a cor do texto. Exemplo: `color: #ff0000;` (vermelho)
1) `color: inherit`: Herda a cor do elemento anterior, o elemento pai. É útil quando você quer garantir que o valor da cor seja o mesmo que o do elemento pai, independentemente de qualquer outra estilização aplicada diretamente ao elemento.
2) `color: initial`: Esse valor faz com que a cor do elemento retorne ao seu valor inicial, ou seja, o valor padrão definido pelo navegador para aquela propriedade (que, no caso do `color`, geralmente é preto).
3) `color: unset`: O valor `unset` tem uma definição que depende da propriedade em questão:
	1. Se a propriedade é **herdável**, como a `color`, o `unset` faz com que a propriedade se comporte como `inherit`, ou seja, herde o valor do elemento pai.
	2. Se a propriedade **não** é herdável, o `unset` faz com que ela se comporte como `initial`, retornando ao valor inicial (padrão do navegador).




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


- `background-size`: Define o tamanho da imagem de fundo. Existem alguns valores, como: `left`, `right`, `top`, `bottom`, `center`, `contain` (caber verticalmente e horizontalmente o que puder, mas sem esticá-los), `cover` (cobrir tudo), `%`, `em`, etc. Você consegue determinar os outros lados do elemento, adicionando 2 ou mais valores, como: `background-size: center bottom;`.
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
- `position`: Define o método de posicionamento de um elemento. Valores: 
1) `static`
2) `relative`
3) `absolute` (independente de onde ele fique, a configuração vai ser aplicada)
4) `fixed`
5) `sticky`

Exemplo: `position: absolute;

`
- `top`, `right`, `bottom`, `left`: Define a posição de elementos posicionados. Exemplo: `top: 10px; left: 20px;
- `z-index`: Define em qual camada aquele elemento está.
- `float`: Posiciona um elemento à esquerda ou direita de seu container. Valores: `left`, `right`, `none` Exemplo: `float: left;`
- `clear`: Controla o comportamento de elementos ao lado de elementos flutuantes. Valores: `left`, `right`, `both`, `none` Exemplo: `clear: both;`




## 4. **Dimensões**

Existem diversas unidades de medida para passar nesses atributos de dimensões. Como:
- `in` (polegada)
- `cm` (Centímetros)
- `px` (Pixels)
- `mm` (Milímetros)
- in (Polegadas)
- pt
- pc
- vw (Viewport Width, largura da tela)
- vh (Viewport Height, altura da tela)
Se o valor passado for só o número, sem a unidade de medida depois do número, o navegador já vai previamente entender que estamos falando de pixels (px).


- `width`: Define a largura de um elemento. Exemplo: `width: 300px;` ou `width: 50%;`.
- `height`: Define a altura de um elemento. Exemplo: `height: 200px;`.
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
```css
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
```html
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

- `margin`: Define a margem externa de um elemento. Exemplos: 
1. `margin: 10px;` (Todos os lados possuem 10px.)
2. `margin: 10px 5px;` (Top e bottom possuem 10px, direita e esquerda possuem 5px.)
3. `margin: 10px 20px 30px;` (top: 10px, right e left; 20px, bottom: 30px.)
4. `margin: 10px 20px 30px 40px;` (top: 10px, right: 20px, bottom: 30px, left: 40px.)
Lembre sempre do sentido horário.
1) `auto`: Calcula automaticamente horizontalmente para a caixa ficar no centro. Esse cálculo não consegue ser feito verticalmente.
2) `%`: Se baseia em porcentagem para definir os tamanhos.
3) Margin Collapsing: Quando 2 elementos de tipo `display: block` estão com por exemplo:

Div 1) `bottom: 10px;`
Div 2 (Que está em baixo da Div 1)) `top: 15px;`

O resultado será de que o espaçamento entre os 2 elementos não vai ser a soma dos 2, e sim o maior valor entre os 2 vai ser o definido. Nesse caso, o espaçamento entre os 2 será de 15px.
Vale lembrar que se um elemento tem `display: inline;`, o resultado será a soma dos 2 espaços, não pegará o maior entre os 2, como acontece com o `display: block;`.

4) Caso queira, também existem as propriedades para cada lado, é bom usá-las quando você quer mudar só 1 lado em específico, porém os outros permanecem iguais:
1. `margin-top`;
2. `margin-right`;
3. `margin-bottom`;
4. `margin-left`.


5) Cuidado com os padrões dos navegadores, existem navegadores que colocam `margin` e outros elementos um padrão, onde você adiciona mais ainda no seu código, e o resultado não é o que você estava esperando, o que você pode fazer é:
```css
* {
	margin: 0px
}
```
Aqui, você está aplicando 0 de margem para todos os elementos. Ao invés desse asterísco, poderia ter `html` no lugar, tanto faz.



- `padding`: Define o preenchimento interno de um elemento. Exemplos: 
1. `padding: 15px;` (Todos os lados possuem 15px.)
2. `padding: 5px 10px;` (top e bottom: 5px, right e left: 10px.)
3. `padding: 15px 10px 5px;` (top: 15px, right e left: 10px, bottom: 5px.)
4. `padding: 15px 10px 5px 3px;` (top: 15px, right: 10px, bottom: 5px, left: 3px.)

1) Não existe `auto` aqui.
2) Caso queira, também existem as propriedades para cada lado, é bom usá-las quando você quer mudar só 1 lado em específico, porém os outros permanecerem iguais:
1. `padding-top`;
2. `padding-right`;
3. `padding-bottom`;
4. `padding-left`.


3) Cuidado com os padrões dos navegadores, existem navegadores que colocam `padding` e outros elementos um padrão, onde você adiciona mais ainda no seu código, e o resultado não é o que você estava esperando, o que você pode fazer é:
```css
* {
	padding: 0px
}
```




- `border`: Define a borda de um elemento. Exemplo: `border: 1px solid black;`
### Componentes da Propriedade `border`
Ela é composta por três partes principais:

- **Largura da borda** (`border-width`)
- **Estilo da borda** (`border-style`)
- **Cor da borda** (`border-color`)
Você pode definir cada uma delas separadamente ou usar a propriedade abreviada `border` para configurar tudo de uma vez.

#### a) **`border-width`** (Largura da borda)
Especifica a espessura da borda. Você pode usar valores como:
- Palavras-chave: `thin`, `medium`, `thick`


#### b) **`border-style`** (Estilo da borda)
Define o tipo de traçado da borda. Existem vários estilos que você pode usar:

- `none`: Sem borda
- `solid`: Uma linha contínua
- `dashed`: Uma linha pontilhada
- `dotted`: Uma linha de pontos
- `double`: Duas linhas
- `groove`: Uma borda em relevo que parece afundada
- `ridge`: Uma borda em relevo que parece elevada
- `inset`: Faz a borda parecer afundada em relação ao elemento
- `outset`: Faz a borda parecer elevada em relação ao elemento


#### c) **`border-color`** (Cor da borda)
Define a cor da borda. Pode usar nomes de cores, valores em hexadecimal, `rgb`, `rgba`, ou até usar palavras-chave como `transparent` (transparente).



### Propriedade abreviada `border`
Você pode combinar tudo em uma única linha usando a propriedade `border`. **A ORDEM É: LARGURA, ESTILO E COR.**
Exemplo:
```css
border: 2px solid blue;
```
Isso define uma borda de 2 pixels, sólida, na cor azul.


### Borda por lado
Se quiser aplicar bordas diferentes para cada lado (esquerda, direita, cima, baixo), você pode usar propriedades específicas:
- `border-top`
- `border-right`
- `border-bottom`
- `border-left`
Cada uma dessas propriedades aceita as mesmas regras de largura, estilo e cor.
**Exemplo:**
```css
border-top: 5px dotted green;
border-left: 3px solid black;
```




- `border-radius`: Arredonda os cantos de um elemento. Exemplo: `border-radius: 5px;`




- `outline`: À primeira vista, ele pode parecer similar ao `border`, mas existe uma diferença importante: o `outline` não afeta o fluxo de layout da página. Ele é uma borda _não encaixada_ ao redor do elemento, geralmente usado para destacar o foco de um elemento, como quando um botão é selecionado.
### Diferenças principais entre `outline` e `border`:
- **Espaçamento**: O `outline` não leva em consideração o tamanho do elemento. Ele pode "flutuar" ao redor do elemento, enquanto o `border` ocupa espaço dentro da caixa do elemento.
- **Não arredondável**: Você não pode aplicar `border-radius` a um `outline`.
- **Comportamento de foco**: `outline` é frequentemente usado para destacar elementos que estão no foco (por exemplo, ao usar a tecla Tab para navegar em um formulário).


### Diferença no comportamento de espaço e layout:
O `outline` não ocupa espaço no documento. Ele é desenhado "sobre" o conteúdo do elemento, enquanto o `border` empurra o conteúdo para dentro, afetando o tamanho final do elemento.


### Componentes da Propriedade `outline`
Assim como `border`, o `outline` tem largura, estilo e cor.


#### a) **`outline-width`** (Largura do contorno)
Funciona da mesma forma que `border-width`. Define a espessura do contorno.


#### b) **`outline-style`** (Estilo do contorno)
Funciona como o `border-style`, com as mesmas opções: `solid`, `dotted`, `dashed`, etc.


#### c) **`outline-color`** (Cor do contorno)
Define a cor do contorno.




- `outline-offset`: Define a distância entre o contorno `outline` e o elemento.


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
- `<position>`: Muda em qual parte uma imagem 2D está sendo exibida.
### Manipulando imagens 2D com a tag `<position>`
- `top`: Topo.
- `right`: Direita.
- `left`: Esquerda.
- `bottom`: Fundo, embaixo.
- `center`: Centro.

**Exemplos de uso:**
```css
.box {
	background-image: url(https://unsplash.com/photos/macbook-pro-on-black-wooden-table-PNbDkQ2DDgM);
	background-position: top left; /* Canto superior esquerdo da imagem */
}
```
Você consegue misturar os atributos. Como `right center` (Centro da imagem, porém na região direita da imagem).





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
```css
@font-face {
    font-family: 'MinhaFonte';
    src: url('minha-fonte.woff2') format('woff2');
}
```


## 4. **Animações**

- **`@keyframes`**: Define uma animação CSS, especificando as etapas da animação. Exemplo:
```css
@keyframes nomeAnimacao {
    from { opacity: 0; }
    to { opacity: 1; }
}
```


## 5. **Páginas e Impressão**

- **`@page`**: Controla a aparência de documentos impressos, como margens e tamanho da página. Exemplo:
```css
@page {
    margin: 1cm;
}
```

- **`@media print`**: Aplica estilos específicos quando um documento está sendo impresso. Exemplo:
```css
@media print {
    body {
        color: black;
        background: white;
    }
}
```


## 6. **Regras de Documentos e Componentes**

- **`@document`**: Aplica estilos a documentos baseados em sua URL ou outras características (não amplamente suportado). Exemplo:
```css
@document url("https://example.com/") {
    h1 {
        color: red;
    }
}
```

- **`@layer`**: Controla a ordem de aplicação de camadas de estilos, garantindo que as regras CSS se sobreponham da maneira desejada (CSS Cascade Layers). Exemplo:
```css
@layer base {
    body {
        margin: 0;
    }
}
```


## 7. **Suporte para Condições de Propriedades**

- **`@supports not`**: Aplica estilos se uma propriedade **não** for suportada. Exemplo:
```css
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
```css
@container (max-width: 600px) {
    .item {
        font-size: 14px;
    }
}
```


## 10. **Outras At-Rules**

- **`@counter-style`**: Define estilos personalizados para listas numeradas. Exemplo:
```css
@counter-style minha-contagem {
    system: cyclic;
    symbols: "A" "B" "C";
    suffix: ". ";
}
```

- **`@viewport`**: Define configurações para a viewport em dispositivos móveis (pouco utilizado). Exemplo:
```css
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
```html
<h1 class="titulo-vermelho">Título 1</h1>
<h1 class="titulo-vermelho">Título 2</h1>
<h1 class="titulo-vermelho">Título 3</h1>
```
No CSS:
```css
.titulo-vermelho {
    color: red;
    font-size: 24px;
}
```
- **`.titulo-vermelho`** é o nome da classe (note o ponto `.` antes do nome no CSS).
- Qualquer elemento com a classe `titulo-vermelho` receberá as propriedades de estilo definidas: cor vermelha e tamanho de fonte 24px.

## USANDO MAIS DE UMA CLASSE EM UM ELEMENTO
Você pode dar mais de uma classe à um elemento. Por exemplo:

no HTML:
```html
<h1 class="vermelho grande">Texto</h1>
```
no CSS:
```css
.vermelho {
	color: red;
}

.grande {
	font-size: 2em;
}
```
Nesse exemplo, o elemento `<h1>` vai ser vermelho (`vermelho`), e vai ficar com o dobro de seu tamanho (`grande`).



# IDS
**ID** é uma forma de identificar **um único** elemento de maneira única na página. Enquanto uma classe pode ser usada em vários elementos, um ID é exclusivo para um único elemento, como um CPF (ou documento de identidade) para pessoas.

#### Analogia: Identidade Única
Imagine que em uma escola, cada aluno tem seu próprio número de matrícula. Esse número é único e identifica apenas aquele aluno. No HTML, o ID faz o mesmo para um elemento específico.

IDs são usados quando você quer aplicar um estilo único a um elemento específico, sem compartilhar esse estilo com outros elementos.

#### Exemplo Prático:
Suponha que você tenha um título na página que quer destacar com uma cor e tamanho únicos.

No HTML:
```html
<h1 id="titulo-unico">Título Único</h1>
```
No CSS:
```css
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
```css
p {
    color: black;
}
p {
    color: blue;
}
```
Neste exemplo, o texto será azul porque o segundo estilo é o último.

- **Especificidade:** Seletores mais específicos (como IDs) têm prioridade sobre seletores mais genéricos (como elementos).
```css
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

```css
p {
    color: blue;
}
```

- **Seletores de Classe:** Aplicam estilos a elementos que possuem uma determinada classe. Classes são como etiquetas que você pode colar em diferentes móveis (elementos).
```css
.destaque {
    color: orange;
    font-weight: bold;
}
```
Aplicação:
```css
<p class="destaque">Texto destacado.</p>
```

- **Seletores de ID:** Aplicam estilos a um único elemento que possui um ID específico. Como um número de série único para um móvel.
```css
#cabecalho {
    background-color: lightgrey;
}
```
Aplicação:
```html
<div id="cabecalho">Cabeçalho do site</div>
```

- **Seletores de atributo:** Aplicam estilos a todos os elementos que tiverem um atributo específico. É caracterizada pelos `[]`.
```css
[title] {
	color: yellow;
}
```
Aqui, todos os elementos que tiverem o atributo `title` neles, terão a cor amarela.




- **Pseudo-classes:** Essas permitem que você selecione elementos que estão em um **estado especial**. Pense nisso como se você tivesse uma regra que só se aplica quando algo **acontece** com o elemento. Aqui estão algumas das mais comuns:

1. **`:hover`**: Quando o mouse está sobre o elemento
Imagine que você tem um botão e quer que ele mude de cor só quando o usuário passa o mouse sobre ele. Isso é como se o botão ficasse com uma "luz" especial quando alguém olha para ele mais de perto.
```css
button:hover {
    background-color: lightblue;
}
```

2. **`:focus`**: Quando o elemento está focado
Isso se aplica quando um campo, como uma caixa de texto, está "ativo" — ou seja, o usuário clicou nele ou está digitando algo. É como se o campo de texto estivesse **no centro das atenções**.
```css
input:focus {
    border: 2px solid green;
}
```

3. **`:nth-child()`**: Seleciona um filho específico dentro de um pai
Essa pseudo-classe é como se você estivesse escolhendo um **móvel específico dentro de uma sala cheia de móveis iguais**. Você pode escolher, por exemplo, a terceira cadeira de uma fileira.
```css
li:nth-child(2) {
    color: red;
}
```
Aplicação:
```html
<ul>
  <li>Primeiro item</li>
  <li>Segundo item</li>
  <li>Terceiro item</li>
</ul>
```
Nesse exemplo, o segundo item da lista (`li:nth-child(2)`) vai ficar com a cor vermelha.

1) `even`: Seleciona os elementos de índices pares.
2) `odd`: Seleciona os elementos de índices ímpares.


 4. **`:first-child`** e **`:last-child`**: Seleciona o primeiro ou o último filho
Essas pseudo-classes são como se você estivesse decorando o **primeiro** ou o **último** móvel em uma fila de móveis.
```css
p:first-child {
    font-weight: bold;
}
p:last-child {
    font-style: italic;
}
```
Aplicação:
```html
<div>
  <p>Primeiro parágrafo</p>
  <p>Segundo parágrafo</p>
  <p>Último parágrafo</p>
</div>
```
O primeiro parágrafo ficará em negrito, enquanto o último ficará em itálico.


5. **`:not()`**: Seleciona tudo, exceto o que você definir
Essa é como se você estivesse dizendo: "Quero estilizar todos os móveis da sala, menos aquele sofá vermelho."
```css
button:not(.cancelar) {
    background-color: green;
}
```
Aplicação:
```html
<button class="confirmar">Confirmar</button>
<button class="cancelar">Cancelar</button>
```
Aqui, todos os botões **que não têm** a classe `cancelar` terão um fundo verde. No exemplo, só o botão de "Confirmar" será afetado.


6. **`:nth-of-type()`**: Seleciona um tipo específico de filho
Parece com o `nth-child()`, mas a diferença é que aqui você escolhe o número de um tipo específico de elemento, por exemplo, o terceiro `parágrafo`, mesmo que haja outros tipos de elementos entre eles.
```css
p:nth-of-type(2) {
    color: blue;
}
```
Aplicação:
```html
<div>
  <p>Primeiro parágrafo</p>
  <h2>Um título</h2>
  <p>Segundo parágrafo</p>
  <p>Terceiro parágrafo</p>
</div>
```
Nesse caso, o segundo parágrafo vai ficar azul, ignorando o fato de que há um título no meio.

7. **`:disabled`**: Se trata de um elemento que foi desabilitado.
8. **`:required`**: Se trata de um elemento que é obrigatório.




- **Pseudo-Elementos**: São elementos que são adicionados pelo próprio CSS, exemplos:
1. `::before`: Antes de um elemento, faça tal coisa. Esse pseudo-elemento precisa de um `content; "";` dentro dele, mesmo que ela não tenha nada dentro.
2. `::after`: Depois de um elemento, faça tal coisa. Esse pseudo-elemento precisa de um `content; "";` dentro dela, mesmo que ela não tenha nada dentro.
3. `::first-line`: Pega a primeira linha de um texto. E isso se adapta com o tamanho da tela do dispositivo.





# **MEDIA QUERIES E RESPONSIVIDADE**
CSS também permite criar designs responsivos que se adaptam a diferentes tamanhos de tela usando media queries. Pense nisso como ajustar a decoração da sua casa de acordo com o tamanho do cômodo.

Exemplo:
```css
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






# **FLEXBOX CSS**
**O que é o Flexbox?**
O Flexbox (ou _Flexible Box Layout_) é um sistema de layout em CSS que foi criado para facilitar o alinhamento e a distribuição de itens dentro de um contêiner, mesmo quando o tamanho dos itens ou do contêiner é dinâmico ou desconhecido. Ele é ideal para construir interfaces responsivas, permitindo que os elementos dentro de um contêiner se ajustem de acordo com o espaço disponível.



### **1. Conceito Básico**
Para usar o Flexbox, é necessário definir um elemento como contêiner flexível, usando a propriedade `display: flex;`. Isso transforma os elementos filhos dentro do contêiner em _"itens flexíveis"_ e os comportamentos de layout dentro desse contêiner passam a ser controlados pelas propriedades do Flexbox.

**Exemplo básico:**
HTML:
```html
<div class="flex-container">
    <div class="item">Item 1</div>
    <div class="item">Item 2</div>
    <div class="item">Item 3</div>
</div>
```

CSS:
```css
  .flex-container {
    display: flex;
  }

  .item {
    background-color: lightblue;
    padding: 10px;
    margin: 5px;
    border: 1px solid #000;
  }
```
No exemplo acima, o `div` com a classe `flex-container` é o **contêiner flexível** e os `divs` internos (`item`) são os **itens flexíveis**.



### **2. Eixos do Flexbox**
O Flexbox trabalha com dois eixos principais:
- **Eixo principal (main axis)**: Por padrão, este é o eixo horizontal, onde os itens são dispostos da esquerda para a direita. No entanto, isso pode mudar dependendo da propriedade `flex-direction`.
- **Eixo cruzado (cross axis)**: Este é o eixo perpendicular ao eixo principal. Ou seja, se o eixo principal é horizontal, o eixo cruzado será vertical, e vice-versa.



### **3. Propriedades do Contêiner Flexível**
Estas são as principais propriedades que controlam o comportamento de um contêiner Flexbox:

#### 3.1 `flex-direction`
Define a direção do fluxo dos itens no contêiner.

- `row`: Itens são organizados na linha (horizontal) (padrão).
- `row-reverse`: Itens são organizados na linha, mas em ordem reversa.
- `column`: Itens são organizados em coluna (vertical).
- `column-reverse`: Itens são organizados em coluna, mas de baixo para cima.
```css
.flex-container {
  display: flex;
  flex-direction: row; /* ou row-reverse, column, column-reverse */
}
```

#### 3.2 `justify-content`
Alinha os itens ao longo do **eixo principal** (horizontal por padrão).

- `flex-start`: Alinha os itens ao início do contêiner (padrão).
- `flex-end`: Alinha os itens ao final do contêiner.
- `center`: Alinha os itens no centro.
- `space-between`: Espaço igual entre os itens, sem espaço nas extremidades.
- `space-around`: Espaço igual entre os itens, com espaço nas extremidades.
- `space-evenly`: Espaçamento igual entre os itens e nas extremidades.
```css
.flex-container {
  justify-content: center; /* ou flex-start, flex-end, space-between, etc. */
}
```



#### 3.3 `align-items`
Controla o alinhamento dos itens no **eixo cruzado** (vertical por padrão).

- `flex-start`: Alinha os itens ao topo do contêiner.
- `flex-end`: Alinha os itens ao final do contêiner.
- `center`: Alinha os itens no centro vertical do contêiner.
- `baseline`: Alinha os itens na linha base do conteúdo.
- `stretch`: Faz os itens se esticarem para preencher o contêiner (padrão se não houver tamanho fixo).
```css
.flex-container {
  align-items: center; /* ou flex-start, flex-end, baseline, etc. */
}
```



#### 3.4 `align-content`
Define como múltiplas linhas (caso haja um "wrap") são distribuídas no contêiner, em relação ao **eixo cruzado**.

- `flex-start`: Linhas empilhadas no topo.
- `flex-end`: Linhas empilhadas no final.
- `center`: Linhas empilhadas no centro.
- `space-between`: Espaço igual entre as linhas.
- `space-around`: Espaço igual ao redor de cada linha.
- `stretch`: Linhas esticam para ocupar o contêiner inteiro (padrão).
```css
.flex-container {
  align-content: space-between; /* ou flex-start, flex-end, center, etc. */
}
```



#### 3.5 `flex-wrap`
Define se os itens devem quebrar em múltiplas linhas, caso não caibam em uma só linha.

- `nowrap`: Todos os itens permanecem em uma linha (padrão).
- `wrap`: Itens quebram em novas linhas quando necessário.
- `wrap-reverse`: Itens quebram em novas linhas, mas com a ordem inversa.
```css
.flex-container {
  flex-wrap: wrap; /* ou nowrap, wrap-reverse */
}
```




### **4. Propriedades dos Itens Flexíveis**

Agora, vamos ver as propriedades que você pode aplicar diretamente nos **itens flexíveis**.

#### 4.1 `flex-grow`

Determina quanto um item pode crescer em relação aos outros itens. O valor é numérico e a proporção de crescimento entre os itens é baseada nos seus valores.

- `0`: O item não cresce além de seu tamanho inicial (padrão).
- `1` ou mais: O item pode crescer para preencher o espaço disponível.

```css
.item {
  flex-grow: 1; /* O item pode crescer */
}
```
#### 4.2 `flex-shrink`
Define a capacidade do item de encolher, se necessário. Também usa valores numéricos.

- `0`: O item não pode encolher.
- `1`: O item pode encolher proporcionalmente ao espaço disponível.


#### 4.3 `flex-basis`
Determina o tamanho inicial do item antes de qualquer espaço extra ser distribuído. Pode ser um valor de comprimento (ex: `px`, `em`, `%`) ou a palavra `auto`.
```css
.item {
  flex-basis: 200px; /* Tamanho inicial do item */
}
```


#### 4.4 `align-self`
Permite que o item tenha um alinhamento diferente dos outros itens no eixo cruzado.

- `auto`: Usa o valor do `align-items` do contêiner (padrão).
- `flex-start`: Alinha o item no início do contêiner.
- `flex-end`: Alinha o item no final do contêiner.
- `center`: Alinha o item no centro vertical do contêiner.
- `baseline`: Alinha o item na linha base do conteúdo.
- `stretch`: Faz o item se esticar para preencher o contêiner.




## 5. Exemplo Completo
HTML:
```html
<div class="flex-container">
    <div class="item">Item 1</div>
    <div class="item">Item 2</div>
    <div class="item">Item 3</div>
</div>
```

CSS:
```css
  .flex-container {
    display: flex;
    flex-direction: row;
    justify-content: space-between;
    align-items: center;
    flex-wrap: wrap;
    height: 300px;
    background-color: lightgray;
}

  .item {
    flex-grow: 1;
    flex-basis: 100px;
    margin: 10px;
    background-color: lightblue;
    padding: 20px;
    text-align: center;
}
```




## **6. Recapitulando Propriedades e Atributos do Flexbox**
Aqui está uma lista rápida das propriedades que controlam o Flexbox:

#### **Propriedades do Contêiner**
- `display: flex;`
- `flex-direction: row | row-reverse | column | column-reverse`
- `justify-content: flex-start | flex-end | center | space-between | space-around | space-evenly`
- `align-items: flex-start | flex-end | center | baseline | stretch`
- `align-content: flex-start | flex-end | center | space-between | space-around | stretch`
- `flex-wrap: nowrap | wrap | wrap-reverse`

#### **Propriedades dos Itens**
- `flex-grow: 0 | 1 | ...`
- `flex-shrink: 0 | 1 | ...`
- `flex-basis: auto | (valor)`
- `align-self: auto | flex-start | flex-end | center | baseline | stretch`




# Flex Sizing
O conceito de **flex sizing** refere-se a como os elementos dentro de um container Flexbox (itens flexíveis) se ajustam e ocupam o espaço disponível com base nas propriedades do modelo Flexbox, como `flex-grow`, `flex-shrink`, e `flex-basis`. Essas propriedades controlam o comportamento de redimensionamento dos itens flexíveis, permitindo que você crie layouts que se adaptem de forma eficiente a diferentes tamanhos de tela.

Vamos entender cada uma dessas propriedades que formam a base do "flex sizing":


### 1. **`flex-grow`** (Crescimento Flexível)
A propriedade `flex-grow` controla o **quanto um item deve crescer em relação aos outros** dentro de um container flexível quando houver **espaço extra disponível**. O valor de `flex-grow` é um número, onde:

- Se `flex-grow: 0`, o item não cresce e mantém seu tamanho original, mesmo que haja espaço extra.
- Se `flex-grow: 1`, o item pode crescer para ocupar todo o espaço extra disponível no container.
- Se vários itens tiverem `flex-grow: 1`, eles dividirão o espaço extra igualmente.
- Se um item tiver `flex-grow: 2` e outro `flex-grow: 1`, o primeiro item crescerá duas vezes mais que o segundo.

**Exemplo:**
```css
.item1 {
  flex-grow: 2; /* Este item vai crescer mais */
}

.item2 {
  flex-grow: 1; /* Este item vai crescer menos */
}
```
Aqui, o `.item1` ocupará duas vezes mais espaço que o `.item2` se houver espaço extra.



### 2. **`flex-shrink`** (Encolhimento Flexível)
A propriedade `flex-shrink` controla **quanto um item pode encolher** quando **não houver espaço suficiente** no container flexível. O valor de `flex-shrink` também é um número:

- Se `flex-shrink: 0`, o item não encolherá, mantendo seu tamanho original, mesmo que não haja espaço suficiente no container.
- Se `flex-shrink: 1`, o item pode encolher para se ajustar ao espaço disponível.
- Se vários itens tiverem `flex-shrink: 1`, eles encolherão igualmente.
- Se um item tiver `flex-shrink: 2` e outro `flex-shrink: 1`, o primeiro item encolherá duas vezes mais que o segundo.

**Exemplo:**
```css
.item1 {
  flex-shrink: 2; /* Este item vai encolher mais */
}

.item2 {
  flex-shrink: 1; /* Este item vai encolher menos */
}
```
Se o container ficar muito pequeno, o `.item1` vai encolher mais do que o `.item2`, tornando-se proporcionalmente menor.



### 3. **`flex-basis`** (Tamanho Base Flexível)
A propriedade `flex-basis` define o **tamanho inicial** de um item flexível antes de ele começar a crescer ou encolher com base nas propriedades `flex-grow` ou `flex-shrink`. Basicamente, ela especifica o "tamanho ideal" do item.

Você pode definir o `flex-basis` com um valor de comprimento (`px`, `%`, etc.) ou deixar como `auto` (padrão, que usa o tamanho definido pelas propriedades de largura e altura).

- Se `flex-basis: 200px`, o item terá 200px de largura antes de aplicar as regras de crescimento e encolhimento.
- Se `flex-basis: 0`, o item começará sem largura e dependerá totalmente de `flex-grow` para ocupar espaço.

**Exemplo:**
```css
.item1 {
  flex-basis: 200px; /* Este item começa com 200px de largura */
}

.item2 {
  flex-basis: 100px; /* Este item começa com 100px de largura */
}
```
Aqui, o `.item1` terá o dobro do tamanho inicial do `.item2`, mas ainda pode crescer ou encolher com base em `flex-grow` e `flex-shrink`.



### 4. **`flex` (Shorthand)**: Combinação de `flex-grow`, `flex-shrink`, e `flex-basis`
A propriedade `flex` é uma abreviação que combina os três parâmetros: `flex-grow`, `flex-shrink`, e `flex-basis`. A sintaxe é:
```css
flex: <flex-grow> <flex-shrink> <flex-basis>;
```

Por exemplo, ao definir:
```css
.item {
  flex: 1 1 200px;
}
```
Isso significa que o item pode **crescer** (`flex-grow: 1`), **encolher** (`flex-shrink: 1`), e tem um **tamanho base inicial de 200px** (`flex-basis: 200px`).

Se você definir `flex: 1`, isso é o mesmo que definir `flex: 1 1 0`, ou seja, o item cresce e encolhe igualmente e seu tamanho base é 0.

### Exemplo Final:
```css
.item1 {
  flex: 2 1 100px; /* Cresce mais e tem um tamanho base de 100px */
}

.item2 {
  flex: 1 2 200px; /* Cresce menos e encolhe mais, com tamanho base de 200px */
}
```


### Resumo:
- **`flex-grow`**: Controla o crescimento de um item quando há espaço extra.
- **`flex-shrink`**: Controla o encolhimento de um item quando não há espaço suficiente.
- **`flex-basis`**: Define o tamanho inicial de um item antes de crescer ou encolher.
- **`flex` (shorthand)**: Combina `flex-grow`, `flex-shrink`, e `flex-basis` em uma única propriedade.

Essas três propriedades juntas formam o comportamento de "flex sizing" em layouts flexíveis, permitindo que os itens dentro de um container se ajustem de maneira eficiente, seja para expandir ou contrair conforme o espaço disponível.







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




# QUAL A MELHOR FORMA DE ESCREVER AS CORES NO VSCODE, BASEADO NOS 4 TIPOS QUE EXISTEM

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
Para importar uma fonte de outro lugar, você precisa do código embedado dela. Pode ser tanto um `<link>` (HTML) quanto um `@import`(CSS) (O `<link>` é um pouco mais rápido que o `@import`, então geralmente é preferível que você use o `<link>` dentro do documento HTML.).

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
- em (Baseada no tamanho da fonte do pai, se o pai tiver 16px, o elemento em questão com `2em` terá 32px.)
- ex (Baseada no tamanho do "x" da fonte)
- rem (Baseada no tamanho do "M" da fonte, só que no root.)
### Root
É o tamanho padrão já definido no navegador.
Usamos o `rem` porque o `em` pega o tamanho do pai, só que: se o tamanho do pai for um tamanho muito grande, e queremos nos basear no tamanho padrão que seria se aquele elemento pai não tivesse sido alterado. Usamos o `rem` para isso.

Para alterar o tamanho padrão dos elementos no root, você seleciona o elemento html no seu CSS e muda o que quiser mudar.


- vw
- vh (Baseada no tamanho do dispositivo)
- %

**A W3 recomenda a utilização SOMENTE do px, em e do rem.**
16px é o tamanho padrão das fontes, geralmente.
16px geralmente = 1em

**Exemplos:**
`font-size: 2em;`
`font-size: 20px;`



# FONTES EXTERNAS, COMO USAR

Quando a fonte é geralmente famosa e existe em um site que disponibilize o código para você utilizar, é preferível.
```css
@import url('https://fonts.googleapis.com/css2?family=Work+Sans:ital,wght@0,100..900;1,100..900&display=swap');
```

Mas quando a fonte não está num site como o Google Fonts, você vai precisar baixar ela, tendo o arquivo `.ttf` ou `.otf`, você utiliza o `@font-face`:
```css
@font-face {
	font-family: 'Love';
	src: url('fonts/love larry.ttf') format('truetype');
	font-weight: normal;
	font-style: normal;
}
```
Caso queira usar uma fonte externa com mais de uma extensão de arquivo, você adiciona um outro `url` do lado, assim:

```css
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





# **FIGMA**
https://www.figma.com/

O **Figma** é uma ferramenta de design colaborativo usada principalmente para criar interfaces de usuário (UI), protótipos interativos e layouts visuais para aplicativos e sites. Se você não sabe nada sobre o Figma, pense nele como uma mistura de uma prancheta de desenho com funções poderosas de colaboração em tempo real, tudo acessado diretamente do navegador. Vou quebrar isso em partes mais simples para te ajudar a entender o que faz o Figma ser tão especial e por que ele é amplamente utilizado no design de interfaces hoje em dia.

### 1. **Ferramenta de Design**
Pense no Figma como um papel digital gigante. Designers o usam para criar **mockups** (representações visuais de uma interface) ou **protótipos** (uma simulação interativa de como um aplicativo ou site funcionaria). No Figma, você pode criar botões, menus, ícones, e tudo o mais que compõe uma interface de usuário. É como usar ferramentas como o **Photoshop** ou **Illustrator**, mas mais focado em criar telas de aplicativos ou websites.

#### Analogia:
Imagine que você está montando uma casa de Lego. Cada peça de Lego seria um elemento da interface que você está projetando, como um botão ou um ícone. O Figma é a mesa onde você monta esses Legos, só que a mesa é digital e cheia de ferramentas que ajudam você a cortar, colar, alinhar e organizar os blocos.

### 2. **Colaboração em Tempo Real**
Um dos recursos mais poderosos do Figma é a capacidade de trabalhar **em equipe**, todos ao mesmo tempo e no mesmo arquivo. Em vez de cada pessoa fazer uma parte do design em separado e depois juntar tudo (como era comum com outras ferramentas), no Figma todo mundo pode ver e editar o trabalho de todos em tempo real, como se estivessem todos escrevendo no mesmo documento de texto.

#### Analogia:
Imagine que você está pintando um grande mural com seus amigos. Em vez de cada um pegar uma parte do mural, vocês todos podem pintar ao mesmo tempo na mesma parede, vendo o que os outros estão fazendo em tempo real. Assim, se você precisar ajustar algo para combinar com o que o outro pintou, pode fazer isso na hora, sem esperar.

### 3. **Baseado na Nuvem**
O Figma funciona completamente online, no navegador. Não precisa instalar nada no seu computador (embora também exista uma versão desktop opcional). Isso significa que você pode acessar seus arquivos de design de qualquer lugar e a qualquer momento, bastando ter acesso à internet.

#### Analogia:
É como ter seus projetos de design guardados em uma pasta na nuvem, como o Google Drive. Não importa onde você esteja, se você tiver uma conexão com a internet, pode abrir e editar seus arquivos.

### 4. **Protótipos Interativos**
Além de criar o design estático (os visuais), o Figma permite que você conecte diferentes telas e crie **prototipagem**, que é a simulação do comportamento de uma aplicação real. Você pode definir como os botões funcionam, como as páginas mudam, e até criar animações. Isso é extremamente útil para apresentar a ideia de como um aplicativo vai funcionar sem precisar programar nada.

#### Analogia:
Pense no protótipo como se fosse uma peça de teatro de um aplicativo. Você monta as cenas (as telas) e depois ensaia como os personagens (os elementos interativos) devem se mover e interagir uns com os outros. Tudo isso sem ter que "construir" o aplicativo de verdade.

### 5. **Componentes e Estilos**
O Figma também tem um sistema de **componentes reutilizáveis**. Imagine que você criou um botão que será usado em várias partes de um aplicativo. Em vez de desenhar esse botão várias vezes, você pode criar um "componente". Depois, quando você precisar mudar algo nesse botão, muda o componente uma vez, e a alteração será aplicada a todas as cópias dele no projeto. Isso economiza muito tempo.

Além disso, ele tem **estilos de design**, onde você define padrões para cores, tipografias (fontes) e espaçamentos, para garantir que todo o design mantenha uma consistência visual.

#### Analogia:
Imagine que você é um chefe de cozinha. Em vez de fazer um molho do zero toda vez que vai cozinhar, você faz um grande lote e guarda na geladeira. Toda vez que precisar do molho, você usa o que já preparou. Se precisar mudar algo na receita, basta mudar o molho na geladeira, e todos os pratos feitos com ele vão ser atualizados.

### 6. **Integração com Desenvolvedores**
Depois que o design está pronto, os desenvolvedores precisam transformar esse design em código. O `Figma` facilita muito essa transição, fornecendo especificações detalhadas do design diretamente no arquivo. Isso inclui medidas, cores, e até mesmo códigos CSS que os desenvolvedores podem usar para construir o projeto.

#### Analogia:
É como se o Figma fosse um arquiteto que desenha os planos detalhados de uma casa e depois entrega esses planos para o construtor, que vai seguir todas as medidas exatas para construir a casa no mundo real.

### Resumo das principais funcionalidades:
1. **Design UI/UX**: Criação de interfaces de usuário e experiências.
2. **Colaboração em Tempo Real**: Trabalhe junto com outras pessoas, em qualquer lugar.
3. **Baseado na Nuvem**: Não precisa instalar nada, e você pode acessar de qualquer lugar.
4. **Protótipos Interativos**: Simule o funcionamento de um aplicativo sem programar.
5. **Componentes e Estilos**: Crie peças reutilizáveis e padrões de design consistentes.
6. **Integração com Desenvolvedores**: Facilita a transição do design para o código.
