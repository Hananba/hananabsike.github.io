<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Hanan Absike, PhD - Astrophysicist</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }

        :root {
            --deep-space: #000720;
            --cosmic-purple: #1a063d;
            --stellar-blue: #001a3a;
            --accent-neon: #00eeff;
            --text-glow: #e6f7ff;
        }

        body {
            background: radial-gradient(ellipse at bottom, #0a0a2e 0%, #000013 100%);
            color: var(--text-glow);
            line-height: 1.7;
            min-height: 100vh;
            overflow-x: hidden;
            position: relative;
        }

        /* Galaxy Background */
        #galaxy-bg {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            z-index: -1;
            overflow: hidden;
        }

        .star {
            position: absolute;
            background-color: white;
            border-radius: 50%;
            animation: twinkle var(--duration, 4s) infinite ease-in-out;
        }

        @keyframes twinkle {
            0%, 100% { opacity: 0.2; transform: scale(0.5); }
            50% { opacity: 1; transform: scale(1); }
        }

        .nebula {
            position: absolute;
            border-radius: 50%;
            filter: blur(60px);
            opacity: 0.3;
        }

        /* Navigation menu */
        nav.navtop {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            background-color: rgba(10, 5, 30, 0.85);
            padding: 15px 0;
            text-align: center;
            border-bottom: 1px solid var(--accent-neon);
            z-index: 1000;
            backdrop-filter: blur(5px);
            box-shadow: 0 5px 25px rgba(0, 238, 255, 0.1);
        }

        nav.navtop a {
            color: var(--accent-neon);
            text-decoration: none;
            margin: 0 15px;
            font-size: 1.1em;
            transition: all 0.4s ease;
            padding: 8px 15px;
            border-radius: 30px;
            font-weight: 500;
            text-shadow: 0 0 5px rgba(0, 238, 255, 0.7);
        }

        nav.navtop a:hover {
            color: white;
            background: rgba(0, 238, 255, 0.15);
            box-shadow: 0 0 15px rgba(0, 238, 255, 0.4);
            transform: translateY(-3px);
        }

        /* Main content */
        .content {
            max-width: 1400px;
            margin: 100px auto 60px;
            padding: 30px;
            display: flex;
            flex-direction: column;
            align-items: center;
        }

        /* Welcome section */
        .welcome-section {
            background: rgba(10, 5, 40, 0.4);
            padding: 40px;
            text-align: center;
            border-radius: 20px;
            margin-bottom: 50px;
            border: 1px solid rgba(0, 238, 255, 0.3);
            box-shadow: 0 0 40px rgba(0, 170, 255, 0.2);
            backdrop-filter: blur(5px);
            max-width: 900px;
            transform: rotate(-1deg);
            position: relative;
            z-index: 10;
        }

        .welcome-section::before {
            content: "";
            position: absolute;
            top: -10px;
            left: -10px;
            right: -10px;
            bottom: -10px;
            border: 1px solid rgba(0, 238, 255, 0.2);
            border-radius: 25px;
            z-index: -1;
        }

        .welcome-section h1 {
            font-size: 3.2rem;
            margin-bottom: 15px;
            color: var(--accent-neon);
            text-shadow: 0 0 20px rgba(0, 238, 255, 0.8);
            font-weight: 300;
        }

        .welcome-section p {
            font-size: 1.4rem;
            opacity: 0.9;
            letter-spacing: 1px;
        }

        /* Profile section */
        .profile-section {
            display: flex;
            flex-wrap: wrap;
            justify-content: center;
            gap: 50px;
            margin-bottom: 60px;
            width: 100%;
        }

        .profile-card {
            background: rgba(10, 5, 40, 0.4);
            border-radius: 20px;
            padding: 30px;
            border: 1px solid rgba(0, 238, 255, 0.3);
            box-shadow: 0 0 40px rgba(0, 170, 255, 0.2);
            backdrop-filter: blur(5px);
            max-width: 500px;
            transform: rotate(2deg);
            position: relative;
            z-index: 10;
        }

        .profile-card:nth-child(2) {
            transform: rotate(-1deg);
            margin-top: 40px;
        }

        .profile-card::before {
            content: "";
            position: absolute;
            top: -10px;
            left: -10px;
            right: -10px;
            bottom: -10px;
            border: 1px solid rgba(0, 238, 255, 0.2);
            border-radius: 25px;
            z-index: -1;
        }

        .profile-photo {
            width: 100%;
            max-width: 250px;
            border-radius: 15px;
            border: 2px solid var(--accent-neon);
            box-shadow: 0 0 30px rgba(0, 238, 255, 0.5);
            margin: 0 auto 25px;
            display: block;
        }

        .profile-title {
            text-align: center;
            margin-bottom: 25px;
        }

        .profile-title h1 {
            font-size: 2.4rem;
            color: var(--accent-neon);
            text-shadow: 0 0 15px rgba(0, 238, 255, 0.6);
            margin-bottom: 10px;
            font-weight: 300;
        }

        .profile-title p {
            font-size: 1.1rem;
            opacity: 0.8;
        }

        .section-title {
            color: var(--accent-neon);
            margin-bottom: 20px;
            padding-bottom: 10px;
            border-bottom: 1px solid rgba(0, 238, 255, 0.4);
            font-size: 1.8rem;
            display: flex;
            align-items: center;
            gap: 12px;
            font-weight: 300;
        }

        .section-title i {
            text-shadow: 0 0 10px rgba(0, 238, 255, 0.7);
        }

        ul {
            list-style-type: none;
            padding-left: 20px;
        }

        ul li {
            padding: 12px 0;
            padding-left: 35px;
            position: relative;
            border-left: 1px solid rgba(0, 238, 255, 0.2);
            margin-left: 10px;
            transition: all 0.4s;
            font-size: 1.1rem;
        }

        ul li:hover {
            border-left: 1px solid var(--accent-neon);
            background: rgba(0, 238, 255, 0.05);
            padding-left: 40px;
        }

        ul li:before {
            content: "✦";
            color: var(--accent-neon);
            position: absolute;
            left: 0;
            font-size: 1.4rem;
            top: 10px;
            text-shadow: 0 0 8px rgba(0, 238, 255, 0.7);
        }

        /* Info cards */
        .info-cards {
            display: flex;
            flex-wrap: wrap;
            justify-content: center;
            gap: 40px;
            width: 100%;
            margin-bottom: 60px;
        }

        .info-card {
            background: rgba(10, 5, 40, 0.4);
            border-radius: 20px;
            padding: 30px;
            border: 1px solid rgba(0, 238, 255, 0.3);
            box-shadow: 0 0 40px rgba(0, 170, 255, 0.2);
            backdrop-filter: blur(5px);
            width: 100%;
            max-width: 400px;
            transform: rotate(-2deg);
            position: relative;
            z-index: 10;
        }

        .info-card:nth-child(2) {
            transform: rotate(1deg);
            margin-top: 30px;
        }

        .info-card:nth-child(3) {
            transform: rotate(3deg);
            margin-top: -20px;
        }

        .info-card::before {
            content: "";
            position: absolute;
            top: -10px;
            left: -10px;
            right: -10px;
            bottom: -10px;
            border: 1px solid rgba(0, 238, 255, 0.2);
            border-radius: 25px;
            z-index: -1;
        }

        .education-item {
            margin-bottom: 20px;
            padding-left: 25px;
            border-left: 1px solid rgba(0, 238, 255, 0.2);
        }

        .education-item strong {
            color: var(--accent-neon);
            display: block;
            font-size: 1.2rem;
            margin-bottom: 5px;
        }

        .contact-links a {
            display: block;
            color: var(--text-glow);
            text-decoration: none;
            padding: 12px 0;
            padding-left: 40px;
            transition: all 0.4s;
            position: relative;
            font-size: 1.1rem;
        }

        .contact-links a:hover {
            color: var(--accent-neon);
            padding-left: 50px;
            text-shadow: 0 0 8px rgba(0, 238, 255, 0.7);
        }

        .contact-links a i {
            position: absolute;
            left: 0;
            top: 50%;
            transform: translateY(-50%);
            font-size: 1.4rem;
            width: 35px;
            color: var(--accent-neon);
            text-shadow: 0 0 8px rgba(0, 238, 255, 0.7);
        }

        /* Footer section */
        .footer-section {
            text-align: center;
            padding: 40px 20px;
            margin-top: 40px;
            width: 100%;
            border-top: 1px solid rgba(0, 238, 255, 0.3);
            max-width: 900px;
            transform: rotate(1deg);
        }

        .visitor-counter {
            background: rgba(0, 26, 51, 0.3);
            padding: 20px;
            border-radius: 15px;
            display: inline-block;
            margin: 30px 0;
            border: 1px solid rgba(0, 238, 255, 0.2);
            box-shadow: 0 0 20px rgba(0, 170, 255, 0.2);
            backdrop-filter: blur(5px);
        }

        .visitor-counter img {
            filter: drop-shadow(0 0 5px var(--accent-neon));
        }

        .copyright {
            color: rgba(230, 247, 255, 0.6);
            font-size: 1rem;
            margin-top: 30px;
            text-shadow: 0 0 5px rgba(0, 238, 255, 0.3);
        }

        /* Animations */
        @keyframes float {
            0%, 100% { transform: translateY(0) rotate(var(--rotate, 0deg)); }
            50% { transform: translateY(-20px) rotate(var(--rotate, 0deg)); }
        }

        .floating {
            animation: float 8s ease-in-out infinite;
        }

        /* Responsive design */
        @media (max-width: 1100px) {
            .profile-section {
                flex-direction: column;
                align-items: center;
            }
            
            .profile-card:nth-child(2) {
                margin-top: 0;
            }
            
            .info-cards {
                flex-direction: column;
                align-items: center;
            }
            
            .info-card {
                margin-top: 40px !important;
                transform: rotate(0) !important;
            }
        }

        @media (max-width: 768px) {
            .welcome-section h1 {
                font-size: 2.4rem;
            }
            
            .welcome-section p {
                font-size: 1.2rem;
            }
            
            nav.navtop a {
                font-size: 0.9rem;
                margin: 0 8px;
                padding: 6px 12px;
            }
            
            .content {
                padding: 20px 15px;
                margin-top: 80px;
            }
            
            .profile-card, .info-card {
                padding: 25px;
            }
        }

        @media (max-width: 480px) {
            .welcome-section {
                padding: 30px 20px;
            }
            
            .welcome-section h1 {
                font-size: 2rem;
            }
            
            nav.navtop {
                padding: 12px 0;
            }
            
            nav.navtop a {
                font-size: 0.8rem;
                margin: 0 5px;
                padding: 5px 8px;
            }
            
            .section-title {
                font-size: 1.6rem;
            }
        }
    </style>
</head>
<body>
    <!-- Galaxy Background -->
    <div id="galaxy-bg"></div>
    
    <!-- Navigation menu -->
    <nav class="navtop">
        <a href="#home"><i class="fas fa-home"></i> Home</a>
        <a href="#experience"><i class="fas fa-flask"></i> Experience</a>
        <a href="#publications"><i class="fas fa-book"></i> Publications</a>
        <a href="#teaching"><i class="fas fa-graduation-cap"></i> Teaching</a>
        <a href="#activities"><i class="fas fa-hands-helping"></i> Activities</a>
        <a href="#interests"><i class="fas fa-seedling"></i> Interests</a>
        <a href="#phd"><i class="fas fa-brain"></i> PhD Project</a>
        <a href="#contact"><i class="fas fa-envelope"></i> Contact</a>
    </nav>
    
    <div class="content">
        <!-- Welcome banner -->
        <div class="welcome-section floating" style="--rotate: -1deg;">
            <h1>✨ Welcome to My Cosmic Journey ✨</h1>
            <p>Exploring the Universe Through Physics and Computation 🌌🪐🧠</p>
        </div>
        
        <!-- Profile section -->
        <div class="profile-section">
            <div class="profile-card floating" style="--rotate: 2deg;">
                <img src="doc/123.jpg" alt="Dr. Hanan Absike" class="profile-photo">
                
                <div class="profile-title">
                    <h1>Dr. Hanan Absike</h1>
                    <p>PhD in Physics | Computational Scientist</p>
                </div>
                
                <div class="contact-links">
                    <h2 class="section-title"><i class="fas fa-link"></i> Connect With Me</h2>
                    <a href="https://scholar.google.com/citations?user=vj-nkYIAAAAJ" target="_blank">
                        <i class="fab fa-google"></i> Google Scholar
                    </a>
                    <a href="https://www.researchgate.net/profile/H-Absike" target="_blank">
                        <i class="fab fa-researchgate"></i> ResearchGate
                    </a>
                    <a href="#">
                        <i class="fas fa-file-pdf"></i> Download CV (PDF)
                    </a>
                </div>
            </div>
            
            <div class="profile-card floating" style="--rotate: -1deg;">
                <h2 class="section-title"><i class="fas fa-seedling"></i> Research Interests</h2>
                <ul>
                    <li>Material Modelling & Simulation</li>
                    <li>Quantum Transport Phenomena</li>
                    <li>Experimental Physics Techniques</li>
                    <li>Scientific Computing & Algorithms</li>
                    <li>High-Performance Computing</li>
                    <li>Computational Astrophysics</li>
                </ul>
                
                <h2 class="section-title" style="margin-top: 30px;"><i class="fas fa-code"></i> Technical Expertise</h2>
                <ul>
                    <li>Python & Scientific Libraries</li>
                    <li>Quantum ESPRESSO & VASP</li>
                    <li>High-Performance Computing</li>
                    <li>Data Analysis & Visualization</li>
                    <li>MATLAB & Numerical Methods</li>
                    <li>Machine Learning in Physics</li>
                </ul>
            </div>
        </div>
        
        <!-- Info cards -->
        <div class="info-cards">
            <div class="info-card floating" style="--rotate: -2deg;">
                <h2 class="section-title"><i class="fas fa-graduation-cap"></i> Education</h2>
                
                <div class="education-item">
                    <strong>PhD in Physics (2019)</strong>
                    <p>University of Mohammed V, Rabat</p>
                    <p>Thesis: Advanced Materials Simulation Techniques</p>
                </div>
                
                <div class="education-item">
                    <strong>MSc in Computational Physics (2015)</strong>
                    <p>University of Mohammed V, Rabat</p>
                    <p>Focus: Quantum Systems Modeling</p>
                </div>
                
                <div class="education-item">
                    <strong>BSc in Physics (2013)</strong>
                    <p>University of Mohammed V, Rabat</p>
                    <p>Specialization: Theoretical Physics</p>
                </div>
            </div>
            
            <div class="info-card floating" style="--rotate: 1deg;">
                <h2 class="section-title"><i class="fas fa-star"></i> Research Focus</h2>
                <p style="font-size: 1.1rem; line-height: 1.8; margin-bottom: 25px;">
                    My research explores the intersection of computational physics and material science, 
                    focusing on quantum transport phenomena in novel materials. I combine advanced simulation 
                    techniques with experimental validation to unlock new understandings of material behaviors 
                    at atomic scales.
                </p>
                
                <h2 class="section-title"><i class="fas fa-project-diagram"></i> Current Projects</h2>
                <ul>
                    <li>Quantum transport in 2D materials</li>
                    <li>HPC simulations of material defects</li>
                    <li>Machine learning for material discovery</li>
                    <li>Experimental validation of computational models</li>
                    <li>Development of new simulation algorithms</li>
                </ul>
            </div>
            
            <div class="info-card floating" style="--rotate: 3deg;">
                <h2 class="section-title"><i class="fas fa-paper-plane"></i> Get In Touch</h2>
                <p style="font-size: 1.1rem; line-height: 1.8; margin-bottom: 25px;">
                    I'm always open to discussing new research collaborations, speaking opportunities, 
                    or potential teaching positions. Feel free to reach out through any of the platforms below.
                </p>
                
                <div class="contact-links">
                    <a href="mailto:contact@hananabsike.com">
                        <i class="fas fa-envelope"></i> contact@hananabsike.com
                    </a>
                    <a href="#">
                        <i class="fas fa-university"></i> University Profile
                    </a>
                    <a href="#">
                        <i class="fab fa-linkedin"></i> LinkedIn Profile
                    </a>
                </div>
                
                <h2 class="section-title" style="margin-top: 30px;"><i class="fas fa-globe"></i> Location</h2>
                <p style="font-size: 1.1rem;">
                    <i class="fas fa-map-marker-alt" style="color: var(--accent-neon); margin-right: 10px;"></i> 
                    Rabat, Morocco
                </p>
            </div>
        </div>
        
        <!-- Footer section -->
        <div class="footer-section">
            <h2 class="section-title"><i class="fas fa-rocket"></i> Explore the Cosmos of Knowledge</h2>
            <p style="font-size: 1.2rem; max-width: 800px; margin: 25px auto;">
                "The most beautiful thing we can experience is the mysterious. It is the source of all true art and science." 
                - Albert Einstein
            </p>
            
            <div class="visitor-counter">
                <img src="https://visitor-badge.glitch.me/badge?page_id=hananabsike.hananabsike" alt="visitor badge">
                <p style="margin-top: 15px; font-size: 1.1rem;">🔭 You're visitor number above 👆 — thanks for exploring my universe!</p>
            </div>
            
            <p class="copyright">
                This interstellar portfolio is maintained by Dr. Hanan Absike • For collaboration or teaching opportunities, please reach out
            </p>
        </div>
    </div>

    <script>
        // Create dynamic stars for galaxy background
        function createGalaxy() {
            const galaxy = document.getElementById('galaxy-bg');
            const starCount = 200;
            const nebulaCount = 5;
            
            // Create stars
            for (let i = 0; i < starCount; i++) {
                const star = document.createElement('div');
                star.classList.add('star');
                
                // Random properties
                const size = Math.random() * 3;
                const posX = Math.random() * 100;
                const posY = Math.random() * 100;
                const duration = 2 + Math.random() * 8;
                const delay = Math.random() * 5;
                
                star.style.width = `${size}px`;
                star.style.height = `${size}px`;
                star.style.left = `${posX}%`;
                star.style.top = `${posY}%`;
                star.style.animationDelay = `${delay}s`;
                star.style.setProperty('--duration', `${duration}s`);
                
                galaxy.appendChild(star);
            }
            
            // Create nebulas
            for (let i = 0; i < nebulaCount; i++) {
                const nebula = document.createElement('div');
                nebula.classList.add('nebula');
                
                // Random properties
                const width = 200 + Math.random() * 300;
                const height = 200 + Math.random() * 300;
                const posX = Math.random() * 100;
                const posY = Math.random() * 100;
                const colors = ['#3a1c71', '#162b78', '#5d3f6a', '#2c1b47', '#1e3f5a'];
                const color = colors[Math.floor(Math.random() * colors.length)];
                
                nebula.style.width = `${width}px`;
                nebula.style.height = `${height}px`;
                nebula.style.left = `${posX}%`;
                nebula.style.top = `${posY}%`;
                nebula.style.backgroundColor = color;
                
                galaxy.appendChild(nebula);
            }
        }
        
        // Initialize galaxy on load
        document.addEventListener('DOMContentLoaded', function() {
            createGalaxy();
            
            // Add floating animation to all floating elements with random delays
            document.querySelectorAll('.floating').forEach(el => {
                el.style.animationDelay = `${Math.random() * 2}s`;
            });
            
            // Add scroll effect to navigation
            window.addEventListener('scroll', function() {
                const nav = document.querySelector('nav.navtop');
                if (window.scrollY > 50) {
                    nav.style.background = 'rgba(10, 5, 30, 0.95)';
                    nav.style.padding = '12px 0';
                    nav.style.boxShadow = '0 5px 25px rgba(0, 238, 255, 0.15)';
                } else {
                    nav.style.background = 'rgba(10, 5, 30, 0.85)';
                    nav.style.padding = '15px 0';
                    nav.style.boxShadow = '0 5px 25px rgba(0, 238, 255, 0.1)';
                }
            });
            
            // Smooth scrolling for anchor links
            document.querySelectorAll('a[href^="#"]').forEach(anchor => {
                anchor.addEventListener('click', function (e) {
                    e.preventDefault();
                    document.querySelector(this.getAttribute('href')).scrollIntoView({
                        behavior: 'smooth'
                    });
                });
            });
        });
    </script>
</body>
</html>
