# projeto_lagarta_02H

### Alunos:

- Guilherme Pinho - 10755529
- Moabe da Silva Guedes Rêgo - 10748053
- Ryan Silva de Sousa - 10757255

---

## Processo de Ideação

Inicialmente partimos de um brainstorming tentando buscar ideias relacionadas a assuntos próximos de nós, como comércios de familiares e amigos. A partir disso, expandimos esse pensamento inicial e chegamos em estabelecimentos maiores, porém, que ainda apresentam dificuldade em se adaptar a internet e essa transição entre catalogar seus produtos físicos em um campo virtual.

Nossas principais ideias foram: Um site de brechó, visto que, muitos brechós focam em vender seu catálogo apenas em redes sociais, o que muitas vezes não passa a confiança, segurança e profissionalidade necessária que um site próprio pode passar (além de uma organização muito mais prática); e um site para bibliotecas ou sebos, que além dos pontos anteriores, também concentra outras informações relevantes sobre o local, como o seu acervo online, programação e eventos, convite para fazer o seu próprio evento, entre outros.

Por fim, como parte do grupo votou no brechó e a outra parte na biblioteca, decidimos jogar as opções em uma roda de sorteio online para ter a nossa escolha, tendo como resultado a opção da biblioteca.

---

## Caráter Extensionista

Escolhemos focar nos Sebos/Bibliotecas levando em consideração os que recebem grandes quantidades de livros por semanas e não possuem integração com seus serviços na web. Atuaremos em ajudar a melhorar a visibilidade, quantidade de vendas, prestígio, organização e consequentemente disponibilizar os acessos a literatura mais amplos. Nosso website irá considerar todas essas necessidades para maximizar os ganhos potenciais e economia para estes tipos de comércio.

---

## Wireframe

![imagem1](wiredesk.jpg)
![imagem2](wiremobile.jpg)

---

## Tutorial HTML

### Head

```html
<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link rel="stylesheet" href="index.css">
    <link rel="icon" type="image/x-icon" href="iconerickriordan.png">
    <title> Biblioteca </title>
</head>
```

Em nosso head temos as tags metas que contém as configurações de responsividade da home e das definições de caracteres especiais, links para arquivos externos que virão posteriormente, o título da página e o ícone da página.

---

### Body

#### Header (Menu)

```html
<header class="menu">
    <img src="logorickriordan.png" alt="Logo da biblioteca Rick Riordan" class="logo"> 
    <nav class="links">
        <button id="mudar_tema">...</button> 
        <a href=""> EVENTOS </a> 
        <a href=""> PROGRAMAÇÃO</a> 
        <a href=""> ACERVO </a> 
        <a href="" id="contato"> CONTATO </a> 
    </nav>
</header>
```

Fizemos um header onde ficará localizado o menu da página com a logo e nesse menu teremos nossos links `<a>` que redirecionarão para as páginas posteriores do site. Atualizamos o header utilizando uma estrutura mais semântica com `<nav>`, além da implementação do botão de troca de tema (dark/light mode), que utiliza ícones SVG e interação com JavaScript.

---

#### Section (Plano de fundo biblioteca e Carrossel)

```html
<section class="carrossel">
    <img src="capabiblioteca.png" class="slide ativo">
    <img src="capa2.png" class="slide">
    <img src="capa3.png" class="slide">

    <button class="prev">❮</button>
    <button class="next">❯</button>
</section>
```

Section contendo as 3 imagens que serão usadas para o carrossel, definindo as classes da imagem principal como `.slide ativo` (que vai estar aberto quando iniciar o site) e os restantes apenas como `.slide` que serão transformados em ativo conforme o JavaScript. Abaixo também temos dois botões para não depender apenas do carrossel automático, podendo passar para a próxima imagem clicando neles.

---

#### Main

Início do conteúdo principal da página `<main>` com 3 sections.

##### Section (3 Cards)

```html
<section> <!-- 1º Section com os 3 cards principais(3 sections) -->
    <section> <!-- 1º Card (Programação)-->
        <header>
            <a href="programacao.html">
                <img src="cardprogramacao.jpg" alt="">
            </a>
        </header>
        <div>
            <article>
                <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Sequi, repudiandae!</p>
            </article>
        </div>
    </section>
```

O 1º Section contém 3 cards direcionados para as 3 páginas mais relevantes da biblioteca: A de programações com detalhes de datas e futuras oficinas, do Acervo e de eventos para marcar algum evento próprio como um lançamento de livro. Nisso cada card tem o seu header com uma imagem clicável, e uma div com seu article e parágrafo com um texto simples explicando cada card.

---

##### 2º Section

```html
<section> <!-- 2º Section -->
    <div> <!-- Promoção/Evento -->
        <article>
            <img src="eventoprox.jpg" alt="">
            <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Iste pariatur libero architecto in...</p>
        </article>
    </div>
    <div> <!-- Livros em alta-->
        <article>
            <img src="livroemalta.jpg" alt="">
            <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Iste debitis eum a aut dolore beatae...</p>
        </article>
    </div>
</section>
```

Nesse segundo Section nós o separamos em duas divs pois dividirão a tela ao meio com seus respectivos conteúdos textuais contidos em `<p>` no article e imagens ilustrativas nas tags `<img>`.

---

##### 3º Section

```html
<section> <!-- 3º Section -->
    <div> <!-- Sobre nós -->
        <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Quisquam aspernatur dolore ut!...</p>
    </div>
    <div> <!-- Local -->
        <link rel="stylesheet" href="">
    </div>
</section>
```

O 3º Section vai seguir o mesmo espaço e estrutura dos sections passados, porém dividido em duas divs, uma apenas com um parágrafo falando sobre a biblioteca, e a outra com o local (fictício) dessa biblioteca, com um `link rel` para posteriormente adicionarmos o mapa do Google.

---

#### Footer

```html
<footer>
    <p>R. Conselheiro Brotero, 1353 - Santa Cecilia, São Paulo - SP, 01232-011</p>
    <section>
        <p>Desenvolvido por:</p>
        <figure>
            <img src="iconeguilherme.png" alt="">
            <figcaption>Guilherme Pinho</figcaption>
        </figure>
        <figure>
            <img src="iconemoabe.png" alt="">
            <figcaption>Moabe Guedes</figcaption>
        </figure>
        <figure>
            <img src="iconeryan.png" alt="">
            <figcaption>Ryan Sousa</figcaption>
        </figure>
    </section>
</footer>
```

Ao fim da página temos o nosso footer, onde nele tem a localização fictícia da nossa biblioteca virtual. Apresentamos também no final os desenvolvedores deste projeto, mostrando nossos nomes e ícones.

---

## Tutorial CSS

### Reset CSS

```css
html, body, div, span, applet, object, iframe,
h1, h2, h3, h4, h5, h6, p, blockquote, pre,
a, abbr, acronym, address, big, cite, code,
del, dfn, em, img, ins, kbd, q, s, samp,
small, strike, b, sub, sup, tt, var,
b, u, i, center,
dl, dt, dd, ol, ul, li,
fieldset, form, label, legend,
table, caption, tbody, tfoot, thead, tr, th, td,
article, aside, canvas, details, embed,
figure, figcaption, footer, header, hgroup,
menu, nav, output, ruby, section, summary,
time, mark, audio, video {
    margin: 0;
    padding: 0;
    border: 0;
    font-size: 100%;
    font: inherit;
    vertical-align: baseline;
    box-sizing: border-box;
} /* CSS reset */
```

Aqui aplicamos o reset da página zerando as margens, paddings, borders etc. para facilitar as estilizações que iremos utilizar nas classes dos elementos.

---

### Configuração html e body geral

```css
html {
    background-color: #fffff0;
}

body {
    padding-top: 180px; /* ajustar o começo do body para não ficar atrás do menu */
}
```

Aqui ajustamos a cor de fundo da página e colocamos um `padding-top` para a imagem não ficar atrás do nosso menu de navegação.

---

### Header

```css
/* Menu superior fixo na tela */
.menu {
    background-color: #B4C3D2;
    padding: 15px 50px;
    position: fixed;
    width: 100%;
    top: 0;
    display: flex;
    align-items: center;
    justify-content: space-between;
}

.links {
    display: flex;
    gap: 80px;
}

/* Logo do menu superior */
.logo {
    width: 150px;
}

/* Fonte geral do menu superior */
.links a {
    text-decoration: none;
    padding: 5px;
    font-family: 'Trebuchet MS', 'Lucida Sans Unicode', 'Lucida Grande', 'Lucida Sans', Arial, sans-serif;
    color: black;
}

/* Botão de contato do menu superior */
#contato {
    border: 3px solid black;
    padding: 5px;
    font-weight: bold;
}
```

Criamos 3 classes para separar a estilização dos elementos. A primeira classe `.menu` é respectiva a todo o header e é onde foram colocados a cor de fundo, posição fixa ao descer a barra de rolagem, display flex para alinhar horizontalmente, top para colar no topo da página e width 100% para usar toda a tela. `.links` é a classe da div que contém display flex e um espaço entre eles. `.links a` refere-se à estilização dos textos. Logo após, criamos um id para o link contato pois queríamos deixá-lo diferente dos restantes.

---

### 1º Section

```css
.sectioncards {
    display: flex;
    justify-content: space-around;
    align-items: center;
    padding-top: 60px;
    padding-bottom: 60px;
    background-color: #D1DCE8;
}

.imgcards {
    width: 500px;
    margin-bottom: 10px;
    border-radius: 25px;
}

.textocards {
    font-family: 'Gill Sans', 'Gill Sans MT', Calibri, 'Trebuchet MS', sans-serif;
}
```

No 1º section (que contém 3 cards com texto e imagem) temos 3 classes de personalização. A `.sectioncards` serve para dar forma ao 1º section e dispor os conteúdos interiores da forma que queríamos. Tem um flexbox para alinhar os conteúdos horizontalmente, com espaço entre si e alinhados no centro. No `.imgcards` alteramos apenas as 3 imagens, modificando o tamanho, arredondando as bordas e aumentando a margem inferior para espaçar da legenda. No `.textocards` alteramos apenas a fonte dos textos desse section.

---

### 2º Section

```css
.sectionpromocaoelivros {
    display: flex;
    justify-content: center;
    align-items: center;
    margin: 20px 0;
    padding: 30px 0;
}

.imgsection2 {
    max-width: 20%;
    height: auto;
    border-radius: 25px;
}

.titulosection2 {
    font-family: 'Gill Sans', 'Gill Sans MT', Calibri, 'Trebuchet MS', sans-serif;
    font-weight: bold;
    font-size: 20px;
}

.textosection2 {
    font-family: 'Gill Sans', 'Gill Sans MT', Calibri, 'Trebuchet MS', sans-serif;
    inline-size: 300px;
    text-align: justify;
    text-indent: 30px;
}

.bloco1section2 {
    margin: 0 30px;
}

.linhavertical {
    height: 400px;
    border: 1px solid black;
    margin: 0 15px;
}

.bloco2section2 {
    margin: 0 30px;
}
```

Nesta section mostramos nossos eventos próximos e livros em alta. Diferente do section 1, aqui usamos `justify-content` centralizado e diminuímos o padding para 30px. Colocamos `inline-size` para quebrar os textos, além de uma linha vertical com altura, margem e borda definidos para separar os conteúdos. Os blocos 1 e 2 têm margem para separar os textos da imagem.

---

### 3º Section

```css
.sectionfinal {
    display: flex;
    justify-content: space-between;
    align-items: center;
    background-color: #B4C3D2;
    padding: 30px 0;
}

.sobrenos {
    inline-size: 300px;
    margin: auto;
}

.local {
    margin: auto;
}

.local img {
    max-width: 100%;
    width: 400px;
}
```

No 3º section seguimos no mesmo molde dos anteriores, utilizamos um flexbox para alinhar e espaçar os conteúdos, com uma cor de fundo e um padding para espaçar o conteúdo das bordas. O `.sobrenos` tem `inline-size` para quebrar o texto em mais de uma linha e o `.local` tem ajuste na margem e tamanho da imagem do mapa.

---

### Footer — Geral

```css
.footerprincipal {
    background-color: gray;
    padding: 30px 0;
}

.footersection {
    display: flex;
    justify-content: center;
    align-items: center;
    gap: 50px;
}
```

No footer aplicamos uma cor mais escura, um padding para espaçar o conteúdo das bordas e um flexbox com o conteúdo centralizado e um gap para separar os figures interiores.

---

### Footer — Equipe de Desenvolvimento

```css
.footerfigure {
    display: flex;
    flex-direction: column;
    justify-content: space-around;
    align-items: center;
}

.footerimgequipe {
    width: 150px;
    height: 150px;
    border-radius: 50%;
    margin-top: 15px;
}

.footertexto {
    text-align: center;
    font-family: 'Gill Sans', 'Gill Sans MT', Calibri, 'Trebuchet MS', sans-serif;
}

.footernomealuno {
    margin-top: 10px;
}
```

Dentro do section no footer, temos um figure para cada pessoa da equipe, com um flexbox em coluna para deixar o nome abaixo da imagem, centralizado. A classe `.footerimgequipe` define o tamanho das imagens e as deixa em formato circular. Nas últimas 2 classes apenas centralizamos o texto, mudamos a fonte e adicionamos uma margem para separar os nomes das imagens.

---

## JavaScript

### Feature: Dark Mode

```javascript
const button = document.getElementById("mudar_tema");

button.addEventListener("click", () => {
    document.body.classList.toggle("dark-mode");

    if (document.body.classList.contains("dark-mode")) {
        localStorage.setItem("theme", "dark");
    } else {
        localStorage.setItem("theme", "light");
    }
});
```

Primeiro declaramos uma constante `button` e pegamos pelo `getElementById("mudar_tema")` para logo após adicionarmos um evento ao clicar nesse botão com o `button.addEventListener("click", () => {`. O evento disparado muda a estilização da página com o `document.body.classList.toggle("dark-mode")`, que altera as cores do body padrão. O trecho `if/else` verifica qual classe está ativa e salva a preferência no `localStorage`. O `.toggle` alterna a classe dark-mode no body — se não tiver, adiciona; se já existir, remove.

---

### Feature: Carrossel

#### Definição de variáveis e constantes

```javascript
const slides = document.querySelectorAll(".slide");
const next = document.querySelector(".next");
const prev = document.querySelector(".prev");

let index = 0;
```

Criamos 3 constantes e 1 variável. As constantes estabelecem uma conexão direta com o HTML, selecionando todos os elementos `.slide` e os botões de navegação `.next` e `.prev`. A variável `index` funciona como um marcador de posição, indicando qual slide está ativo. Começa em zero, ou seja, o primeiro slide é exibido por padrão.

#### Função mostrarSlide

```javascript
function mostrarSlide(i) {
    slides.forEach(slide => slide.classList.remove("ativo"));
    slides[i].classList.add("ativo");
}
```

A função `mostrarSlide` é o núcleo lógico do código. Ela percorre todos os slides removendo a classe `"ativo"` de cada um (ocultando todos), e em seguida adiciona essa classe apenas ao slide correspondente ao índice recebido como parâmetro.

#### Botões de navegação

```javascript
next.addEventListener("click", () => {
    index = (index + 1) % slides.length;
    mostrarSlide(index);
});

prev.addEventListener("click", () => {
    index = (index - 1 + slides.length) % slides.length;
    mostrarSlide(index);
});
```

No botão **próximo**, o índice é incrementado e o operador `%` garante que, ao chegar no último slide, o carrossel volte automaticamente para o primeiro. No botão **anterior**, o índice é decrementado; para evitar valores negativos, o código soma o tamanho total de slides antes de aplicar o módulo.

#### Avanço automático

```javascript
// Automático (troca a cada 3 segundos)
setInterval(() => {
    index = (index + 1) % slides.length;
    mostrarSlide(index);
}, 3000);
```

O `setInterval` executa o avanço de slide a cada 3 segundos automaticamente, mesmo sem interação do usuário.

---

## CSS do Dark Mode

```css
:root {
    --bg-color: #fffff0;
    --text-color: #000000;
    --card-bg: #f5f5f5;
    --menu-color: #B4C3D2;
    --footer-color: gray;
    --border-color: #000000;
    --button-bg: rgba(0,0,0,0.5);
    --button-text: #ffffff;
    --iconmudartema-color: rgb(0, 0, 0);

    /* Espaçamentos padronizados */
    --spacing-small: 10px;
    --spacing-medium: 20px;
    --spacing-large: 40px;
}

body {
    background-color: var(--bg-color);
    color: var(--text-color);
    transition: background-color 0.3s, color 0.3s;
}

.dark-mode {
    --bg-color: #7f8e9c;
    --text-color: #ffffff;
    --card-bg: #1e1e1e;
    --menu-color: #4e5c69;
    --footer-color: #001e27;
    --border-color: #ffffff;
    --button-bg: rgba(255,255,255,0.2);
    --button-text: #ffffff;
    --iconmudartema-color: yellow;
}

#mudar_tema {
    background-color: transparent;
    border: none;
    cursor: pointer;
}
```

No `:root` definimos variáveis CSS com as cores padrões do site (modo claro). No `body` especificamos a mudança de cor com uma transição suave de 0.3 segundos. A classe `.dark-mode` redefine essas variáveis com cores mais escuras. O `#mudar_tema` remove a borda e o fundo do botão, e muda o cursor para "mãozinha" ao passar por cima.

---

## CSS do Carrossel

```css
.carrossel {
    position: relative;
    width: 100%;
    height: 400px;
    overflow: hidden;
}

.slide {
    position: absolute;
    width: 100%;
    height: 100%;
    object-fit: cover;
    opacity: 0;
    transition: opacity 0.5s ease;
}

.slide.ativo {
    opacity: 1;
}

/* Botões */
.prev, .next {
    position: absolute;
    top: 50%;
    transform: translateY(-50%);
    font-size: 30px;
    background: rgba(0,0,0,0.5);
    color: white;
    border: none;
    cursor: pointer;
    padding: 10px;
}

.prev { left: 10px; }
.next { right: 10px; }
```

O `.carrossel` usa `position: relative` como referência para os elementos internos com `position: absolute`. O `overflow: hidden` esconde as partes dos slides que saem da área. Todos os `.slide` ficam empilhados com `opacity: 0` por padrão; o `.slide.ativo` recebe `opacity: 1`, e a `transition` cria o efeito de fade suave. Os botões são posicionados absolutamente e centralizados verticalmente com `top: 50%` + `translateY(-50%)`.

---

## CSS Responsivo (Mobile — Media Query)

```css
@media (max-width: 768px) {

    /* =========================
       MENU (TOPO DA PÁGINA)
       ========================= */

    .menu {
        flex-direction: column;
        gap: 5px;
        padding: 8px;
    }

    /*
    O menu originalmente é horizontal. Em telas pequenas mudamos para coluna,
    fazendo com que logo e links fiquem empilhados.
    */

    .logo {
        width: 80px;
    }

    .links {
        display: flex;
        align-items: center;
        flex-wrap: wrap;
        justify-content: center;
        gap: 0.5rem;
    }

    .links a,
    #mudar_tema {
        display: flex;
        align-items: center;
        justify-content: center;
        padding: 2px 4px;
        font-size: 12px;
    }

    #contato {
        border: 1px solid var(--border-color);
        padding: 3px 6px;
        font-weight: bold;
        font-size: 14px;
    }

    #mudar_tema {
        transform: scale(0.8);
    }


    /* =========================
       TÍTULO PRINCIPAL
       ========================= */

    .tituloinicial {
        font-size: 20px;
        margin: 15px 0;
    }


    /* =========================
       CARROSSEL
       ========================= */

    .carrossel {
        height: 180px;
    }

    .prev, .next {
        font-size: 18px;
        padding: 5px;
    }


    /* =========================
       SECTION 1 (CARDS)
       ========================= */

    .sectioncards {
        flex-direction: column;
        align-items: center;
        gap: var(--spacing-large);
    }

    .sectioncards section {
        max-width: 260px;
    }

    .textocards {
        font-size: 13px;
        padding: 0 10px;
    }


    /* =========================
       SECTION 2
       ========================= */

    .sectionpromocaoelivros {
        flex-direction: column;
        gap: 15px;
        padding: 20px 10px;
    }

    .imgsection2 {
        max-width: 200px;
        margin: 0 10px;
    }

    .titulo1section2,
    .titulo2section2 {
        font-size: 16px;
        text-align: center;
    }

    .textosection2 {
        font-size: 13px;
        text-align: center;
        text-indent: 0;
        padding: 0 10px;
    }

    .linhavertical {
        display: none;
    }

    .linhahorizontal {
        display: block;
    }


    /* =========================
       SECTION 3 (FINAL)
       ========================= */

    .sectionfinal {
        flex-direction: column;
        gap: 20px;
        padding: 20px 10px;
    }

    .sobrenos {
        max-width: 260px;
    }

    .titulosobrenos {
        font-size: 18px;
    }

    .sobrenos p {
        font-size: 13px;
    }

    .local {
        width: 100%;
        padding-top: 15px;
    }

    .local iframe {
        width: 95%;
        height: 180px;
        border-radius: 10px;
        display: block;
        margin: 0 auto;
    }


    /* =========================
       FOOTER
       ========================= */

    .footersection {
        flex-direction: row;
        justify-content: center;
        gap: 20px;
        flex-wrap: wrap;
    }

    .footerimgequipe {
        width: 60px;
        height: 60px;
    }

    .footernomealuno {
        font-size: 11px;
        text-align: center;
    }

    .footerfigure {
        width: 80px;
    }

    .footertexto {
        font-size: 12px;
        padding: 0 10px;
    }
}
```

Este bloco de media query é ativado quando a largura da tela for de até 768px (tablets e celulares). As principais adaptações são:

- **Menu**: passa de horizontal para coluna, com elementos menores e `flex-wrap` nos links
- **Carrossel**: altura reduzida de 400px para 180px
- **Cards (Section 1)**: empilhados em coluna com largura máxima de 260px
- **Section 2**: layout em coluna, linha vertical removida e substituída por linha horizontal
- **Section 3**: elementos empilhados, mapa ocupa 95% da largura com `margin: auto`
- **Footer**: continua em linha mas com `flex-wrap`, imagens e textos reduzidos

---

## HTML Atualizado (index.html)

Versão final do `index.html` com todas as melhorias aplicadas: textos reais substituindo o Lorem Ipsum, atributos `alt` descritivos nas imagens, ícone SVG no botão de tema, mapa do Google Maps via `<iframe>` e JavaScript movido para arquivo externo `script.js`.

```html
<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link rel="stylesheet" href="index.css">
    <link rel="icon" type="image/x-icon" href="iconerickriordan.png">
    <title> Biblioteca </title>
</head>
<body>
    <header class="menu">
        <img src="logorickriordan.png" alt="Logo da biblioteca Rick Riordan" class="logo"> 
        <nav class="links">
            <button id="mudar_tema"><svg xmlns="http://www.w3.org/2000/svg" width="22" height="22" fill="currentColor" class="bi bi-brightness-high-fill" viewBox="0 0 16 16">
                <path d="M12 8a4 4 0 1 1-8 0 4 4 0 0 1 8 0M8 0a.5.5 0 0 1 .5.5v2a.5.5 0 0 1-1 0v-2A.5.5 0 0 1 8 0m0 13a.5.5 0 0 1 .5.5v2a.5.5 0 0 1-1 0v-2A.5.5 0 0 1 8 13m8-5a.5.5 0 0 1-.5.5h-2a.5.5 0 0 1 0-1h2a.5.5 0 0 1 .5.5M3 8a.5.5 0 0 1-.5.5h-2a.5.5 0 0 1 0-1h2A.5.5 0 0 1 3 8m10.657-5.657a.5.5 0 0 1 0 .707l-1.414 1.415a.5.5 0 1 1-.707-.708l1.414-1.414a.5.5 0 0 1 .707 0m-9.193 9.193a.5.5 0 0 1 0 .707L3.05 13.657a.5.5 0 0 1-.707-.707l1.414-1.414a.5.5 0 0 1 .707 0m9.193 2.121a.5.5 0 0 1-.707 0l-1.414-1.414a.5.5 0 0 1 .707-.707l1.414 1.414a.5.5 0 0 1 0 .707M4.464 4.465a.5.5 0 0 1-.707 0L2.343 3.05a.5.5 0 1 1 .707-.707l1.414 1.414a.5.5 0 0 1 0 .708"/>
                </svg>
            </button> 
            <a href=""> EVENTOS </a> 
            <a href=""> PROGRAMAÇÃO</a> 
            <a href=""> ACERVO </a> 
            <a href="" id="contato"> CONTATO </a> 
        </nav>
    </header>
    <section class="carrossel">
        <img src="capabiblioteca.png" class="slide ativo">
        <img src="capa2.png" class="slide">
        <img src="capa3.png" class="slide">
    
        <button class="prev">❮</button>
        <button class="next">❯</button>
    </section>
    <h1 class="tituloinicial">Conheça a nossa Biblioteca!</h1>
    <main> 
        <section class="sectioncards"> <!-- 1º Section com os 3 cards principais(3 sections) -->
            <section> <!-- 1º Card (Programação)-->
                <header>
                    <a href="programacao.html">
                        <img src="cardprogramacao.jpg" alt="Imagem retratando a programação da biblioteca, contendo uma peça sendo realizada para crianças." class="imgcards">
                    </a>
                </header>
                    <article>
                        <h3 class="titulosection1">Programação</h3>
                        <p class="textocards">Confira a programação da nossa biblioteca, com atividades culturais, oficinas criativas e momentos especiais pensados para crianças, jovens e adultos.</p>
                    </article>
            </section>

            <section> <!-- 2º Card (Acervo) -->
                <header>
                    <a href="acervo.html">
                        <img src="cardacervo.jpg" alt="Imagem retratando o acervo, contendo uma estante cheia de livros se estendo até o fim da foto." class="imgcards">
                    </a>
                </header>
                    <article>
                        <h3 class="titulosection1">Acervo</h3>
                        <p class="textocards">Explore nosso acervo com uma grande variedade de livros, desde clássicos da literatura até obras contemporâneas para todos os gostos.</p>
                    </article>
            </section>

            <section> <!-- 3º Card (Eventos) -->
                <header>
                    <a href="eventos.html">
                        <img src="cardeventos.jpg" alt="Imagem retratando os eventos que podem ser realizados na biblioteca, contendo o lançamento de um livro de um escritor, juntamente a outras pessoas." class="imgcards">
                    </a>
                </header>
                    <article>
                        <h3 class="titulosection1">Faça o seu evento!</h3>
                        <p class="textocards">Participe dos nossos eventos, como lançamentos de livros, rodas de leitura e encontros com autores que aproximam você do universo literário.</p>
                    </article>
            </section>         
        </section>

        <section class="sectionpromocaoelivros"> <!-- 2º Section -->
            <img src="eventoprox.jpg" alt="Imagem retratando os próximos eventos que irão ocorrer, contendo uma dinâmica com crianças sentadas em círculo." class="imgsection2">
                <article class="bloco1section2"> <!-- Promoção/Evento -->
                    <h3 class="titulo1section2">Eventos Próximos</h3>
                    <p class="textosection2">Fique por dentro dos próximos eventos da biblioteca! Teremos contação de histórias, oficinas educativas e atividades interativas para todas as idades ao longo do mês.</p>
                </article>
            
            <div class="linhavertical"></div>  
            <div class="linhahorizontal"></div>

                <article class="bloco2section2"> <!-- Livro em alta-->
                    <h3 class="titulo2section2">Livro em Alta</h3>
                    <p class="textosection2">Descubra o livro em destaque da semana, escolhido pelos nossos leitores. Uma obra envolvente que promete encantar e despertar o interesse pela leitura.</p>
                </article>
            <img src="livroemalta.jpg" alt="Imagem com o atual livro em alta, neste caso, o livro 'Perigoso! Este livro contém coelhos!'" class="imgsection2">
        </section>

        <section class="sectionfinal"> <!-- 3º Section -->
            <article class="sobrenos"> <!-- Sobre nós -->
                <h3 class="titulosobrenos">Sobre Nós</h3>
                <p>Somos um espaço dedicado ao incentivo à leitura, ao conhecimento e à cultura. Nossa missão é proporcionar um ambiente acolhedor onde todos possam aprender, explorar e se conectar através dos livros.</p>
            </article>
            <div class="local"> <!-- Local -->
                <iframe src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d3657.0720126121896!2d-46.682935!3d-23.565856999999998!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x94ce572d94233575%3A0xac043ea588d47e1a!2sLivraria%20da%20Travessa!5e0!3m2!1spt-BR!2sbr!4v1775683529936!5m2!1spt-BR!2sbr" width="600" height="450" style="border:0;" allowfullscreen="" loading="lazy" referrerpolicy="no-referrer-when-downgrade"></iframe>
            </div>
        </section>
    </main>
    <footer class="footerprincipal">
        <p class="footertexto" style="margin-bottom: 30px;">R. Conselheiro Brotero, 1353 - Santa Cecilia, São Paulo - SP, 01232-011</p>
        <p class="footertexto">Desenvolvido por:</p>
        <section class="footersection">
            <figure class="footerfigure">
                <img src="iconeguilherme.png" alt="Imagem de perfil do membro do grupo Guilherme Pinho" class="footerimgequipe">
                <figcaption class="footernomealuno">Guilherme Pinho</figcaption>
            </figure>
            <figure class="footerfigure">
                <img src="iconemoabe.png" alt="Imagem de perfil do membro do grupo Moabe Guedes" class="footerimgequipe">
                <figcaption class="footernomealuno">Moabe Guedes</figcaption>
            </figure>
            <figure class="footerfigure">
                <img src="iconeryan.png" alt="Imagem de perfil do membro do grupo Ryan Sousa" class="footerimgequipe">
                <figcaption class="footernomealuno">Ryan Sousa</figcaption>
            </figure>
        </section>
    </footer>
    <script src="script.js"></script>
</body>
</html>
```

---

## JavaScript Atualizado (script.js)

Versão final do JavaScript separado em arquivo externo `script.js`. Nessa atualização, o dark mode foi aprimorado para também trocar o ícone do botão (sol/lua) e a logo da página ao alternar entre os temas, além de carregar o tema salvo no `localStorage` assim que a página é aberta. O intervalo do carrossel automático também foi ajustado de 3 para 5 segundos.

### Dark Mode

```javascript
const button = document.getElementById("mudar_tema");
const logo = document.querySelector(".logo");
const temaSalvo = localStorage.getItem("theme");

// Aplicar tema salvo ao carregar a página
if (button){
    if (temaSalvo === "dark") {
        document.body.classList.add("dark-mode");

        button.innerHTML = `<svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" fill="currentColor" class="bi bi-moon-fill" viewBox="0 0 16 16">
        <path d="M6 .278a.77.77 0 0 1 .08.858 7.2 7.2 0 0 0-.878 3.46c0 4.021 3.278 7.277 7.318 7.277q.792-.001 1.533-.16a.79.79 0 0 1 .81.316.73.73 0 0 1-.031.893A8.35 8.35 0 0 1 8.344 16C3.734 16 0 12.286 0 7.71 0 4.266 2.114 1.312 5.124.06A.75.75 0 0 1 6 .278"/>
        </svg>`;

        logo.src = "logorickriordan-dark.png";

    } else {
        button.innerHTML = `<svg xmlns="http://www.w3.org/2000/svg" width="22" height="22" fill="currentColor" class="bi bi-brightness-high-fill" viewBox="0 0 16 16">
        <path d="M12 8a4 4 0 1 1-8 0 4 4 0 0 1 8 0M8 0a.5.5 0 0 1 .5.5v2a.5.5 0 0 1-1 0v-2A.5.5 0 0 1 8 0m0 13a.5.5 0 0 1 .5.5v2a.5.5 0 0 1-1 0v-2A.5.5 0 0 1 8 13m8-5a.5.5 0 0 1-.5.5h-2a.5.5 0 0 1 0-1h2a.5.5 0 0 1 .5.5M3 8a.5.5 0 0 1-.5.5h-2a.5.5 0 0 1 0-1h2A.5.5 0 0 1 3 8m10.657-5.657a.5.5 0 0 1 0 .707l-1.414 1.415a.5.5 0 1 1-.707-.708l1.414-1.414a.5.5 0 0 1 .707 0m-9.193 9.193a.5.5 0 0 1 0 .707L3.05 13.657a.5.5 0 0 1-.707-.707l1.414-1.414a.5.5 0 0 1 .707 0m9.193 2.121a.5.5 0 0 1-.707 0l-1.414-1.414a.5.5 0 0 1 .707-.707l1.414 1.414a.5.5 0 0 1 0 .707M4.464 4.465a.5.5 0 0 1-.707 0L2.343 3.05a.5.5 0 1 1 .707-.707l1.414 1.414a.5.5 0 0 1 0 .708"/>
        </svg>`;

        logo.src = "logorickriordan.png";
    }

    button.addEventListener("click", () => {
        document.body.classList.toggle("dark-mode");

        if (document.body.classList.contains("dark-mode")) {
            localStorage.setItem("theme", "dark");
            button.innerHTML = `<svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" fill="currentColor" class="bi bi-moon-fill" viewBox="0 0 16 16">
            <path d="M6 .278a.77.77 0 0 1 .08.858 7.2 7.2 0 0 0-.878 3.46c0 4.021 3.278 7.277 7.318 7.277q.792-.001 1.533-.16a.79.79 0 0 1 .81.316.73.73 0 0 1-.031.893A8.35 8.35 0 0 1 8.344 16C3.734 16 0 12.286 0 7.71 0 4.266 2.114 1.312 5.124.06A.75.75 0 0 1 6 .278"/>
            </svg>`;
            logo.src = "logorickriordan-dark.png";

        } else {
            localStorage.setItem("theme", "light");
            button.innerHTML = `<svg xmlns="http://www.w3.org/2000/svg" width="22" height="22" fill="currentColor" class="bi bi-brightness-high-fill" viewBox="0 0 16 16">
            <path d="M12 8a4 4 0 1 1-8 0 4 4 0 0 1 8 0M8 0a.5.5 0 0 1 .5.5v2a.5.5 0 0 1-1 0v-2A.5.5 0 0 1 8 0m0 13a.5.5 0 0 1 .5.5v2a.5.5 0 0 1-1 0v-2A.5.5 0 0 1 8 13m8-5a.5.5 0 0 1-.5.5h-2a.5.5 0 0 1 0-1h2a.5.5 0 0 1 .5.5M3 8a.5.5 0 0 1-.5.5h-2a.5.5 0 0 1 0-1h2A.5.5 0 0 1 3 8m10.657-5.657a.5.5 0 0 1 0 .707l-1.414 1.415a.5.5 0 1 1-.707-.708l1.414-1.414a.5.5 0 0 1 .707 0m-9.193 9.193a.5.5 0 0 1 0 .707L3.05 13.657a.5.5 0 0 1-.707-.707l1.414-1.414a.5.5 0 0 1 .707 0m9.193 2.121a.5.5 0 0 1-.707 0l-1.414-1.414a.5.5 0 0 1 .707-.707l1.414 1.414a.5.5 0 0 1 0 .707M4.464 4.465a.5.5 0 0 1-.707 0L2.343 3.05a.5.5 0 1 1 .707-.707l1.414 1.414a.5.5 0 0 1 0 .708"/>
            </svg>`;
            logo.src = "logorickriordan.png";
        }
    });
}
```

Nessa versão atualizada do dark mode, além de alternar as cores da página, o JavaScript também troca o ícone do botão entre sol (modo claro) e lua (modo escuro) usando `button.innerHTML` com SVGs do Bootstrap Icons. A logo da biblioteca também é trocada para uma versão adaptada ao tema escuro (`logorickriordan-dark.png`). A constante `temaSalvo` verifica o `localStorage` assim que a página carrega, garantindo que o tema preferido do usuário seja aplicado automaticamente a cada visita, sem precisar clicar no botão novamente. Todo o bloco fica protegido pelo `if (button)` para evitar erros em páginas que não possuem o botão de tema.

---

### Carrossel

```javascript
// Carrossel
const slides = document.querySelectorAll(".slide");
const next = document.querySelector(".next");
const prev = document.querySelector(".prev");

let index = 0;

function mostrarSlide(i) {
    slides.forEach(slide => slide.classList.remove("ativo"));
    slides[i].classList.add("ativo");
}

next.addEventListener("click", () => {
    index = (index + 1) % slides.length;
    mostrarSlide(index);
});

prev.addEventListener("click", () => {
    index = (index - 1 + slides.length) % slides.length;
    mostrarSlide(index);
});

// Automático (troca a cada 5 segundos)
setInterval(() => {
    index = (index + 1) % slides.length;
    mostrarSlide(index);
}, 5000);
```

A lógica do carrossel se mantém a mesma da versão anterior, com a única alteração sendo o intervalo do avanço automático, que passou de 3000ms (3 segundos) para 5000ms (5 segundos), dando mais tempo para o usuário visualizar cada imagem antes da troca automática.

---
