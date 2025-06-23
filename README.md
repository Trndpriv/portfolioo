# portfolioo
‎about.html
+27
-15
Lines changed: 27 additions & 15 deletions
Original file line number	Diff line number	Diff line change
@@ -20,27 +20,39 @@

        <section class="container">

            <h1 class="container_title">
                Sobre mim
            </h1>
            <p class="container_content">
                At vero eos et accusamus et iusto odio dignissimos ducimus qui blanditiis praesentium voluptatum deleniti atque corrupti quos dolores et quas molestias excepturi sint occaecati cupiditate non provident, similique sunt in culpa qui officia deserunt mollitia animi, id est laborum et dolorum fuga.
            </p>
            <p class="container_content">
                Et harum quidem rerum facilis est et expedita distinctio. Nam libero tempore, cum soluta nobis est eligendi optio cumque nihil impedit quo minus id quod maxime placeat facere possimus, omnis voluptas assumenda est, omnis dolor repellendus. Temporibus autem quibusdam et aut officiis debitis aut rerum necessitatibus saepe eveniet ut et voluptates repudiandae sint et molestiae non recusandae. Itaque earum rerum hic tenetur a sapiente delectus, ut aut reiciendis voluptatibus maiores alias consequatur aut perferendis doloribus asperiores ipsum delis forum birol parela maxime infena. Excepteur sint occaecat cupidatat non.
            </p>
            <div class="wrapper">
                <h1 class="container_title">
                    Sobre mim
                </h1>
                
                <div class="container_content">
                    <p>
                        Olá! Meu nome é Alexandre Coelho e sou <strong class="strong--tertiary-color">Desenvolvedor Front-end</strong>. Iniciei minha jornada de aprendizagem do Desenvolvimento Web em 2022, assistindo vídeos e cursos gratuitos.
                    </p>
                    <p>
                        Destaco nesse inicio de jornada os cursos do professor <strong class="strong--tertiary-color">Gustavo Guanabara</strong> e dos vídeos de <strong class="strong--tertiary-color">Rafaella Ballerini</strong>, que me serviram de muita inspiração nesse começo.
                    </p>
                    <p>
                        Em 2023, por motivos escolares, não era viável estudar Desenvolvimento Web. Então eu aguardei, até que no fim de 2023, livre do colégio, adquiro a plataforma de ensino, Alura.
                    </p>
                    <p>
                        Agora com Alura, no inicio de 2024 começo meus estudos, dedicando a me desenvolver nessa área e tendo como ponto de partida Desenvolvimento Front-end
                    </p>
                    <p>
                        Atualmente, minhas melhores tecnologias são HTML, CSS e JS, entretanto também iniciei o estudo de React e TypeScript. Além disso, em agosto irei iniciar o meu curso de <strong class="strong--tertiary-color">Ciência da Computação</strong> pela UESC. 
                    </p>
                </div>
            </div>

        </section>
        <img class="main-img" src="./assets/joanaSantos.png" alt="Joana Santos digitando em um notebook">
        
    </main>

    
    <footer class="information">
        <p>
            Desenvolvido por Alura.
            Projeto Alura - Desenvolvido e Personalizado por Alexandre Coelho
        </p>
    </footer>

‎assets/Imagem.png
-183 KB
Binary file not shown.
‎assets/html.png
-3.13 KB
Binary file not shown.
‎assets/joanaSantos.png
-184 KB
Binary file not shown.
‎css/style.css
+173
-38
Lines changed: 173 additions & 38 deletions
Original file line number	Diff line number	Diff line change
@@ -3,23 +3,26 @@
@import url('https://fonts.googleapis.com/css2?family=Montserrat:wght@400;600&display=swap');

:root {
    --primary-color: #000000;
    --primary-color: #394555;
    --secondary-color: #F6F6F6;
    --tertiary-color: #22D4FD;
    --menu-link-color: #20c0e4;
    --btn-fill-color: #272727;
    --tertiary-color: #FFA500;
    --menu-link-color: #eb9902;
    --btn-fill-color: #00000026;

    --primary-font-family: 'Krona One', sans-serif;
    --secondary-font-family: 'Montserrat', sans-serif;
}

body {
    background-color: black;
    position: relative;
    min-height: 100vh;
    background-color: var(--primary-color);
    color: #F6F6F6;
}

.navigation {
    padding: 2% 0 0 10%;
    padding: 5vh 0 0 10%;
}

.navigation__menu {
@@ -30,7 +33,7 @@ body {
.menu__link {
    color: var(--tertiary-color);
    font-family: var(--secondary-font-family);
    font-size: 24px;
    font-size: 2.4rem;
    font-weight: 600;
    text-decoration: none;
}
@@ -43,48 +46,64 @@ body {

.content {
    display: flex;
    justify-content: space-between;
    align-items: center;
    gap: 82px;
    height: 100%;
    flex-direction: column;

    padding: 5% 10%;
    padding: 5% 10% 150px;
}

.container {
    display: flex;
    flex-direction: column;
    gap: 40px;
    display: grid;
    grid-template-areas:
    "container_title main_img"
    "container_content main_img"
    ;
    column-gap: 10rem;

    width: 47%;
}

.container_title {
    grid-area: container_title;
    font-family: var(--primary-font-family);
    font-size: 3.6rem;
    line-height: 5.6rem;
    font-size: 5.2rem;
    line-height: 6.24rem;
}

.title_strong-aqua {
.strong--tertiary-color {
    color: var(--tertiary-color);
}

.container_content {
    grid-area: container_content;
    font-family: var(--secondary-font-family);
    font-size: 2.4rem;
    line-height: 3.6rem;
    max-width: 650px;
}

.container_links {
.container_content p {
    margin-top: 1.5rem;
}
.main-img {
    grid-area: main_img;
    align-self: center;
    border: 2px solid var(--tertiary-color);
    border-radius: 50%;
}
.links {
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    align-items: center;
    align-self: center;
    gap: 32px;

    width: 60%;
    width: 1020px;
    margin-top: 100px;
}

.links_subtitle {
@@ -94,17 +113,22 @@ body {
    line-height: 4rem;
}

.links_link-aqua {
.links_container {
    display: flex;
    justify-content: space-between;
    width: 100%;
}
.links_link {
    display: flex;
    justify-content: center;
    align-items: center;
    column-gap: 16px;

    width: 100%;
    border: 2px solid var(--tertiary-color);
    border-radius: 8px;
    padding: 21.5px 0;
    padding: 2rem 3rem;

    color: var(--secondary-color);
    font-size: 2.4rem;
@@ -114,19 +138,20 @@ body {
    line-height: 3.6rem;
}

.links_link-aqua:hover {
.links_link:hover {
    background-color: var(--btn-fill-color);

    transform: scale(1.03);
}

.main-img {
    width: 47%
}

.information {
    position: absolute;
    bottom: 0;
    background-color: var(--tertiary-color);

    width: 100%;
    padding: 24px 0px;

    color: var(--primary-color);
@@ -136,26 +161,136 @@ body {
    text-align: center;
}

@media (max-width: 1200px) {
@media  screen and (max-width: 1280px) {
    .container {
        gap: 5px 5rem;
    }
    .container_title {
        font-size: 3.6rem;
        line-height: 4.35rem;
    }
    .container_content {
        font-size: 1.8rem;
        line-height: 2.7rem;
    }
    .links {
        width: 768px;
    }
}
@media (max-width: 920px) {
    .navigation {
        padding: 10% 0 0;
        padding: 5% 0 0;
    }

    .navigation__menu {
        justify-content: center;
    }

    .content {
    .container {
        display: flex;
        flex-direction: column-reverse;
        gap: 5rem;
    }

        padding: 5%;
    .container_title {
        font-size: 3.2rem;
        line-height: 4.8rem;
    }

    .container {
    .container_title br {
        display: none;
    }
    .links {
        width: auto;
    }

    .main-img {
        width: 60%;
    .links_container {
        flex-direction: column;
        gap: 2rem;
        width: 100%;
    }
    .information {
        font-size: 1.8rem;
        line-height: 2.7rem;
    }
}
@media (max-width: 710px) {
    .navigation {
        padding: 10% 0 0;
    }
    .content {
        padding: 10% 10% 150px;
    }
    .container {
        gap: 1rem;
    }
    .container_title {
        text-align: center;
        font-size: 2.8rem;
        line-height: 4.2rem;
    }
    .container_title br {
        display: block;
    }
    .container_content {
        max-width: 480px;
    }
    .information {
        font-size: 1.6rem;
        line-height: 2.4rem;
    }
}
@media screen and (max-width: 490px) {
    .container_content {
        font-size: 1.6rem;
        line-height: 2.4rem;
    }
    .links_subtitle {
        font-size: 1.8rem;
        line-height: 1.5em;
    }
    .links_link {
        font-size: 1.8rem;
        line-height: 1.5em; 
    }
    .information {
        font-size: 1.4rem;
        line-height: 1.2em;
    }
}
@media screen and (max-width: 360px) {
    .menu__link {
        font-size: 2.2rem;
        line-height: 1.5em;
    }
}
@media screen and (max-width: 320px) {
    .navigation__menu {
        gap: 30px;
    }
    .container_content {
        max-width: 280px;
        margin-left: 5px;
    }
}
‎index.html
+25
-23
Lines changed: 25 additions & 23 deletions
Original file line number	Diff line number	Diff line change
@@ -17,47 +17,49 @@
    </header>

    <main class="content">
        
        <section class="container">
            <section class="container">
                <div class="wrapper">
                    <h1 class="container_title">
                        Desenvolvedor <br>
                        <strong class="strong--tertiary-color">Front-end!</strong>
                    </h1>
                    <div class="container_content">
                        <p>
                            Olá, Sou Alexandre Coelho! Desenvolvedor Front-end e estudo Desenvolvimento Web. Minhas principais tecnologias são <strong class="strong--tertiary-color">HTML</strong>, <strong class="strong--tertiary-color">CSS</strong> e <strong class="strong--tertiary-color">JS</strong>.
                        </p>
                        <p>Almejo me tornar um <strong class="strong--tertiary-color">Desenvolvedor FullStack</strong> e atualmente estou me especializando no Front-end.</p>
                    </div>
                </div>

            <h1 class="container_title">
                Tenha uma página web de qualidade <strong class="title_strong-aqua">com um bom Front-end!</strong>
            </h1>
            <p class="container_content">
                Olá, Sou Alexandre Coelho! Estudante de Desenvolvimento Web com conhecimento em HTML, CSS e JS.

                Almejo por ser um Desenvolvedor FullStack e atualmente estou me especializando no Front-end.
            </p>
            
            <div class="container_links">
                <h2 class="links_subtitle">Acesse minhas redes:</h2>
                <img class="main-img" src="https://github.com/coelhoalexandre.png" alt="Foto de Perfil de Alexandre Coelho no GitHub">
            </section>
        <section class="links">
            <h2 class="links_subtitle">Acesse minhas redes:</h2>

                <a class="links_link-aqua" href="https://github.com/coelhoalexandre">
            <div class="links_container">
                <a class="links_link" href="https://github.com/coelhoalexandre" target="_blank">
                    <img src="./assets/github.png" alt="GitHub Logo">
                    GitHub
                </a>
                <a class="links_link-aqua" href="https://www.linkedin.com/in/-coelhoalexandre/">
                <a class="links_link" href="https://www.linkedin.com/in/-coelhoalexandre/" target="_blank">
                    <img src="./assets/linkedin.png" alt="LinkedIn Logo">
                    LinkedIn
                </a>
                <a class="links_link-aqua" href="https://www.instagram.com/coelhoalexandre_/">
                <a class="links_link" href="https://www.instagram.com/coelhoalexandre_/" target="_blank">
                    <img src="./assets/instagram.png" alt="Instagram Logo">
                    Instagram
                </a>
            </div>
        </section>

        <img class="main-img" src="./assets/joanaSantos.png" alt="Joana Santos digitando em um notebook">
        </section>

    </main>
    
    <footer class="information">
