<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Chico Ferreira Fotografia | Eventos, Casamentos e Empresarial</title>
    <link href="https://cdn.jsdelivr.net/npm/tailwindcss@2.2.19/dist/tailwind.min.css" rel="stylesheet">
    <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/@fancyapps/ui@4.0/dist/fancybox.css">
    <link href="https://cdn.jsdelivr.net/npm/swiper@8/swiper-bundle.min.css" rel="stylesheet">
    <link href="https://cdn.jsdelivr.net/npm/boxicons@2.1.4/css/boxicons.min.css" rel="stylesheet">
    <style>
        :root {
            --primary-color: #e5d0c3;
            --secondary-color: #d0e5e3;
            --accent-color: #c3d0e5;
            --text-color: #4a4a4a;
            --light-bg: #f9f7f5;
        }
        body {
            font-family: 'Montserrat', sans-serif;
            color: var(--text-color);
            background-color: var(--light-bg);
        }
        .section-title {
            position: relative;
            display: inline-block;
            margin-bottom: 2rem;
        }
        .section-title::after {
            content: "";
            position: absolute;
            bottom: -10px;
            left: 0;
            width: 60px;
            height: 3px;
            background-color: var(--primary-color);
        }
        .header-nav {
            background-color: rgba(255, 255, 255, 0.9);
            transition: all 0.3s ease;
        }
        .header-nav.scrolled {
            box-shadow: 0 4px 6px -1px rgba(0, 0, 0, 0.1);
        }
        .swiper-pagination-bullet-active {
            background-color: var(--primary-color) !important;
        }
        .category-tab.active {
            background-color: var(--primary-color);
            color: white;
        }
        .gallery-item {
            transition: all 0.3s ease;
        }
        .gallery-item:hover {
            transform: scale(1.03);
        }
        .testimonial-card {
            background-color: white;
            border-radius: 8px;
            box-shadow: 0 4px 6px rgba(0, 0, 0, 0.05);
            transition: all 0.3s ease;
        }
        .testimonial-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 15px rgba(0, 0, 0, 0.1);
        }
        .instagram-post {
            transition: all 0.3s ease;
        }
        .instagram-post:hover {
            transform: scale(1.05);
        }
        .blog-card {
            transition: all 0.3s ease;
            background-color: white;
            border-radius: 8px;
            overflow: hidden;
            box-shadow: 0 4px 6px rgba(0, 0, 0, 0.05);
        }
        .blog-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 15px rgba(0, 0, 0, 0.1);
        }
        .contact-form input,
        .contact-form textarea,
        .contact-form select {
            background-color: white;
            border: 1px solid #e2e8f0;
            border-radius: 4px;
            padding: 0.75rem;
            transition: all 0.3s ease;
        }
        .contact-form input:focus,
        .contact-form textarea:focus,
        .contact-form select:focus {
            border-color: var(--primary-color);
            outline: none;
            box-shadow: 0 0 0 3px rgba(229, 208, 195, 0.3);
        }
        .btn-primary {
            background-color: var(--primary-color);
            color: white;
            transition: all 0.3s ease;
        }
        .btn-primary:hover {
            background-color: #d8c0b3;
            transform: translateY(-2px);
        }
        .swiper-container {
            height: 100vh;
        }
        @media (max-width: 768px) {
            .swiper-container {
                height: 60vh;
            }
        }
        /* Mobile menu */
        .mobile-menu {
            display: none;
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background-color: white;
            z-index: 50;
            padding: 2rem;
        }
        .mobile-menu.active {
            display: block;
        }
    </style>
</head>
<body>
    <!-- Header & Navigation -->
    <header class="header-nav fixed w-full z-50 py-4">
        <div class="container mx-auto px-4 flex justify-between items-center">
            <div class="text-2xl font-bold">Chico Ferreira</div>
            <nav class="hidden md:block">
                <ul class="flex space-x-6">
                    <li><a href="#inicio" class="hover:text-opacity-70">Início</a></li>
                    <li><a href="#galeria" class="hover:text-opacity-70">Galeria</a></li>
                    <li><a href="#sobre" class="hover:text-opacity-70">Conheça-me</a></li>
                    <li><a href="#depoimentos" class="hover:text-opacity-70">Depoimentos</a></li>
                    <li><a href="#blog" class="hover:text-opacity-70">Blog</a></li>
                    <li><a href="#contato" class="hover:text-opacity-70">Contato</a></li>
                </ul>
            </nav>
            <button class="md:hidden" id="menuBtn">
                <i class='bx bx-menu text-2xl'></i>
            </button>
        </div>
    </header>

    <!-- Mobile Menu -->
    <div class="mobile-menu" id="mobileMenu">
        <div class="flex justify-end">
            <button id="closeMenuBtn">
                <i class='bx bx-x text-3xl'></i>
            </button>
        </div>
        <ul class="flex flex-col space-y-6 mt-8 text-xl">
            <li><a href="#inicio" class="block py-2">Início</a></li>
            <li><a href="#galeria" class="block py-2">Galeria</a></li>
            <li><a href="#sobre" class="block py-2">Conheça-me</a></li>
            <li><a href="#depoimentos" class="block py-2">Depoimentos</a></li>
            <li><a href="#blog" class="block py-2">Blog</a></li>
            <li><a href="#contato" class="block py-2">Contato</a></li>
        </ul>
    </div>

    <!-- Hero Section with Slider -->
    <section id="inicio" class="relative h-screen">
        <div class="swiper-container">
            <div class="swiper-wrapper">
                <div class="swiper-slide">
                    <div class="bg-cover bg-center h-full" style="background-image: url('https://images.unsplash.com/photo-1519741497674-611481863552?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80');">
                        <div class="bg-black bg-opacity-40 h-full flex items-center">
                            <div class="container mx-auto px-4 text-white">
                                <h1 class="text-4xl md:text-6xl font-bold mb-4">Fotografia de Eventos</h1>
                                <p class="text-xl md:text-2xl mb-8 max-w-2xl">Capturando momentos especiais para recordações eternas</p>
                                <a href="#contato" class="bg-white text-gray-800 px-8 py-3 rounded-lg font-medium hover:bg-opacity-90 transition-all">Solicitar Orçamento</a>
                            </div>
                        </div>
                    </div>
                </div>
                <div class="swiper-slide">
                    <div class="bg-cover bg-center h-full" style="background-image: url('https://images.unsplash.com/photo-1511285560929-80b456fea0bc?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80');">
                        <div class="bg-black bg-opacity-40 h-full flex items-center">
                            <div class="container mx-auto px-4 text-white">
                                <h1 class="text-4xl md:text-6xl font-bold mb-4">Casamentos Inesquecíveis</h1>
                                <p class="text-xl md:text-2xl mb-8 max-w-2xl">A arte de preservar o amor em cada detalhe</p>
                                <a href="#contato" class="bg-white text-gray-800 px-8 py-3 rounded-lg font-medium hover:bg-opacity-90 transition-all">Solicitar Orçamento</a>
                            </div>
                        </div>
                    </div>
                </div>
                <div class="swiper-slide">
                    <div class="bg-cover bg-center h-full" style="background-image: url('https://images.unsplash.com/photo-1551818255-e6e10975bc17?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80');">
                        <div class="bg-black bg-opacity-40 h-full flex items-center">
                            <div class="container mx-auto px-4 text-white">
                                <h1 class="text-4xl md:text-6xl font-bold mb-4">Fotografia Empresarial</h1>
                                <p class="text-xl md:text-2xl mb-8 max-w-2xl">Elevando a imagem de sua empresa com profissionalismo</p>
                                <a href="#contato" class="bg-white text-gray-800 px-8 py-3 rounded-lg font-medium hover:bg-opacity-90 transition-all">Solicitar Orçamento</a>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
            <div class="swiper-pagination"></div>
        </div>
    </section>

    <!-- Gallery Section -->
    <section id="galeria" class="py-20 bg-white">
        <div class="container mx-auto px-4">
            <h2 class="text-3xl font-bold section-title">Galeria de Trabalhos</h2>
            
            <!-- Category Tabs -->
            <div class="flex flex-wrap justify-center gap-2 mb-8">
                <button class="category-tab active px-4 py-2 rounded-full text-sm font-medium" data-category="all">Todos</button>
                <button class="category-tab px-4 py-2 rounded-full text-sm font-medium" data-category="casamentos">Casamentos</button>
                <button class="category-tab px-4 py-2 rounded-full text-sm font-medium" data-category="aniversarios">Aniversários</button>
                <button class="category-tab px-4 py-2 rounded-full text-sm font-medium" data-category="eventos">Eventos</button>
                <button class="category-tab px-4 py-2 rounded-full text-sm font-medium" data-category="empresarial">Empresarial</button>
            </div>
            
            <!-- Gallery Grid -->
            <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-4">
                <!-- Casamentos -->
                <a href="https://images.unsplash.com/photo-1537633552985-df8429e8048b?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80" data-fancybox="gallery" data-category="casamentos" class="gallery-item block overflow-hidden rounded-lg">
                    <img src="https://images.unsplash.com/photo-1537633552985-df8429e8048b?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80" alt="Casamento" class="w-full h-64 object-cover transition-all duration-300 hover:scale-110">
                </a>
                <a href="https://images.unsplash.com/photo-1519225421980-715cb0215aed?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80" data-fancybox="gallery" data-category="casamentos" class="gallery-item block overflow-hidden rounded-lg">
                    <img src="https://images.unsplash.com/photo-1519225421980-715cb0215aed?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80" alt="Casamento" class="w-full h-64 object-cover transition-all duration-300 hover:scale-110">
                </a>
                
                <!-- Aniversários -->
                <a href="https://images.unsplash.com/photo-1530103862676-de8c9debad1d?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80" data-fancybox="gallery" data-category="aniversarios" class="gallery-item block overflow-hidden rounded-lg">
                    <img src="https://images.unsplash.com/photo-1530103862676-de8c9debad1d?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80" alt="Aniversário" class="w-full h-64 object-cover transition-all duration-300 hover:scale-110">
                </a>
                <a href="https://images.unsplash.com/photo-1464349153735-7db50ed83c84?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80" data-fancybox="gallery" data-category="aniversarios" class="gallery-item block overflow-hidden rounded-lg">
                    <img src="https://images.unsplash.com/photo-1464349153735-7db50ed83c84?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80" alt="Aniversário" class="w-full h-64 object-cover transition-all duration-300 hover:scale-110">
                </a>
                
                <!-- Eventos -->
                <a href="https://images.unsplash.com/photo-1511578314322-379afb476865?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80" data-fancybox="gallery" data-category="eventos" class="gallery-item block overflow-hidden rounded-lg">
                    <img src="https://images.unsplash.com/photo-1511578314322-379afb476865?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80" alt="Evento" class="w-full h-64 object-cover transition-all duration-300 hover:scale-110">
                </a>
                <a href="https://images.unsplash.com/photo-1540575467063-178a50c2df87?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80" data-fancybox="gallery" data-category="eventos" class="gallery-item block overflow-hidden rounded-lg">
                    <img src="https://images.unsplash.com/photo-1540575467063-178a50c2df87?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80" alt="Evento" class="w-full h-64 object-cover transition-all duration-300 hover:scale-110">
                </a>
                
                <!-- Empresarial -->
                <a href="https://images.unsplash.com/photo-1600880292203-757bb62b4baf?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80" data-fancybox="gallery" data-category="empresarial" class="gallery-item block overflow-hidden rounded-lg">
                    <img src="https://images.unsplash.com/photo-1600880292203-757bb62b4baf?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80" alt="Empresarial" class="w-full h-64 object-cover transition-all duration-300 hover:scale-110">
                </a>
                <a href="https://images.unsplash.com/photo-1542744173-8e7e53415bb0?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80" data-fancybox="gallery" data-category="empresarial" class="gallery-item block overflow-hidden rounded-lg">
                    <img src="https://images.unsplash.com/photo-1542744173-8e7e53415bb0?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80" alt="Empresarial" class="w-full h-64 object-cover transition-all duration-300 hover:scale-110">
                </a>
            </div>
        </div>
    </section>

    <!-- About Section -->
    <section id="sobre" class="py-20 bg-gray-50">
        <div class="container mx-auto px-4">
            <div class="flex flex-col md:flex-row items-center gap-10">
                <div class="md:w-1/2">
                    <img src="https://images.unsplash.com/photo-1521747116042-5a810fda9664?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80" alt="Chico Ferreira" class="rounded-lg shadow-lg">
                </div>
                <div class="md:w-1/2">
                    <h2 class="text-3xl font-bold section-title">Conheça-me</h2>
                    <p class="mb-4 text-lg">Olá! Sou Chico Ferreira, fotógrafo profissional especializado em capturar momentos especiais há mais de 8 anos.</p>
                    <p class="mb-4">Minha paixão pela fotografia começou cedo, quando ganhei minha primeira câmera. Desde então, venho aprimorando minha técnica e sensibilidade para contar histórias através de imagens.</p>
                    <p class="mb-6">Especializo-me em fotografias de eventos, casamentos, aniversários e fotografia empresarial. Cada sessão é única e personalizada, pois acredito que cada momento merece ser eternizado com sua própria narrativa visual.</p>
                    <div class="flex flex-col sm:flex-row gap-4">
                        <div class="text-center bg-white p-4 rounded-lg shadow-sm">
                            <span class="text-3xl font-bold text-gray-800">250+</span>
                            <p class="text-gray-600">Eventos</p>
                        </div>
                        <div class="text-center bg-white p-4 rounded-lg shadow-sm">
                            <span class="text-3xl font-bold text-gray-800">120+</span>
                            <p class="text-gray-600">Casamentos</p>
                        </div>
                        <div class="text-center bg-white p-4 rounded-lg shadow-sm">
                            <span class="text-3xl font-bold text-gray-800">4.9/5</span>
                            <p class="text-gray-600">Avaliação</p>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Testimonials Section -->
    <section id="depoimentos" class="py-20 bg-white">
        <div class="container mx-auto px-4">
            <h2 class="text-3xl font-bold section-title text-center">O que meus clientes dizem</h2>
            <div class="testimonial-slider mt-10">
                <div class="swiper-container testimonial-swiper">
                    <div class="swiper-wrapper">
                        <div class="swiper-slide p-4">
                            <div class="testimonial-card p-6">
                                <div class="flex items-center mb-4">
                                    <div class="mr-4">
                                        <div class="w-12 h-12 bg-gray-200 rounded-full overflow-hidden">
                                            <img src="https://randomuser.me/api/portraits/women/32.jpg" alt="Cliente" class="w-full h-full object-cover">
                                        </div>
                                    </div>
                                    <div>
                                        <h4 class="font-bold">Marina Silva</h4>
                                        <p class="text-sm text-gray-600">Casamento, Julho 2023</p>
                                    </div>
                                </div>
                                <p class="text-gray-700">"O Chico é incrível! Ele capturou nosso casamento de uma forma tão natural e emocionante. As fotos ficaram perfeitas e retratam exatamente a essência daquele dia especial. Super recomendo!"</p>
                                <div class="mt-4 flex text-yellow-400">
                                    <i class='bx bxs-star'></i>
                                    <i class='bx bxs-star'></i>
                                    <i class='bx bxs-star'></i>
                                    <i class='bx bxs-star'></i>
                                    <i class='bx bxs-star'></i>
                                </div>
                            </div>
                        </div>
                        <div class="swiper-slide p-4">
                            <div class="testimonial-card p-6">
                                <div class="flex items-center mb-4">
                                    <div class="mr-4">
                                        <div class="w-12 h-12 bg-gray-200 rounded-full overflow-hidden">
                                            <img src="https://randomuser.me/api/portraits/men/45.jpg" alt="Cliente" class="w-full h-full object-cover">
                                        </div>
                                    </div>
                                    <div>
                                        <h4 class="font-bold">Carlos Mendes</h4>
                                        <p class="text-sm text-gray-600">Aniversário Corporativo, Março 2023</p>
                                    </div>
                                </div>
                                <p class="text-gray-700">"Contratamos o Chico para o aniversário da empresa e ele superou todas as expectativas. Profissional, pontual e muito talentoso. As fotos captaram todos os momentos importantes da celebração. Já estamos planejando contratá-lo novamente!"</p>
                                <div class="mt-4 flex text-yellow-400">
                                    <i class='bx bxs-star'></i>
                                    <i class='bx bxs-star'></i>
                                    <i class='bx bxs-star'></i>
                                    <i class='bx bxs-star'></i>
                                    <i class='bx bxs-star-half'></i>
                                </div>
                            </div>
                        </div>
                        <div class="swiper-slide p-4">
                            <div class="testimonial-card p-6">
                                <div class="flex items-center mb-4">
                                    <div class="mr-4">
                                        <div class="w-12 h-12 bg-gray-200 rounded-full overflow-hidden">
                                            <img src="https://randomuser.me/api/portraits/women/68.jpg" alt="Cliente" class="w-full h-full object-cover">
                                        </div>
                                    </div>
                                    <div>
                                        <h4 class="font-bold">Paula Rodrigues</h4>
                                        <p class="text-sm text-gray-600">15 Anos da Filha, Outubro 2022</p>
                                    </div>
                                </div>
                                <p class="text-gray-700">"As fotos da festa de 15 anos da minha filha ficaram sensacionais! O Chico tem um olhar especial para capturar momentos de emoção. Muito atencioso com todos os convidados. Estamos apaixonados pelo resultado!"</p>
                                <div class="mt-4 flex text-yellow-400">
                                    <i class='bx bxs-star'></i>
                                    <i class='bx bxs-star'></i>
                                    <i class='bx bxs-star'></i>
                                    <i class='bx bxs-star'></i>
                                    <i class='bx bxs-star'></i>
                                </div>
                            </div>
                        </div>
                    </div>
                    <div class="swiper-pagination testimonial-pagination mt-6"></div>
                </div>
            </div>
        </div>
    </section>

    <!-- Instagram Section -->
    <section class="py-20 bg-gray-50">
        <div class="container mx-auto px-4">
            <h2 class="text-3xl font-bold section-title text-center">Instagram</h2>
            <p class="text-center mb-10">Siga-me no Instagram para ver mais trabalhos <a href="https://instagram.com" target="_blank" class="text-blue-500 hover:underline">@chicoferreirafotografia</a></p>
            
            <div class="grid grid-cols-2 md:grid-cols-4 gap-4">
                <a href="#" class="instagram-post block overflow-hidden rounded-lg">
                    <img src="https://images.unsplash.com/photo-1519741497674-611481863552?ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=60" alt="Instagram post" class="w-full h-64 object-cover transition-all duration-300 hover:scale-110">
                </a>
                <a href="#" class="instagram-post block overflow-hidden rounded-lg">
                    <img src="https://images.unsplash.com/photo-1511285560929-80b456fea0bc?ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=60" alt="Instagram post" class="w-full h-64 object-cover transition-all duration-300 hover:scale-110">
                </a>
                <a href="#" class="instagram-post block overflow-hidden rounded-lg">
                    <img src="https://images.unsplash.com/photo-1519225421980-715cb0215aed?ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=60" alt="Instagram post" class="w-full h-64 object-cover transition-all duration-300 hover:scale-110">
                </a>
                <a href="#" class="instagram-post block overflow-hidden rounded-lg">
                    <img src="https://images.unsplash.com/photo-1530103862676-de8c9debad1d?ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=60" alt="Instagram post" class="w-full h-64 object-cover transition-all duration-300 hover:scale-110">
                </a>
            </div>
        </div>
    </section>

    <!-- Blog Section -->
    <section id="blog" class="py-20 bg-white">
        <div class="container mx-auto px-4">
            <h2 class="text-3xl font-bold section-title">Blog</h2>
            
            <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8 mt-10">
                <div class="blog-card">
                    <div class="overflow-hidden h-48">
                        <img src="https://images.unsplash.com/photo-1496318447583-f524534e9ce1?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80" alt="Blog post" class="w-full h-full object-cover transition-all duration-300 hover:scale-110">
                    </div>
                    <div class="p-6">
                        <p class="text-sm text-gray-500 mb-2">12 de Maio, 2023</p>
                        <h3 class="text-xl font-bold mb-2">Como escolher o fotógrafo ideal para seu casamento</h3>
                        <p class="text-gray-700 mb-4">Dicas importantes para ajudar casais a escolherem o profissional que vai eternizar o grande dia...</p>
                        <a href="#" class="text-sm font-medium hover:underline">Continuar lendo →</a>
                    </div>
                </div>
                
                <div class="blog-card">
                    <div class="overflow-hidden h-48">
                        <img src="https://images.unsplash.com/photo-1554048612-b6a482bc67e5?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80" alt="Blog post" class="w-full h-full object-cover transition-all duration-300 hover:scale-110">
                    </div>
                    <div class="p-6">
                        <p class="text-sm text-gray-500 mb-2">28 de Abril, 2023</p>
                        <h3 class="text-xl font-bold mb-2">A importância da fotografia corporativa para sua empresa</h3>
                        <p class="text-gray-700 mb-4">Como uma boa fotografia profissional pode elevar a imagem da sua empresa e transmitir credibilidade...</p>
                        <a href="#" class="text-sm font-medium hover:underline">Continuar lendo →</a>
                    </div>
                </div>
                
                <div class="blog-card">
                    <div class="overflow-hidden h-48">
                        <img src="https://images.unsplash.com/photo-1603380608623-7f0e1e5c8f6f?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80" alt="Blog post" class="w-full h-full object-cover transition-all duration-300 hover:scale-110">
                    </div>
                    <div class="p-6">
                        <p class="text-sm text-gray-500 mb-2">5 de Abril, 2023</p>
                        <h3 class="text-xl font-bold mb-2">Tendências de fotografia para aniversários em 2023</h3>
                        <p class="text-gray-700 mb-4">Conheça as tendências que estão fazendo sucesso nas festas de aniversário neste ano...</p>
                        <a href="#" class="text-sm font-medium hover:underline">Continuar lendo →</a>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Contact Section -->
    <section id="contato" class="py-20 bg-gray-50">
        <div class="container mx-auto px-4">
            <div class="flex flex-col md:flex-row gap-10">
                <div class="md:w-1/2">
                    <h2 class="text-3xl font-bold section-title">Contato</h2>
                    <p class="mb-6">Entre em contato para agendar uma consulta ou solicitar um orçamento.</p>
                    
                    <div class="flex items-center mb-4">
                        <div class="w-10 h-10 rounded-full bg-primary-color flex items-center justify-center mr-4">
                            <i class='bx bx-envelope text-white'></i>
                        </div>
                        <div>
                            <p class="text-sm text-gray-600">Email</p>
                            <p class="font-medium">contato@chicoferreira.com</p>
                        </div>
                    </div>
                    
                    <div class="flex items-center mb-4">
                        <div class="w-10 h-10 rounded-full bg-primary-color flex items-center justify-center mr-4">
                            <i class='bx bx-phone text-white'></i>
                        </div>
                        <div>
                            <p class="text-sm text-gray-600">Telefone</p>
                            <p class="font-medium">(11) 98765-4321</p>
                        </div>
                    </div>
                    
                    <div class="flex items-center mb-6">
                        <div class="w-10 h-10 rounded-full bg-primary-color flex items-center justify-center mr-4">
                            <i class='bx bx-map text-white'></i>
                        </div>
                        <div>
                            <p class="text-sm text-gray-600">Localização</p>
                            <p class="font-medium">São Paulo, SP - Brasil</p>
                        </div>
                    </div>
                    
                    <div class="flex gap-4">
                        <a href="#" class="w-10 h-10 rounded-full bg-gray-800 flex items-center justify-center text-white hover:bg-gray-700 transition-colors">
                            <i class='bx bxl-instagram'></i>
                        </a>
                        <a href="#" class="w-10 h-10 rounded-full bg-gray-800 flex items-center justify-center text-white hover:bg-gray-700 transition-colors">
                            <i class='bx bxl-facebook'></i>
                        </a>
                        <a href="#" class="w-10 h-10 rounded-full bg-gray-800 flex items-center justify-center text-white hover:bg-gray-700 transition-colors">
                            <i class='bx bxl-whatsapp'></i>
                        </a>
                    </div>
                </div>
                
                <div class="md:w-1/2">
                    <form class="contact-form bg-white p-6 rounded-lg shadow-sm">
                        <div class="grid grid-cols-1 md:grid-cols-2 gap-4 mb-4">
                            <div>
                                <label for="name" class="block text-sm font-medium text-gray-700 mb-1">Nome</label>
                                <input type="text" id="name" name="name" class="w-full" required>
                            </div>
                            <div>
                                <label for="email" class="block text-sm font-medium text-gray-700 mb-1">Email</label>
                                <input type="email" id="email" name="email" class="w-full" required>
                            </div>
                        </div>
                        
                        <div class="mb-4">
                            <label for="phone" class="block text-sm font-medium text-gray-700 mb-1">Telefone</label>
                            <input type="tel" id="phone" name="phone" class="w-full">
                        </div>
                        
                        <div class="mb-4">
                            <label for="service" class="block text-sm font-medium text-gray-700 mb-1">Serviço de Interesse</label>
                            <select id="service" name="service" class="w-full">
                                <option value="">Selecione um serviço</option>
                                <option value="casamento">Fotografia de Casamento</option>
                                <option value="aniversario">Fotografia de Aniversário</option>
                                <option value="evento">Fotografia de Eventos</option>
                                <option value="empresarial">Fotografia Empresarial</option>
                                <option value="outro">Outro</option>
                            </select>
                        </div>
                        
                        <div class="mb-4">
                            <label for="date" class="block text-sm font-medium text-gray-700 mb-1">Data do Evento (se aplicável)</label>
                            <input type="date" id="date" name="date" class="w-full">
                        </div>
                        
                        <div class="mb-4">
                            <label for="message" class="block text-sm font-medium text-gray-700 mb-1">Mensagem</label>
                            <textarea id="message" name="message" rows="4" class="w-full" required></textarea>
                        </div>
                        
                        <div class="mb-4">
                            <label class="flex items-center">
                                <input type="checkbox" class="mr-2">
                                <span class="text-sm text-gray-700">Concordo em receber atualizações e promoções por email</span>
                            </label>
                        </div>
                        
                        <button type="submit" class="w-full py-3 px-4 bg-primary-color text-white rounded-lg font-medium hover:bg-opacity-90 transition-colors">Enviar Mensagem</button>
                    </form>
                </div>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer class="bg-gray-900 text-white py-10">
        <div class="container mx-auto px-4">
            <div class="flex flex-col md:flex-row justify-between items-center">
                <div class="mb-6 md:mb-0">
                    <h3 class="text-2xl font-bold mb-2">Chico Ferreira</h3>
                    <p class="text-gray-400">Fotografia profissional para seus momentos especiais</p>
                </div>
                
                <div class="flex flex-col md:flex-row gap-8">
                    <div>
                        <h4 class="text-lg font-semibold mb-3">Links Rápidos</h4>
                        <ul class="space-y-2">
                            <li><a href="#inicio" class="text-gray-400 hover:text-white transition-colors">Início</a></li>
                            <li><a href="#galeria" class="text-gray-400 hover:text-white transition-colors">Galeria</a></li>
                            <li><a href="#sobre" class="text-gray-400 hover:text-white transition-colors">Conheça-me</a></li>
                            <li><a href="#depoimentos" class="text-gray-400 hover:text-white transition-colors">Depoimentos</a></li>
                        </ul>
                    </div>
                    
                    <div>
                        <h4 class="text-lg font-semibold mb-3">Serviços</h4>
                        <ul class="space-y-2">
                            <li><a href="#" class="text-gray-400 hover:text-white transition-colors">Casamentos</a></li>
                            <li><a href="#" class="text-gray-400 hover:text-white transition-colors">Aniversários</a></li>
                            <li><a href="#" class="text-gray-400 hover:text-white transition-colors">Eventos</a></li>
                            <li><a href="#" class="text-gray-400 hover:text-white transition-colors">Fotografia Empresarial</a></li>
                        </ul>
                    </div>
                </div>
            </div>
            
            <div class="mt-8 pt-8 border-t border-gray-800 text-center text-gray-500">
                <p>&copy; 2023 Chico Ferreira Fotografia. Todos os direitos reservados.</p>
            </div>
        </div>
    </footer>

    <!-- Scripts -->
    <script src="https://cdn.jsdelivr.net/npm/swiper@8/swiper-bundle.min.js"></script>
    <script src="https://cdn.jsdelivr.net/npm/@fancyapps/ui@4.0/dist/fancybox.umd.js"></script>
    <script>
        // Initialize Swiper
        const heroSwiper = new Swiper('.swiper-container', {
            loop: true,
            autoplay: {
                delay: 5000,
                disableOnInteraction: false,
            },
            pagination: {
                el: '.swiper-pagination',
                clickable: true,
            },
        });
        
        const testimonialSwiper = new Swiper('.testimonial-swiper', {
            slidesPerView: 1,
            spaceBetween: 30,
            pagination: {
                el: '.testimonial-pagination',
                clickable: true,
            },
            breakpoints: {
                640: {
                    slidesPerView: 1,
                },
                768: {
                    slidesPerView: 2,
                },
                1024: {
                    slidesPerView: 3,
                },
            },
        });
        
        // Header scroll effect
        window.addEventListener('scroll', function() {
            const header = document.querySelector('.header-nav');
            if (window.scrollY > 50) {
                header.classList.add('scrolled');
            } else {
                header.classList.remove('scrolled');
            }
        });
        
        // Gallery category filter
        const categoryTabs = document.querySelectorAll('.category-tab');
        const galleryItems = document.querySelectorAll('.gallery-item');
        
        categoryTabs.forEach(tab => {
            tab.addEventListener('click', () => {
                // Remove active class from all tabs
                categoryTabs.forEach(t => t.classList.remove('active'));
                
                // Add active class to clicked tab
                tab.classList.add('active');
                
                const category = tab.getAttribute('data-category');
                
                // Show/hide gallery items based on category
                galleryItems.forEach(item => {
                    if (category === 'all' || item.getAttribute('data-category') === category) {
                        item.style.display = 'block';
                    } else {
                        item.style.display = 'none';
                    }
                });
            });
        });
        
        // Initialize FancyBox
        Fancybox.bind("[data-fancybox]", {
            // Options here
        });
        
        // Mobile menu
        const menuBtn = document.getElementById('menuBtn');
        const closeMenuBtn = document.getElementById('closeMenuBtn');
        const mobileMenu = document.getElementById('mobileMenu');
        const mobileMenuLinks = mobileMenu.querySelectorAll('a');
        
        menuBtn.addEventListener('click', () => {
            mobileMenu.classList.add('active');
        });
        
        closeMenuBtn.addEventListener('click', () => {
            mobileMenu.classList.remove('active');
        });
        
        mobileMenuLinks.forEach(link => {
            link.addEventListener('click', () => {
                mobileMenu.classList.remove('active');
            });
        });
        
        // Contact form
        const contactForm = document.querySelector('.contact-form');
        
        contactForm.addEventListener('submit', (e) => {
            e.preventDefault();
            // Here you would normally send the form data to a server
            alert('Obrigado por sua mensagem! Entraremos em contato em breve.');
            contactForm.reset();
        });
    </script>
</body>
</html>
