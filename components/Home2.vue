<template>
  <v-flex class="background__base">
    dupa
  <v-btn icon fixed class="btn__play" large color="rgb(254,105,36)" elevation="15"><v-icon color="white" size="30" >fas fa-play</v-icon></v-btn>
  <v-btn rounded fixed large class="info" color="rgb(191,62,0)" >info</v-btn>
  <v-flex class="logo__name">
    <v-img :src="logo"></v-img>
    <v-flex class="logo__app">app <span class="logo__version">v3</span></v-flex>
  </v-flex>
  <v-flex class="logo__elipse">
  </v-flex>
  </v-flex>
</template>

<script>
  import logo from '../assets/piio.svg'
  export default {
    name: 'Home2',
    data () {
      return {
        logo,
      }
    }
  };
</script>

<style scoped lang="sass">
  .background
    &__base
      z-index: 1
      position: fixed
      width: 100%
      height: 100%
      background: rgb(110,110,110)
      overflow: hidden

</style>
