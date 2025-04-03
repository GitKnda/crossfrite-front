<template>
    <div class="contact">
        <section class="formulaire">
            <h1>Formulaire</h1>
            <form>
                <div class="ligne">
                    <input class="espace-formulaire" type="text" placeholder="Nom" />
                    <input class="espace-formulaire" type="text" placeholder="Prénom" />
                </div>
                <input class="espace-formulaire" type="email" placeholder="Email" />
                <textarea class="espace-formulaire" placeholder="Message"></textarea>
                <div class="btn-container">
                    <button type="submit">Envoyer</button>
                </div>
            </form>
        </section>
        
        <div>
            <h2>Contact</h2>
            <p>Adresse : 123 Rue de la Salle, Sportville</p>
            <p>Téléphone : +33 6 12 34 56 78</p>
            <iframe src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d20221.462063890576!2d3.145282750433393!3d50.68871340445741!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x47c32891f6ff8a69%3A0x40af13e816459b0!2s59100%20Roubaix!5e0!3m2!1sfr!2sfr!4v1743088351551!5m2!1sfr!2sfr" width="600" height="450" style="border:0;" allowfullscreen="" loading="lazy" referrerpolicy="no-referrer-when-downgrade"></iframe>
        </div>
    </div>
</template>

<script setup>
defineOptions({
    name: "Contact",
});
</script>

<style scoped>
.contact {
  text-align: center;
  color: white;
  max-width: 1200px;
  margin: 0 auto;
}

.formulaire {
  padding: 20px;
}

h1 {
  font-size: 24px;
  margin-bottom: 50px;
  color: white;
}

button {
  padding: 10px 15px;
  background-color: #f5f0eb;
  color: #b98b20;
  text-decoration: none;
  font-weight: bold;
  border-radius: 5px;
  transition: 0.3s;
  cursor: pointer;
}

button:hover {
  background-color: #deba2d;
  color: #232528;
}

.espace-formulaire {
    padding: 10px;
    margin: 5px;
    width: 100%;
}

.ligne {
    display: flex;
    justify-content: space-between;
}

.ligne .espace-formulaire {
    width: 48%;
}

.btn-container {
    display: flex;
    justify-content: center;
    margin-top: 10px;
}

form {
    display: flex;
    flex-direction: column;
    align-items: center;
    width: 50%;
    margin: 0 auto;
}
</style>
