<template>
  <nav class="menu">
    <ul class="menu_header">
      <li><a href="#">Header Componente</a></li>
      <li><a href="#">Home</a></li>
      <li><a href="#">Projetos</a></li>
      <li><a href="#">Contato</a></li>
    </ul>
  </nav>
</template>

<script>
export default {
  name: 'Header'
};
</script>

<style scoped>
nav {
  width: 100%;
  display: grid;
  padding: 0 10px 10px 0;
  margin: 0 0 20px 0;
  /* background-color: antiquewhite; */
  justify-content: center;
  align-content: center;

  background-color: rgba(37, 36, 36, 0.692);
}

nav > ul {
  display: grid;
  width: 100%;
  list-style-type: none;
  text-decoration: none;
  vertical-align: baseline;
}
ul > li {
  padding: 0.625rem;
  text-align: center;
  margin: 10px 20px 10px 20px;
}
ul > li > a {
  color: rgb(245, 239, 239);
  padding: 0.625rem;
  background-color: transparent;
}
/* a:visited {
  color: rgba(68, 248, 122, 0.685);
} */
a:hover {
  color: rgba(0, 195, 255, 0.87);
}
nav > .menu_header {
  grid-template-columns: repeat(4, 1fr);

  vertical-align: baseline;
}

/* ul {
  list-style: none;
  display: flex;
  background-color: #111;
}
li {
  margin-right: 10px;
}
a {
  color: #ddd;
  text-decoration: none;
  transition: 0.5s;
}
a:hover {
  color: turquoise;
} */
</style>