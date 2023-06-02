<script setup>
// Tableau des réalisations
import Realisation from "@/components/Realisation.vue";
import {onMounted} from "vue";

const realisations = [
  {
    image: 'numbers-01.jpg',
    titre: 'Tableau le chiffre 1',
    description: 'Expérimentation de couleurs'
  },
  {
    image: 'numbers-02.jpg',
    titre: 'Tableau le chiffre 2',
    description: 'Jeu de fondus'
  },
  {
    image: 'numbers-06.jpg',
    titre: 'Tableau le chiffre 6',
    description: '80\'s style'
  },
  {
    image: 'numbers-09.jpg',
    titre: 'Tableau le chiffre 9',
    description: 'Travail avec les pinceaux'
  },
  {
    image: 'numbers-12.jpg',
    titre: 'Tableau le chiffre 12',
    description: 'Répétition de formes'
  }
]

//Étape 5 - Modifier le titre du document HTML <title>
//Ajouter le lifecycle hook beforeMount aux pages PageAccueil.vue
onMounted(() => {
  document.title = "Laure Dinateur | Graphiste"
})


</script>

<template>
  <main>
    <!-- Titre principal du site, il ne doit y en avoir qu'un dans la page et
       il faut le placer dans <main> -->
    <h1>Mes réalisations</h1>


<!--    <ul class="realisations">-->
<!--      <Realisation-->
<!--      />-->
<!--      <li-->
<!--          v-for="reali in realisations"-->
<!--          :key="reali.titre"-->
<!--      >-->
<!--        <a :href="'img/' + reali.image">-->
<!--          <figure>-->
<!--            <img :src="'img/' + reali.image" :alt="reali.titre" />-->
<!--            <figcaption>{{ reali.description }}</figcaption>-->
<!--          </figure>-->
<!--        </a>-->
<!--      </li>-->
<!--    </ul>-->

<!--    faire l'etape 4-5
c'est a dire appele a la vue realisation qui contient deja props titre image et discription-->
    <ul class="realisations">
      <Realisation
          v-for="reali in realisations"
          :key="reali.titre"
          :image="reali.image"
          :titre="reali.titre"
          :description="reali.description"
      />

    </ul>
  </main>
</template>

<style scoped>
.realisations {
  list-style-type: none; /* suppression des puces */
  margin: 0;
  padding: 0;
}
</style>