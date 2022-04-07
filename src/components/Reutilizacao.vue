<template>
  <div class="reutilizacao">
    <div class="reutilizacao_body">
      <h2>Componente Reutilização</h2>
      <button @click="ativar(), limpar()">Clique Aqui! Reutilização</button>
      <p>
        <span class="ativado" v-show="ativou">Ativado!</span>
      </p>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Reutilizacao',
  data() {
    return {
      ativou: false
    };
  },
  methods: {
    ativar() {
      this.ativou = !this.ativou;
    },
    limpar() {
      setTimeout(() => (this.ativou = ''), 1500);
    }
  }
};
</script>

<style scoped>
.reutilizacao {
  width: 100%;
  padding: 5rem;
  display: grid;
  grid-template-columns: 1fr;
  grid-template-rows: repeat(2, 1fr);
  justify-content: center;
  gap: 10px;
}
.reutilizacao > .reutilizacao_body {
  background-color: rgba(0, 0, 0, 0.651);
  color: rgb(253, 250, 250);
  padding: 1rem;
}
.reutilizacao_body > h2 {
  width: 100%;
  height: 50px;
}
.ativado {
  width: 100%;
  display: grid;
  font-size: 3rem;
  color: red;
  text-align: center;
}
</style>
