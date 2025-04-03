<template>
  <div class="home">
    <section class="abonnement">
      <h1>Nos abonnements</h1>

      <!-- Modal -->
      <div v-if="isModalOpen" class="modal-container">
        <div class="overlay" @click="toggleModal"></div>
        <div class="modal">
          <button class="close-modal" @click="toggleModal">X</button>
          <h1>Conditions d’engagement</h1>
          <p>Avant de confirmer votre abonnement, veuillez lire attentivement les conditions suivantes :<br>
            Durée d’engagement
            Mensuel : renouvellement automatique chaque mois, annulable à tout moment.
            Trimestriel : engagement de 3 mois, renouvellement automatique à l’échéance.
            Annuel : engagement de 12 mois, renouvellement automatique à l’échéance.<br>
            Paiement & Facturation
            Le paiement est effectué en une seule fois au début de chaque période d’abonnement.
            En cas d’échec de paiement, l’accès au service peut être suspendu jusqu’à régularisation.<br>
            Annulation & Résiliation
            L’abonnement mensuel peut être annulé à tout moment avant la prochaine échéance.
            Les abonnements trimestriel et annuel sont non remboursables mais peuvent être annulés pour empêcher le renouvellement.
            Vous pouvez gérer votre abonnement depuis votre espace client.<br>
            Renouvellement Automatique
            Par défaut, votre abonnement est renouvelé automatiquement à la fin de chaque période.
            Vous pouvez désactiver le renouvellement dans les paramètres de votre compte avant la date d’échéance.<br>Support & Assistance
            Pour toute question ou réclamation, contactez notre support via [email/contact].<br><br>En confirmant votre abonnement, vous acceptez nos Conditions Générales d’Utilisation.</p>
        </div>
      </div>

      <!-- Tableau des abonnements -->
      <table>
        <thead>
          <tr>
            <th class="thTitre">Formule</th>
            <th class="thTitre">Tarif</th>
          </tr>
        </thead>
        <tbody>
          <tr>
            <td>Mensuel</td>
            <td>9,99€/mois</td>
          </tr>
          <tr>
            <td>Trimestriel</td>
            <td>27,99€/3 mois (soit 9,33€/mois)</td>
          </tr>
          <tr>
            <td>Annuel</td>
            <td>99,99€/an (soit 8,33€/mois)</td>
          </tr>
        </tbody>
      </table>
    </section>

    <!-- Bouton d'ouverture du modal -->
    <button class="modal-btn" @click="toggleModal">Conditions : Engagement minimum de 1 mois.</button>
  </div>
</template>

<script setup>
import { ref } from "vue";

// Variable réactive pour gérer l'état du modal
const isModalOpen = ref(false);

// Fonction pour ouvrir/fermer le modal
const toggleModal = () => {
  isModalOpen.value = !isModalOpen.value;
};
</script>

<style scoped>
/* Style global */
.home {
  text-align: center;
  color: white;
  max-width: 1200px;
  margin: 0 auto;
}

.abonnement {
  padding: 20px;
}

h1 {
  font-size: 24px;
  margin-bottom: 50px;
  color: white;
}

table {
  table-layout: fixed;
  width: 100%;
  border-collapse: collapse;
  border: 3px solid rgb(255, 255, 255);
}

.thTitre {
  font-size: 24px;
}

th, td {
  border: 3px solid rgb(255, 255, 255);
  padding: 20px 10px;
}

/*gerer la taille de la colonne formule du tableau */
th:first-child, td:first-child {
  width: 30%;
}

/*gerer la taille de la colonne tarif du tableau */
th:last-child, td:last-child {
  width: 70%;
}

/* Bouton */
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

.modal-btn {
  padding: 10px 14px;
  font-size: 18px;
  margin: 100px auto;
  display: block;
  min-width: 150px;
  cursor: pointer;
}

/* Modal centré */
.modal-container {
  position: fixed;
  top: 0;
  left: 0;
  width: 100vw;
  height: 100vh;
  background: rgba(0, 0, 0, 0.5);
  display: flex;
  align-items: center;
  justify-content: center;
}

.overlay {
  position: absolute;
  width: 100%;
  height: 100%;
  background: rgba(0, 0, 0, 0.5);
}

/* Correction du centrage */
.modal {
  position: fixed;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  width: 95%;
  max-width: 500px;
  min-width: 300px;
  padding: 30px;
  background: #fff;
  border-radius: 10px;
  text-align: center;
}

.close-modal {
  padding: 8px 10px;
  border: none;
  border-radius: 5px;
  font-size: 18px;
  position: absolute;
  top: 10px;
  right: 10px;
  cursor: pointer;
  background: #ff365e;
  color: #fff;
}

.modal h1 {
  margin-bottom: 10px;
  font-weight: 500;
  color: black;
}

.modal p {
  line-height: 1.4;
  margin-bottom: 5px;
  color: black;
}
</style>
