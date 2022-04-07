<template>
  <h1>Meu nome é: {{ nome }}</h1>
</template>

<script>
export default {
  name: 'LifeCyrcle',
  data() {
    return {
      nome: 'Ainda não sei'
    };
  },
  created() {
    setTimeout(() => {
      this.nome = 'Matheus';
    }, 1000);
  },
  mounted() {
    setTimeout(() => {
      this.nome = 'Pedro';
    }, 2000);
    this.lifeCycle();
  },
  methods: {
    lifeCycle() {
      console.log('Executou');
    }
  }
};
</script>

<style>
</style>