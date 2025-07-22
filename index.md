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
  height: 60px; /* Ajuster selon la hauteur du menu */
  margin-top: -60px;
  visibility: hidden;
}

/* Conteneur principal */
.content {
  padding-top: 70px; /* Doit correspondre à la hauteur du menu */
  position: relative; /* Pour positionnement relatif */
}

/* Style pour le conteneur de la photo et du titre */
.header-container {
  display: flex;
  align-items: flex-start; /* Alignement en haut */
  gap: 20px; /* Espacement entre la photo et le texte */
  margin-bottom: 20px;
}

/* Style pour la photo */
.profile-photo {
  width: 180px;
  border-radius: 10px;
  box-shadow: 0 0 10px #00e5ff;
  flex-shrink: 0; /* Empêche le rétrécissement */
}

/* Style pour le titre */
.profile-title {
  flex-grow: 1; /* Prend l'espace disponible */
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

<div class="content">
  <link rel="stylesheet" href="assets/css/style.css">

  <div style="background: linear-gradient(90deg, #0a0a0a 0%, #001f3f 100%); padding: 20px; text-align: center; color: #00e5ff; margin-top: 10px; margin-bottom: 20px;">
    <h1>✨ Welcome! ✨</h1>
    <p>Exploring the Universe Through my expertise 🌌🪐🧠</p>
  </div>

  <!-- Conteneur pour la photo et le titre -->
  <div class="header-container">
    <img src="doc/123.jpg" class="profile-photo">
    
    <div class="profile-title">
      <h1 id="home">👩‍🔬 Hanan Absike, PhD</h1>
    </div>
  </div>

  <hr>

  <!-- Le reste de votre contenu... -->
