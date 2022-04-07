<template>
  <div>
    <h2>Info</h2>
    <div class="props_compEmail">
      <h2>Props</h2>
      <!-- <p class="props_compEmail_p"> {{ compEmail }} - {{ email }} </p> -->
      <p class="props_compEmail_p">
        {{ compEmail }} - {{ email }} - {{ propsEmail }}
      </p>
    </div>
    <p v-if="esta_trabalhando"> Estou trabalhando no momento. </p>
    <p v-else>Estou em busca de novas oportunidades!</p>
    <P> Utilizo as seguintes tecnologias para back-end: </P>
    <ul>
      <li
        v-for="(technology, index) in backend_technologies"
        v-bind:key="index"
      >
        {{ technology }}
      </li>
    </ul>
    <p> Utilizo as seguintes tecnologias para front-end: </p>
    <ul>
      <li v-for="technology in frontend_technologies" :key="technology.id">
        {{ technology.language }}
      </li>
    </ul>
    <div>
      <button @click="showEmail">{{ textoBotao }}</button>
    </div>
    <p v-show="mostrar_email">Mande uma mensagem para: {{ email }}</p>
    <div class="portifolio">
      <a
        class="portifolio_link"
        v-bind:href="meu_link"
        target="_blank"
        rel="noopener noreferrer"
        >Clique aqui para acessar meu portfólio</a
      >
    </div>
    <Picture />
    <Form />
  </div>
</template>

<script>
import Picture from './Picture.vue';
import Form from './Form.vue';
export default {
  name: 'Info',
  components: {
    Picture,
    Form
  },
  props: {
    compEmail: String,
    propsEmail: String
  },
  data() {
    return {
      esta_trabalhando: false,
      mostrar_email: false,
      email: 'matheus@email.com',
      meu_link: 'https://www.google.com.br',
      textoBotao: 'Mostrar e-mail',
      backend_technologies: ['JavaScript', 'PHP', 'Python'],
      frontend_technologies: [
        {
          id: 1,
          language: 'HTML'
        },
        {
          id: 2,
          language: 'CSS'
        },
        {
          id: 3,
          language: 'Vue'
        }
      ]
    };
  },
  methods: {
    showEmail() {
      this.mostrar_email = !this.mostrar_email;
      if (!this.mostrar_email) {
        this.textoBotao = 'Mostrar e-mail';
      } else {
        this.textoBotao = 'Esconder e-mail';
      }
    }
  }
};
</script>

<style scoped>
.portifolio {
  width: 100%;
  display: grid;
  justify-content: center;
  align-content: center;
  text-align: justify;
  margin: 20px;
  padding: 2rem;
  background-color: rgba(0, 0, 0, 0.658);
}
.portifolio > .portifolio_link {
  text-decoration: none;
  font-size: 1.2em;
  background-color: transparent;
}
.props_compEmail {
  width: 100%;
  display: grid;
  background-color: rgba(0, 0, 0, 0.733);
  padding: 0.625rem;
}
.props_compEmail_p {
  padding: 5px;
  margin: 10px 0 10px 0;
  text-align: center;
  font-size: 2.3em;
}
</style>