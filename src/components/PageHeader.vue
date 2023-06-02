<script setup>

</script>

<template>
  <header>
    <!-- Logo du site -->
    <router-link class="logo" to="/">
      <div class="nom">Laure Dinateur</div>
      <div class="metier">Graphiste</div>
    </router-link>
<!--    menu de navigation qui est dans l'entete-->
<!--    dans le to il faut mettre le name du path qui est dans index.js-->
      <nav>
        <router-link to="/" exact-active-class="actif">Accueil</router-link>
        <RouterLink to="/contact" exact-active-class="actif">Me Contacter</RouterLink>
        <RouterLink to="/infos" exact-active-class="actif" >Qui suis-je ?</RouterLink>
      </nav>
  </header>
</template>

<style scoped>
/***********************
******** HEADER ********
***********************/

header {
  background-color: #011627;
  padding: 5px 0 0 0;
  margin: 0 0 30px 0;
}

header .logo {
  text-align: center;
  margin: 0;
}

header .nom {
  color: #2ec4b6;
  font-size: 1.75rem;
  margin: 15px 0;
  line-height: 0.8;
}

header .metier {
  color: #e71d36;
  margin: -5px 0 0; /*-5px haut 0 g/d 0 bas */
}

/***********************
******** NAV MENU ******
************************/
header nav {
  text-align: center;
  padding: 10px 0;
  margin: 20px 0 0;
}

header nav ul {
  list-style: none;
  margin: 0 10px;
  padding: 0;
}

header nav ul li {
  display: inline-block;
}

header nav a,
header nav a:visited {
  color: #fdfffc;
  padding: 15px 10px;
  font-weight: 800;
}

header nav a.actif,
header nav a:hover {
  color: #2ec4b6;
}

header nav a[href='/'] {
  display: none;
}
</style>