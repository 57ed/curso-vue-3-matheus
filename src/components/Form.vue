<template>
  <div>
    <h1>Formulário</h1>
    <h2>Meu Formulário:</h2>
    <form @submit="enviarFormulario($event)">
      <div>
        <input type="text" v-model="name" />
      </div>
      <div>
        <input type="text" v-model="email" />
      </div>
      <div>
        <input type="submit" value="Enviar" />
      </div>
    </form>
  </div>
</template>

<script>
export default {
  name: 'Form',
  data() {
    return {
      name: '',
      email: ''
    };
  },
  methods: {
    enviarFormulario(e) {
      e.preventDefault();

      const name = this.name;
      const email = this.email;

      console.log('Formulário Enviado!');
      console.log(`O nome é ${name}`);
      console.log(`O email é ${email}`);
    }
  }
};
</script>

<style scoped>
h2 {
  text-align: center;
  color: rgb(15, 180, 180);
  font-size: 2em;
  padding-block: 2rem;
}
input[type='text'] {
  width: 100%;
  padding: 12px 20px;
  margin: 8px 0;
  display: inline-block;
  border: 1px solid rgb(15, 180, 180);
  border-radius: 6px;
  box-sizing: border-box;
  font-size: 1em;
}

input[type='submit'] {
  width: 100%;
  background-color: rgb(15, 180, 180);
  color: white;
  padding: 14px 20px;
  margin: 8px 0;
  border: none;
  border-radius: 6px;
  cursor: pointer;
  font-size: 1.5em;
}

input[type='submit']:hover {
  background-color: #06d4f8;
}

div {
  border-radius: 5px;
  background-color: rgba(82, 78, 78, 0.589);
  padding: 20px;
  font-family: cursive;
}
</style>