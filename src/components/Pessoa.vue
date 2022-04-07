<template>
  <div>
    <h2>Esta é descrição da pessoa: {{ nome }}</h2>
    <!-- <Info compEmail="joao@email.com" /> -->
    <Info :propsEmail="propsEmail" />
  </div>
</template>

<script>
import Info from './Info.vue';
import Form from './Form.vue';
export default {
  name: 'Pessoa',
  components: {
    Info,
    Form
  },
  data() {
    return {
      nome: 'Matheus',
      propsEmail: 'oswaldo@email.com'
    };
  }
};
</script>

<style>
</style>
