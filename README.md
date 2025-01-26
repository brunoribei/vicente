
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Vicente Sonorização | Excelência em Sonorização e Iluminação</title>
    <meta name="description" content="Empresa líder em sonorização e iluminação para eventos. Oferecemos soluções profissionais para shows, casamentos e eventos corporativos.">
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Montserrat:wght@400;500;600;700&display=swap" rel="stylesheet">
    <style>
        /* Reset and base styles */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        :root {
            --primary: #2563eb;
            --primary-dark: #1d4ed8;
            --secondary: #0f172a;
            --accent: #f59e0b;
            --text: #334155;
            --text-light: #64748b;
            --background: #ffffff;
            --background-alt: #f8fafc;
            --border: #e2e8f0;
        }

        html {
            scroll-behavior: smooth;
            scroll-padding-top: 5rem;
        }

        body {
            font-family: 'Montserrat', sans-serif;
            line-height: 1.6;
            color: var(--text);
            background: var(--background);
        }

        /* Typography */
        h1, h2, h3, h4, h5, h6 {
            line-height: 1.2;
            color: var(--secondary);
        }

        .section-title {
            font-size: 2.5rem;
            font-weight: 700;
            text-align: center;
            margin-bottom: 3rem;
            position: relative;
            padding-bottom: 1rem;
        }

        .section-title::after {
            content: '';
            position: absolute;
            bottom: 0;
            left: 50%;
            transform: translateX(-50%);
            width: 80px;
            height: 4px;
            background: var(--primary);
            border-radius: 2px;
        }

        /* Layout */
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 1.5rem;
        }

        section {
            padding: 6rem 0;
        }

        /* Navigation */
        .navbar {
            position: fixed;
            top: 0;
            left: 0;
            right: 0;
            background: rgba(255, 255, 255, 0.95);
            backdrop-filter: blur(10px);
            box-shadow: 0 1px 3px rgba(0,0,0,0.1);
            z-index: 1000;
            transition: all 0.3s ease;
        }

        .navbar.scrolled {
            background: white;
            box-shadow: 0 2px 10px rgba(0,0,0,0.1);
        }

        .nav-container {
            height: 80px;
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .logo {
            display: flex;
            align-items: center;
            gap: 0.75rem;
            font-size: 1.5rem;
            font-weight: 700;
            color: var(--secondary);
            text-decoration: none;
            transition: color 0.3s;
        }

        .logo:hover {
            color: var(--primary);
        }

        .nav-links {
            display: flex;
            gap: 2.5rem;
        }

        .nav-links a {
            color: var(--text);
            text-decoration: none;
            font-weight: 500;
            transition: color 0.3s;
            position: relative;
        }

        .nav-links a::after {
            content: '';
            position: absolute;
            bottom: -4px;
            left: 0;
            width: 0;
            height: 2px;
            background: var(--primary);
            transition: width 0.3s ease;
        }

        .nav-links a:hover {
            color: var(--primary);
        }

        .nav-links a:hover::after {
            width: 100%;
        }

        /* Hero Section */
        .hero {
            height: 100vh;
            min-height: 600px;
            position: relative;
            display: flex;
            align-items: center;
            color: white;
            overflow: hidden;
        }

        .hero::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            background: linear-gradient(rgba(0,0,0,0.7), rgba(0,0,0,0.7)),
                        url('https://images.unsplash.com/photo-1470229722913-7c0e2dbbafd3?ixlib=rb-1.2.1&auto=format&fit=crop&w=1950&q=80');
            background-size: cover;
            background-position: center;
            background-attachment: fixed;
            z-index: -1;
            animation: zoomBg 20s infinite alternate;
        }

        @keyframes zoomBg {
            from { transform: scale(1); }
            to { transform: scale(1.1); }
        }

        .hero-content {
            max-width: 800px;
            margin: 0 auto;
            padding: 2rem;
            text-align: center;
            animation: fadeInUp 1s ease;
        }

        .hero h1 {
            font-size: 3.5rem;
            font-weight: 700;
            margin-bottom: 1.5rem;
            color: white;
            line-height: 1.2;
        }

        .hero p {
            font-size: 1.25rem;
            margin-bottom: 2rem;
            opacity: 0.9;
        }

        /* Services Section */
        .services {
            background: var(--background-alt);
        }

        .services-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 2rem;
        }

        .service-card {
            background: white;
            padding: 2.5rem;
            border-radius: 1rem;
            box-shadow: 0 4px 6px rgba(0,0,0,0.05);
            transition: all 0.3s ease;
            position: relative;
            overflow: hidden;
        }

        .service-card::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 4px;
            background: var(--primary);
            transform: scaleX(0);
            transform-origin: left;
            transition: transform 0.3s ease;
        }

        .service-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 8px 15px rgba(0,0,0,0.1);
        }

        .service-card:hover::before {
            transform: scaleX(1);
        }

        .service-icon {
            color: var(--primary);
            margin-bottom: 1.5rem;
        }

        .service-card h3 {
            font-size: 1.5rem;
            margin-bottom: 1rem;
        }

        /* Portfolio Section */
        .portfolio-tabs {
            display: flex;
            justify-content: center;
            gap: 1rem;
            margin-bottom: 3rem;
            flex-wrap: wrap;
        }

        .portfolio-tab {
            padding: 0.75rem 1.5rem;
            border: none;
            background: none;
            font-size: 1rem;
            font-weight: 500;
            color: var(--text);
            cursor: pointer;
            transition: all 0.3s;
            position: relative;
        }

        .portfolio-tab::after {
            content: '';
            position: absolute;
            bottom: 0;
            left: 0;
            width: 100%;
            height: 2px;
            background: var(--primary);
            transform: scaleX(0);
            transition: transform 0.3s ease;
        }

        .portfolio-tab.active {
            color: var(--primary);
        }

        .portfolio-tab.active::after {
            transform: scaleX(1);
        }

        .portfolio-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
            opacity: 0;
            transform: translateY(20px);
            animation: fadeInUp 0.5s ease forwards;
        }

        .portfolio-item {
            position: relative;
            border-radius: 1rem;
            overflow: hidden;
            aspect-ratio: 16/9;
            box-shadow: 0 4px 6px rgba(0,0,0,0.1);
        }

        .portfolio-item img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            transition: transform 0.5s ease;
        }

        .portfolio-item::after {
            content: '';
            position: absolute;
            inset: 0;
            background: linear-gradient(to top, rgba(0,0,0,0.7), transparent);
            opacity: 0;
            transition: opacity 0.3s ease;
        }

        .portfolio-item:hover img {
            transform: scale(1.1);
        }

        .portfolio-item:hover::after {
            opacity: 1;
        }

        /* Contact Section */
        .contact {
            background: var(--background-alt);
        }

        .contact-grid {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 4rem;
        }

        .contact-form {
            background: white;
            padding: 3rem;
            border-radius: 1rem;
            box-shadow: 0 4px 6px rgba(0,0,0,0.05);
        }

        .form-group {
            margin-bottom: 1.5rem;
        }

        .form-group label {
            display: block;
            margin-bottom: 0.5rem;
            font-weight: 500;
            color: var(--secondary);
        }

        .form-control {
            width: 100%;
            padding: 0.75rem 1rem;
            border: 2px solid var(--border);
            border-radius: 0.5rem;
            font-family: inherit;
            font-size: 1rem;
            transition: border-color 0.3s;
        }

        .form-control:focus {
            outline: none;
            border-color: var(--primary);
        }

        /* Buttons */
        .btn {
            display: inline-flex;
            align-items: center;
            justify-content: center;
            padding: 1rem 2rem;
            border-radius: 9999px;
            font-weight: 600;
            text-decoration: none;
            transition: all 0.3s;
            border: none;
            cursor: pointer;
            font-size: 1rem;
        }

        .btn-primary {
            background: var(--primary);
            color: white;
        }

        .btn-primary:hover {
            background: var(--primary-dark);
            transform: translateY(-2px);
            box-shadow: 0 4px 12px rgba(37, 99, 235, 0.2);
        }

        .btn-outline {
            background: transparent;
            border: 2px solid var(--primary);
            color: var(--primary);
        }

        .btn-outline:hover {
            background: var(--primary);
            color: white;
        }

        /* Animations */
        @keyframes fadeInUp {
            from {
                opacity: 0;
                transform: translateY(20px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        /* Footer */
        footer {
            background: var(--secondary);
            color: white;
            padding: 5rem 0 2rem;
        }

        .footer-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 3rem;
            margin-bottom: 3rem;
        }

        .footer-column h4 {
            color: white;
            font-size: 1.25rem;
            margin-bottom: 1.5rem;
            position: relative;
            padding-bottom: 0.75rem;
        }

        .footer-column h4::after {
            content: '';
            position: absolute;
            bottom: 0;
            left: 0;
            width: 40px;
            height: 2px;
            background: var(--primary);
        }

        .footer-links {
            list-style: none;
        }

        .footer-links li {
            margin-bottom: 0.75rem;
        }

        .footer-links a {
            color: #94a3b8;
            text-decoration: none;
            transition: color 0.3s;
        }

        .footer-links a:hover {
            color: white;
        }

        .social-links {
            display: flex;
            gap: 1rem;
        }

        .social-links a {
            display: flex;
            align-items: center;
            justify-content: center;
            width: 40px;
            height: 40px;
            border-radius: 50%;
            background: rgba(255,255,255,0.1);
            color: white;
            transition: all 0.3s;
        }

        .social-links a:hover {
            background: var(--primary);
            transform: translateY(-3px);
        }

        .copyright {
            text-align: center;
            padding-top: 2rem;
            border-top: 1px solid rgba(255,255,255,0.1);
            color: #94a3b8;
        }

        /* Responsive Design */
        @media (max-width: 768px) {
            .nav-container {
                height: 70px;
            }

            .menu-button {
                display: block;
            }

            .nav-links {
                display: none;
                position: absolute;
                top: 100%;
                left: 0;
                right: 0;
                background: white;
                padding: 1rem;
                box-shadow: 0 2px 4px rgba(0,0,0,0.1);
                flex-direction: column;
                gap: 1rem;
            }

            .nav-links.active {
                display: flex;
            }

            .hero h1 {
                font-size: 2.5rem;
            }

            .contact-grid {
                grid-template-columns: 1fr;
            }

            .section-title {
                font-size: 2rem;
            }
        }
    </style>
</head>
<body>
    <!-- Navigation -->
    <nav class="navbar">
        <div class="container nav-container">
            <a href="#" class="logo">
                <svg xmlns="http://www.w3.org/2000/svg" width="32" height="32" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
                    <path d="M9 18V5l12-2v13"></path>
                    <circle cx="6" cy="18" r="3"></circle>
                    <circle cx="18" cy="16" r="3"></circle>
                </svg>
                Vicente Sonorização
            </a>
            
            <button class="menu-button" aria-label="Menu">
                <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
                    <line x1="3" y1="12" x2="21" y2="12"></line>
                    <line x1="3" y1="6" x2="21" y2="6"></line>
                    <line x1="3" y1="18" x2="21" y2="18"></line>
                </svg>
            </button>

            <div class="nav-links">
                <a href="#home">Home</a>
                <a href="#about">Sobre</a>
                <a href="#services">Serviços</a>
                <a href="#portfolio">Portfólio</a>
                <a href="#contact">Contato</a>
            </div>
        </div>
    </nav>

    <!-- Hero Section -->
    <section id="home" class="hero">
        <div class="hero-content">
            <h1>Transformando eventos em experiências inesquecíveis</h1>
            <p>Soluções profissionais em sonorização e iluminação para seu evento</p>
            <a href="#services" class="btn btn-primary">Conheça Nossos Serviços</a>
        </div>
    </section>

    <!-- About Section -->
    <section id="about">
        <div class="container">
            <h2 class="section-title">Sobre Nós</h2>
            <div class="about-content">
                <p class="text-center mb-8 max-w-3xl mx-auto">
                    Desde 2010, a Vicente Sonorização é referência em qualidade e excelência
                    no mercado de sonorização e iluminação para eventos. Nossa equipe altamente
                    qualificada e equipamentos de última geração garantem resultados excepcionais
                    para cada projeto.
                </p>
                <div class="grid md:grid-cols-2 gap-8 mt-12">
                    <div class="about-card">
                        <h3>Missão</h3>
                        <p>Proporcionar experiências audiovisuais memoráveis através de soluções
                        técnicas inovadoras e atendimento personalizado.</p>
                    </div>
                    <div class="about-card">
                        <h3>Visão</h3>
                        <p>Ser reconhecida como a empresa líder em soluções audiovisuais no
                        Brasil, estabelecendo novos padrões de qualidade no setor.</p>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Services Section -->
    <section id="services" class="services">
        <div class="container">
            <h2 class="section-title">Nossos Serviços</h2>
            <div class="services-grid">
                <div class="service-card">
                    <svg class="service-icon" xmlns="http://www.w3.org/2000/svg" width="48" height="48" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
                        <path d="M3 18v-6a9 9 0 0 1 18 0v6"></path>
                        <path d="M21 19a2 2 0 0 1-2 2h-1a2 2 0 0 1-2-2v-3a2 2 0 0 1 2-2h3zM3 19a2 2 0 0 0 2 2h1a2 2 0 0 0 2-2v-3a2 2 0 0 0-2-2H3z"></path>
                    </svg>
                    <h3>Sonorização Profissional</h3>
                    <p>Equipamentos de última geração e técnicos especializados para garantir
                    a melhor qualidade sonora em seu evento.</p>
                </div>
                <!-- Add other service cards similarly -->
            </div>
        </div>
    </section>

    <!-- Portfolio Section -->
    <section id="portfolio">
        <div class="container">
            <h2 class="section-title">Nosso Portfólio</h2>
            <div class="portfolio-tabs">
                <button class="portfolio-tab active" data-tab="shows">Shows</button>
                <button class="portfolio-tab" data-tab="casamentos">Casamentos</button>
                <button class="portfolio-tab" data-tab="corporativo">Corporativo</button>
            </div>
            <div class="portfolio-grid" id="portfolio-grid"></div>
        </div>
    </section>

    <!-- Contact Section -->
    <section id="contact" class="contact">
        <div class="container">
            <h2 class="section-title">Fale Conosco</h2>
            <div class="contact-grid">
                <form class="contact-form">
                    <div class="form-group">
                        <label for="name">Nome</label>
                        <input type="text" id="name" class="form-control" required>
                    </div>
                    <div class="form-group">
                        <label for="email">Email</label>
                        <input type="email" id="email" class="form-control" required>
                    </div>
                    <div class="form-group">
                        <label for="phone">Telefone</label>
                        <input type="tel" id="phone" class="form-control" required>
                    </div>
                    <div class="form-group">
                        <label for="event-type">Tipo de Evento</label>
                        <select id="event-type" class="form-control" required>
                            <option value="">Selecione</option>
                            <option value="show">Show</option>
                            <option value="casamento">Casamento</option>
                            <option value="corporativo">Evento Corporativo</option>
                            <option value="outro">Outro</option>
                        </select>
                    </div>
                    <div class="form-group">
                        <label for="event-date">Data do Evento</label>
                        <input type="date" id="event-date" class="form-control" required>
                    </div>
                    <div class="form-group">
                        <label for="message">Mensagem</label>
                        <textarea id="message" rows="4" class="form-control" required></textarea>
                    </div>
                    <button type="submit" class="btn btn-primary w-full">Enviar Mensagem</button>
                </form>

                <div class="contact-info">
                    <div class="info-card">
                        <h3>Informações de Contato</h3>
                        <div class="info-list">
                            <div class="info-item">
                                <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
                                    <path d="M22 16.92v3a2 2 0 0 1-2.18 2 19.79 19.79 0 0 1-8.63-3.07 19.5 19.5 0 0 1-6-6 19.79 19.79 0 0 1-3.07-8.67A2 2 0 0 1 4.11 2h3a2 2 0 0 1 2 1.72 12.84 12.84 0 0 0 .7 2.81 2 2 0 0 1-.45 2.11L8.09 9.91a16 16 0 0 0 6 6l1.27-1.27a2 2 0 0 1 2.11-.45 12.84 12.84 0 0 0 2.81.7A2 2 0 0 1 22 16.92z"></path>
                                </svg>
                                <span>(11) 99999-9999</span>
                            </div>
                            <div class="info-item">
                                <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
                                    <path d="M4 4h16c1.1 0 2 .9 2 2v12c0 1.1-.9 2-2 2H4c-1.1 0-2-.9-2-2V6c0-1.1.9-2 2-2z"></path>
                                    <polyline points="22,6 12,13 2,6"></polyline>
                                </svg>
                                <span>contato@vicentesonorizacao.com</span>
                            </div>
                        </div>
                    </div>
                    <div class="info-card">
                        <h3>Horário de Atendimento</h3>
                        <p>Segunda a Sexta: 9h às 18h</p>
                        <p>Sábado: 9h às 13h</p>
                    </div>
                    <a href="https://wa.me/5511999999999" class="btn btn-primary" target="_blank">
                        <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="mr-2">
                            <path d="M21 11.5a8.38 8.38 0 0 1-.9 3.8 8.5 8.5 0 0 1-7.6 4.7 8.38 8.38 0 0 1-3.8-.9L3 21l1.9-5.7a8.38 8.38 0 0 1-.9-3.8 8.5 8.5 0 0 1 4.7-7.6 8.38 8.38 0 0 1 3.8-.9h.5a8.48 8.48 0 0 1 8 8v.5z"></path>
                        </svg>
                        Falar no WhatsApp
                    </a>
                </div>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer>
        <div class="container">
            <div class="footer-grid">
                <div class="footer-column">
                    <h4>Vicente Sonorização</h4>
                    <p>Transformando eventos em experiências inesquecíveis desde 2010.</p>
                </div>
                <div class="footer-column">
                    <h4>Links Rápidos</h4>
                    <ul class="footer-links">
                        <li><a href="#home">Home</a></li>
                        <li><a href="#about">Sobre</a></li>
                        <li><a href="#services">Serviços</a></li>
                        <li><a href="#portfolio">Portfólio</a></li>
                        <li><a href="#contact">Contato</a></li>
                    </ul>
                </div>
                <div class="footer-column">
                    <h4>Redes Sociais</h4>
                    <div class="social-links">
                        <a href="#" target="_blank" aria-label="Instagram">
                            <svg xmlns="http://www.w3.org/2000/svg" width="20" height="20" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
                                <rect x="2" y="2" width="20" height="20" rx="5" ry="5"></rect>
                                <path d="M16 11.37A4 4 0 1 1 12.63 8 4 4 0 0 1 16 11.37z"></path>
                                <line x1="17.5" y1="6.5" x2="17.51" y2="6.5"></line>
                            </svg>
                        </a>
                        <a href="#" target="_blank" aria-label="Facebook">
                            <svg xmlns="http://www.w3.org/2000/svg" width="20" height="20" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
                                <path d="M18 2h-3a5 5 0 0 0-5 5v3H7v4h3v8h4v-8h3l1-4h-4V7a1 1 0 0 1 1-1h3z"></path>
                            </svg>
                        </a>
                        <a href="#" target="_blank" aria-label="YouTube">
                            <svg xmlns="http://www.w3.org/2000/svg" width="20" height="20" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
                                <path d="M22.54 6.42a2.78 2.78 0 0 0-1.94-2C18.88 4 12 4 12 4s-6.88 0-8.6.46a2.78 2.78 0 0 0-1.94 2A29 29 0 0 0 1 11.75a29 29 0 0 0 .46 5.33A2.78 2.78 0 0 0 3.4 19c1.72.46 8.6.46 8.6.46s6.88 0 8.6-.46a2.78 2.78 0 0 0 1.94-2 29 29 0 0 0 .46-5.25 29 29 0 0 0-.46-5.33z"></path>
                                <polygon points="9.75 15.02 15.5 11.75 9.75 8.48 9.75 15.02"></polygon>
                            </svg>
                        </a>
                    </div>
                </div>
            </div>
            <div class="copyright">
                <p> <p>© 2025 Vicente Sonorização - Todos os direitos reservados</p>
            </div>
        </div>
    </footer>

    <script>
        // Navbar scroll effect
        const navbar = document.querySelector('.navbar');
        window.addEventListener('scroll', () => {
            if (window.scrollY > 50) {
                navbar.classList.add('scrolled');
            } else {
                navbar.classList.remove('scrolled');
            }
        });

        // Mobile menu toggle
        const menuButton = document.querySelector('.menu-button');
        const navLinks = document.querySelector('.nav-links');

        menuButton.addEventListener('click', () => {
            menuButton.classList.toggle('active');
            navLinks.classList.toggle('active');
        });

        // Close mobile menu when clicking outside
        document.addEventListener('click', (e) => {
            if (!menuButton.contains(e.target) && !navLinks.contains(e.target)) {
                menuButton.classList.remove('active');
                navLinks.classList.remove('active');
            }
        });

        // Portfolio tabs and gallery
        const portfolioData = {
            shows: [
                'https://images.unsplash.com/photo-1470229722913-7c0e2dbbafd3',
                'https://images.unsplash.com/photo-1501386761578-eac5c94b800a',
                'https://images.unsplash.com/photo-1533174072545-7a4b6ad7a6c3'
            ],
            casamentos: [
                'https://images.unsplash.com/photo-1519741497674-611481863552',
                'https://images.unsplash.com/photo-1511795409834-ef04bbd61622',
                'https://images.unsplash.com/photo-1465495976277-4387d4b0b4c6'
            ],
            corporativo: [
                'https://images.unsplash.com/photo-1505373877841-8d25f7d46678',
                'https://images.unsplash.com/photo-1515187029135-18ee286d815b',
                'https://images.unsplash.com/photo-1528605248644-14dd04022da1'
            ]
        };

        const portfolioGrid = document.getElementById('portfolio-grid');
        const portfolioTabs = document.querySelectorAll('.portfolio-tab');

        function updatePortfolio(category) {
            portfolioGrid.style.opacity = '0';
            portfolioGrid.style.transform = 'translateY(20px)';
            
            setTimeout(() => {
                portfolioGrid.innerHTML = '';
                portfolioData[category].forEach(url => {
                    const item = document.createElement('div');
                    item.className = 'portfolio-item';
                    item.innerHTML = `
                        <img src="${url}?ixlib=rb-1.2.1&auto=format&fit=crop&w=600&q=80" alt="Portfolio item">
                    `;
                    portfolioGrid.appendChild(item);
                });
                
                portfolioGrid.style.opacity = '1';
                portfolioGrid.style.transform = 'translateY(0)';
            }, 300);
        }

        portfolioTabs.forEach(tab => {
            tab.addEventListener('click', () => {
                portfolioTabs.forEach(t => t.classList.remove('active'));
                tab.classList.add('active');
                updatePortfolio(tab.dataset.tab);
            });
        });

        // Initialize portfolio with shows
        updatePortfolio('shows');

        // Smooth scrolling for navigation links
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();
                const target = document.querySelector(this.getAttribute('href'));
                if (target) {
                    const headerOffset = 80;
                    const elementPosition = target.getBoundingClientRect().top;
                    const offsetPosition = elementPosition + window.pageYOffset - headerOffset;

                    window.scrollTo({
                        top: offsetPosition,
                        behavior: 'smooth'
                    });
                    
                    // Close mobile menu after clicking
                    menuButton.classList.remove('active');
                    navLinks.classList.remove('active');
                }
            });
        });

        // Form submission with validation
        const contactForm = document.querySelector('.contact-form');
        contactForm.addEventListener('submit', (e) => {
            e.preventDefault();
            
            // Basic form validation
            const formData = new FormData(contactForm);
            let isValid = true;
            let errorMessage = '';

            for (let [key, value] of formData.entries()) {
                if (!value) {
                    isValid = false;
                    errorMessage = 'Por favor, preencha todos os campos.';
                    break;
                }
            }

            if (isValid) {
                // Here you would typically send the form data to a server
                alert('Mensagem enviada com sucesso! Entraremos em contato em breve.');
                contactForm.reset();
            } else {
                alert(errorMessage);
            }
        });

        // Intersection Observer for animations
        const observerOptions = {
            threshold: 0.1,
            rootMargin: '0px 0px -50px 0px'
        };

        const observer = new IntersectionObserver((entries) => {
            entries.forEach(entry => {
                if (entry.isIntersecting) {
                    entry.target.style.opacity = '1';
                    entry.target.style.transform = 'translateY(0)';
                    observer.unobserve(entry.target);
                }
            });
        }, observerOptions);

        // Observe all sections for animation
        document.querySelectorAll('section:not(.hero)').forEach(section => {
            section.style.opacity = '0';
            section.style.transform = 'translateY(20px)';
            observer.observe(section);
        });
    </script>
</body>
</html>
