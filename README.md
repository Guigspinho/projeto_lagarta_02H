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

~~~html
<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link rel="stylesheet" href="home.css">
	<link rel="icon" type="image/x-icon" href="">
    <title> Biblioteca </title>
</head>
~~~
explicaçao balblabla

















## HTML (index.html)
<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link rel="stylesheet" href="home.css">
	<link rel="icon" type="image/x-icon" href="">
    <title> Biblioteca </title>
</head>
<body>
    <header>
        <img src="logorickriordan.png" alt="Logo">
        <a href=""> EVENTOS </a>
        <a href=""> PROGRAMAÇÃO </a>
        <a href=""> ACERVO </a>
        <a href=""> CONTATO </a>
    </header>
    <section>
        <img src="capabiblioteca.png" alt="Imagem de fundo da biblioteca">
    </section>

    <main> 
        <section> <!-- 1º Section com os 3 cards principais(3 sections) -->
            <section> <!-- 1º Card (Programação)-->
                <header>
                    <img src="cardprogramacao.jpg" alt="">
                </header>
                <div>
                    <article>
                        <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Sequi, repudiandae!</p>
                    </article>
                </div>
            </section>

            <section> <!-- 2º Card (Acervo) -->
                <header>
                    <img src="cardacervo.jpg" alt="">
                </header>
                <div>
                    <article>
                        <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Sequi, repudiandae!</p>
                    </article>
                </div>
            </section>

            <section> <!-- 3º Card (Eventos) -->
                <header>
                    <img src="cardeventos.jpg" alt="">
                </header>
                <div>
                    <article>
                        <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Sequi, repudiandae!</p>
                    </article>
                </div>
            </section>         
        </section>

        <section> <!-- 2º Section -->
            <div> <!-- Promoção/Evento -->
                <article>
                    <img src="eventoprox.jpg" alt="">
                    <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Iste pariatur libero architecto in, consequuntur deserunt ratione voluptate cupiditate aliquam. At provident exercitationem facere ipsa dolorum!</p>
                </article>
            </div>
            <div> <!-- Livros em alta-->
                <article>
                    <img src="livroemalta.jpg" alt="">
                    <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Iste debitis eum a aut dolore beatae, consectetur quam esse fuga odio repellendus natus pariatur dignissimos eos?</p>
                </article>
            </div>
        </section>

        <section> <!-- 3º Section -->
            <div> <!-- Sobre nós -->
                <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Quisquam aspernatur dolore ut! Nisi molestiae nostrum alias, molestias amet nobis itaque.</p>
            </div>
            <div> <!-- Local -->
                <link rel="stylesheet" href="">
            </div>
        </section>
    </main>
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
</body>
</html>



