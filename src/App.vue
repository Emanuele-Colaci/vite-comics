<script>
  import inizio from './components/Header.vue';
  import mezzo from './components/Main.vue';
  import fine from './components/Footer.vue';
  import fasciaAzzurra from './components/FasciaAzzurra.vue';
  export default{
    components: {
      inizio,
      mezzo,
      fine,
      fasciaAzzurra
    }
  }
</script>
<template>
  <div>
    <inizio />
    <mezzo />
    <fasciaAzzurra />
    <fine />
  </div>
</template>
<style lang="scss">
    @use './styles/generals.scss' as *;
    @use './styles/partials/variables' as *;
</style>