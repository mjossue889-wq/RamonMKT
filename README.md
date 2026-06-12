# RamonMKT
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Ramón Espinoza - Marketing Digital & Estrategia de Marca</title>
    <meta name="description" content="Portafolio profesional de Ramón Espinoza. Especialista en marketing digital, estrategia de contenidos y posicionamiento de marca.">
    <meta name="keywords" content="marketing digital, estrategia de marca, social media, contenidos, Mexicali">
    <meta name="author" content="Ramón Espinoza">
    <meta property="og:title" content="Ramón Espinoza - Marketing Digital">
    <meta property="og:description" content="Transformo marcas en resultados. Especialista en estrategia digital y marketing de contenidos.">
    <meta property="og:type" content="website">
    
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        :root {
            --mint: #10B981;
            --purple: #A855F7;
            --cyan: #06B6D4;
            --dark-bg: #0F172A;
            --dark-secondary: #1E293B;
            --dark-text: #F8FAFC;
            --dark-muted: #CBD5E1;
            
            --light-bg: #F8FAFC;
            --light-secondary: #F1F5F9;
            --light-text: #0F172A;
            --light-muted: #64748B;
        }

        body {
            font-family: 'Inter', -apple-system, BlinkMacSystemFont, 'Segoe UI', sans-serif;
            background-color: var(--dark-bg);
            color: var(--dark-text);
            transition: background-color 0.3s ease, color 0.3s ease;
            line-height: 1.6;
        }

        body.light-mode {
            background-color: var(--light-bg);
            color: var(--light-text);
        }

        /* Scrollbar Styling */
        ::-webkit-scrollbar {
            width: 8px;
        }

        ::-webkit-scrollbar-track {
            background: var(--dark-secondary);
        }

        ::-webkit-scrollbar-thumb {
            background: var(--mint);
            border-radius: 4px;
        }

        body.light-mode::-webkit-scrollbar-track {
            background: var(--light-secondary);
        }

        /* Navbar */
        nav {
            position: fixed;
            top: 0;
            width: 100%;
            z-index: 50;
            backdrop-filter: blur(10px);
            border-bottom: 1px solid rgba(16, 185, 129, 0.1);
            background-color: rgba(15, 23, 42, 0.8);
            transition: all 0.3s ease;
        }

        body.light-mode nav {
            background-color: rgba(248, 250, 252, 0.8);
            border-bottom: 1px solid rgba(16, 185, 129, 0.1);
        }

        nav .container {
            max-width: 1280px;
            margin: 0 auto;
            padding: 0 1rem;
            display: flex;
            justify-content: space-between;
            align-items: center;
            height: 64px;
        }

        .logo {
            font-size: 24px;
            font-weight: bold;
            background: linear-gradient(135deg, #06B6D4, #A855F7);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
        }

        nav .nav-links {
            display: none;
            gap: 2rem;
            align-items: center;
        }

        nav .nav-links a {
            color: var(--dark-muted);
            text-decoration: none;
            font-size: 0.875rem;
            font-weight: 500;
            transition: color 0.3s;
        }

        body.light-mode nav .nav-links a {
            color: var(--light-muted);
        }

        nav .nav-links a:hover {
            color: var(--mint);
        }

        .theme-toggle {
            background-color: var(--dark-secondary);
            color: var(--mint);
            border: none;
            padding: 0.5rem;
            border-radius: 0.5rem;
            cursor: pointer;
            font-size: 1rem;
            transition: transform 0.3s;
        }

        body.light-mode .theme-toggle {
            background-color: var(--light-secondary);
        }

        .theme-toggle:hover {
            transform: scale(1.1);
        }

        .mobile-menu {
            display: flex;
            gap: 1rem;
            align-items: center;
        }

        .menu-toggle {
            background: none;
            border: none;
            color: var(--dark-text);
            font-size: 1.5rem;
            cursor: pointer;
            display: none;
        }

        body.light-mode .menu-toggle {
            color: var(--light-text);
        }

        /* Responsive Navbar */
        @media (min-width: 768px) {
            nav .nav-links {
                display: flex;
            }
            .menu-toggle {
                display: none !important;
            }
        }

        @media (max-width: 767px) {
            .menu-toggle {
                display: block;
            }
        }

        /* Hero Section */
        .hero {
            min-height: 100vh;
            display: flex;
            align-items: center;
            justify-content: center;
            padding: 2rem 1rem;
            padding-top: 5rem;
            position: relative;
            overflow: hidden;
        }

        .hero::before {
            content: '';
            position: absolute;
            width: 400px;
            height: 400px;
            background: radial-gradient(circle at 20% 50%, rgba(16, 185, 129, 0.15), transparent 50%);
            border-radius: 50%;
            filter: blur(48px);
            left: 0;
            top: 20%;
        }

        .hero::after {
            content: '';
            position: absolute;
            width: 400px;
            height: 400px;
            background: radial-gradient(circle at 80% 80%, rgba(168, 85, 247, 0.15), transparent 50%);
            border-radius: 50%;
            filter: blur(48px);
            right: 0;
            bottom: 0;
        }

        .hero-content {
            max-width: 56rem;
            text-align: center;
            position: relative;
            z-index: 10;
            animation: fadeInUp 0.8s ease-out;
        }

        @keyframes fadeInUp {
            from {
                opacity: 0;
                transform: translateY(30px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        .hero-badge {
            display: inline-block;
            background-color: var(--mint);
            color: var(--dark-bg);
            font-size: 0.75rem;
            font-weight: 600;
            padding: 0.5rem 1rem;
            border-radius: 2rem;
            margin-bottom: 1.5rem;
        }

        .hero h1 {
            font-size: clamp(2.5rem, 8vw, 3.5rem);
            font-weight: 800;
            margin-bottom: 1.5rem;
            line-height: 1.2;
        }

        .hero h1 .mint {
            color: var(--mint);
        }

        .hero h1 .purple {
            color: var(--purple);
        }

        .hero p {
            font-size: 1.125rem;
            color: var(--dark-muted);
            margin-bottom: 2rem;
            max-width: 32rem;
            margin-left: auto;
            margin-right: auto;
        }

        body.light-mode .hero p {
            color: var(--light-muted);
        }

        .hero-buttons {
            display: flex;
            flex-direction: column;
            gap: 1rem;
            justify-content: center;
            margin-bottom: 3rem;
        }

        @media (min-width: 640px) {
            .hero-buttons {
                flex-direction: row;
            }
        }

        .btn {
            padding: 0.75rem 2rem;
            border-radius: 0.5rem;
            font-weight: 600;
            border: none;
            cursor: pointer;
            text-decoration: none;
            display: inline-flex;
            align-items: center;
            gap: 0.5rem;
            justify-content: center;
            transition: transform 0.3s, box-shadow 0.3s;
        }

        .btn:hover {
            transform: scale(1.05);
        }

        .btn-primary {
            background-color: var(--mint);
            color: var(--dark-bg);
        }

        .btn-secondary {
            border: 2px solid var(--mint);
            color: var(--mint);
            background-color: transparent;
        }

        /* Sections */
        section {
            padding: 5rem 1rem;
        }

        .container {
            max-width: 1280px;
            margin: 0 auto;
        }

        section h2 {
            font-size: clamp(2rem, 5vw, 3rem);
            font-weight: 800;
            margin-bottom: 1rem;
        }

        section > .container > p {
            font-size: 1.125rem;
            color: var(--dark-muted);
            margin-bottom: 4rem;
        }

        body.light-mode section > .container > p {
            color: var(--light-muted);
        }

        /* Timeline */
        .experience-list {
            display: space-y-12;
        }

        .experience-item {
            display: flex;
            gap: 1.5rem;
            margin-bottom: 3rem;
        }

        .experience-timeline {
            display: flex;
            flex-direction: column;
            align-items: center;
        }

        .timeline-dot {
            width: 48px;
            height: 48px;
            background-color: var(--mint);
            color: var(--dark-bg);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-weight: bold;
            font-size: 1.125rem;
        }

        .timeline-line {
            width: 4px;
            height: 96px;
            background-color: var(--mint);
            margin-top: 1rem;
            opacity: 0.3;
        }

        .experience-card {
            flex: 1;
            background-color: var(--dark-secondary);
            padding: 1.5rem;
            border-radius: 0.75rem;
            border: 1px solid rgba(16, 185, 129, 0.25);
            transition: transform 0.3s;
        }

        body.light-mode .experience-card {
            background-color: var(--light-secondary);
        }

        .experience-card:hover {
            transform: scale(1.02);
        }

        .experience-header {
            display: flex;
            justify-content: space-between;
            align-items: flex-start;
            margin-bottom: 1rem;
            flex-wrap: wrap;
            gap: 1rem;
        }

        .experience-company {
            font-size: 1.25rem;
            font-weight: bold;
        }

        .experience-role {
            color: var(--mint);
            font-weight: 600;
            font-size: 0.875rem;
            margin-top: 0.25rem;
        }

        .experience-year {
            color: var(--dark-muted);
            font-size: 0.875rem;
        }

        body.light-mode .experience-year {
            color: var(--light-muted);
        }

        .experience-description {
            color: var(--dark-muted);
            margin-bottom: 1rem;
        }

        body.light-mode .experience-description {
            color: var(--light-muted);
        }

        .achievements {
            margin-bottom: 1rem;
        }

        .achievements-label {
            color: var(--dark-muted);
            font-size: 0.875rem;
            font-weight: 600;
            margin-bottom: 0.5rem;
        }

        body.light-mode .achievements-label {
            color: var(--light-muted);
        }

        .achievements-list {
            list-style: none;
        }

        .achievements-list li {
            color: var(--dark-muted);
            font-size: 0.875rem;
            display: flex;
            align-items: center;
            gap: 0.5rem;
            margin-bottom: 0.25rem;
        }

        body.light-mode .achievements-list li {
            color: var(--light-muted);
        }

        .achievements-list span {
            color: var(--mint);
        }

        .tags {
            display: flex;
            flex-wrap: wrap;
            gap: 0.5rem;
        }

        .tag {
            background-color: rgba(16, 185, 129, 0.2);
            color: var(--mint);
            font-size: 0.75rem;
            padding: 0.25rem 0.75rem;
            border-radius: 9999px;
            font-weight: 500;
        }

        /* Projects Section */
        .projects-bg {
            background-color: var(--dark-secondary);
        }

        body.light-mode .projects-bg {
            background-color: var(--light-secondary);
        }

        .filters {
            display: flex;
            gap: 0.75rem;
            margin-bottom: 3rem;
            flex-wrap: wrap;
        }

        .filter-btn {
            background-color: var(--dark-secondary);
            color: var(--dark-text);
            border: 2px solid var(--mint);
            padding: 0.5rem 1.5rem;
            border-radius: 0.5rem;
            font-weight: 600;
            cursor: pointer;
            transition: all 0.3s;
        }

        body.light-mode .filter-btn {
            background-color: var(--light-secondary);
            color: var(--light-text);
        }

        .filter-btn.active {
            background-color: var(--mint);
            color: var(--dark-bg);
        }

        .filter-btn:hover {
            transform: scale(1.05);
        }

        .projects-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(320px, 1fr));
            gap: 1.5rem;
            margin-bottom: 3rem;
        }

        .project-card {
            background-color: var(--dark-bg);
            padding: 2rem;
            border-radius: 0.75rem;
            border: 1px solid rgba(16, 185, 129, 0.3);
            transition: transform 0.3s, border-color 0.3s;
        }

        body.light-mode .project-card {
            background-color: var(--light-bg);
        }

        .project-card:hover {
            transform: scale(1.05);
            border-color: var(--mint);
        }

        .project-emoji {
            font-size: 3rem;
            margin-bottom: 1rem;
        }

        .project-type {
            background-color: rgba(16, 185, 129, 0.2);
            color: var(--mint);
            font-size: 0.75rem;
            font-weight: 600;
            padding: 0.25rem 0.75rem;
            border-radius: 2rem;
            display: inline-block;
            margin-bottom: 1rem;
        }

        .project-card h3 {
            font-size: 1.5rem;
            margin-bottom: 0.5rem;
        }

        .project-description {
            color: var(--dark-muted);
            margin-bottom: 1.5rem;
        }

        body.light-mode .project-description {
            color: var(--light-muted);
        }

        .project-results {
            margin-bottom: 1.5rem;
        }

        .project-results-label {
            color: var(--dark-muted);
            font-size: 0.875rem;
            font-weight: 600;
            margin-bottom: 0.75rem;
        }

        body.light-mode .project-results-label {
            color: var(--light-muted);
        }

        .project-results-list {
            list-style: none;
        }

        .project-results-list li {
            color: var(--dark-muted);
            font-size: 0.875rem;
            display: flex;
            gap: 0.5rem;
            margin-bottom: 0.5rem;
        }

        body.light-mode .project-results-list li {
            color: var(--light-muted);
        }

        .project-results-list span {
            color: var(--mint);
            flex-shrink: 0;
        }

        .project-tools {
            display: flex;
            flex-wrap: wrap;
            gap: 0.5rem;
        }

        .tool-tag {
            background-color: rgba(168, 85, 247, 0.2);
            color: var(--purple);
            font-size: 0.75rem;
            padding: 0.25rem 0.5rem;
            border-radius: 0.25rem;
            font-weight: 500;
        }

        /* Gallery Placeholder */
        .gallery-placeholder {
            background-color: var(--dark-bg);
            border: 2px dashed rgba(16, 185, 129, 0.3);
            border-radius: 0.75rem;
            padding: 4rem 1rem;
            text-align: center;
            margin-top: 3rem;
        }

        body.light-mode .gallery-placeholder {
            background-color: var(--light-bg);
        }

        .gallery-placeholder p {
            margin-bottom: 1rem;
        }

        .gallery-emoji {
            font-size: 3rem;
            margin-bottom: 1rem;
        }

        /* Skills Section */
        .skills-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 2rem;
        }

        .skill-category {
            background-color: var(--dark-secondary);
            padding: 2rem;
            border-radius: 0.75rem;
            border: 1px solid rgba(16, 185, 129, 0.4);
        }

        body.light-mode .skill-category {
            background-color: var(--light-secondary);
        }

        .skill-category h3 {
            color: var(--mint);
            font-size: 1.125rem;
            font-weight: bold;
            margin-bottom: 1.5rem;
        }

        .skill-item {
            margin-bottom: 1.5rem;
        }

        .skill-name {
            display: flex;
            justify-content: space-between;
            margin-bottom: 0.5rem;
        }

        .skill-bar {
            height: 8px;
            background-color: rgba(16, 185, 129, 0.2);
            border-radius: 9999px;
            overflow: hidden;
        }

        .skill-fill {
            height: 100%;
            background-color: var(--mint);
            border-radius: 9999px;
            animation: fillBar 1.5s ease-out forwards;
        }

        @keyframes fillBar {
            from {
                width: 0;
            }
            to {
                width: var(--skill-width);
            }
        }

        /* Certifications */
        .cert-bg {
            background-color: var(--dark-secondary);
        }

        body.light-mode .cert-bg {
            background-color: var(--light-secondary);
        }

        .certifications-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 1.5rem;
        }

        .cert-card {
            background-color: var(--dark-bg);
            padding: 1.5rem;
            border-radius: 0.75rem;
            border: 1px solid rgba(16, 185, 129, 0.3);
            transition: transform 0.3s;
        }

        body.light-mode .cert-card {
            background-color: var(--light-bg);
        }

        .cert-card:hover {
            transform: scale(1.05);
        }

        .cert-header {
            display: flex;
            justify-content: space-between;
            align-items: flex-start;
            margin-bottom: 1rem;
        }

        .cert-emoji {
            font-size: 2.5rem;
        }

        .cert-badge {
            background-color: rgba(16, 185, 129, 0.2);
            color: var(--mint);
            font-size: 0.75rem;
            font-weight: bold;
            padding: 0.25rem 0.75rem;
            border-radius: 2rem;
        }

        .cert-title {
            font-weight: bold;
            margin-bottom: 0.5rem;
        }

        .cert-issuer {
            color: var(--mint);
            font-size: 0.875rem;
            font-weight: 600;
            margin-bottom: 0.5rem;
        }

        .cert-date {
            color: var(--dark-muted);
            font-size: 0.875rem;
        }

        body.light-mode .cert-date {
            color: var(--light-muted);
        }

        /* Contact Section */
        .contact-content {
            max-width: 48rem;
            margin: 0 auto;
            text-align: center;
        }

        .contact-content h2 {
            margin-bottom: 1.5rem;
        }

        .contact-description {
            font-size: 1.125rem;
            color: var(--dark-muted);
            margin-bottom: 3rem;
        }

        body.light-mode .contact-description {
            color: var(--light-muted);
        }

        .contact-buttons {
            display: flex;
            flex-direction: column;
            gap: 1rem;
            justify-content: center;
            margin-bottom: 3rem;
        }

        @media (min-width: 640px) {
            .contact-buttons {
                flex-direction: row;
            }
        }

        .contact-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 1rem;
        }

        .contact-card {
            background-color: var(--dark-secondary);
            padding: 1.5rem;
            border-radius: 0.5rem;
        }

        body.light-mode .contact-card {
            background-color: var(--light-secondary);
        }

        .contact-card p:first-child {
            color: var(--dark-muted);
            font-size: 0.875rem;
            margin-bottom: 0.5rem;
        }

        body.light-mode .contact-card p:first-child {
            color: var(--light-muted);
        }

        /* Download CV Section */
        .download-section {
            background-color: var(--dark-secondary);
            border-top: 1px solid rgba(16, 185, 129, 0.4);
            padding: 4rem 1rem;
        }

        body.light-mode .download-section {
            background-color: var(--light-secondary);
            border-top: 1px solid rgba(16, 185, 129, 0.2);
        }

        .download-content {
            max-width: 48rem;
            margin: 0 auto;
            display: flex;
            flex-direction: column;
            align-items: center;
            gap: 1.5rem;
            text-align: center;
        }

        @media (min-width: 640px) {
            .download-content {
                flex-direction: row;
                text-align: left;
            }
        }

        .download-text h4 {
            font-weight: bold;
            margin-bottom: 0.5rem;
        }

        .download-text p {
            color: var(--dark-muted);
            font-size: 0.875rem;
        }

        body.light-mode .download-text p {
            color: var(--light-muted);
        }

        /* Footer */
        footer {
            background-color: var(--dark-secondary);
            border-top: 1px solid rgba(16, 185, 129, 0.3);
            padding: 3rem 1rem;
        }

        body.light-mode footer {
            background-color: var(--light-secondary);
        }

        .footer-container {
            max-width: 1280px;
            margin: 0 auto;
        }

        .footer-top {
            display: flex;
            flex-direction: column;
            justify-content: space-between;
            align-items: center;
            gap: 2rem;
            margin-bottom: 2rem;
        }

        @media (min-width: 768px) {
            .footer-top {
                flex-direction: row;
            }
        }

        .footer-brand h3 {
            font-size: 1.5rem;
            font-weight: bold;
            margin-bottom: 0.5rem;
        }

        .footer-brand p {
            color: var(--dark-muted);
            font-size: 0.875rem;
        }

        body.light-mode .footer-brand p {
            color: var(--light-muted);
        }

        .footer-links {
            display: flex;
            gap: 1rem;
        }

        .footer-links a {
            color: var(--mint);
            text-decoration: none;
            font-size: 1.5rem;
            transition: transform 0.3s;
        }

        .footer-links a:hover {
            transform: scale(1.25);
        }

        .footer-bottom {
            border-top: 1px solid rgba(16, 185, 129, 0.2);
            padding-top: 2rem;
            text-align: center;
        }

        .footer-bottom p {
            color: var(--dark-muted);
            font-size: 0.875rem;
            line-height: 1.6;
        }

        body.light-mode .footer-bottom p {
            color: var(--light-muted);
        }

        /* Smooth Scroll */
        html {
            scroll-behavior: smooth;
        }

        /* Mobile Responsive */
        @media (max-width: 640px) {
            section {
                padding: 3rem 1rem;
            }

            .hero {
                padding-top: 4rem;
                padding-bottom: 2rem;
            }

            .hero h1 {
                font-size: 1.875rem;
            }

            .experience-item {
                gap: 1rem;
            }

            .projects-grid {
                grid-template-columns: 1fr;
            }

            .skills-grid {
                grid-template-columns: 1fr;
            }

            .certifications-grid {
                grid-template-columns: 1fr;
            }

            .contact-grid {
                grid-template-columns: 1fr;
            }

            .footer-top {
                flex-direction: column-reverse;
            }
        }

        /* Animations */
        @keyframes slideIn {
            from {
                opacity: 0;
                transform: translateX(-20px);
            }
            to {
                opacity: 1;
                transform: translateX(0);
            }
        }

        .section-item {
            animation: slideIn 0.6s ease-out forwards;
        }

        .scroll-reveal {
            opacity: 0;
            transform: translateY(30px);
            transition: opacity 0.6s ease-out, transform 0.6s ease-out;
        }

        .scroll-reveal.revealed {
            opacity: 1;
            transform: translateY(0);
        }
    </style>
</head>
<body>
    <!-- Navbar -->
    <nav>
        <div class="container">
            <div class="logo">Ramón.</div>
            <div class="nav-links">
                <a href="#inicio">Inicio</a>
                <a href="#experiencia">Experiencia</a>
                <a href="#proyectos">Proyectos</a>
                <a href="#contacto">Contacto</a>
            </div>
            <div class="mobile-menu">
                <button class="theme-toggle" onclick="toggleTheme()">☀️</button>
                <button class="menu-toggle" onclick="toggleMenu()">☰</button>
            </div>
        </div>
    </nav>

    <!-- Hero Section -->
    <section class="hero" id="inicio">
        <div class="hero-content">
            <div class="hero-badge">📍 Mexicali, Baja California</div>
            <h1>Transformo <span class="mint">marcas</span> en <span class="purple">resultados</span></h1>
            <p>Especialista en estrategia digital, marketing de contenidos y posicionamiento de marca. Ayudo a empresas y agencias a conectar con su audiencia y acelerar su crecimiento.</p>
            <div class="hero-buttons">
                <a href="#proyectos" class="btn btn-primary">Ver mis proyectos →</a>
                <a href="#contacto" class="btn btn-secondary">Contáctame</a>
            </div>
            <p style="color: var(--dark-muted); font-size: 0.875rem;">↓ Scroll para conocer más</p>
        </div>
    </section>

    <!-- Experience Section -->
    <section id="experiencia">
        <div class="container">
            <h2>Experiencia</h2>
            <p>Mi recorrido en marketing digital y estrategia de marca</p>

            <div class="experience-list">
                <!-- Experience 1 -->
                <div class="experience-item section-item">
                    <div class="experience-timeline">
                        <div class="timeline-dot">1</div>
                        <div class="timeline-line"></div>
                    </div>
                    <div class="experience-card">
                        <div class="experience-header">
                            <div>
                                <div class="experience-company">Kia Futura</div>
                                <div class="experience-role">Practicante - Marketing Digital</div>
                            </div>
                            <div class="experience-year">2025</div>
                        </div>
                        <p class="experience-description">Estrategias de contenido digital para redes sociales. Análisis de métricas, edición audiovisual y organización de eventos.</p>
                        <div class="achievements">
                            <div class="achievements-label">Logros destacados:</div>
                            <ul class="achievements-list">
                                <li><span>✓</span> Incremento 45% engagement</li>
                                <li><span>✓</span> Evento "Mexi-Can Fest" coordinado</li>
                                <li><span>✓</span> 3.2K followers generados</li>
                            </ul>
                        </div>
                        <div class="tags">
                            <span class="tag">Social Media</span>
                            <span class="tag">Content Strategy</span>
                            <span class="tag">Analytics</span>
                            <span class="tag">Event Management</span>
                        </div>
                    </div>
                </div>

                <!-- Experience 2 -->
                <div class="experience-item section-item">
                    <div class="experience-timeline">
                        <div class="timeline-dot">2</div>
                        <div class="timeline-line"></div>
                    </div>
                    <div class="experience-card">
                        <div class="experience-header">
                            <div>
                                <div class="experience-company">Agencia 3CINCO</div>
                                <div class="experience-role">Publicista - Marketing & BTL</div>
                            </div>
                            <div class="experience-year">2023-2025</div>
                        </div>
                        <p class="experience-description">Diseño y ejecución de estrategias promocionales para empresas y franquicias. Activaciones de marca, marketing tradicional y digital.</p>
                        <div class="achievements">
                            <div class="achievements-label">Logros destacados:</div>
                            <ul class="achievements-list">
                                <li><span>✓</span> 15+ campañas ejecutadas</li>
                                <li><span>✓</span> Eventos: Caffenio, El Nido de los Águilas</li>
                                <li><span>✓</span> Alianzas con microempresas locales</li>
                            </ul>
                        </div>
                        <div class="tags">
                            <span class="tag">BTL</span>
                            <span class="tag">Event Marketing</span>
                            <span class="tag">Brand Activation</span>
                            <span class="tag">Digital Strategy</span>
                        </div>
                    </div>
                </div>

                <!-- Experience 3 -->
                <div class="experience-item section-item">
                    <div class="experience-timeline">
                        <div class="timeline-dot">3</div>
                    </div>
                    <div class="experience-card">
                        <div class="experience-header">
                            <div>
                                <div class="experience-company">Colaboraciones Múltiples</div>
                                <div class="experience-role">Content & Marketing Specialist</div>
                            </div>
                            <div class="experience-year">2023-2025</div>
                        </div>
                        <p class="experience-description">Trabajo con EXE Inmobiliaria, Agencia Musical Piagon, Venus Dentistry y DSC/Flujo Digital.</p>
                        <div class="achievements">
                            <div class="achievements-label">Logros destacados:</div>
                            <ul class="achievements-list">
                                <li><span>✓</span> 4 clientes diferentes</li>
                                <li><span>✓</span> Meta Ads campaigns</li>
                                <li><span>✓</span> Estrategias de posicionamiento</li>
                                <li><span>✓</span> Análisis de comportamiento digital</li>
                            </ul>
                        </div>
                        <div class="tags">
                            <span class="tag">Marketing Digital</span>
                            <span class="tag">Ads Management</span>
                            <span class="tag">Branding</span>
                            <span class="tag">Analytics</span>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Projects Section -->
    <section class="projects-bg" id="proyectos">
        <div class="container">
            <h2>Proyectos Destacados</h2>
            <p>Casos de estudio que demuestran mi expertise</p>

            <div class="filters">
                <button class="filter-btn active" onclick="filterProjects('all')">Todos</button>
                <button class="filter-btn" onclick="filterProjects('academic')">Académicos</button>
                <button class="filter-btn" onclick="filterProjects('professional')">Profesionales</button>
            </div>

            <div class="projects-grid" id="projectsGrid">
                <!-- Projects will be inserted here by JavaScript -->
            </div>

            <div class="gallery-placeholder">
                <div class="gallery-emoji">🎨</div>
                <h4>Galería Visual</h4>
                <p>Pronto: Capturas de campañas reales, diseños y resultados de analytics</p>
                <p style="color: var(--dark-muted); font-size: 0.875rem;">Integrando contenido del Drive...</p>
            </div>
        </div>
    </section>

    <!-- Skills Section -->
    <section id="habilidades">
        <div class="container">
            <h2>Habilidades</h2>
            <p>Competencias verificadas y certificadas</p>

            <div class="skills-grid" id="skillsGrid">
                <!-- Skills will be inserted here by JavaScript -->
            </div>
        </div>
    </section>

    <!-- Certifications Section -->
    <section class="cert-bg">
        <div class="container">
            <h2>Certificaciones</h2>
            <p>Formación continua y especialización profesional</p>

            <div class="certifications-grid" id="certificationsGrid">
                <!-- Certifications will be inserted here by JavaScript -->
            </div>
        </div>
    </section>

    <!-- Contact Section -->
    <section id="contacto">
        <div class="contact-content">
            <h2>¿Hablamos?</h2>
            <p class="contact-description">Estoy abierto a oportunidades en agencias, empresas y proyectos especiales. Conectemos.</p>
            
            <div class="contact-buttons">
                <a href="mailto:jossueramon12@gmail.com" class="btn btn-primary">
                    ✉️ Envía un email
                </a>
                <a href="https://www.linkedin.com/in/jossue-ramon-martinez-espinoza-b56731385" target="_blank" rel="noopener noreferrer" class="btn btn-secondary">
                    🔗 LinkedIn
                </a>
            </div>

            <div class="contact-grid">
                <div class="contact-card">
                    <p>📞 Teléfono</p>
                    <strong>(686) 511-0497</strong>
                </div>
                <div class="contact-card">
                    <p>📧 Email</p>
                    <strong>jossueramon12@gmail.com</strong>
                </div>
            </div>
        </div>
    </section>

    <!-- Download CV Section -->
    <section class="download-section">
        <div class="container">
            <div class="download-content">
                <div class="download-text">
                    <h4>Descarga mi CV completo</h4>
                    <p>Disponible en PDF con historial detallado</p>
                </div>
                <a href="#" class="btn btn-primary" onclick="downloadCV()">
                    ⬇️ Descargar CV
                </a>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer>
        <div class="footer-container">
            <div class="footer-top">
                <div class="footer-brand">
                    <h3>Ramón Espinoza</h3>
                    <p>Marketing Digital | Estrategia de Marca | Growth</p>
                </div>
                <div class="footer-links">
                    <a href="https://www.linkedin.com/in/jossue-ramon-martinez-espinoza-b56731385" target="_blank" rel="noopener noreferrer" title="LinkedIn">🔗</a>
                    <a href="mailto:jossueramon12@gmail.com" title="Email">✉️</a>
                </div>
            </div>

            <div class="footer-bottom">
                <p>© 2026 Ramón Espinoza. Diseño web moderno y responsive. Basado en estrategia digital.<br>
                Disponible para agencias y oportunidades de crecimiento.</p>
            </div>
        </div>
    </footer>

    <script>
        // Data
        const projectsData = [
            {
                id: 1,
                title: 'Bean Plant Based Food',
                type: 'Investigación de Mercado',
                category: 'academic',
                emoji: '📊',
                description: 'Estudio completo de segmentación y perfil del consumidor para restaurante vegano en Mexicali.',
                results: [
                    'Definición clara del perfil demográfico (21-35 años, 70% mujeres)',
                    'Identificación de motivaciones principales (salud, ética animal)',
                    'Recomendaciones estratégicas para posicionamiento'
                ],
                tools: ['Market Research', 'Data Analysis', 'Consumer Insights']
            },
            {
                id: 2,
                title: 'Huellitas Mxcl',
                type: 'Análisis Estratégico & Makeover',
                category: 'academic',
                emoji: '🐾',
                description: 'Investigación y propuesta de transformación de comunicación para refugio de animales con modelo de negocio social.',
                results: [
                    'Estrategia de sostenibilidad económica identificada',
                    'Propuesta de servicios generadores de ingresos (hotel canino)',
                    'Plan integral de comunicación digital'
                ],
                tools: ['Strategic Analysis', 'Business Model', 'Social Media Strategy']
            },
            {
                id: 3,
                title: 'Kia Futura - Content Strategy',
                type: 'Estrategia de Contenido Digital',
                category: 'professional',
                emoji: '🎬',
                description: 'Desarrollo de calendarios de contenido, edición audiovisual y análisis de desempeño en redes sociales.',
                results: [
                    'Calendario de contenido trimestral',
                    'Análisis de engagement y CTR',
                    'Reportes de desempeño mensual'
                ],
                tools: ['Content Planning', 'Video Editing', 'Analytics']
            },
            {
                id: 4,
                title: 'Agencia 3CINCO - Activaciones',
                type: 'Estrategia de Activación de Marca',
                category: 'professional',
                emoji: '🎯',
                description: 'Ejecución de campañas promocionales y activaciones para múltiples empresas y franquicias.',
                results: [
                    '15+ activaciones diseñadas',
                    'Gestión logística integral',
                    'Impacto en visibilidad de marca'
                ],
                tools: ['Event Planning', 'Brand Activation', 'Marketing Execution']
            }
        ];

        const skillsData = {
            'Marketing Digital': ['SEO/SEM', 'Social Media Management', 'Content Strategy', 'Email Marketing', 'Analytics'],
            'Estrategia': ['Posicionamiento de marca', 'Investigación de mercado', 'Consumer Insights', 'Business Strategy', 'Propuestas de valor'],
            'Herramientas': ['Meta Ads', 'Google Analytics', 'Canva', 'CapCut', 'Adobe Básico', 'Excel Avanzado', 'HubSpot'],
            'Soft Skills': ['Análisis crítico', 'Comunicación profesional', 'Gestión de proyectos', 'Trabajo en equipo', 'Resolución de problemas']
        };

        const certificationsData = [
            {
                title: 'Marketing Digital',
                issuer: 'HubSpot Academy',
                date: 'Completado Mayo 2025',
                emoji: '📧',
                badge: 'Verificado'
            },
            {
                title: 'El Camino del Inversor: Método, Fundamentos de Inversión y Riesgo',
                issuer: 'Santander Open Academy',
                date: 'Completado 2025',
                emoji: '💰',
                badge: 'Verificado'
            },
            {
                title: 'Excel Avanzado',
                issuer: 'Santander Open Academy',
                date: 'Completado Junio 2026',
                emoji: '📊',
                badge: 'Nuevo'
            },
            {
                title: 'Inglés Técnico',
                issuer: 'Facultad de Idiomas UABC',
                date: 'Completado',
                emoji: '🌐',
                badge: 'Egresado'
            }
        ];

        // Initialize
        document.addEventListener('DOMContentLoaded', () => {
            renderProjects('all');
            renderSkills();
            renderCertifications();
            setupScrollAnimations();
            setupTheme();
        });

        // Functions
        function toggleTheme() {
            document.body.classList.toggle('light-mode');
            const isDark = !document.body.classList.contains('light-mode');
            localStorage.setItem('theme', isDark ? 'dark' : 'light');
        }

        function setupTheme() {
            const savedTheme = localStorage.getItem('theme');
            if (savedTheme === 'light') {
                document.body.classList.add('light-mode');
                document.querySelector('.theme-toggle').textContent = '🌙';
            }
        }

        function toggleMenu() {
            // Mobile menu functionality can be added here
        }

        function filterProjects(category) {
            renderProjects(category);
            document.querySelectorAll('.filter-btn').forEach(btn => {
                btn.classList.remove('active');
            });
            event.target.classList.add('active');
        }

        function renderProjects(category) {
            const grid = document.getElementById('projectsGrid');
            const filtered = category === 'all' 
                ? projectsData 
                : projectsData.filter(p => p.category === category);

            grid.innerHTML = filtered.map(project => `
                <div class="project-card">
                    <div class="project-emoji">${project.emoji}</div>
                    <div class="project-type">${project.type}</div>
                    <h3>${project.title}</h3>
                    <p class="project-description">${project.description}</p>
                    <div class="project-results">
                        <div class="project-results-label">Resultados:</div>
                        <ul class="project-results-list">
                            ${project.results.map(r => `<li><span>→</span> ${r}</li>`).join('')}
                        </ul>
                    </div>
                    <div class="project-tools">
                        ${project.tools.map(tool => `<span class="tool-tag">${tool}</span>`).join('')}
                    </div>
                </div>
            `).join('');
        }

        function renderSkills() {
            const grid = document.getElementById('skillsGrid');
            grid.innerHTML = Object.entries(skillsData).map(([category, skills]) => `
                <div class="skill-category">
                    <h3>${category}</h3>
                    ${skills.map((skill, idx) => {
                        const width = 75 + Math.random() * 25;
                        return `
                            <div class="skill-item">
                                <div class="skill-name">${skill}</div>
                                <div class="skill-bar">
                                    <div class="skill-fill" style="--skill-width: ${width}%"></div>
                                </div>
                            </div>
                        `;
                    }).join('')}
                </div>
            `).join('');
        }

        function renderCertifications() {
            const grid = document.getElementById('certificationsGrid');
            grid.innerHTML = certificationsData.map(cert => `
                <div class="cert-card">
                    <div class="cert-header">
                        <span class="cert-emoji">${cert.emoji}</span>
                        <span class="cert-badge">${cert.badge}</span>
                    </div>
                    <h4 class="cert-title">${cert.title}</h4>
                    <p class="cert-issuer">${cert.issuer}</p>
                    <p class="cert-date">${cert.date}</p>
                </div>
            `).join('');
        }

        function setupScrollAnimations() {
            const observer = new IntersectionObserver(entries => {
                entries.forEach(entry => {
                    if (entry.isIntersecting) {
                        entry.target.classList.add('revealed');
                    }
                });
            }, { threshold: 0.1 });

            document.querySelectorAll('.experience-item, .project-card, .skill-category, .cert-card').forEach(el => {
                el.classList.add('scroll-reveal');
                observer.observe(el);
            });
        }

        function downloadCV() {
            alert('El CV estará disponible pronto. Por ahora, puedes contactarme directamente en jossueramon12@gmail.com');
        }
    </script>
</body>
</html>
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Ramón Espinoza - Marketing Digital & Estrategia de Marca</title>
    <meta name="description" content="Portafolio profesional de Ramón Espinoza. Especialista en marketing digital, estrategia de contenidos y posicionamiento de marca.">
    <meta name="keywords" content="marketing digital, estrategia de marca, social media, contenidos, Mexicali">
    <meta name="author" content="Ramón Espinoza">
    <meta property="og:title" content="Ramón Espinoza - Marketing Digital">
    <meta property="og:description" content="Transformo marcas en resultados. Especialista en estrategia digital y marketing de contenidos.">
    <meta property="og:type" content="website">
    
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        :root {
            --mint: #10B981;
            --purple: #A855F7;
            --cyan: #06B6D4;
            --dark-bg: #0F172A;
            --dark-secondary: #1E293B;
            --dark-text: #F8FAFC;
            --dark-muted: #CBD5E1;
            
            --light-bg: #F8FAFC;
            --light-secondary: #F1F5F9;
            --light-text: #0F172A;
            --light-muted: #64748B;
        }

        body {
            font-family: 'Inter', -apple-system, BlinkMacSystemFont, 'Segoe UI', sans-serif;
            background-color: var(--dark-bg);
            color: var(--dark-text);
            transition: background-color 0.3s ease, color 0.3s ease;
            line-height: 1.6;
        }

        body.light-mode {
            background-color: var(--light-bg);
            color: var(--light-text);
        }

        /* Scrollbar Styling */
        ::-webkit-scrollbar {
            width: 8px;
        }

        ::-webkit-scrollbar-track {
            background: var(--dark-secondary);
        }

        ::-webkit-scrollbar-thumb {
            background: var(--mint);
            border-radius: 4px;
        }

        body.light-mode::-webkit-scrollbar-track {
            background: var(--light-secondary);
        }

        /* Navbar */
        nav {
            position: fixed;
            top: 0;
            width: 100%;
            z-index: 50;
            backdrop-filter: blur(10px);
            border-bottom: 1px solid rgba(16, 185, 129, 0.1);
            background-color: rgba(15, 23, 42, 0.8);
            transition: all 0.3s ease;
        }

        body.light-mode nav {
            background-color: rgba(248, 250, 252, 0.8);
            border-bottom: 1px solid rgba(16, 185, 129, 0.1);
        }

        nav .container {
            max-width: 1280px;
            margin: 0 auto;
            padding: 0 1rem;
            display: flex;
            justify-content: space-between;
            align-items: center;
            height: 64px;
        }

        .logo {
            font-size: 24px;
            font-weight: bold;
            background: linear-gradient(135deg, #06B6D4, #A855F7);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
        }

        nav .nav-links {
            display: none;
            gap: 2rem;
            align-items: center;
        }

        nav .nav-links a {
            color: var(--dark-muted);
            text-decoration: none;
            font-size: 0.875rem;
            font-weight: 500;
            transition: color 0.3s;
        }

        body.light-mode nav .nav-links a {
            color: var(--light-muted);
        }

        nav .nav-links a:hover {
            color: var(--mint);
        }

        .theme-toggle {
            background-color: var(--dark-secondary);
            color: var(--mint);
            border: none;
            padding: 0.5rem;
            border-radius: 0.5rem;
            cursor: pointer;
            font-size: 1rem;
            transition: transform 0.3s;
        }

        body.light-mode .theme-toggle {
            background-color: var(--light-secondary);
        }

        .theme-toggle:hover {
            transform: scale(1.1);
        }

        .mobile-menu {
            display: flex;
            gap: 1rem;
            align-items: center;
        }

        .menu-toggle {
            background: none;
            border: none;
            color: var(--dark-text);
            font-size: 1.5rem;
            cursor: pointer;
            display: none;
        }

        body.light-mode .menu-toggle {
            color: var(--light-text);
        }

        /* Responsive Navbar */
        @media (min-width: 768px) {
            nav .nav-links {
                display: flex;
            }
            .menu-toggle {
                display: none !important;
            }
        }

        @media (max-width: 767px) {
            .menu-toggle {
                display: block;
            }
        }

        /* Hero Section */
        .hero {
            min-height: 100vh;
            display: flex;
            align-items: center;
            justify-content: center;
            padding: 2rem 1rem;
            padding-top: 5rem;
            position: relative;
            overflow: hidden;
        }

        .hero::before {
            content: '';
            position: absolute;
            width: 400px;
            height: 400px;
            background: radial-gradient(circle at 20% 50%, rgba(16, 185, 129, 0.15), transparent 50%);
            border-radius: 50%;
            filter: blur(48px);
            left: 0;
            top: 20%;
        }

        .hero::after {
            content: '';
            position: absolute;
            width: 400px;
            height: 400px;
            background: radial-gradient(circle at 80% 80%, rgba(168, 85, 247, 0.15), transparent 50%);
            border-radius: 50%;
            filter: blur(48px);
            right: 0;
            bottom: 0;
        }

        .hero-content {
            max-width: 56rem;
            text-align: center;
            position: relative;
            z-index: 10;
            animation: fadeInUp 0.8s ease-out;
        }

        @keyframes fadeInUp {
            from {
                opacity: 0;
                transform: translateY(30px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        .hero-badge {
            display: inline-block;
            background-color: var(--mint);
            color: var(--dark-bg);
            font-size: 0.75rem;
            font-weight: 600;
            padding: 0.5rem 1rem;
            border-radius: 2rem;
            margin-bottom: 1.5rem;
        }

        .hero h1 {
            font-size: clamp(2.5rem, 8vw, 3.5rem);
            font-weight: 800;
            margin-bottom: 1.5rem;
            line-height: 1.2;
        }

        .hero h1 .mint {
            color: var(--mint);
        }

        .hero h1 .purple {
            color: var(--purple);
        }

        .hero p {
            font-size: 1.125rem;
            color: var(--dark-muted);
            margin-bottom: 2rem;
            max-width: 32rem;
            margin-left: auto;
            margin-right: auto;
        }

        body.light-mode .hero p {
            color: var(--light-muted);
        }

        .hero-buttons {
            display: flex;
            flex-direction: column;
            gap: 1rem;
            justify-content: center;
            margin-bottom: 3rem;
        }

        @media (min-width: 640px) {
            .hero-buttons {
                flex-direction: row;
            }
        }

        .btn {
            padding: 0.75rem 2rem;
            border-radius: 0.5rem;
            font-weight: 600;
            border: none;
            cursor: pointer;
            text-decoration: none;
            display: inline-flex;
            align-items: center;
            gap: 0.5rem;
            justify-content: center;
            transition: transform 0.3s, box-shadow 0.3s;
        }

        .btn:hover {
            transform: scale(1.05);
        }

        .btn-primary {
            background-color: var(--mint);
            color: var(--dark-bg);
        }

        .btn-secondary {
            border: 2px solid var(--mint);
            color: var(--mint);
            background-color: transparent;
        }

        /* Sections */
        section {
            padding: 5rem 1rem;
        }

        .container {
            max-width: 1280px;
            margin: 0 auto;
        }

        section h2 {
            font-size: clamp(2rem, 5vw, 3rem);
            font-weight: 800;
            margin-bottom: 1rem;
        }

        section > .container > p {
            font-size: 1.125rem;
            color: var(--dark-muted);
            margin-bottom: 4rem;
        }

        body.light-mode section > .container > p {
            color: var(--light-muted);
        }

        /* Timeline */
        .experience-list {
            display: space-y-12;
        }

        .experience-item {
            display: flex;
            gap: 1.5rem;
            margin-bottom: 3rem;
        }

        .experience-timeline {
            display: flex;
            flex-direction: column;
            align-items: center;
        }

        .timeline-dot {
            width: 48px;
            height: 48px;
            background-color: var(--mint);
            color: var(--dark-bg);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-weight: bold;
            font-size: 1.125rem;
        }

        .timeline-line {
            width: 4px;
            height: 96px;
            background-color: var(--mint);
            margin-top: 1rem;
            opacity: 0.3;
        }

        .experience-card {
            flex: 1;
            background-color: var(--dark-secondary);
            padding: 1.5rem;
            border-radius: 0.75rem;
            border: 1px solid rgba(16, 185, 129, 0.25);
            transition: transform 0.3s;
        }

        body.light-mode .experience-card {
            background-color: var(--light-secondary);
        }

        .experience-card:hover {
            transform: scale(1.02);
        }

        .experience-header {
            display: flex;
            justify-content: space-between;
            align-items: flex-start;
            margin-bottom: 1rem;
            flex-wrap: wrap;
            gap: 1rem;
        }

        .experience-company {
            font-size: 1.25rem;
            font-weight: bold;
        }

        .experience-role {
            color: var(--mint);
            font-weight: 600;
            font-size: 0.875rem;
            margin-top: 0.25rem;
        }

        .experience-year {
            color: var(--dark-muted);
            font-size: 0.875rem;
        }

        body.light-mode .experience-year {
            color: var(--light-muted);
        }

        .experience-description {
            color: var(--dark-muted);
            margin-bottom: 1rem;
        }

        body.light-mode .experience-description {
            color: var(--light-muted);
        }

        .achievements {
            margin-bottom: 1rem;
        }

        .achievements-label {
            color: var(--dark-muted);
            font-size: 0.875rem;
            font-weight: 600;
            margin-bottom: 0.5rem;
        }

        body.light-mode .achievements-label {
            color: var(--light-muted);
        }

        .achievements-list {
            list-style: none;
        }

        .achievements-list li {
            color: var(--dark-muted);
            font-size: 0.875rem;
            display: flex;
            align-items: center;
            gap: 0.5rem;
            margin-bottom: 0.25rem;
        }

        body.light-mode .achievements-list li {
            color: var(--light-muted);
        }

        .achievements-list span {
            color: var(--mint);
        }

        .tags {
            display: flex;
            flex-wrap: wrap;
            gap: 0.5rem;
        }

        .tag {
            background-color: rgba(16, 185, 129, 0.2);
            color: var(--mint);
            font-size: 0.75rem;
            padding: 0.25rem 0.75rem;
            border-radius: 9999px;
            font-weight: 500;
        }

        /* Projects Section */
        .projects-bg {
            background-color: var(--dark-secondary);
        }

        body.light-mode .projects-bg {
            background-color: var(--light-secondary);
        }

        .filters {
            display: flex;
            gap: 0.75rem;
            margin-bottom: 3rem;
            flex-wrap: wrap;
        }

        .filter-btn {
            background-color: var(--dark-secondary);
            color: var(--dark-text);
            border: 2px solid var(--mint);
            padding: 0.5rem 1.5rem;
            border-radius: 0.5rem;
            font-weight: 600;
            cursor: pointer;
            transition: all 0.3s;
        }

        body.light-mode .filter-btn {
            background-color: var(--light-secondary);
            color: var(--light-text);
        }

        .filter-btn.active {
            background-color: var(--mint);
            color: var(--dark-bg);
        }

        .filter-btn:hover {
            transform: scale(1.05);
        }

        .projects-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(320px, 1fr));
            gap: 1.5rem;
            margin-bottom: 3rem;
        }

        .project-card {
            background-color: var(--dark-bg);
            padding: 2rem;
            border-radius: 0.75rem;
            border: 1px solid rgba(16, 185, 129, 0.3);
            transition: transform 0.3s, border-color 0.3s;
        }

        body.light-mode .project-card {
            background-color: var(--light-bg);
        }

        .project-card:hover {
            transform: scale(1.05);
            border-color: var(--mint);
        }

        .project-emoji {
            font-size: 3rem;
            margin-bottom: 1rem;
        }

        .project-type {
            background-color: rgba(16, 185, 129, 0.2);
            color: var(--mint);
            font-size: 0.75rem;
            font-weight: 600;
            padding: 0.25rem 0.75rem;
            border-radius: 2rem;
            display: inline-block;
            margin-bottom: 1rem;
        }

        .project-card h3 {
            font-size: 1.5rem;
            margin-bottom: 0.5rem;
        }

        .project-description {
            color: var(--dark-muted);
            margin-bottom: 1.5rem;
        }

        body.light-mode .project-description {
            color: var(--light-muted);
        }

        .project-results {
            margin-bottom: 1.5rem;
        }

        .project-results-label {
            color: var(--dark-muted);
            font-size: 0.875rem;
            font-weight: 600;
            margin-bottom: 0.75rem;
        }

        body.light-mode .project-results-label {
            color: var(--light-muted);
        }

        .project-results-list {
            list-style: none;
        }

        .project-results-list li {
            color: var(--dark-muted);
            font-size: 0.875rem;
            display: flex;
            gap: 0.5rem;
            margin-bottom: 0.5rem;
        }

        body.light-mode .project-results-list li {
            color: var(--light-muted);
        }

        .project-results-list span {
            color: var(--mint);
            flex-shrink: 0;
        }

        .project-tools {
            display: flex;
            flex-wrap: wrap;
            gap: 0.5rem;
        }

        .tool-tag {
            background-color: rgba(168, 85, 247, 0.2);
            color: var(--purple);
            font-size: 0.75rem;
            padding: 0.25rem 0.5rem;
            border-radius: 0.25rem;
            font-weight: 500;
        }

        /* Gallery Placeholder */
        .gallery-placeholder {
            background-color: var(--dark-bg);
            border: 2px dashed rgba(16, 185, 129, 0.3);
            border-radius: 0.75rem;
            padding: 4rem 1rem;
            text-align: center;
            margin-top: 3rem;
        }

        body.light-mode .gallery-placeholder {
            background-color: var(--light-bg);
        }

        .gallery-placeholder p {
            margin-bottom: 1rem;
        }

        .gallery-emoji {
            font-size: 3rem;
            margin-bottom: 1rem;
        }

        /* Skills Section */
        .skills-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 2rem;
        }

        .skill-category {
            background-color: var(--dark-secondary);
            padding: 2rem;
            border-radius: 0.75rem;
            border: 1px solid rgba(16, 185, 129, 0.4);
        }

        body.light-mode .skill-category {
            background-color: var(--light-secondary);
        }

        .skill-category h3 {
            color: var(--mint);
            font-size: 1.125rem;
            font-weight: bold;
            margin-bottom: 1.5rem;
        }

        .skill-item {
            margin-bottom: 1.5rem;
        }

        .skill-name {
            display: flex;
            justify-content: space-between;
            margin-bottom: 0.5rem;
        }

        .skill-bar {
            height: 8px;
            background-color: rgba(16, 185, 129, 0.2);
            border-radius: 9999px;
            overflow: hidden;
        }

        .skill-fill {
            height: 100%;
            background-color: var(--mint);
            border-radius: 9999px;
            animation: fillBar 1.5s ease-out forwards;
        }

        @keyframes fillBar {
            from {
                width: 0;
            }
            to {
                width: var(--skill-width);
            }
        }

        /* Certifications */
        .cert-bg {
            background-color: var(--dark-secondary);
        }

        body.light-mode .cert-bg {
            background-color: var(--light-secondary);
        }

        .certifications-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 1.5rem;
        }

        .cert-card {
            background-color: var(--dark-bg);
            padding: 1.5rem;
            border-radius: 0.75rem;
            border: 1px solid rgba(16, 185, 129, 0.3);
            transition: transform 0.3s;
        }

        body.light-mode .cert-card {
            background-color: var(--light-bg);
        }

        .cert-card:hover {
            transform: scale(1.05);
        }

        .cert-header {
            display: flex;
            justify-content: space-between;
            align-items: flex-start;
            margin-bottom: 1rem;
        }

        .cert-emoji {
            font-size: 2.5rem;
        }

        .cert-badge {
            background-color: rgba(16, 185, 129, 0.2);
            color: var(--mint);
            font-size: 0.75rem;
            font-weight: bold;
            padding: 0.25rem 0.75rem;
            border-radius: 2rem;
        }

        .cert-title {
            font-weight: bold;
            margin-bottom: 0.5rem;
        }

        .cert-issuer {
            color: var(--mint);
            font-size: 0.875rem;
            font-weight: 600;
            margin-bottom: 0.5rem;
        }

        .cert-date {
            color: var(--dark-muted);
            font-size: 0.875rem;
        }

        body.light-mode .cert-date {
            color: var(--light-muted);
        }

        /* Contact Section */
        .contact-content {
            max-width: 48rem;
            margin: 0 auto;
            text-align: center;
        }

        .contact-content h2 {
            margin-bottom: 1.5rem;
        }

        .contact-description {
            font-size: 1.125rem;
            color: var(--dark-muted);
            margin-bottom: 3rem;
        }

        body.light-mode .contact-description {
            color: var(--light-muted);
        }

        .contact-buttons {
            display: flex;
            flex-direction: column;
            gap: 1rem;
            justify-content: center;
            margin-bottom: 3rem;
        }

        @media (min-width: 640px) {
            .contact-buttons {
                flex-direction: row;
            }
        }

        .contact-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 1rem;
        }

        .contact-card {
            background-color: var(--dark-secondary);
            padding: 1.5rem;
            border-radius: 0.5rem;
        }

        body.light-mode .contact-card {
            background-color: var(--light-secondary);
        }

        .contact-card p:first-child {
            color: var(--dark-muted);
            font-size: 0.875rem;
            margin-bottom: 0.5rem;
        }

        body.light-mode .contact-card p:first-child {
            color: var(--light-muted);
        }

        /* Download CV Section */
        .download-section {
            background-color: var(--dark-secondary);
            border-top: 1px solid rgba(16, 185, 129, 0.4);
            padding: 4rem 1rem;
        }

        body.light-mode .download-section {
            background-color: var(--light-secondary);
            border-top: 1px solid rgba(16, 185, 129, 0.2);
        }

        .download-content {
            max-width: 48rem;
            margin: 0 auto;
            display: flex;
            flex-direction: column;
            align-items: center;
            gap: 1.5rem;
            text-align: center;
        }

        @media (min-width: 640px) {
            .download-content {
                flex-direction: row;
                text-align: left;
            }
        }

        .download-text h4 {
            font-weight: bold;
            margin-bottom: 0.5rem;
        }

        .download-text p {
            color: var(--dark-muted);
            font-size: 0.875rem;
        }

        body.light-mode .download-text p {
            color: var(--light-muted);
        }

        /* Footer */
        footer {
            background-color: var(--dark-secondary);
            border-top: 1px solid rgba(16, 185, 129, 0.3);
            padding: 3rem 1rem;
        }

        body.light-mode footer {
            background-color: var(--light-secondary);
        }

        .footer-container {
            max-width: 1280px;
            margin: 0 auto;
        }

        .footer-top {
            display: flex;
            flex-direction: column;
            justify-content: space-between;
            align-items: center;
            gap: 2rem;
            margin-bottom: 2rem;
        }

        @media (min-width: 768px) {
            .footer-top {
                flex-direction: row;
            }
        }

        .footer-brand h3 {
            font-size: 1.5rem;
            font-weight: bold;
            margin-bottom: 0.5rem;
        }

        .footer-brand p {
            color: var(--dark-muted);
            font-size: 0.875rem;
        }

        body.light-mode .footer-brand p {
            color: var(--light-muted);
        }

        .footer-links {
            display: flex;
            gap: 1rem;
        }

        .footer-links a {
            color: var(--mint);
            text-decoration: none;
            font-size: 1.5rem;
            transition: transform 0.3s;
        }

        .footer-links a:hover {
            transform: scale(1.25);
        }

        .footer-bottom {
            border-top: 1px solid rgba(16, 185, 129, 0.2);
            padding-top: 2rem;
            text-align: center;
        }

        .footer-bottom p {
            color: var(--dark-muted);
            font-size: 0.875rem;
            line-height: 1.6;
        }

        body.light-mode .footer-bottom p {
            color: var(--light-muted);
        }

        /* Smooth Scroll */
        html {
            scroll-behavior: smooth;
        }

        /* Mobile Responsive */
        @media (max-width: 640px) {
            section {
                padding: 3rem 1rem;
            }

            .hero {
                padding-top: 4rem;
                padding-bottom: 2rem;
            }

            .hero h1 {
                font-size: 1.875rem;
            }

            .experience-item {
                gap: 1rem;
            }

            .projects-grid {
                grid-template-columns: 1fr;
            }

            .skills-grid {
                grid-template-columns: 1fr;
            }

            .certifications-grid {
                grid-template-columns: 1fr;
            }

            .contact-grid {
                grid-template-columns: 1fr;
            }

            .footer-top {
                flex-direction: column-reverse;
            }
        }

        /* Animations */
        @keyframes slideIn {
            from {
                opacity: 0;
                transform: translateX(-20px);
            }
            to {
                opacity: 1;
                transform: translateX(0);
            }
        }

        .section-item {
            animation: slideIn 0.6s ease-out forwards;
        }

        .scroll-reveal {
            opacity: 0;
            transform: translateY(30px);
            transition: opacity 0.6s ease-out, transform 0.6s ease-out;
        }

        .scroll-reveal.revealed {
            opacity: 1;
            transform: translateY(0);
        }
    </style>
</head>
<body>
    <!-- Navbar -->
    <nav>
        <div class="container">
            <div class="logo">Ramón.</div>
            <div class="nav-links">
                <a href="#inicio">Inicio</a>
                <a href="#experiencia">Experiencia</a>
                <a href="#proyectos">Proyectos</a>
                <a href="#contacto">Contacto</a>
            </div>
            <div class="mobile-menu">
                <button class="theme-toggle" onclick="toggleTheme()">☀️</button>
                <button class="menu-toggle" onclick="toggleMenu()">☰</button>
            </div>
        </div>
    </nav>

    <!-- Hero Section -->
    <section class="hero" id="inicio">
        <div class="hero-content">
            <div class="hero-badge">📍 Mexicali, Baja California</div>
            <h1>Transformo <span class="mint">marcas</span> en <span class="purple">resultados</span></h1>
            <p>Especialista en estrategia digital, marketing de contenidos y posicionamiento de marca. Ayudo a empresas y agencias a conectar con su audiencia y acelerar su crecimiento.</p>
            <div class="hero-buttons">
                <a href="#proyectos" class="btn btn-primary">Ver mis proyectos →</a>
                <a href="#contacto" class="btn btn-secondary">Contáctame</a>
            </div>
            <p style="color: var(--dark-muted); font-size: 0.875rem;">↓ Scroll para conocer más</p>
        </div>
    </section>

    <!-- Experience Section -->
    <section id="experiencia">
        <div class="container">
            <h2>Experiencia</h2>
            <p>Mi recorrido en marketing digital y estrategia de marca</p>

            <div class="experience-list">
                <!-- Experience 1 -->
                <div class="experience-item section-item">
                    <div class="experience-timeline">
                        <div class="timeline-dot">1</div>
                        <div class="timeline-line"></div>
                    </div>
                    <div class="experience-card">
                        <div class="experience-header">
                            <div>
                                <div class="experience-company">Kia Futura</div>
                                <div class="experience-role">Practicante - Marketing Digital</div>
                            </div>
                            <div class="experience-year">2025</div>
                        </div>
                        <p class="experience-description">Estrategias de contenido digital para redes sociales. Análisis de métricas, edición audiovisual y organización de eventos.</p>
                        <div class="achievements">
                            <div class="achievements-label">Logros destacados:</div>
                            <ul class="achievements-list">
                                <li><span>✓</span> Incremento 45% engagement</li>
                                <li><span>✓</span> Evento "Mexi-Can Fest" coordinado</li>
                                <li><span>✓</span> 3.2K followers generados</li>
                            </ul>
                        </div>
                        <div class="tags">
                            <span class="tag">Social Media</span>
                            <span class="tag">Content Strategy</span>
                            <span class="tag">Analytics</span>
                            <span class="tag">Event Management</span>
                        </div>
                    </div>
                </div>

                <!-- Experience 2 -->
                <div class="experience-item section-item">
                    <div class="experience-timeline">
                        <div class="timeline-dot">2</div>
                        <div class="timeline-line"></div>
                    </div>
                    <div class="experience-card">
                        <div class="experience-header">
                            <div>
                                <div class="experience-company">Agencia 3CINCO</div>
                                <div class="experience-role">Publicista - Marketing & BTL</div>
                            </div>
                            <div class="experience-year">2023-2025</div>
                        </div>
                        <p class="experience-description">Diseño y ejecución de estrategias promocionales para empresas y franquicias. Activaciones de marca, marketing tradicional y digital.</p>
                        <div class="achievements">
                            <div class="achievements-label">Logros destacados:</div>
                            <ul class="achievements-list">
                                <li><span>✓</span> 15+ campañas ejecutadas</li>
                                <li><span>✓</span> Eventos: Caffenio, El Nido de los Águilas</li>
                                <li><span>✓</span> Alianzas con microempresas locales</li>
                            </ul>
                        </div>
                        <div class="tags">
                            <span class="tag">BTL</span>
                            <span class="tag">Event Marketing</span>
                            <span class="tag">Brand Activation</span>
                            <span class="tag">Digital Strategy</span>
                        </div>
                    </div>
                </div>

                <!-- Experience 3 -->
                <div class="experience-item section-item">
                    <div class="experience-timeline">
                        <div class="timeline-dot">3</div>
                    </div>
                    <div class="experience-card">
                        <div class="experience-header">
                            <div>
                                <div class="experience-company">Colaboraciones Múltiples</div>
                                <div class="experience-role">Content & Marketing Specialist</div>
                            </div>
                            <div class="experience-year">2023-2025</div>
                        </div>
                        <p class="experience-description">Trabajo con EXE Inmobiliaria, Agencia Musical Piagon, Venus Dentistry y DSC/Flujo Digital.</p>
                        <div class="achievements">
                            <div class="achievements-label">Logros destacados:</div>
                            <ul class="achievements-list">
                                <li><span>✓</span> 4 clientes diferentes</li>
                                <li><span>✓</span> Meta Ads campaigns</li>
                                <li><span>✓</span> Estrategias de posicionamiento</li>
                                <li><span>✓</span> Análisis de comportamiento digital</li>
                            </ul>
                        </div>
                        <div class="tags">
                            <span class="tag">Marketing Digital</span>
                            <span class="tag">Ads Management</span>
                            <span class="tag">Branding</span>
                            <span class="tag">Analytics</span>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Projects Section -->
    <section class="projects-bg" id="proyectos">
        <div class="container">
            <h2>Proyectos Destacados</h2>
            <p>Casos de estudio que demuestran mi expertise</p>

            <div class="filters">
                <button class="filter-btn active" onclick="filterProjects('all')">Todos</button>
                <button class="filter-btn" onclick="filterProjects('academic')">Académicos</button>
                <button class="filter-btn" onclick="filterProjects('professional')">Profesionales</button>
            </div>

            <div class="projects-grid" id="projectsGrid">
                <!-- Projects will be inserted here by JavaScript -->
            </div>

            <div class="gallery-placeholder">
                <div class="gallery-emoji">🎨</div>
                <h4>Galería Visual</h4>
                <p>Pronto: Capturas de campañas reales, diseños y resultados de analytics</p>
                <p style="color: var(--dark-muted); font-size: 0.875rem;">Integrando contenido del Drive...</p>
            </div>
        </div>
    </section>

    <!-- Skills Section -->
    <section id="habilidades">
        <div class="container">
            <h2>Habilidades</h2>
            <p>Competencias verificadas y certificadas</p>

            <div class="skills-grid" id="skillsGrid">
                <!-- Skills will be inserted here by JavaScript -->
            </div>
        </div>
    </section>

    <!-- Certifications Section -->
    <section class="cert-bg">
        <div class="container">
            <h2>Certificaciones</h2>
            <p>Formación continua y especialización profesional</p>

            <div class="certifications-grid" id="certificationsGrid">
                <!-- Certifications will be inserted here by JavaScript -->
            </div>
        </div>
    </section>

    <!-- Contact Section -->
    <section id="contacto">
        <div class="contact-content">
            <h2>¿Hablamos?</h2>
            <p class="contact-description">Estoy abierto a oportunidades en agencias, empresas y proyectos especiales. Conectemos.</p>
            
            <div class="contact-buttons">
                <a href="mailto:jossueramon12@gmail.com" class="btn btn-primary">
                    ✉️ Envía un email
                </a>
                <a href="https://www.linkedin.com/in/jossue-ramon-martinez-espinoza-b56731385" target="_blank" rel="noopener noreferrer" class="btn btn-secondary">
                    🔗 LinkedIn
                </a>
            </div>

            <div class="contact-grid">
                <div class="contact-card">
                    <p>📞 Teléfono</p>
                    <strong>(686) 511-0497</strong>
                </div>
                <div class="contact-card">
                    <p>📧 Email</p>
                    <strong>jossueramon12@gmail.com</strong>
                </div>
            </div>
        </div>
    </section>

    <!-- Download CV Section -->
    <section class="download-section">
        <div class="container">
            <div class="download-content">
                <div class="download-text">
                    <h4>Descarga mi CV completo</h4>
                    <p>Disponible en PDF con historial detallado</p>
                </div>
                <a href="#" class="btn btn-primary" onclick="downloadCV()">
                    ⬇️ Descargar CV
                </a>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer>
        <div class="footer-container">
            <div class="footer-top">
                <div class="footer-brand">
                    <h3>Ramón Espinoza</h3>
                    <p>Marketing Digital | Estrategia de Marca | Growth</p>
                </div>
                <div class="footer-links">
                    <a href="https://www.linkedin.com/in/jossue-ramon-martinez-espinoza-b56731385" target="_blank" rel="noopener noreferrer" title="LinkedIn">🔗</a>
                    <a href="mailto:jossueramon12@gmail.com" title="Email">✉️</a>
                </div>
            </div>

            <div class="footer-bottom">
                <p>© 2026 Ramón Espinoza. Diseño web moderno y responsive. Basado en estrategia digital.<br>
                Disponible para agencias y oportunidades de crecimiento.</p>
            </div>
        </div>
    </footer>

    <script>
        // Data
        const projectsData = [
            {
                id: 1,
                title: 'Bean Plant Based Food',
                type: 'Investigación de Mercado',
                category: 'academic',
                emoji: '📊',
                description: 'Estudio completo de segmentación y perfil del consumidor para restaurante vegano en Mexicali.',
                results: [
                    'Definición clara del perfil demográfico (21-35 años, 70% mujeres)',
                    'Identificación de motivaciones principales (salud, ética animal)',
                    'Recomendaciones estratégicas para posicionamiento'
                ],
                tools: ['Market Research', 'Data Analysis', 'Consumer Insights']
            },
            {
                id: 2,
                title: 'Huellitas Mxcl',
                type: 'Análisis Estratégico & Makeover',
                category: 'academic',
                emoji: '🐾',
                description: 'Investigación y propuesta de transformación de comunicación para refugio de animales con modelo de negocio social.',
                results: [
                    'Estrategia de sostenibilidad económica identificada',
                    'Propuesta de servicios generadores de ingresos (hotel canino)',
                    'Plan integral de comunicación digital'
                ],
                tools: ['Strategic Analysis', 'Business Model', 'Social Media Strategy']
            },
            {
                id: 3,
                title: 'Kia Futura - Content Strategy',
                type: 'Estrategia de Contenido Digital',
                category: 'professional',
                emoji: '🎬',
                description: 'Desarrollo de calendarios de contenido, edición audiovisual y análisis de desempeño en redes sociales.',
                results: [
                    'Calendario de contenido trimestral',
                    'Análisis de engagement y CTR',
                    'Reportes de desempeño mensual'
                ],
                tools: ['Content Planning', 'Video Editing', 'Analytics']
            },
            {
                id: 4,
                title: 'Agencia 3CINCO - Activaciones',
                type: 'Estrategia de Activación de Marca',
                category: 'professional',
                emoji: '🎯',
                description: 'Ejecución de campañas promocionales y activaciones para múltiples empresas y franquicias.',
                results: [
                    '15+ activaciones diseñadas',
                    'Gestión logística integral',
                    'Impacto en visibilidad de marca'
                ],
                tools: ['Event Planning', 'Brand Activation', 'Marketing Execution']
            }
        ];

        const skillsData = {
            'Marketing Digital': ['SEO/SEM', 'Social Media Management', 'Content Strategy', 'Email Marketing', 'Analytics'],
            'Estrategia': ['Posicionamiento de marca', 'Investigación de mercado', 'Consumer Insights', 'Business Strategy', 'Propuestas de valor'],
            'Herramientas': ['Meta Ads', 'Google Analytics', 'Canva', 'CapCut', 'Adobe Básico', 'Excel Avanzado', 'HubSpot'],
            'Soft Skills': ['Análisis crítico', 'Comunicación profesional', 'Gestión de proyectos', 'Trabajo en equipo', 'Resolución de problemas']
        };

        const certificationsData = [
            {
                title: 'Marketing Digital',
                issuer: 'HubSpot Academy',
                date: 'Completado Mayo 2025',
                emoji: '📧',
                badge: 'Verificado'
            },
            {
                title: 'El Camino del Inversor: Método, Fundamentos de Inversión y Riesgo',
                issuer: 'Santander Open Academy',
                date: 'Completado 2025',
                emoji: '💰',
                badge: 'Verificado'
            },
            {
                title: 'Excel Avanzado',
                issuer: 'Santander Open Academy',
                date: 'Completado Junio 2026',
                emoji: '📊',
                badge: 'Nuevo'
            },
            {
                title: 'Inglés Técnico',
                issuer: 'Facultad de Idiomas UABC',
                date: 'Completado',
                emoji: '🌐',
                badge: 'Egresado'
            }
        ];

        // Initialize
        document.addEventListener('DOMContentLoaded', () => {
            renderProjects('all');
            renderSkills();
            renderCertifications();
            setupScrollAnimations();
            setupTheme();
        });

        // Functions
        function toggleTheme() {
            document.body.classList.toggle('light-mode');
            const isDark = !document.body.classList.contains('light-mode');
            localStorage.setItem('theme', isDark ? 'dark' : 'light');
        }

        function setupTheme() {
            const savedTheme = localStorage.getItem('theme');
            if (savedTheme === 'light') {
                document.body.classList.add('light-mode');
                document.querySelector('.theme-toggle').textContent = '🌙';
            }
        }

        function toggleMenu() {
            // Mobile menu functionality can be added here
        }

        function filterProjects(category) {
            renderProjects(category);
            document.querySelectorAll('.filter-btn').forEach(btn => {
                btn.classList.remove('active');
            });
            event.target.classList.add('active');
        }

        function renderProjects(category) {
            const grid = document.getElementById('projectsGrid');
            const filtered = category === 'all' 
                ? projectsData 
                : projectsData.filter(p => p.category === category);

            grid.innerHTML = filtered.map(project => `
                <div class="project-card">
                    <div class="project-emoji">${project.emoji}</div>
                    <div class="project-type">${project.type}</div>
                    <h3>${project.title}</h3>
                    <p class="project-description">${project.description}</p>
                    <div class="project-results">
                        <div class="project-results-label">Resultados:</div>
                        <ul class="project-results-list">
                            ${project.results.map(r => `<li><span>→</span> ${r}</li>`).join('')}
                        </ul>
                    </div>
                    <div class="project-tools">
                        ${project.tools.map(tool => `<span class="tool-tag">${tool}</span>`).join('')}
                    </div>
                </div>
            `).join('');
        }

        function renderSkills() {
            const grid = document.getElementById('skillsGrid');
            grid.innerHTML = Object.entries(skillsData).map(([category, skills]) => `
                <div class="skill-category">
                    <h3>${category}</h3>
                    ${skills.map((skill, idx) => {
                        const width = 75 + Math.random() * 25;
                        return `
                            <div class="skill-item">
                                <div class="skill-name">${skill}</div>
                                <div class="skill-bar">
                                    <div class="skill-fill" style="--skill-width: ${width}%"></div>
                                </div>
                            </div>
                        `;
                    }).join('')}
                </div>
            `).join('');
        }

        function renderCertifications() {
            const grid = document.getElementById('certificationsGrid');
            grid.innerHTML = certificationsData.map(cert => `
                <div class="cert-card">
                    <div class="cert-header">
                        <span class="cert-emoji">${cert.emoji}</span>
                        <span class="cert-badge">${cert.badge}</span>
                    </div>
                    <h4 class="cert-title">${cert.title}</h4>
                    <p class="cert-issuer">${cert.issuer}</p>
                    <p class="cert-date">${cert.date}</p>
                </div>
            `).join('');
        }

        function setupScrollAnimations() {
            const observer = new IntersectionObserver(entries => {
                entries.forEach(entry => {
                    if (entry.isIntersecting) {
                        entry.target.classList.add('revealed');
                    }
                });
            }, { threshold: 0.1 });

            document.querySelectorAll('.experience-item, .project-card, .skill-category, .cert-card').forEach(el => {
                el.classList.add('scroll-reveal');
                observer.observe(el);
            });
        }

        function downloadCV() {
            alert('El CV estará disponible pronto. Por ahora, puedes contactarme directamente en jossueramon12@gmail.com');
        }
    </script>
</body>
</html>
