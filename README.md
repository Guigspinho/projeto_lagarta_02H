# projeto_lagarta_02H

### Alunos:

Guilherme Pinho - 10755529

Moabe da Silva Guedes Rêgo - 10748053

Ryan Silva de Sousa - 10757255

## Processo de Ideação

Inicialmente partimos de um brainstorming tentando buscar ideias relacionadas a assuntos próximos de nós, como comércios de familiares e amigos. A partir disso, expandimos esse pensamento inicial e chegamos em estabelecimentos maiores, porém, que ainda apresentam dificuldade em se adaptar a internet e essa transição entre catalogar seus produtos físicos em um campo virtual. 

Nossas principais ideias foram: Um site de brechó, visto que, muitos brechós focam em vender seu catálogo apenas em redes sociais, o que muitas vezes não passa a confiança, segurança e profissionalidade necessária que um site próprio pode passar (além de uma organização muito mais prática); e um site para bibliotecas ou sebos, que além dos pontos anteriores, também concentra outras informações relevantes sobre o local, como o seu acervo online, programação e eventos, convite para fazer o seu próprio evento, entre outros.

Por fim, como parte do grupo votou no brechó e a outra parte na biblioteca, decidimos jogar as opções em uma roda de sorteio online para ter a nossa escolha, tendo como resultado a opção da biblioteca.

## Caráter Extensionista

Escolhemos focar nos Sebos/Bibliotecas levando em consideração os que recebem grandes quantidades de livros por semanas e não possuem integração com seus serviços na web.Atuaremos em ajudar a melhorar a visibilidade, quantidade de vendas, prestígio, organização e consequentemente disponibilizar os acessos a literatura mais amplos.Nosso website irá considerar todas essas necessidades para maximar os ganhos potenciais e economia para estes tipos de comércio

##  Wireframe
![imagem1](wiredesk.jpg)
![imagem2](wiremobile.jpg)

## Tutorial HTML

### Head
~~~html
<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link rel="stylesheet" href="index.css">
	<link rel="icon" type="image/x-icon" href="iconerickriordan.png">
    <title> Biblioteca </title>
</head>
~~~
Em nosso head temos as tags metas que contém as configurações de resposividade da home e das definições de caracteres especiais, links para arquivos externos e o título da página.

#### Fim do Head

### Body

#### Header (Menu)
~~~html
<header class="menu">
    <img src="logorickriordan.png" alt="Logo da biblioteca Rick Riordan" class="logo"> 
    <nav class="links">
        <button id="mudar_tema"></button>
        <a href=""> EVENTOS </a> 
        <a href=""> PROGRAMAÇÃO</a> 
        <a href=""> ACERVO </a> 
        <a href="" id="contato"> CONTATO </a> 
    </nav>
</header>
~~~
Fizemos um header onde ficará localizado o menu da página com a logo, links de navegação e um botão responsável por alternar entre tema claro e escuro.

#### Section (Carrossel)
~~~html
<section class="carrossel">
    <img src="capabiblioteca.png" class="slide ativo">
    <img src="capa2.png" class="slide">
    <img src="capa3.png" class="slide">

    <button class="prev">❮</button>
    <button class="next">❯</button>
</section>
~~~
Section contendo as imagens do carrossel. A classe "ativo" define qual imagem está visível. Os botões permitem navegação manual além da automática feita pelo JavaScript.

### Main

#### 1º Section (Cards)
~~~html
<section class="sectioncards">
~~~
Contém três cards principais: Programação, Acervo e Eventos. Cada card possui imagem clicável, título e descrição.

#### 2º Section
~~~html
<section class="sectionpromocaoelivros">
~~~
Dividido em dois blocos:
- Eventos próximos
- Livro em alta

Possui também uma linha divisória que muda de vertical para horizontal no mobile.

#### 3º Section
~~~html
<section class="sectionfinal">
~~~
Dividido em:
- Sobre nós
- Local (mapa do Google via iframe)

#### Fim do Main

### Footer
~~~html
<footer class="footerprincipal">
~~~
Contém endereço e equipe de desenvolvimento com imagens e nomes.

#### Fim do HTML

---

## Tutorial CSS

### RESET CSS
~~~css
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}
~~~
Zera estilos padrão do navegador.

---

### Variáveis CSS (Tema)

~~~css
:root {
    --bg-color: #fffff0;
    --text-color: #000;
    --menu-color: #B4C3D2;
}
~~~
Utilizamos variáveis para facilitar a troca de tema.

---

### Dark Mode

~~~css
.dark-mode {
    --bg-color: #7f8e9c;
    --text-color: #ffffff;
}
~~~
Ao aplicar essa classe no body, todo o site muda automaticamente de cor.

---

### Header

~~~css
.menu {
    position: sticky;
    top: 0;
    display: flex;
}
~~~
Menu fixo no topo com flexbox para alinhamento.

---

### Cards

~~~css
.sectioncards {
    display: flex;
    flex-wrap: wrap;
}
~~~
Cards organizados com flexbox e responsivos.

Efeito hover:
~~~css
img:hover {
    transform: scale(1.05);
}
~~~

---

### Section 2

~~~css
.sectionpromocaoelivros {
    display: flex;
}
~~~
Organização lado a lado (desktop) e coluna (mobile).

Linha divisória:
~~~css
.linhavertical
.linhahorizontal
~~~

---

### Section Final

~~~css
.sectionfinal {
    display: flex;
}
~~~
Organiza conteúdo de Sobre e Local.

---

### Footer

~~~css
.footersection {
    display: flex;
}
~~~
Alinha equipe.

---

### Carrossel

~~~css
.slide {
    opacity: 0;
}
.slide.ativo {
    opacity: 1;
}
~~~
Controla qual imagem aparece.

---

### Responsividade

~~~css
@media (max-width: 768px)
~~~
Adapta layout para celular:
- Menu em coluna
- Sections empilhadas
- Imagens menores

---

## JavaScript

### Dark Mode

~~~javascript
const button = document.getElementById("mudar_tema");
const temaSalvo = localStorage.getItem("theme");
~~~

Verifica o tema salvo e aplica automaticamente.

~~~javascript
document.body.classList.toggle("dark-mode");
~~~

Alterna o tema ao clicar.

~~~javascript
localStorage.setItem("theme", "dark");
~~~

Salva preferência do usuário.

Também há troca dinâmica de ícone e logo conforme o tema.

---

## Carrossel

### Variáveis

~~~javascript
const slides = document.querySelectorAll(".slide");
let index = 0;
~~~

### Função principal

~~~javascript
function mostrarSlide(i)
~~~

Remove o slide ativo e ativa o novo.

### Botões

~~~javascript
next.addEventListener("click", ...)
prev.addEventListener("click", ...)
~~~

### Automático

~~~javascript
setInterval(() => {
}, 5000);
~~~

Troca os slides automaticamente a cada 5 segundos.

---

## Conclusão

Nosso projeto implementa:

- Site responsivo
- Dark mode com persistência
- Carrossel automático e manual
- Layout moderno com flexbox

Aplicamos conceitos importantes de HTML, CSS e JavaScript para criar uma experiência completa e funcional.
