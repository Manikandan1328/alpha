<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>ALPHA</title>
    <style>
        /* --- CSS Styles --- */
        :root {
            --primary-blue: #004dff;
            --dark-blue: #003cc0;
            --dark-bg: #1a1a1a;
            --light-bg: #f5f5f5;
            --text-dark: #333;
            --text-light: #fff;
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: Arial, sans-serif;
            scroll-behavior: smooth;
        }

        body {
            background-color: white;
            color: var(--text-dark);
        }

        .container {
            width: 90%;
            max-width: 1200px;
            margin: 0 auto;
        }

        /* --- Header/Navigation --- */
        header {
            background-color: rgb(255, 255, 255);
            padding: 15px 0;
            border-bottom: 1px solid #eee;
            position: sticky;
            top: 0;
            z-index: 1000;
        }

        nav {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .logo-text {
            display: flex;
            align-items: center;
            font-size: 24px;
            font-weight: bold;
            color: var(--text-dark);
            text-decoration: none;
        }

        .logo-text img {
            height: 80px; /* Adjust based on your logo image size */
            margin-right: 8px;
        }

        .nav-links a {
            margin-left: 25px;
            text-decoration: none;
            color: var(--text-dark);
            font-weight: 500;
            transition: color 0.3s;
        }

        .nav-links a:hover {
            color: var(--primary-blue);
        }

        /* --- Hero Section (Home) --- */
        #home {
            min-height: 80vh;
            display: flex;
            align-items: center;
            justify-content: center;
            text-align: center;
            padding: 100px 0;
        }

        .hero-content {
            max-width: 800px;
        }

        .logo-large {
            height: 250px;
            width: auto;
            margin-bottom: 20px;
        }

        .hero-content h1 {
            font-size: 48px;
            font-weight: 800;
            margin-bottom: 10px;
            color: var(--text-dark);
        }

        .hero-content h1 span {
            color: var(--primary-blue);
        }

        .hero-content p {
            font-size: 18px;
            color: #666;
            margin-bottom: 30px;
        }

        .btn-primary {
            display: inline-block;
            background-color: var(--primary-blue);
            color: var(--text-light);
            padding: 12px 30px;
            text-decoration: none;
            border-radius: 5px;
            font-weight: bold;
            transition: background-color 0.3s, transform 0.3s;
        }

        .btn-primary:hover {
            background-color: var(--dark-blue);
            transform: translateY(-2px);
        }

        /* --- About Section --- */
        #about {
            background-color: var(--light-bg);
            padding: 100px 0;
            display: flex;
            align-items: center;
        }

        .about-content {
            display: flex;
            gap: 50px;
            align-items: center;
        }

        .about-image {
            flex: 1;
        }

        .about-image img {
            width: 100%;
            height: auto;
            border-radius: 10px;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.1);
        }

        .about-text {
            flex: 1;
            padding-right: 50px;
        }

        .about-text h2 {
            font-size: 36px;
            font-weight: 800;
            margin-bottom: 10px;
        }

        .about-text h2 span {
            color: var(--primary-blue);
        }

        .about-text hr {
            width: 80px;
            height: 3px;
            background-color: var(--primary-blue);
            border: none;
            margin-bottom: 20px;
        }

        .about-text p {
            font-size: 16px;
            line-height: 1.6;
        }

        /* --- Services Section --- */
        #services {
            padding: 100px 0;
            text-align: center;
        }

        #services h2 {
            font-size: 36px;
            margin-bottom: 5px;
        }

        #services p.subtitle {
            font-size: 18px;
            color: #666;
            margin-bottom: 50px;
        }

        .services-grid {
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 30px;
        }

        .service-card {
            background-color: #fff;
            padding: 40px 20px;
            border-radius: 10px;
            box-shadow: 0 5px 20px rgba(0, 0, 0, 0.05);
            transition: transform 0.3s, box-shadow 0.3s;
            text-align: center;
        }

        /* Hover Animation */
        .service-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 15px 35px rgba(0, 0, 0, 0.1);
        }

        .service-icon {
            font-size: 40px;
            color: var(--primary-blue);
            background-color: var(--light-bg);
            border-radius: 50%;
            width: 70px;
            height: 70px;
            display: inline-flex;
            justify-content: center;
            align-items: center;
            margin-bottom: 20px;
        }

        .service-card h3 {
            font-size: 20px;
            margin-bottom: 10px;
        }

        .service-card p {
            font-size: 14px;
            color: #666;
        }

        /* --- Contact Section --- */
        #contact {
            background-color: var(--light-bg);
            padding: 100px 0;
            text-align: center;
        }

        #contact h2 {
            font-size: 36px;
            margin-bottom: 5px;
        }

        #contact p.subtitle {
            font-size: 18px;
            color: #666;
            margin-bottom: 40px;
        }

        .contact-details {
            display: flex;
            justify-content: center;
            gap: 80px;
        }

        .contact-item {
            display: flex;
            align-items: center;
            margin-bottom: 15px;
            font-size: 18px;
            color: var(--text-dark);
        }

        .contact-item .icon {
            font-size: 24px;
            color: var(--primary-blue);
            margin-right: 15px;
        }

        .contact-group {
            text-align: left;
        }

        .contact-group a {
            text-decoration: none;
            color: var(--text-dark);
            display: block;
        }
        
        .contact-group a:hover {
            color: var(--primary-blue);
        }
        
        /* --- Footer --- */
        footer {
            background-color: var(--dark-bg);
            color: var(--text-light);
            padding: 30px 0;
            text-align: center;
        }

        .footer-logo {
            display: flex;
            justify-content: center;
            align-items: center;
            font-size: 20px;
            font-weight: bold;
            margin-bottom: 10px;
        }

        .footer-logo img {
            height: 25px;
            margin-right: 8px;
            filter: brightness(0) invert(1); /* Makes the logo white for the dark background */
        }

        footer p {
            font-size: 14px;
            color: #aaa;
        }
    </style>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css">
</head>
<body>

    <header>
        <div class="container">
            <nav>
                <a href="#home" class="logo-text">
                    <img src="Screenshot 2025-10-28 080229.png" alt="Alpha Logo">
                    Alpha
                </a>
                <div class="nav-links">
                    <a href="#home">Home</a>
                    <a href="#services">Services</a>
                    <a href="#about">About</a>
                    <a href="#contact">Contact</a>
                </div>
            </nav>
        </div>
    </header>

    <section id="home" class="container">
        <div class="hero-content">
             <img src="Screenshot 2025-10-28 080229.png" alt="Alpha Logo" class="logo-large">
            <h1>Think smart! <span>Think alpha!</span></h1>
            <p>We Build Digital Experiences That Matter.</p>
            <a href="#services" class="btn-primary">Explore Our Services</a>
        </div>
    </section>

    <section id="about">
        <div class="container about-content">
            <div class="about-image">
                <img src="ChatGPT Image Oct 25, 2025, 04_16_40 PM.png" alt="Autumnal leaves">
            </div>
            <div class="about-text">
                <h2>We Are <span>Team Alpha</span></h2>
                <hr>
                <p>We are a collective of **well-trained and passionate creators, designers, and developers**. We are excited to partner with you and transform your vision into a stunning digital reality. Your success is the motivation behind every project we create.</p>
            </div>
        </div>
    </section>

    <section id="services">
        <div class="container">
            <h2>Our Services</h2>
            <p class="subtitle">Innovative solutions to grow your business.</p>
            <div class="services-grid">
                <div class="service-card">
                    <div class="service-icon"><i class="fas fa-code"></i></div>
                    <h3>Web Development</h3>
                    <p>Creating stunning, responsive, and high-performance websites tailored to your business needs.</p>
                </div>

                <div class="service-card">
                    <div class="service-icon"><i class="fas fa-robot"></i></div>
                    <h3>Chatbot Development</h3>
                    <p>Engage your customers 24/7 with intelligent and conversational AI-powered chatbots.</p>
                </div>

                <div class="service-card">
                    <div class="service-icon"><i class="fas fa-palette"></i></div>
                    <h3>Graphic Design</h3>
                    <p>From logos to branding, we create visually compelling designs that tell your story.</p>
                </div>

                <div class="service-card">
                    <div class="service-icon"><i class="fas fa-chart-line"></i></div>
                    <h3>Digital Marketing</h3>
                    <p>Boost your online presence and reach your target audience with our data-driven marketing strategies.</p>
                </div>

                <div class="service-card">
                    <div class="service-icon"><i class="fas fa-video"></i></div>
                    <h3>Video Editing</h3>
                    <p>Professional video editing services to make your content shine and capture attention.</p>
                </div>

                <div class="service-card">
                    <div class="service-icon"><i class="fas fa-search"></i></div>
                    <h3>SEO Optimization</h3>
                    <p>Improve your search engine rankings and drive organic traffic with our expert SEO services.</p>
                </div>
            </div>
        </div>
    </section>

    <section id="contact">
        <div class="container">
            <h2>Get In Touch</h2>
            <p class="subtitle">We'd love to hear from you. Let's build something amazing together.</p>

            <div class="contact-details">
                <div class="contact-group">
                    <div class="contact-item">
                        <span class="icon"><i class="fas fa-envelope"></i></span>
                        <a href="mailto:thinkalpha.work@gmail.com">thinkalpha.work@gmail.com</a>
                    </div>
                </div>
                <div class="contact-group">
                    <div class="contact-item">
                        <span class="icon"><i class="fas fa-phone"></i></span>
                        <a href="tel:+919600406677">+91 9600406677</a>
                    </div>
                    <div class="contact-item" style="margin-top: -10px;">
                        <span class="icon"><i class="fas fa-phone"></i></span>
                        <a href="tel:+919003431011">+91 9003431011</a>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <footer>
        <div class="container">
            <div class="footer-logo">
                <img src="Screenshot 2025-10-28 080229.png" alt="Alpha Logo">
                Alpha
            </div>
            <p>&copy; 2025 Alpha. All rights reserved.</p>
            <p>Think smart! Think alpha!</p>
        </div>
    </footer>

    <script>
        document.addEventListener('DOMContentLoaded', function() {
            // Select all navigation links
            const navLinks = document.querySelectorAll('nav a');

            navLinks.forEach(link => {
                link.addEventListener('click', function(e) {
                    // Prevent default anchor link behavior
                    e.preventDefault();

                    // Get the target section's ID from the href attribute (e.g., '#services')
                    const targetId = this.getAttribute('href');
                    const targetElement = document.querySelector(targetId);

                    if (targetElement) {
                        // Calculate the position to scroll to
                        // The 'offsetTop' is the distance from the top of the document to the element.
                        // We subtract the header height (approx 60px) to account for the sticky header.
                        const headerHeight = 60; 
                        const offsetPosition = targetElement.offsetTop - headerHeight;

                        // Smoothly scroll to the calculated position
                        window.scrollTo({
                            top: offsetPosition,
                            behavior: 'smooth'
                        });
                    }
                });
            });
        });
    </script>

</body>
</html>
