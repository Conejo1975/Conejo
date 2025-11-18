<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>GameZone - Descargas, Trucos y Guías</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }

        :root {
            --primary: #1a1a2e;
            --secondary: #16213e;
            --accent: #0f3460;
            --highlight: #e94560;
            --text: #f1f1f1;
            --gray: #8a8a8a;
            --card-bg: #222831;
        }

        body {
            background-color: var(--primary);
            color: var(--text);
            line-height: 1.6;
        }

        /* Header */
        header {
            background: linear-gradient(135deg, var(--secondary), var(--accent));
            padding: 1rem 5%;
            box-shadow: 0 4px 12px rgba(0,0,0,0.3);
            position: sticky;
            top: 0;
            z-index: 100;
        }

        .header-content {
            display: flex;
            justify-content: space-between;
            align-items: center;
            max-width: 1400px;
            margin: 0 auto;
        }

        .logo {
            display: flex;
            align-items: center;
            gap: 12px;
        }

        .logo i {
            font-size: 2.2rem;
            color: var(--highlight);
        }

        .logo h1 {
            font-size: 1.8rem;
            font-weight: 800;
            background: linear-gradient(to right, #ff6b6b, #ffd166);
            -webkit-background-clip: text;
            background-clip: text;
            color: transparent;
            letter-spacing: 1px;
        }

        nav ul {
            display: flex;
            list-style: none;
            gap: 1.5rem;
        }

        nav a {
            color: var(--text);
            text-decoration: none;
            font-weight: 600;
            font-size: 1.1rem;
            padding: 0.5rem 1rem;
            border-radius: 5px;
            transition: all 0.3s ease;
        }

        nav a:hover, nav a.active {
            background-color: rgba(233, 69, 96, 0.2);
            color: var(--highlight);
        }

        .search-bar {
            display: flex;
            align-items: center;
        }

        .search-bar input {
            padding: 0.6rem 1rem;
            border: none;
            border-radius: 25px 0 0 25px;
            background-color: rgba(255,255,255,0.1);
            color: white;
            width: 200px;
            outline: none;
        }

        .search-bar button {
            background-color: var(--highlight);
            border: none;
            color: white;
            padding: 0.6rem 1.2rem;
            border-radius: 0 25px 25px 0;
            cursor: pointer;
            transition: background 0.3s;
        }

        .search-bar button:hover {
            background-color: #d63050;
        }

        /* Hero Section */
        .hero {
            background: linear-gradient(rgba(16, 52, 96, 0.85), rgba(10, 30, 60, 0.9)), url('https://images.unsplash.com/photo-1550745165-9bc0b252726f?ixlib=rb-4.0.3') center/cover no-repeat;
            padding: 5rem 5%;
            text-align: center;
            margin-bottom: 2rem;
        }

        .hero h2 {
            font-size: 3.2rem;
            margin-bottom: 1rem;
            text-shadow: 0 2px 10px rgba(0,0,0,0.5);
        }

        .hero p {
            font-size: 1.4rem;
            max-width: 800px;
            margin: 0 auto 2rem;
            color: #e0e0e0;
        }

        .btn {
            display: inline-block;
            background: linear-gradient(to right, var(--highlight), #ff6b6b);
            color: white;
            padding: 0.9rem 2.5rem;
            border-radius: 30px;
            text-decoration: none;
            font-weight: bold;
            font-size: 1.1rem;
            transition: transform 0.3s, box-shadow 0.3s;
            box-shadow: 0 4px 15px rgba(233, 69, 96, 0.4);
        }

        .btn:hover {
            transform: translateY(-3px);
            box-shadow: 0 7px 20px rgba(233, 69, 96, 0.6);
        }

        /* Categories */
        .container {
            max-width: 1400px;
            margin: 0 auto;
            padding: 0 5%;
        }

        .section-title {
            display: flex;
            align-items: center;
            gap: 15px;
            margin: 2.5rem 0 1.5rem;
            padding-bottom: 0.5rem;
            border-bottom: 2px solid var(--highlight);
        }

        .section-title i {
            color: var(--highlight);
            font-size: 1.8rem;
        }

        .section-title h2 {
            font-size: 2rem;
            font-weight: 700;
        }

        .categories {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 1.5rem;
            margin-bottom: 3rem;
        }

        .category-card {
            background: linear-gradient(145deg, var(--card-bg), #1d212a);
            border-radius: 12px;
            overflow: hidden;
            transition: transform 0.3s, box-shadow 0.3s;
            box-shadow: 0 5px 15px rgba(0,0,0,0.2);
        }

        .category-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 12px 25px rgba(0,0,0,0.3);
        }

        .category-img {
            height: 160px;
            background-size: cover;
            background-position: center;
        }

        .category-content {
            padding: 1.2rem;
        }

        .category-content h3 {
            font-size: 1.4rem;
            margin-bottom: 0.5rem;
            color: #ffd166;
        }

        .category-content p {
            color: var(--gray);
            font-size: 0.95rem;
        }

        /* Posts Grid */
        .posts-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(320px, 1fr));
            gap: 2rem;
            margin-bottom: 3rem;
        }

        .post-card {
            background: var(--card-bg);
            border-radius: 12px;
            overflow: hidden;
            box-shadow: 0 5px 15px rgba(0,0,0,0.2);
            transition: all 0.4s ease;
        }

        .post-card:hover {
            transform: scale(1.02);
            box-shadow: 0 10px 25px rgba(0,0,0,0.3);
        }

        .post-img {
            height: 200px;
            background-size: cover;
            background-position: center;
        }

        .post-content {
            padding: 1.5rem;
        }

        .post-meta {
            display: flex;
            gap: 15px;
            margin-bottom: 1rem;
            color: var(--gray);
            font-size: 0.85rem;
        }

        .post-meta span {
            display: flex;
            align-items: center;
            gap: 5px;
        }

        .post-content h3 {
            font-size: 1.5rem;
            margin-bottom: 0.8rem;
            line-height: 1.3;
        }

        .post-content p {
            color: var(--gray);
            margin-bottom: 1.2rem;
            font-size: 0.95rem;
        }

        .post-tags {
            display: flex;
            flex-wrap: wrap;
            gap: 0.5rem;
            margin-top: 1rem;
        }

        .tag {
            background: rgba(233, 69, 96, 0.15);
            color: var(--highlight);
            padding: 0.3rem 0.8rem;
            border-radius: 20px;
            font-size: 0.8rem;
        }

        /* Sidebar */
        .sidebar {
            margin-top: 2rem;
        }

        .widget {
            background: var(--card-bg);
            border-radius: 12px;
            padding: 1.5rem;
            margin-bottom: 1.8rem;
            box-shadow: 0 4px 12px rgba(0,0,0,0.15);
        }

        .widget h3 {
            font-size: 1.4rem;
            margin-bottom: 1.2rem;
            color: #ffd166;
            padding-bottom: 0.5rem;
            border-bottom: 1px solid rgba(255,255,255,0.1);
        }

        .popular-games li {
            display: flex;
            align-items: center;
            padding: 0.8rem 0;
            border-bottom: 1px solid rgba(255,255,255,0.05);
        }

        .popular-games li:last-child {
            border-bottom: none;
        }

        .game-icon {
            width: 50px;
            height: 50px;
            border-radius: 8px;
            margin-right: 1rem;
            background-size: cover;
            background-position: center;
        }

        .game-info h4 {
            font-size: 1rem;
            margin-bottom: 0.2rem;
        }

        .game-info .rating {
            color: #ffd166;
            font-size: 0.85rem;
        }

        .newsletter input {
            width: 100%;
            padding: 0.8rem;
            margin-bottom: 0.8rem;
            border-radius: 8px;
            border: 1px solid rgba(255,255,255,0.1);
            background: rgba(255,255,255,0.05);
            color: white;
        }

        .social-links {
            display: flex;
            gap: 1rem;
            margin-top: 1rem;
        }

        .social-links a {
            display: flex;
            align-items: center;
            justify-content: center;
            width: 36px;
            height: 36px;
            border-radius: 50%;
            background: rgba(255,255,255,0.1);
            color: white;
            transition: all 0.3s;
        }

        .social-links a:hover {
            background: var(--highlight);
            transform: translateY(-3px);
        }

        /* Footer */
        footer {
            background: var(--secondary);
            padding: 3rem 5%;
            margin-top: 3rem;
        }

        .footer-content {
            max-width: 1400px;
            margin: 0 auto;
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 2.5rem;
        }

        .footer-col h3 {
            font-size: 1.4rem;
            margin-bottom: 1.5rem;
            color: #ffd166;
            position: relative;
            padding-bottom: 0.5rem;
        }

        .footer-col h3::after {
            content: '';
            position: absolute;
            left: 0;
            bottom: 0;
            width: 50px;
            height: 2px;
            background: var(--highlight);
        }

        .footer-col ul {
            list-style: none;
        }

        .footer-col ul li {
            margin-bottom: 0.8rem;
        }

        .footer-col ul li a {
            color: var(--gray);
            text-decoration: none;
            transition: color 0.3s;
        }

        .footer-col ul li a:hover {
            color: var(--highlight);
            padding-left: 5px;
        }

        .copyright {
            text-align: center;
            padding-top: 2.5rem;
            margin-top: 2.5rem;
            border-top: 1px solid rgba(255,255,255,0.1);
            color: var(--gray);
            font-size: 0.9rem;
        }

        /* Responsive */
        @media (max-width: 768px) {
            .header-content {
                flex-direction: column;
                gap: 1rem;
            }
            
            nav ul {
                flex-wrap: wrap;
                justify-content: center;
            }
            
            .search-bar {
                width: 100%;
                justify-content: center;
            }
            
            .hero h2 {
                font-size: 2.2rem;
            }
            
            .hero p {
                font-size: 1.1rem;
            }
        }

        @media (max-width: 480px) {
            .logo h1 {
                font-size: 1.5rem;
            }
            
            .search-bar input {
                width: 150px;
            }
        }
    </style>
</head>
<body>
    <!-- Header -->
    <header>
        <div class="header-content">
            <div class="logo">
                <i class="fas fa-gamepad"></i>
                <h1>GameZone</h1>
            </div>
            <nav>
                <ul>
                    <li><a href="#" class="active">Inicio</a></li>
                    <li><a href="#">Descargas</a></li>
                    <li><a href="#">Trucos</a></li>
                    <li><a href="#">Guías</a></li>
                    <li><a href="#">Noticias</a></li>
                    <li><a href="#">Foro</a></li>
                </ul>
            </nav>
            <div class="search-bar">
                <input type="text" placeholder="Buscar juego, truco o guía...">
                <button><i class="fas fa-search"></i></button>
            </div>
        </div>
    </header>

    <!-- Hero Section -->
    <section class="hero">
        <h2>Tu Zona de Juegos Favorita</h2>
        <p>Descargas seguras, trucos exclusivos, guías detalladas y ayuda profesional para todos tus juegos favoritos.</p>
        <a href="#" class="btn">Explorar Juegos</a>
    </section>

    <!-- Main Content -->
    <div class="container">
        <!-- Categories -->
        <div class="section-title">
            <i class="fas fa-th-large"></i>
            <h2>Categorías Populares</h2>
        </div>
        <div class="categories">
            <div class="category-card">
                <div class="category-img" style="background-image: url('https://images.unsplash.com/photo-1552820728-8b83bb6b773f?ixlib=rb-4.0.3');"></div>
                <div class="category-content">
                    <h3>Acción y Aventura</h3>
                    <p>Los mejores títulos de acción y aventura con descargas directas y trucos exclusivos.</p>
                </div>
            </div>
            <div class="category-card">
                <div class="category-img" style="background-image: url('https://images.unsplash.com/photo-1542751371-adc38448a05e?ixlib=rb-4.0.3');"></div>
                <div class="category-content">
                    <h3>Deportes</h3>
                    <p>Fútbol, baloncesto, carreras y más. Patches, mods y mejoras para tus deportes favoritos.</p>
                </div>
            </div>
            <div class="category-card">
                <div class="category-img" style="background-image: url('https://images.unsplash.com/photo-1511512578047-dfb367046420?ixlib=rb-4.0.3');"></div>
                <div class="category-content">
                    <h3>Estrategia</h3>
                    <p>Domina la estrategia con nuestras guías detalladas y trucos para juegos de estrategia.</p>
                </div>
            </div>
            <div class="category-card">
                <div class="category-img" style="background-image: url('https://images.unsplash.com/photo-1550745165-9bc0b252726f?ixlib=rb-4.0.3');"></div>
                <div class="category-content">
                    <h3>RPG</h3>
                    <p>Mundos épicos, personajes memorables y secretos ocultos en los mejores RPG.</p>
                </div>
            </div>
        </div>

        <!-- Featured Posts -->
        <div class="section-title">
            <i class="fas fa-fire"></i>
            <h2>Destacados esta Semana</h2>
        </div>
        <div class="posts-grid">
            <div class="post-card">
                <div class="post-img" style="background-image: url('https://images.unsplash.com/photo-1552820728-8b83bb6b773f?ixlib=rb-4.0.3');"></div>
                <div class="post-content">
                    <div class="post-meta">
                        <span><i class="far fa-calendar"></i> 15 Nov 2025</span>
                        <span><i class="far fa-folder"></i> Descargas</span>
                    </div>
                    <h3>Cyberpunk 2077: Edición Definitiva - Descarga Directa</h3>
                    <p>Versión completa con todos los DLCs y parches actualizados. Incluye mods recomendados y guía de instalación paso a paso.</p>
                    <div class="post-tags">
                        <span class="tag">Cyberpunk 2077</span>
                        <span class="tag">Descarga Segura</span>
                        <span class="tag">Edición Completa</span>
                    </div>
                </div>
            </div>
            <div class="post-card">
                <div class="post-img" style="background-image: url('https://images.unsplash.com/photo-1542751371-adc38448a05e?ixlib=rb-4.0.3');"></div>
                <div class="post-content">
                    <div class="post-meta">
                        <span><i class="far fa-calendar"></i> 12 Nov 2025</span>
                        <span><i class="far fa-folder"></i> Trucos</span>
                    </div>
                    <h3>10 Trucos Secretos de FIFA 26 que Nadie Conoce</h3>
                    <p>Descubre combinaciones de botones, movimientos especiales y estrategias para dominar cualquier partido.</p>
                    <div class="post-tags">
                        <span class="tag">FIFA 26</span>
                        <span class="tag">Trucos Avanzados</span>
                        <span class="tag">Tutorial</span>
                    </div>
                </div>
            </div>
            <div class="post-card">
                <div class="post-img" style="background-image: url('https://images.unsplash.com/photo-1550745165-9bc0b252726f?ixlib=rb-4.0.3');"></div>
                <div class="post-content">
                    <div class="post-meta">
                        <span><i class="far fa-calendar"></i> 10 Nov 2025</span>
                        <span><i class="far fa-folder"></i> Guías</span>
                    </div>
                    <h3>Guía Completa: Cómo Completar Elden Ring sin Morir</h3>
                    <p>Estrategias para cada jefe, builds recomendados y rutas óptimas para completar el juego sin una sola muerte.</p>
                    <div class="post-tags">
                        <span class="tag">Elden Ring</span>
                        <span class="tag">Guía Definitiva</span>
                        <span class="tag">Sin Muertes</span>
                    </div>
                </div>
            </div>
        </div>

        <!-- Sidebar -->
        <div class="sidebar">
            <div class="widget">
                <h3>Juegos Populares</h3>
                <ul class="popular-games">
                    <li>
                        <div class="game-icon" style="background-image: url('https://images.unsplash.com/photo-1542751371-adc38448a05e?ixlib=rb-4.0.3');"></div>
                        <div class="game-info">
                            <h4>FIFA 26</h4>
                            <div class="rating"><i class="fas fa-star"></i> 4.8</div>
                        </div>
                    </li>
                    <li>
                        <div class="game-icon" style="background-image: url('https://images.unsplash.com/photo-1552820728-8b83bb6b773f?ixlib=rb-4.0.3');"></div>
                        <div class="game-info">
                            <h4>Cyberpunk 2077</h4>
                            <div class="rating"><i class="fas fa-star"></i> 4.9</div>
                        </div>
                    </li>
                    <li>
                        <div class="game-icon" style="background-image: url('https://images.unsplash.com/photo-1511512578047-dfb367046420?ixlib=rb-4.0.3');"></div>
                        <div class="game-info">
                            <h4>Civilization VII</h4>
                            <div class="rating"><i class="fas fa-star"></i> 4.7</div>
                        </div>
                    </li>
                    <li>
                        <div class="game-icon" style="background-image: url('https://images.unsplash.com/photo-1550745165-9bc0b252726f?ixlib=rb-4.0.3');"></div>
                        <div class="game-info">
                            <h4>Elden Ring</h4>
                            <div class="rating"><i class="fas fa-star"></i> 4.9</div>
                        </div>
                    </li>
                </ul>
            </div>

            <div class="widget">
                <h3>Newsletter</h3>
                <p>Recibe las últimas descargas, trucos y guías directamente en tu correo.</p>
                <form class="newsletter">
                    <input type="email" placeholder="Tu correo electrónico">
                    <button class="btn" type="submit">Suscribirse</button>
                </form>
                <div class="social-links">
                    <a href="#"><i class="fab fa-facebook-f"></i></a>
                    <a href="#"><i class="fab fa-twitter"></i></a>
                    <a href="#"><i class="fab fa-youtube"></i></a>
                    <a href="#"><i class="fab fa-discord"></i></a>
                </div>
            </div>
        </div>
    </div>

    <!-- Footer -->
    <footer>
        <div class="footer-content">
            <div class="footer-col">
                <h3>GameZone</h3>
                <p>Tu fuente número uno para descargas seguras, trucos exclusivos y guías detalladas de videojuegos.</p>
            </div>
            <div class="footer-col">
                <h3>Enlaces Rápidos</h3>
                <ul>
                    <li><a href="#">Inicio</a></li>
                    <li><a href="#">Descargas</a></li>
                    <li><a href="#">Trucos</a></li>
                    <li><a href="#">Guías</a></li>
                    <li><a href="#">Foro</a></li>
                </ul>
            </div>
            <div class="footer-col">
                <h3>Categorías</h3>
                <ul>
                    <li><a href="#">Acción y Aventura</a></li>
                    <li><a href="#">Deportes</a></li>
                    <li><a href="#">Estrategia</a></li>
                    <li><a href="#">RPG</a></li>
                    <li><a href="#">Indie</a></li>
                </ul>
            </div>
            <div class="footer-col">
                <h3>Contacto</h3>
                <ul>
                    <li><i class="fas fa-envelope"></i> contacto@gamezone.com</li>
                    <li><i class="fas fa-phone"></i> +34 900 123 456</li>
                    <li><i class="fas fa-map-marker-alt"></i> Madrid, España</li>
                </ul>
            </div>
        </div>
        <div class="copyright">
            <p>&copy; 2025 GameZone. Todos los derechos reservados. Este sitio es solo con fines educativos y de entretenimiento.</p>
        </div>
    </footer>

    <script>
        // Simple interactive elements
        document.addEventListener('DOMContentLoaded', function() {
            // Active menu item
            const navLinks = document.querySelectorAll('nav a');
            navLinks.forEach(link => {
                link.addEventListener('click', function(e) {
                    e.preventDefault();
                    navLinks.forEach(l => l.classList.remove('active'));
                    this.classList.add('active');
                });
            });

            // Newsletter form submission
            const newsletterForm = document.querySelector('.newsletter');
            if (newsletterForm) {
                newsletterForm.addEventListener('submit', function(e) {
                    e.preventDefault();
                    const email = this.querySelector('input').value;
                    if (email && email.includes('@')) {
                        alert('¡Gracias por suscribirte a GameZone! Pronto recibirás nuestras novedades.');
                        this.reset();
                    } else {
                        alert('Por favor, introduce un correo electrónico válido.');
                    }
                });
            }

            // Smooth scrolling for anchor links
            document.querySelectorAll('a[href^="#"]').forEach(anchor => {
                anchor.addEventListener('click', function(e) {
                    e.preventDefault();
                    const target = document.querySelector(this.getAttribute('href'));
                    if (target) {
                        window.scrollTo({
                            top: target.offsetTop - 80,
                            behavior: 'smooth'
                        });
                    }
                });
            });
        });
    </script>
</body>
</html>

