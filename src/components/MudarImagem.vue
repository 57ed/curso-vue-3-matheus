<template>
  <div>
    <button @click="$emit('mudarImagem')">Troca imagem perfil</button>
  </div>
</template>

<script>
export default {
  name: 'MudarImagem',
  emits: ['mudarImagem']
};
</script>

<style>
</style>