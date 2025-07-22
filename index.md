---
layout: default
---

<style>
/* Menu fixe en haut */
nav.navtop {
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  background-color: #000;
  padding: 10px 0;
  text-align: center;
  border-bottom: 1px solid #00e5ff;
  font-family: monospace;
  z-index: 1000;
  box-shadow: 0 2px 10px rgba(0, 229, 255, 0.3);
}

nav.navtop a {
  color: #00e5ff;
  text-decoration: none;
  margin: 0 15px;
  font-size: 1.1em;
  transition: all 0.3s ease;
  padding: 5px 10px;
  border-radius: 4px;
}

nav.navtop a:hover {
  text-shadow: 0 0 5px #00ffff;
  background: rgba(0, 229, 255, 0.1);
}

/* Correction pour l'ancrage sous menu fixe */
:target::before {
  content: "";
  display: block;
  height: 60px;
  margin-top: -60px;
  visibility: hidden;
}

/* Conteneur principal */
.content {
  padding-top: 70px;
  position: relative;
  display: grid;
  grid-template-columns: 200px 1fr;
  gap: 30px;
  max-width: 1200px;
  margin: 0 auto;
}

/* Colonne gauche - Photo */
.left-column {
  text-align: center;
}

.profile-photo {
  width: 180px;
  border-radius: 10px;
  box-shadow: 0 0 10px #00e5ff;
  margin-top: 20px;
}

/* Colonne droite - Contenu */
.right-column {
  padding-right: 20px;
}

/* Supprimer le gras des titres */
h1, h2, h3 {
  font-weight: normal !important;
}

.welcome-section {
  background: linear-gradient(90deg, #0a0a0a 0%, #001f3f 100%);
  padding: 20px;
  text-align: center;
  color: #00e5ff;
  margin-bottom: 30px;
  grid-column: 1 / -1;
}

.stars {
  background: transparent url('https://raw.githubusercontent.com/CodeExplainedRepo/HTML-CSS-Star-Background/master/img/stars.png') repeat top center;
  position: fixed;
  top: 0; left: 0;
  width: 100%; height: 100%;
  z-index: -1;
  animation: move-stars 200s linear infinite;
}

@keyframes move-stars {
  0% { background-position: 0 0; }
  100% { background-position: 10000px 5000px; }
}

/* Style pour les listes */
ul {
  padding-left: 20px;
}

ul li {
  margin-bottom: 8px;
}

/* Responsive */
@media (max-width: 768px) {
  .content {
    grid-template-columns: 1fr;
    padding-top: 60px;
  }
  
  .left-column {
    text-align: center;
    margin-bottom: 20px;
  }
  
  nav.navtop a {
    font-size: 0.9em;
    margin: 0 8px;
    padding: 3px 5px;
  }
}
</style>

<nav class="navtop">
  <a href="#home">🏠 Home</a>
  <a href="#experience">🧪 Expérience</a>
  <a href="#publications">📚 Publications</a>
  <a href="#teaching">🎓 Enseignement</a>
  <a href="#service">🤝 Activités</a>
  <a href="#interests">🌱 Intérêts</a>
  <a href="#phd">🧠 Projet PhD</a>
  <a href="#cv">📄 CV</a>
</nav>

<div class="stars"></div>

<div class="content">
  <div class="welcome-section">
    <h1>✨ Welcome! ✨</h1>
    <p>Exploring the Universe Through my expertise 🌌🪐🧠</p>
  </div>
  
  <!-- Colonne gauche - Photo -->
  <div class="left-column">
    <img src="doc/123.jpg" class="profile-photo">
  </div>
  
  <!-- Colonne droite - Contenu principal -->
  <div class="right-column">
    <h1 id="home">👩‍🔬 Hanan Absike, PhD</h1>
    
    <hr>
    
    <h2 id="interests">🌱 Interests</h2>
    <ul>
      <li>Material Modelling</li>
      <li>Quantum transport</li>
      <li>Experimental Physics</li>
      <li>Scientific programming</li>
      <li>HPC Calculations</li>
    </ul>
    
    <hr>
    
    <h3>🔗 Contact ME :</h3>
    <ul>
      <li>🔬 <a href="https://scholar.google.com/citations?user=vj-nkYIAAAAJ">Google Scholar</a></li>
      <li>📘 <a href="https://www.researchgate.net/profile/H-Absike">ResearchGate</a></li>
      <li>💼 CV PDF à venir</li>
    </ul>
    
    <hr>
    
    <h3>🧪 Education :</h3>
    <ul>
      <li>PhD in Physics, 2019<br>University of Mohammed V RABAT</li>
      <li>MSc in Computational Physics, 2015<br>University of Mohammed V RABAT</li>
      <li>BSc in Science Physics, 2013<br>University of Mohammed V RABAT</li>
    </ul>
    
    <hr>
    
    <h1>✨ Enjoy physics ✨</h1>
    <p>Computational material, Material modelling Quantum transport, Experimental physics... 🌌</p>
    
    <p align="center">
      <img src="https://visitor-badge.glitch.me/badge?page_id=hananabsike.hananabsike" alt="visitor badge"/>
      <br>
      🔢 You're visitor number above 👆 — thanks for stopping by!
    </p>
    
    <p style="color:#999; font-size: 14px; margin-top: 3rem;">
      Ce site est maintenu par Dr. Hanan Absike – pour toute collaboration ou proposition d'enseignement, merci de me contacter.
    </p>
  </div>
</div>
