<script setup>

// je defenit une proprieté props pour recevoir
// les pour me facilté les taches

defineProps(['image', 'titre', 'description'])

</script>

<template>
  <li>
    <a :href="'img/' + image">
      <figure>
        <img :src="'img/' + image" :alt="titre" />
        <figcaption>{{ description }}</figcaption>
      </figure>
    </a>
  </li>
</template>

<style scoped>


.realisations li {
  display: inline-block;
  width: 45%;
  margin: 2.5%;
  vertical-align: top;
}

.realisations li a {
  color: #011627;
}

.realisations figure {
  margin: 0;
  background-color: #e7e9eb;
}

.realisations figcaption {
  padding: 10px;
  font-size: 1rem;
}

/* Pour les écrans >= 480px */
@media only screen and (min-width: 480px) {
  /*Passage sur 3 cols*/
  .realisations li {
    width: calc(100% / 3 - 5%);
  }
}
</style>