<template>
  <div class="home">
    <section class="intro">
      <h1>Bienvenue</h1>
      <p>
        Et quoniam mirari posse quosdam peregrinos existimo haec lecturos forsitan, si contigerit, quamobrem cum oratio ad ea monstranda deflexerit quae Romae gererentur, nihil praeter seditiones narratur et tabernas et vilitates harum similis alias, summatim causas perstringam nusquam a veritate sponte propria digressurus.
      </p>
    </section>

    <section class="coachs">
      <h2>Nos Coachs</h2>
      <div class="coach-container">
        <div class="coach-card">
          <img src="@/assets/coach1.png" alt="Coach Axel" class="coach-img" />
          <p class="coach-name">LEPAZE Axel</p>
        </div>
        <div class="coach-card">
          <img src="@/assets/coach2.png" alt="Coach Adrien" class="coach-img" />
          <p class="coach-name">CURIE Marie</p>
        </div>
      </div>
    </section>
  </div>
</template>

<script setup>
defineOptions({
  name: "Home",
});
</script>

<style scoped>
/* Section principale */
.home {
  text-align: center;
  color: white;
  max-width: 1200px;
  margin: 0 auto;
}

/* Bienvenue */
.intro {
  padding: 20px;
}

h1 {
  font-size: 24px;
  margin-bottom: 10px;
  color: white;
}

/* Coachs */
.coachs {
  margin-top: 50px;
}

h2 {
  font-size: 24px;
  font-weight: bold;
  margin-bottom: 30px;
}

/* Grille des coachs */
.coach-container {
  display: flex;
  justify-content: center;
  gap: 40px;
}

/* Carte coach */
.coach-card {
  text-align: center;
}

.coach-img {
  width: 150px;
  height: 150px;
  border-radius: 50%;
  object-fit: cover;
  border: 3px solid #DEBA2D;
}

.coach-name {
  color: #DEBA2D;
  font-weight: bold;
  margin-top: 10px;
}
</style>
