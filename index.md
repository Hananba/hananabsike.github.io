---
layout: none
---

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title> Hanan ABSIKE, PhD </title>
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

        /* Main content - Two-column layout */
        .content {
            max-width: 1400px;
            margin: 100px auto 60px;
            padding: 30px;
            display: flex;
            flex-wrap: wrap;
            gap: 30px;
        }

        /* Left column - Profile section */
        .left-column {
            flex: 1;
            min-width: 350px;
            display: flex;
            flex-direction: column;
            gap: 30px;
        }

        /* Right column - Content sections */
        .right-column {
            flex: 2;
            min-width: 500px;
            display: flex;
            flex-direction: column;
            gap: 30px;
        }

        /* Vertical sections */
        .vertical-section {
            background: rgba(10, 5, 40, 0.4);
            border-radius: 8px;
            padding: 40px;
            border: 1px solid var(--accent-neon);
            box-shadow: 0 0 40px rgba(0, 170, 255, 0.2);
            backdrop-filter: blur(5px);
            position: relative;
            z-index: 10;
            width: 100%;
        }

        /* Profile section */
        .profile-section {
            display: flex;
            flex-direction: column;
            align-items: center;
            text-align: center;
        }

        .profile-photo {
            width: 220px;
            height: 350px;
            border-radius: 50%;
            border: 2px solid var(--accent-neon);
            box-shadow: 0 0 30px rgba(0, 238, 255, 0.5);
            margin-bottom: 30px;
            object-fit: cover;
            background: linear-gradient(45deg, #0d324d, #7f5a83);
        }

        .profile-title h1 {
            font-size: 2.8rem;
            color: var(--accent-neon);
            text-shadow: 0 0 15px rgba(0, 238, 255, 0.6);
            margin-bottom: 15px;
            font-weight: 300;
        }

        .profile-title p {
            font-size: 1.4rem;
            opacity: 0.9;
            letter-spacing: 1px;
            margin-bottom: 30px;
        }

        .section-title {
            color: var(--accent-neon);
            margin-bottom: 25px;
            padding-bottom: 10px;
            border-bottom: 1px solid var(--accent-neon);
            font-size: 1.8rem;
            display: flex;
            align-items: center;
            justify-content: center;
            gap: 12px;
            font-weight: 300;
        }

        .contact-links {
            display: flex;
            flex-direction: column;
            gap: 15px;
            margin-top: 20px;
            width: 100%;
        }

        .contact-links a {
            display: flex;
            align-items: center;
            color: var(--text-glow);
            text-decoration: none;
            padding: 12px 20px;
            transition: all 0.4s;
            border-radius: 8px;
            background: rgba(0, 26, 51, 0.3);
            border: 1px solid rgba(0, 238, 255, 0.3);
        }

        .contact-links a:hover {
            color: var(--accent-neon);
            text-shadow: 0 0 8px rgba(0, 238, 255, 0.7);
            background: rgba(0, 238, 255, 0.1);
            transform: translateY(-3px);
        }

        .contact-links a i {
            font-size: 1.4rem;
            margin-right: 10px;
            color: var(--accent-neon);
            text-shadow: 0 0 8px rgba(0, 238, 255, 0.7);
        }

        /* Welcome section */
        .welcome-section {
            text-align: center;
            padding: 50px 30px;
            height: 100%;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
        }

        .welcome-section h1 {
            font-size: 3.2rem;
            color: var(--accent-neon);
            text-shadow: 0 0 20px rgba(0, 238, 255, 0.8);
            margin-bottom: 30px;
            font-weight: 300;
            line-height: 1.2;
        }

        .welcome-section p {
            font-size: 1.8rem;
            opacity: 0.9;
            letter-spacing: 1px;
            line-height: 1.6;
            max-width: 900px;
            margin: 0 auto 30px;
        }

        .cosmic-animation {
            position: relative;
            width: 300px;
            height: 300px;
            margin-top: 20px;
        }

        .orbit {
            position: absolute;
            border: 1px solid rgba(0, 238, 255, 0.3);
            border-radius: 50%;
            transform: translate(-50%, -50%);
            left: 50%;
            top: 50%;
        }

        .planet {
            position: absolute;
            border-radius: 50%;
            background: var(--accent-neon);
            box-shadow: 0 0 20px rgba(0, 238, 255, 0.7);
            transform: translate(-50%, -50%);
        }

        /* Content sections */
        .content-section {
            margin-bottom: 20px;
        }

        .content-section h2 {
            color: var(--accent-neon);
            font-size: 2.2rem;
            margin-bottom: 25px;
            text-shadow: 0 0 15px rgba(0, 238, 255, 0.6);
            display: flex;
            align-items: center;
            gap: 12px;
        }

        .content-section p {
            font-size: 1.2rem;
            line-height: 1.8;
            margin-bottom: 20px;
        }

        .content-section ul {
            list-style-type: none;
            padding-left: 20px;
        }

        .content-section li {
            padding: 12px 0;
            padding-left: 35px;
            position: relative;
            font-size: 1.1rem;
        }

        .content-section li:before {
            content: "✦";
            color: var(--accent-neon);
            position: absolute;
            left: 0;
            font-size: 1.4rem;
            top: 10px;
            text-shadow: 0 0 8px rgba(0, 238, 255, 0.7);
        }

        .education-item {
            margin-bottom: 25px;
            padding-left: 20px;
            border-left: 1px solid rgba(0, 238, 255, 0.3);
        }

        .education-item h3 {
            color: var(--accent-neon);
            font-size: 1.5rem;
            margin-bottom: 8px;
        }

        /* Shining elements */
        .shine {
            position: absolute;
            width: 30px;
            height: 30px;
            background-color: rgba(255, 255, 255, 0.8);
            border-radius: 50%;
            box-shadow: 0 0 20px 5px rgba(255, 255, 255, 0.9);
            animation: shineEffect 3s infinite alternate;
            z-index: 5;
        }

        @keyframes shineEffect {
            0% { opacity: 0.3; transform: scale(0.8); }
            100% { opacity: 1; transform: scale(1.2); }
        }

        /* Footer section */
        .footer-section {
            text-align: center;
            padding: 40px 20px;
            margin-top: 20px;
            border-top: 1px solid var(--accent-neon);
        }

        .visitor-counter {
            background: rgba(0, 26, 51, 0.3);
            padding: 20px;
            border-radius: 8px;
            display: inline-block;
            margin: 30px 0;
            border: 1px solid var(--accent-neon);
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

        /* Responsive design */
        @media (max-width: 992px) {
            .content {
                flex-direction: column;
            }
            
            .left-column, .right-column {
                min-width: 100%;
            }
        }

        @media (max-width: 768px) {
            .content {
                padding: 20px 15px;
                margin-top: 80px;
            }
            
            .vertical-section {
                padding: 30px 20px;
            }
            
            .welcome-section h1 {
                font-size: 2.5rem;
            }
            
            .welcome-section p {
                font-size: 1.4rem;
            }
            
            nav.navtop a {
                font-size: 0.9rem;
                margin: 0 8px;
                padding: 6px 12px;
            }
            
            .profile-title h1 {
                font-size: 2.2rem;
            }
            
            .cosmic-animation {
                width: 250px;
                height: 250px;
            }
        }

        @media (max-width: 480px) {
            .welcome-section h1 {
                font-size: 2rem;
            }
            
            .welcome-section p {
                font-size: 1.2rem;
            }
            
            nav.navtop {
                padding: 12px 0;
                display: flex;
                flex-wrap: wrap;
                justify-content: center;
            }
            
            nav.navtop a {
                font-size: 0.8rem;
                margin: 5px;
                padding: 5px 8px;
            }
            
            .section-title {
                font-size: 1.6rem;
            }
            
            .profile-photo {
                width: 180px;
                height: 280px;
            }
            
            .cosmic-animation {
                width: 200px;
                height: 200px;
            }
        }
    </style>
</head>
<body>
    <!-- Galaxy Background -->
    <div id="galaxy-bg"></div>
    
    <!-- Shining elements -->
    <div class="shine" style="top: 20%; left: 15%;"></div>
    <div class="shine" style="top: 40%; left: 85%;"></div>
    <div class="shine" style="top: 70%; left: 30%;"></div>
    <div class="shine" style="top: 80%; left: 70%;"></div>
    
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
        <!-- Left Column -->
        <div class="left-column">
            <!-- Profile section -->
            <div class="vertical-section profile-section" id="home">
                <img src="doc/123.jpg" alt="Dr. Hanan Absike" class="profile-photo">
                
                <div class="profile-title">
                    <h1>Dr. Hanan Absike</h1>
                    <p>PhD in Physics | Computational Scientist</p>
                </div>
                
                <h2 class="section-title"><i class="fas fa-link"></i> Connect With Me</h2>
                <div class="contact-links">
                    <a href="https://scholar.google.com/citations?user=vj-nkYIAAAAJ" target="_blank">
                        <i class="fab fa-google"></i> Google Scholar
                    </a>
                    <a href="https://www.researchgate.net/profile/H-Absike" target="_blank">
                        <i class="fab fa-researchgate"></i> ResearchGate
                    </a>
                    <a href="#">
                        <i class="fas fa-file-pdf"></i> Download CV (PDF)
                    </a>
                    <a href="mailto:hanan@example.com">
                        <i class="fas fa-envelope"></i> Email Me
                    </a>
                    <a href="https://linkedin.com/in/hananabsike" target="_blank">
                        <i class="fab fa-linkedin"></i> LinkedIn
                    </a>
                </div>
            </div>
            
            <!-- Technical Expertise -->
            <div class="vertical-section">
                <div class="content-section">
                    <h2><i class="fas fa-code"></i> Technical Expertise</h2>
                    <p>I leverage advanced computational tools to explore fundamental properties of materials:</p>
                    <ul>
                        <li>Python & Scientific Libraries</li>
                        <li>Quantum ESPRESSO & VASP</li>
                        <li>High-Performance Computing</li>
                        <li>MATLAB & Numerical Methods</li>
                        <li>Data Analysis & Visualization</li>
                        <li>Machine Learning in Physics</li>
                    </ul>
                </div>
            </div>
        </div>
        
        <!-- Right Column -->
        <div class="right-column">
            <!-- Welcome section -->
            <div class="vertical-section welcome-section">
                <h1>✨ Welcome to My Cosmic Journey ✨</h1>
                <p>Exploring the Universe Through Physics and Computation 🌌🪐🧠</p>
                
                <div class="cosmic-animation">
                    <div class="orbit" style="width: 280px; height: 280px;"></div>
                    <div class="orbit" style="width: 200px; height: 200px;"></div>
                    <div class="orbit" style="width: 120px; height: 120px;"></div>
                    
                    <div class="planet" id="planet1" style="width: 40px; height: 40px;"></div>
                    <div class="planet" id="planet2" style="width: 30px; height: 30px;"></div>
                    <div class="planet" id="planet3" style="width: 20px; height: 20px;"></div>
                </div>
            </div>
            
            <!-- Research Interests -->
            <div class="vertical-section">
                <div class="content-section">
                    <h2><i class="fas fa-seedling"></i> Research Interests</h2>
                    <p>My research explores the intersection of computational physics and material science, focusing on quantum phenomena at atomic scales.</p>
                    <ul>
                        <li>Material Modelling & Simulation</li>
                        <li>Quantum Transport Phenomena</li>
                        <li>Experimental Physics Techniques</li>
                        <li>High-Performance Computing</li>
                        <li>Computational Astrophysics</li>
                    </ul>
                </div>
            </div>
            
            <!-- Education -->
            <div class="vertical-section">
                <div class="content-section">
                    <h2><i class="fas fa-graduation-cap"></i> Education</h2>
                    <div class="education-item">
                        <h3>PhD in Physics (2019)</h3>
                        <p>University of Mohammed V, Rabat</p>
                        <p>Thesis: Advanced Materials Simulation Techniques</p>
                    </div>
                    <div class="education-item">
                        <h3>MSc in Computational Physics (2015)</h3>
                        <p>University of Mohammed V, Rabat</p>
                        <p>Focus: Quantum Systems Modeling</p>
                    </div>
                    <div class="education-item">
                        <h3>BSc in Physics (2013)</h3>
                        <p>University of Mohammed V, Rabat</p>
                        <p>Specialization: Theoretical Physics</p>
                    </div>
                </div>
            </div>
            
            <!-- Current Projects -->
            <div class="vertical-section">
                <div class="content-section">
                    <h2><i class="fas fa-project-diagram"></i> Current Projects</h2>
                    <p>My current research focuses on cutting-edge problems in computational physics and material science.</p>
                    <ul>
                        <li>Quantum transport in 2D materials</li>
                        <li>HPC simulations of material defects</li>
                        <li>Machine learning for material discovery</li>
                        <li>Experimental validation of computational models</li>
                        <li>Development of new simulation algorithms</li>
                    </ul>
                </div>
            </div>
            
            <!-- Footer section -->
            <div class="footer-section">
                <div class="visitor-counter">
                    <img src="https://visitor-badge.glitch.me/badge?page_id=hananabsike.hananabsike" alt="visitor badge">
                    <p style="margin-top: 15px; font-size: 1.1rem;">🔭 You are visitor number above 👆 — thank you for exploring my universe!</p>
                </div>
                
                <p class="copyright">
                    This cosmic portfolio is maintained by Dr. Hanan Absike • For collaboration or teaching opportunities, please contact me
                </p>
            </div>
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
        
        // Animate planets
        function animatePlanets() {
            const planet1 = document.getElementById('planet1');
            const planet2 = document.getElementById('planet2');
            const planet3 = document.getElementById('planet3');
            
            let angle1 = 0;
            let angle2 = 0;
            let angle3 = 0;
            
            setInterval(() => {
                angle1 += 0.005;
                angle2 += 0.008;
                angle3 += 0.012;
                
                // Planet 1 (outer orbit)
                const x1 = Math.cos(angle1) * 140;
                const y1 = Math.sin(angle1) * 140;
                planet1.style.left = `calc(50% + ${x1}px)`;
                planet1.style.top = `calc(50% + ${y1}px)`;
                
                // Planet 2 (middle orbit)
                const x2 = Math.cos(angle2) * 100;
                const y2 = Math.sin(angle2) * 100;
                planet2.style.left = `calc(50% + ${x2}px)`;
                planet2.style.top = `calc(50% + ${y2}px)`;
                
                // Planet 3 (inner orbit)
                const x3 = Math.cos(angle3) * 60;
                const y3 = Math.sin(angle3) * 60;
                planet3.style.left = `calc(50% + ${x3}px)`;
                planet3.style.top = `calc(50% + ${y3}px)`;
            }, 20);
        }
        
        // Initialize on load
        document.addEventListener('DOMContentLoaded', function() {
            createGalaxy();
            animatePlanets();
            
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
