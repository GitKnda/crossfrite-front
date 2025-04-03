<template>
  <div id="app">
    <header>
      <img src="@/assets/logo.png" alt="CrossFrite Logo" class="logo" />
      <h1>CROSSFRITE</h1>
      <nav>
        <router-link to="/">ACCUEIL</router-link>
        <router-link to="/subscription">ABONNEMENT</router-link>
        <router-link to="/contact">CONTACT</router-link>
      </nav>
    </header>
    <router-view />
  </div>
</template>

<script setup>
defineOptions({
  name: "App",
});
</script>

<style>
/* Global styles */
body {
  margin: 0;
  padding: 0;
  height: 100%; /* Assure que l'élément couvre toute la hauteur de la fenêtre */
  font-family: Arial, sans-serif;
  background-color: #1d1813;
}
/*before permet de contrôler l'opacité de l'image sans affecter les autres éléments*/
#app::before {
  content: "";
  position: absolute; /*permet à l'image de couvrir tout l'écran du top au bottom*/ 
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  background-image: url("@/assets/fond.png"); /* Vérifie que le chemin est correct */
  background-size: cover; /*permet que l'image reste unique*/
  opacity: 0.1; /* Applique l'opacité sur l'image*/
  z-index: -1; /* Assure que l'image de fond est derrière tout le contenu */
}

/* Header */
header {
  display: flex;
  align-items: center;
  justify-content: center; /* Centre tous les éléments */
  gap: 20px;
  background-color: rgba(30, 30, 30, 0.8); /* nav semi-transparent */
  padding: 10px 20px;
  position: relative;
  z-index: 1;/* Assure que l'image de fond est devant tout le contenu */
  
}

/* Logo */
.logo {
  height: 60px;
  position: absolute;
  left: 20px;
}

/* Titre */
h1 {
  color: #DEBA2D;
  font-size: 24px;
  font-weight: bold;
  text-align: center;
}

/* Navigation */
nav {
  display: flex;
  gap: 15px;
  position: absolute;
  right: 20px;
}

/*contour des "boutons" */
nav a {
  padding: 10px 15px;
  background-color: #f5f0eb;
  color: #b98b20;
  text-decoration: none;
  font-weight: bold;
  border-radius: 5px;
  transition: 0.3s;
}

/*nav mouse hover*/
nav a:hover {
  background-color: #deba2d;
  color: #232528;
}
</style>
