<template>
  <div>
    <h1>Picture</h1>
    <div class="picture_avatar">
      <img :src="avatar" :alt="descricao" />
    </div>
    <!-- <Reutilizacao /> -->
    <MudarImagem @mudar-imagem="trocarImagem" />
  </div>
</template>

<script>
// import Reutilizacao from './Reutilizacao.vue';
import MudarImagem from './MudarImagem.vue';
export default {
  name: 'Picture',
  // components: { Reutilizacao },
  components: { MudarImagem },
  data() {
    return {
      avatar: '/img/avatar.png',
      descricao: 'Matheus Battisti'
    };
  },
  methods: {
    trocarImagem() {
      this.avatar = '/img/avatar2.png/';
    }
  }
};
</script>

<style>
img {
  width: 250px;
}
.picture_avatar {
  display: grid;
  justify-content: center;
  align-content: center;
}
</style>