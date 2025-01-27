<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="LHC Serviços e Locações - Locação de escavadeiras e caminhões basculantes.">
    <meta name="keywords" content="locação de equipamentos, escavadeiras, caminhões basculantes, terraplenagem">
    <meta name="author" content="LHC Serviços e Locações">
    <title>LHC Serviços e Locações</title>
    <style>
        /* Estilos Gerais */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        body {
            font-family: Arial, sans-serif;
            line-height: 1.6;
            background-color: #f4f4f4;
            color: #333;
        }
        header {
            background: url('escavadeira.jpg') no-repeat center center/cover;
            height: 70vh;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            color: white;
            text-align: center;
            padding: 20px;
        }
        header h1 {
            font-size: 3em;
            text-shadow: 2px 2px 5px rgba(0, 0, 0, 0.7);
        }
        header p {
            font-size: 1.2em;
            margin-top: 10px;
            text-shadow: 1px 1px 3px rgba(0, 0, 0, 0.7);
        }
        header .cta-button {
            margin-top: 20px;
            padding: 10px 20px;
            background-color: #ff8c00;
            color: white;
            font-size: 1.2em;
            border: none;
            border-radius: 5px;
            cursor: pointer;
            transition: background-color 0.3s ease;
        }
        header .cta-button:hover {
            background-color: #e07600;
        }

        /* Navegação */
        nav {
            background-color: #003d80;
            padding: 10px 20px;
            text-align: center;
        }
        nav a {
            color: white;
            text-decoration: none;
            margin: 0 15px;
            font-size: 1.1em;
            font-weight: bold;
            transition: color 0.3s ease;
        }
        nav a:hover {
            color: #ffa500;
        }

        /* Seções */
        section {
            padding: 40px 20px;
            max-width: 1200px;
            margin: auto;
        }
        section h2 {
            font-size: 2em;
            color: #003d80;
            margin-bottom: 20px;
        }
        section p, ul li {
            font-size: 1.1em;
            margin-bottom: 15px;
        }

        /* Imagens */
        .responsive-img {
            max-width: 100%;
            height: auto;
            border-radius: 10px;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
            margin: 20px 0;
        }

        /* Botões de redes sociais */
        .contato-links {
            display: flex;
            justify-content: center;
            align-items: center;
            gap: 20px;
            margin-top: 20px;
        }
        .contato-links img {
            width: 50px;
            height: 50px;
            transition: transform 0.3s ease;
        }
        .contato-links img:hover {
            transform: scale(1.1);
        }

        /* Formulário */
        form {
            background: #f9f9f9;
            padding: 20px;
            border: 1px solid #ddd;
            border-radius: 5px;
            max-width: 600px;
            margin: auto;
        }
        form input, form textarea, form button {
            width: 100%;
            padding: 10px;
            margin-bottom: 10px;
            border: 1px solid #ddd;
            border-radius: 5px;
        }
        form button {
            background-color: #003d80;
            color: white;
            font-size: 1.1em;
            border: none;
            cursor: pointer;
            transition: background-color 0.3s ease;
        }
        form button:hover {
            background-color: #ff8c00;
        }

        /* Rodapé */
        footer {
            background-color: #0056b3;
            color: white;
            text-align: center;
            padding: 15px;
            margin-top: 20px;
        }
        footer p {
            font-size: 0.9em;
        }

        /* Responsividade */
        @media (max-width: 768px) {
            header h1 {
                font-size: 2em;
            }
            header p {
                font-size: 1em;
            }
            .contato-links img {
                width: 40px;
                height: 40px;
            }
            .responsive-img {
                margin: 10px 0;
            }
        }

        @media (max-width: 480px) {
            nav a {
                font-size: 0.8em;
            }
            .contato-links img {
                width: 35px;
                height: 35px;
            }
        }
        .servicos-img {
        width: 100%; /* Faz a imagem ocupar 100% do espaço disponível inicialmente */
        max-width: 550px; /* Limita a largura máxima a 550px */
        height: auto; /* Mantém a proporção da imagem */
        max-height: 550px; /* Limita a altura máxima a 550px */
        border-radius: 10px; /* Adiciona bordas arredondadas (opcional) */
        box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2); /* Adiciona uma sombra (opcional) */
        margin: 20px auto; /* Centraliza a imagem horizontalmente */

        }
        .imagem-centralizada {
            display: block;
            margin-left: auto;
            margin-right: auto;
            width: 50%; /* Define o tamanho da imagem (50% da largura do contêiner) */
            max-width: 400px; /* Limita a largura máxima da imagem */
            height: auto; /* Mantém a proporção da imagem */
            border-radius: 10px; /* Adiciona bordas arredondadas (opcional) */
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2); /* Adiciona uma sombra (opcional) */

        }

        .galeria {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(150px, 1fr)); /* Responsivo */
            gap: 20px; /* Espaçamento entre as fotos */
            padding: 20px;
        }

        .galeria img {
            width: 100%; /* As imagens ocupam toda a célula */
            height: auto; /* Mantém a proporção */
            border-radius: 10px; /* Cantos arredondados */
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2); /* Sombra suave */
            transition: transform 0.3s ease; /* Efeito ao passar o mouse */
        }

        .galeria img:hover {
            transform: scale(1.05); /* Aumenta levemente ao passar o mouse */
        }

        /* Botão de Voltar ao Topo */
        #back-to-top {
            position: fixed;
            bottom: 20px;
            right: 20px;
            background-color: #003d80;
            color: white;
            border: none;
            padding: 10px 15px;
            border-radius: 50%;
            font-size: 1.2em;
            cursor: pointer;
            display: none;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
        }
        #back-to-top:hover {
            background-color: #ff8c00;
        }

         </style>
        </head>
        <body>
    <!-- Cabeçalho com imagem de destaque -->
    <header>
        <h1>LHC Serviços e Locações</h1>
        <p>Especialistas em Locação de Escavadeiras e Caminhões Basculantes</p>
        <button class="cta-button">Solicite um Orçamento Agora</button>
    </header>

    <!-- Navegação -->
    <nav>
        <a href="#inicio">Página Inicial</a>
        <a href="#sobre">Sobre Nós</a>
        <a href="#servicos">Serviços</a>
        <a href="#equipamentos">Equipamentos</a>
        <a href="#orcamento">Solicitação de Orçamento</a>
        <a href="#contato">Contato</a>
    </nav>

    <!-- Seções do site -->
    <section id="inicio">
        <h2>Bem-vindo à LHC Serviços e Locações</h2>
        <p>Oferecemos soluções completas em locação de equipamentos pesados para atender às necessidades de construção civil, infraestrutura, mineração e terraplenagem.</p>
    </section>

    <section id="sobre">
        <h2>Sobre Nós</h2>
        <p>Fundada em 2022, a LHC Serviços e Locações é referência no mercado de locação de equipamentos pesados. Nossa missão é oferecer qualidade, eficiência e segurança em cada projeto, sempre priorizando a satisfação dos nossos clientes.</p>
    </section>

    <section id="servicos">
        <h2>Nossos Serviços</h2>
        <ul>
            <li>✔ Locação de escavadeiras modernas e eficientes</li>
            <li>✔ Locação de caminhões basculantes para transporte de materiais</li>
            <li>✔ Equipamentos para terraplenagem e obras de infraestrutura</li>
            <li>✔ Manutenção Preventiva In Loco</li>
        </ul>
        <img src="motivos.png" alt="Imagem de caminhão basculante" class="imagem-centralizada">
    </section>

    <section id="equipamentos">
        <h2>Equipamentos</h2>
        <p>Confira nossa linha de equipamentos de alta performance disponíveis para locação:</p>
        <ul>
            <li>Escavadeiras hidráulicas</li>
            <li>Caminhões basculantes</li>
            <li>Caminhão 3/4 carroceria</li>
        <div class="galeria">
            <img src="Imagem do WhatsApp de 2025-01-26 à(s) 08.21.10_baaa7612.jpg" alt="Escavadeira hidráulica">
            <img src="Imagem do WhatsApp de 2025-01-14 à(s) 09.59.12_023c5ae8.jpg" alt="Caminhão basculante">
            <img src="Imagem do WhatsApp de 2025-01-26 à(s) 08.26.27_1a7e9d69.jpg" alt="Caminhão 3/4">
            <img src="Imagem do WhatsApp de 2025-01-26 à(s) 08.21.47_1a1ad352.jpg" alt="Retroescavadeira">
            <img src="caminhão_caçamba.jpg" alt="Motoniveladora">
        </div>
    </section>
    <section id="orcamento">
        <h2>Solicitação de Orçamento</h2>
        <form>
            <label for="nome">Nome:</label>
            <input type="text" id="nome" name="nome" placeholder="Seu nome completo" required>
            
            <label for="email">E-mail:</label>
            <input type="email" id="email" name="email" placeholder="Seu e-mail" required>

            <label for="telefone">Telefone:</label>
            <input type="tel" id="telefone" name="telefone" placeholder="Seu telefone">
            
            <label for="mensagem">Mensagem:</label>
            <textarea id="mensagem" name="mensagem" rows="5" placeholder="Descreva o serviço ou equipamento necessário"></textarea>
            
            <button type="submit">Enviar Solicitação</button>
        </form>
    </section>

    <section id="contato">
        <h2>Contato</h2>
        <p>Entre em contato conosco para mais informações:</p>
        <ul>
            <li><strong>Telefone:</strong> (34) 99199-9095</li>
            <li><strong>E-mail:</strong> leandrocrds.eng@gmail.com</li>
            <li><strong>Endereço:</strong> Rua Santa Catarina, 373, Uberaba-MG</li>
        </ul>
        <div class="contato-links">
            <a href="https://wa.me/5534991999095" target="_blank">
                <img src="https://upload.wikimedia.org/wikipedia/commons/6/6b/WhatsApp.svg" alt="WhatsApp">
            </a>
            <a href="https://www.instagram.com/lhc.servicos.locacoes" target="_blank">
                <img src="https://upload.wikimedia.org/wikipedia/commons/a/a5/Instagram_icon.png" alt="Instagram">
            </a>
        </div>
    </section>

    <footer>
        <p>&copy; 2025 LHC Serviços e Locações. Todos os direitos reservados.</p>
    </footer>

    <!-- Botão de Voltar ao Topo -->
    <button id="back-to-top">↑</button>

    <script>
        // Mostrar o botão de "Voltar ao Topo" ao rolar a página
        const backToTopButton = document.getElementById('back-to-top');

        window.addEventListener('scroll', () => {
            if (window.scrollY > 300) {
                backToTopButton.style.display = 'block';
            } else {
                backToTopButton.style.display = 'none';
            }
        });

        backToTopButton.addEventListener('click', () => {
            window.scrollTo({ top: 0, behavior: 'smooth' });
        });
    </script>
</body>
</html>
