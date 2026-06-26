<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Agro Forte, Futuro Sustentável</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    
    <style>
        /* Configurações Gerais e Reset */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            scroll-behavior: smooth;
        }

        :root {
            --cor-principal: #2e7d32; /* Verde Agro */
            --cor-escura: #1b5e20;
            --cor-destaque: #81c784;
            --cor-texto: #333333;
            --cor-fundo-claro: #f4f7f4;
            --branco: #ffffff;
        }

        body {
            color: var(--cor-texto);
            background-color: var(--branco);
            line-height: 1.6;
        }

        .container {
            width: 90%;
            max-width: 1200px;
            margin: 0 auto;
            padding: 60px 0;
        }

        /* Cabeçalho e Menu */
        header {
            background-color: var(--branco);
            box-shadow: 0 2px 10px rgba(0,0,0,0.1);
            position: sticky;
            top: 0;
            z-index: 1000;
        }

        .navbar {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 20px 0;
        }

        .logo {
            font-size: 1.5rem;
            font-weight: bold;
            color: var(--cor-principal);
        }

        .logo span {
            color: var(--cor-texto);
        }

        .logo i {
            margin-right: 8px;
        }

        nav ul {
            display: flex;
            list-style: none;
            align-items: center;
        }

        nav ul li {
            margin-left: 25px;
        }

        nav ul li a {
            text-decoration: none;
            color: var(--cor-texto);
            font-weight: 500;
            transition: color 0.3s;
        }

        nav ul li a:hover {
            color: var(--cor-principal);
        }

        .btn-nav {
            background-color: var(--cor-principal);
            color: var(--branco) !important;
            padding: 8px 16px;
            border-radius: 20px;
            transition: background 0.3s !important;
        }

        .btn-nav:hover {
            background-color: var(--cor-escura);
        }

        /* Seção Hero (Banner Principal) */
        .hero {
            background: linear-gradient(rgba(0, 0, 0, 0.5), rgba(0, 0, 0, 0.5)), 
                        url('https://images.unsplash.com/photo-1500937386664-56d1dfef3854?auto=format&fit=crop&w=1920&q=80') no-repeat center center/cover;
            height: 80vh;
            display: flex;
            align-items: center;
            color: var(--branco);
            text-align: center;
        }

        .hero-content h1 {
            font-size: 3.5rem;
            margin-bottom: 10px;
            font-weight: 800;
        }

        .hero-content p {
            font-size: 1.5rem;
            margin-bottom: 30px;
            font-weight: 300;
        }

        .btn-principal {
            display: inline-block;
            background-color: var(--cor-principal);
            color: var(--branco);
            padding: 12px 30px;
            text-decoration: none;
            border-radius: 5px;
            font-weight: bold;
            border: none;
            cursor: pointer;
            transition: background 0.3s, transform 0.2s;
        }

        .btn-principal:hover {
            background-color: var(--cor-escura);
            transform: translateY(-2px);
        }

        /* Seção Pilares */
        .pilares h2 {
            text-align: center;
            margin-bottom: 40px;
            font-size: 2rem;
        }

        .cards-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
        }

        .card {
            background-color: var(--branco);
            padding: 40px 30px;
            border-radius: 8px;
            text-align: center;
            box-shadow: 0 4px 15px rgba(0,0,0,0.05);
            border-top: 5px solid var(--cor-principal);
            transition: transform 0.3s;
        }

        .card:hover {
            transform: translateY(-5px);
        }

        .card i {
            font-size: 3rem;
            color: var(--cor-principal);
            margin-bottom: 20px;
        }

        .card h3 {
            margin-bottom: 15px;
            font-size: 1.3rem;
        }

        /* Seção Sobre */
        .sobre {
            background-color: var(--cor-fundo-claro);
            background-image: linear-gradient(to right, rgba(244,247,244,0.9), rgba(244,247,244,0.7)),
                              url('https://images.unsplash.com/photo-1605000797499-95a51c5269ae?auto=format&fit=crop&w=800&q=80');
            background-repeat: no-repeat;
            background-position: right center;
            background-size: contain;
        }

        .sobre-container {
            display: flex;
        }

        .sobre-texto {
            max-width: 600px;
        }

        .sobre-texto h2 {
            font-size: 2rem;
            margin-bottom: 20px;
        }

        .sobre-texto p {
            margin-bottom: 15px;
            font-size: 1.1rem;
        }

        /* Seção Contato */
        .contato {
            text-align: center;
            max-width: 600px;
        }

        .contato h2 {
            font-size: 2rem;
            margin-bottom: 10px;
        }

        .contato p {
            margin-bottom: 30px;
        }

        #form-contato {
            display: flex;
            flex-direction: column;
            gap: 15px;
        }

        .form-group input, .form-group textarea {
            width: 100%;
            padding: 12px;
            border: 1px solid #ccc;
            border-radius: 5px;
            font-size: 1rem;
            outline: none;
        }

        .form-group input:focus, .form-group textarea:focus {
            border-color: var(--cor-principal);
        }

        #feedback-form {
            margin-top: 20px;
            padding: 15px;
            border-radius: 5px;
            font-weight: bold;
        }

        .sucesso {
            background-color: #d4edda;
            color: #155724;
        }

        .escondido {
            display: none;
        }

        /* Rodapé */
        footer {
            background-color: #1e241e;
            color: #a0a0a0;
            text-align: center;
            padding: 30px 0;
            font-size: 0.9rem;
        }

        /* Responsividade Básica */
        @media (max-width: 768px) {
            nav { display: none; }
            .hero-content h1 { font-size: 2.3rem; }
            .hero-content p { font-size: 1.1rem; }
            .sobre { background-image: none; }
        }
    </style>
</head>
<body>

    <header>
        <div class="navbar container">
            <div class="logo">
                <i class="fa-solid fa-leaf"></i> Agro<span>Sustentável</span>
            </div>
            <nav>
                <ul>
                    <li><a href="#inicio">Início</a></li>
                    <li><a href="#pilares">Pilares</a></li>
                    <li><a href="#sobre">Sobre Nós</a></li>
                    <li><a href="#contato" class="btn-nav">Contato</a></li>
                </ul>
            </nav>
        </div>
    </header>

    <section id="inicio" class="hero">
        <div class="hero-content container">
            <h1>Agro Forte, Futuro Sustentável</h1>
            <p>Equilíbrio entre produção e meio ambiente</p>
            <a href="#pilares" class="btn-principal">Conheça Nossas Soluções</a>
        </div>
    </section>

    <section id="pilares" class="pilares container">
        <h2>Como Unimos Produtividade e Conservação</h2>
        <div class="cards-grid">
            <div class="card">
                <i class="fa-solid fa-seedling"></i>
                <h3>Tecnologia Verde</h3>
                <p>Uso de bioinsumos e drones para otimizar o plantio, reduzindo o impacto ambiental e aumentando a eficiência.</p>
            </div>
            <div class="card">
                <i class="fa-solid fa-droplet"></i>
                <h3>Gestão Hídrica</h3>
                <p>Sistemas inteligentes de irrigação que evitam o desperdício e preservam nossos recursos mais preciosos.</p>
            </div>
            <div class="card">
                <i class="fa-solid fa-solar-panel"></i>
                <h3>Energia Limpa</h3>
                <p>Matriz energética baseada em fontes renováveis, como solar e biomassa, alimentando o campo do amanhã.</p>
            </div>
        </div>
    </section>

    <section id="sobre" class="sobre">
        <div class="container sobre-container">
            <div class="sobre-texto">
                <h2>O Futuro do Campo é Consciente</h2>
                <p>Acreditamos que a força do agronegócio não precisa caminhar na contramão da preservação. O verdadeiro progresso nasce do equilíbrio: produzir alimentos e matéria-prima de alta qualidade para o mundo, enquanto protegemos o solo, a água e a biodiversidade.</p>
                <p>Implementamos práticas de agricultura regenerativa e monitoramento em tempo real para garantir que cada hectare produza o seu máximo com o mínimo de pegada ecológica.</p>
            </div>
        </div>
    </section>

    <section id="contato" class="contato container">
        <h2>Fale Conosco</h2>
        <p>Quer saber como transformar sua produção ou apoiar o agro sustentável? Envie uma mensagem!</p>
        <form id="form-contato">
            <div class="form-group">
                <input type="text" id="nome" placeholder="Seu Nome" required>
            </div>
            <div class="form-group">
                <input type="email" id="email" placeholder="Seu E-mail" required>
            </div>
            <div class="form-group">
                <textarea id="mensagem" placeholder="Sua Mensagem" rows="5" required></textarea>
            </div>
            <button type="submit" class="btn-principal">Enviar Mensagem</button>
        </form>
        <div id="feedback-form" class="escondido"></div>
    </section>

    <footer>
        <p>&copy; 2026 AgroSustentável. Cultivando um amanhã melhor.</p>
    </footer>

    <script>
        document.addEventListener('DOMContentLoaded', () => {
            const form = document.getElementById('form-contato');
            const feedback = document.getElementById('feedback-form');

            form.addEventListener('submit', (e) => {
                e.preventDefault();

                const nome = document.getElementById('nome').value;
                const email = document.getElementById('email').value;

                if (nome && email) {
                    feedback.textContent = `Obrigado pelo contato, ${nome}! Sua mensagem sobre o Agro Sustentável foi recebida com sucesso.`;
                    feedback.className = 'sucesso';
                    
                    form.reset();

                    setTimeout(() => {
                        feedback.className = 'escondido';
                    }, 5000);
                }
            });
        });
    </script>
</body>
</html>
