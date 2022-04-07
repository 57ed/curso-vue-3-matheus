<template>
  <div>
    <Header />
    <PrimeiroComponente />
    <!-- ou <primeiro-componente /> -->
    <p class="paragrafo-pai">O dado de app é: {{ testando }}</p>
    <LifeCycle />
    <Pessoa />
  </div>
</template>

<script>
import PrimeiroComponente from './components/PrimeiroComponente.vue';
import LifeCycle from '@/components/LifeCycle';
import Pessoa from '@/components/Pessoa';
import Header from '@/components/Header';
export default {
  name: 'App',
  components: {
    PrimeiroComponente,
    LifeCycle,
    Pessoa,
    Header
  },
  data() {
    return {
      testando: 'Teste'
    };
  }
};
</script>

<style>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
body {
  width: 1350px;
  overflow-x: hidden;
  padding: 10px;
  margin: 0 10px 0 0;
  /* border: 1px solid red; */
  background-color: #333;
  color: #fff;
  font-size: 1.125em;
}
div {
  width: 100%;
  padding: 0.5%;
  margin: 5px 0 10px;
}

h1,
h2 {
  width: 100%;
  font-family: cursive;
  color: rgba(0, 195, 255, 0.685);
  text-align: center;
}
h1 {
  font-size: 2em;
}
h2 {
  font-size: 1.5em;
}
p {
  font-family: 'Times New Roman', Times, serif;
  text-align: start;
}
ul {
  width: 400px;
  display: grid;
  grid-template-columns: 1fr;
  justify-content: center;
  gap: 10px;
  margin: 20px 0 20px 10px;
  list-style-type: none;
  text-decoration: none;
}
ul > li {
  background-color: rgba(0, 0, 0, 0.589);
  padding: 0.625rem;
}
ul > li > a {
  color: rgb(245, 239, 239);
  cursor: pointer;
}
a {
  background-color: rgba(0, 0, 0, 0.589);
  padding: 0.625rem;
  color: rgb(245, 239, 239);
  cursor: pointer;
  text-decoration: none;
}

/* a:visited {
  color: rgba(68, 248, 122, 0.685);
} */
a:hover {
  color: rgba(0, 195, 255, 0.87);
}
.teste {
  background-color: black;
}
button {
  width: 90%;
  display: inline-block;
  background-color: rgba(0, 238, 255, 0.63);
  color: rgba(255, 255, 255, 0.973);
  padding: 10px;
  text-align: center;
  margin: 4px;
  border: 1px solid rgb(46, 143, 143);
  border-radius: 50px;
  font-size: 1.5em;
  cursor: pointer;
  margin: 20px 0 20px 10px;
}
button:hover {
  background-color: rgba(5, 72, 77, 0.63);
  color: rgba(255, 255, 255, 0.993);
  border: 1px solid rgb(46, 143, 143);
  border-radius: 50px;
}
</style>
