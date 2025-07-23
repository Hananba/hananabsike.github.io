<!DOCTYPE html>
<html lang="fr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Hanan Absike, PhD - Physicienne</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }

        :root {
            --deep-blue: #001a33;
            --navy-blue: #00264d;
            --dark-blue: #000d1a;
            --accent-blue: #00aaff;
            --light-blue: #66ccff;
            --text-color: #e6f7ff;
        }

        body {
            background: linear-gradient(135deg, var(--dark-blue) 0%, var(--deep-blue) 100%);
            color: var(--text-color);
            line-height: 1.6;
            min-height: 100vh;
            position: relative;
            overflow-x: hidden;
        }

        /* Background effects */
        .stars {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: transparent url('https://i.imgur.com/2YX9X0s.png') repeat top center;
            z-index: -1;
            animation: move-stars 200s linear infinite;
        }

        @keyframes move-stars {
            0% { background-position: 0 0; }
            100% { background-position: 10000px 5000px; }
        }

        /* Navigation menu */
        nav.navtop {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            background-color: rgba(0, 13, 26, 0.9);
            padding: 15px 0;
            text-align: center;
            border-bottom: 1px solid var(--accent-blue);
            z-index: 1000;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.5);
            backdrop-filter: blur(5px);
        }

        nav.navtop a {
            color: var(--light-blue);
            text-decoration: none;
            margin: 0 15px;
            font-size: 1.1em;
            transition: all 0.3s ease;
            padding: 8px 15px;
            border-radius: 4px;
            font-weight: 500;
        }

        nav.navtop a:hover {
            color: white;
            background: rgba(0, 170, 255, 0.2);
            text-shadow: 0 0 10px var(--accent-blue);
        }

        /* Main content */
        .content {
            max-width: 1200px;
            margin: 90px auto 40px;
            padding: 20px;
            display: grid;
            grid-template-columns: 250px 1fr;
            gap: 30px;
        }

        /* Welcome banner */
        .welcome-section {
            background: linear-gradient(90deg, rgba(0, 13, 26, 0.8) 0%, rgba(0, 38, 77, 0.8) 100%);
            padding: 25px;
            text-align: center;
            border-radius: 10px;
            margin-bottom: 30px;
            grid-column: 1 / -1;
            border: 1px solid rgba(0, 170, 255, 0.3);
            box-shadow: 0 0 20px rgba(0, 170, 255, 0.2);
        }

        .welcome-section h1 {
            font-size: 2.5rem;
            margin-bottom: 10px;
            color: var(--light-blue);
            text-shadow: 0 0 15px var(--accent-blue);
        }

        .welcome-section p {
            font-size: 1.2rem;
            opacity: 0.9;
        }

        /* Left column - profile */
        .left-column {
            background: rgba(0, 13, 26, 0.7);
            border-radius: 15px;
            padding: 20px;
            border: 1px solid rgba(0, 170, 255, 0.3);
            box-shadow: 0 0 20px rgba(0, 170, 255, 0.2);
            height: fit-content;
        }

        .profile-photo {
            width: 100%;
            border-radius: 10px;
            border: 2px solid var(--accent-blue);
            box-shadow: 0 0 20px rgba(0, 170, 255, 0.4);
            margin-bottom: 20px;
        }

        .contact-box {
            background: rgba(0, 26, 51, 0.6);
            border-radius: 10px;
            padding: 15px;
            margin-top: 20px;
            border: 1px solid rgba(0, 170, 255, 0.2);
        }

        .contact-box h3 {
            color: var(--light-blue);
            border-bottom: 1px solid var(--accent-blue);
            padding-bottom: 10px;
            margin-bottom: 15px;
            font-size: 1.3rem;
        }

        .contact-links a {
            display: block;
            color: var(--light-blue);
            text-decoration: none;
            padding: 8px 0;
            transition: all 0.3s;
        }

        .contact-links a:hover {
            color: white;
            padding-left: 10px;
            text-shadow: 0 0 8px var(--accent-blue);
        }

        .contact-links i {
            width: 25px;
            margin-right: 10px;
            color: var(--accent-blue);
        }

        /* Right column - content */
        .right-column {
            background: rgba(0, 13, 26, 0.7);
            border-radius: 15px;
            padding: 30px;
            border: 1px solid rgba(0, 170, 255, 0.3);
            box-shadow: 0 0 20px rgba(0, 170, 255, 0.2);
        }

        .section-title {
            color: var(--light-blue);
            margin-bottom: 20px;
            padding-bottom: 10px;
            border-bottom: 2px solid var(--accent-blue);
            font-size: 1.8rem;
            display: flex;
            align-items: center;
            gap: 10px;
        }

        .section-content {
            margin-bottom: 30px;
        }

        ul {
            list-style-type: none;
            padding-left: 10px;
        }

        ul li {
            padding: 8px 0;
            padding-left: 30px;
            position: relative;
            border-left: 2px solid rgba(0, 170, 255, 0.3);
            margin-left: 10px;
            transition: all 0.3s;
        }

        ul li:hover {
            border-left: 2px solid var(--accent-blue);
            background: rgba(0, 170, 255, 0.05);
            border-radius: 0 5px 5px 0;
        }

        ul li:before {
            content: "•";
            color: var(--accent-blue);
            position: absolute;
            left: 0;
            font-size: 1.5rem;
            top: 2px;
        }

        .education-item {
            margin-bottom: 15px;
            padding-left: 20px;
            border-left: 2px solid rgba(0, 170, 255, 0.2);
        }

        .education-item strong {
            color: var(--light-blue);
            display: block;
            font-size: 1.1rem;
        }

        /* Footer section */
        .footer-section {
            text-align: center;
            padding: 30px;
            margin-top: 40px;
            grid-column: 1 / -1;
            border-top: 1px solid rgba(0, 170, 255, 0.3);
        }

        .visitor-counter {
            background: rgba(0, 26, 51, 0.6);
            padding: 15px;
            border-radius: 10px;
            display: inline-block;
            margin: 20px 0;
            border: 1px solid rgba(0, 170, 255, 0.2);
        }

        .copyright {
            color: rgba(230, 247, 255, 0.6);
            font-size: 0.9rem;
            margin-top: 20px;
        }

        /* Responsive design */
        @media (max-width: 900px) {
            .content {
                grid-template-columns: 1fr;
                margin-top: 80px;
            }
            
            .left-column {
                order: 2;
            }
            
            nav.navtop a {
                font-size: 0.9rem;
                margin: 0 8px;
                padding: 6px 10px;
            }
            
            .welcome-section h1 {
                font-size: 2rem;
            }
        }

        @media (max-width: 600px) {
            nav.navtop {
                padding: 10px 0;
            }
            
            nav.navtop a {
                font-size: 0.8rem;
                margin: 0 5px;
                padding: 5px 8px;
            }
            
            .content {
                padding: 10px;
                margin-top: 70px;
            }
            
            .welcome-section {
                padding: 15px;
            }
            
            .welcome-section h1 {
                font-size: 1.8rem;
            }
        }
    </style>
</head>
<body>
    <div class="stars"></div>
    
    <!-- Navigation menu -->
    <nav class="navtop">
        <a href="#home"><i class="fas fa-home"></i> Home</a>
        <a href="#experience"><i class="fas fa-flask"></i> Expérience</a>
        <a href="#publications"><i class="fas fa-book"></i> Publications</a>
        <a href="#teaching"><i class="fas fa-graduation-cap"></i> Enseignement</a>
        <a href="#service"><i class="fas fa-hands-helping"></i> Activités</a>
        <a href="#interests"><i class="fas fa-seedling"></i> Intérêts</a>
        <a href="#phd"><i class="fas fa-brain"></i> Projet PhD</a>
        <a href="#cv"><i class="fas fa-file-alt"></i> CV</a>
    </nav>
    
    <div class="content">
        <!-- Welcome banner -->
        <div class="welcome-section">
            <h1>✨ Welcome! ✨</h1>
            <p>Exploring the Universe Through my expertise 🌌🪐🧠</p>
        </div>
        
        <!-- Left column - Profile photo and contact -->
        <div class="left-column">
            <img src="https://images.unsplash.com/photo-1573496359142-b8d87734a5a2?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=400&q=80" alt="Hanan Absike" class="profile-photo">
            
            <div class="contact-box">
                <h3><i class="fas fa-link"></i> Contact ME</h3>
                <div class="contact-links">
                    <a href="https://scholar.google.com/citations?user=vj-nkYIAAAAJ" target="_blank">
                        <i class="fab fa-google"></i> Google Scholar
                    </a>
                    <a href="https://www.researchgate.net/profile/H-Absike" target="_blank">
                        <i class="fab fa-researchgate"></i> ResearchGate
                    </a>
                    <a href="#">
                        <i class="fas fa-file-pdf"></i> CV PDF à venir
                    </a>
                </div>
            </div>
        </div>
        
        <!-- Right column - Main content -->
        <div class="right-column">
            <h1 id="home" class="section-title">👩‍🔬 Hanan Absike, PhD</h1>
            
            <div class="section-content">
                <h2 id="interests" class="section-title"><i class="fas fa-seedling"></i> Interests</h2>
                <ul>
                    <li>Material Modelling</li>
                    <li>Quantum transport</li>
                    <li>Experimental Physics</li>
                    <li>Scientific programming</li>
                    <li>HPC Calculations</li>
                </ul>
            </div>
            
            <div class="section-content">
                <h2 class="section-title"><i class="fas fa-graduation-cap"></i> Education</h2>
                <div class="education-item">
                    <strong>PhD in Physics, 2019</strong>
                    <p>University of Mohammed V RABAT</p>
                </div>
                <div class="education-item">
                    <strong>MSc in Computational Physics, 2015</strong>
                    <p>University of Mohammed V RABAT</p>
                </div>
                <div class="education-item">
                    <strong>BSc in Science Physics, 2013</strong>
                    <p>University of Mohammed V RABAT</p>
                </div>
            </div>
            
            <div class="section-content">
                <h2 class="section-title"><i class="fas fa-brain"></i> Research Focus</h2>
                <ul>
                    <li>Computational material science</li>
                    <li>Quantum transport phenomena</li>
                    <li>Material modeling and simulation</li>
                    <li>High-performance computing applications</li>
                    <li>Experimental validation of theoretical models</li>
                </ul>
            </div>
            
            <div class="section-content">
                <h2 class="section-title"><i class="fas fa-code"></i> Technical Skills</h2>
                <ul>
                    <li>Python (NumPy, SciPy, Pandas)</li>
                    <li>MATLAB & Simulink</li>
                    <li>Quantum ESPRESSO</li>
                    <li>VASP</li>
                    <li>LAMMPS</li>
                    <li>High-Performance Computing (HPC)</li>
                </ul>
            </div>
            
            <div class="section-content">
                <h1 class="section-title"><i class="fas fa-star"></i> Enjoy Physics</h1>
                <p style="font-size: 1.2rem; line-height: 1.8; margin-top: 15px;">
                    Computational material, Material modelling Quantum transport, Experimental physics... 🌌
                    My passion lies at the intersection of theoretical physics and computational methods, 
                    exploring the fundamental properties of materials to unlock new possibilities in technology 
                    and scientific understanding.
                </p>
            </div>
        </div>
        
        <!-- Footer section -->
        <div class="footer-section">
            <div class="visitor-counter">
                <img src="https://visitor-badge.glitch.me/badge?page_id=hananabsike.hananabsike" alt="visitor badge">
                <p>🔢 You're visitor number above 👆 — thanks for stopping by!</p>
            </div>
            
            <p class="copyright">
                Ce site est maintenu par Dr. Hanan Absike – pour toute collaboration ou proposition d'enseignement, merci de me contacter.
            </p>
        </div>
    </div>

    <script>
        // Simple effect for navigation on scroll
        window.addEventListener('scroll', function() {
            const nav = document.querySelector('nav.navtop');
            if (window.scrollY > 50) {
                nav.style.background = 'rgba(0, 13, 26, 0.95)';
                nav.style.padding = '10px 0';
                nav.style.boxShadow = '0 5px 15px rgba(0, 0, 0, 0.7)';
            } else {
                nav.style.background = 'rgba(0, 13, 26, 0.9)';
                nav.style.padding = '15px 0';
                nav.style.boxShadow = '0 5px 15px rgba(0, 0, 0, 0.5)';
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
    </script>
</body>
</html>
