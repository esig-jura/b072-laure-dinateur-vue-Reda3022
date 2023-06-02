<script setup>

</script>

<template>
  <footer>
    <nav>
      <ul>
        <li>
          <a href="https://twitter.com/lauredi">
            <img src="../../public/img/facebook-draw.png" alt="Twitter">
          </a>
        </li>
        <li>
          <a href="https://www.facebook.com/laure.dinateur">
            <img src="../../public/img/facebook-draw.png" alt="Facebook">
          </a>
        </li>
      </ul>
    </nav>

    <div>&copy;2021 Laure Dinateur</div>
    <!-- Utiliser les HTML entities pour intégrer des caractères spéciaux à
    votre page comme le copyright : © => &copy;
    Référence : https://dev.w3.org/html5/html-author/charref
    -->
  </footer>
</template>

<style scoped>
/***********************
******** FOOTER ********
************************/

footer {
  text-align: center;
  padding: 50px 0 0; /* 50px en haut */
}

footer nav {
  margin-bottom: 1rem;
}

footer ul {
  list-style: none;
  padding: 0;
  margin: 0;
}

footer ul li {
  display: inline-block;
}

footer ul li img {
  width: 50px;
  height: 50px;
  margin: 0 15px;

  -webkit-filter: grayscale(1);
  filter: grayscale(1);

  -webkit-transition: -webkit-filter 500ms linear;
  transition: filter 500ms linear;
}

footer ul li img:hover {
  -webkit-filter: grayscale(0);
  filter: grayscale(0);
}

</style>