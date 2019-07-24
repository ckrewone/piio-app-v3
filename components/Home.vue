




<template>
  <v-flex class="background__base">
    <v-btn icon fixed class="play" large color="rgb(254,105,36)" elevation="15"><v-icon color="white" size="30" >fas fa-play</v-icon></v-btn>
    <v-btn rounded fixed large class="info" color="rgb(191,62,0)" >info</v-btn>
    <v-flex class="logo__name">
      <v-img :src="logo"></v-img>
      <v-flex class="logo__app">app <span class="logo__version">v3</span></v-flex>
    </v-flex>
    <v-flex class="logo__elipse">
    </v-flex>
    <v-card class="background__card--first" color="rgb(254,105,36)" :elevation="elevCounters[0]"></v-card>
    <v-card class="background__card--second" color="rgb(253,77,22)" :elevation="elevCounters[1]"></v-card>
    <v-card class="background__card--third" color="rgb(191,62,0)" :elevation="elevCounters[2]"></v-card>
    <v-card class="background__card--fourth" color="rgb(255,255,255)" :elevation="elevCounters[3]"></v-card>
    <v-card class="background__card--fifth" color="rgb(196,196,196)" :elevation="elevCounters[4]"></v-card>
    <v-card class="background__card--sixth" color="rgb(110,110,110)" :elevation="elevCounters[5]"></v-card>
  </v-flex>
</template>

<script>
  import logo from '../assets/piio.svg';

  export default {
    name: 'home',
    layout: 'default',
    data() {
      return {
        logo,
        increase: 1,
        decrease: -1,
        elevCounters: [15, 8, 2, 2, 8, 15],
      };
    },
  };
</script>

<style lang="sass">
  .info
    z-index: 10
    top: 30px
    right: 30px
    bottom: 20vh
    .play
      z-index: 11
      bottom: 20vh
      left: 50vw
      margin-left: -50px !important
      width: 100px !important
      height: 100px !important
    .background
      &__base
        z-index: -1
        position: fixed
        width: 100%
        height: 100%
        background: rgb(110,110,110)
        overflow: hidden
      &__card
        &--first
          height: 100vh
          z-index: 5
          transform: rotate(6deg)
          position: absolute
          width: 200vw
          text-align: center
          margin: -75vh 0vw 0vw 0vw
          overflow: hidden
        &--second
          z-index: 4
          height: 100vh
          transform: rotate(12deg)
          position: absolute
          width: 200vw
          text-align: center
          margin: -65vh 0vw 0vw 0vw
          overflow: hidden
        &--third
          z-index: 3
          height: 100vh
          transform: rotate(15deg)
          position: absolute
          width: 200vw
          text-align: center
          margin: -85vh 0vw 0vw 0vw
          overflow: hidden
        &--fourth
          z-index: 2
          height: 100vh
          transform: rotate(-12deg)
          position: absolute
          width: 200vw
          text-align: center
          margin: -30vh 0vw 0vw 0vw
          overflow: hidden
        &--fifth
          z-index: 1
          height: 100vh
          transform: rotate(-15deg)
          position: fixed
          width: 200vw
          text-align: center
          margin: -120vh 0vw 0vw 0vw
          overflow: hidden
    .logo
      &__name
        z-index: 7
        width: 500px
        position: fixed
        top: 50vh
        left: 50vw
        margin-left: -330px
        margin-top: -270px
      &__app
        font-family: 'Roboto', sans-serif
        font-weight: 200
        font-size: 30px
        color: white
        display: inline-block
        position: fixed
        top: 57vh
        left: 55vw
      &__version
        font-size: 14px
      &__elipse
        z-index: 6
        height: 140px
        position: fixed
        left: 50vw
        top: 50vh
        margin-top: -70px
        margin-left: -90px
        width: 180px
        border-radius: 90px / 70px
        -moz-border-radius: 100px / 50px
        transform: rotate(45deg)
        -webkit-transform: rotate(45deg)
        -moz-transform: rotate(45deg)
        -o-transform: rotate(45deg)
        -webkit-box-shadow: -20px 30px 23px 0px rgba(0,0,0,0.5)
        -moz-box-shadow: -20px 30px 23px 0px rgba(0,0,0,0.5)
        box-shadow: -5px 10px 23px 0px rgba(0,0,0,0.5)
        background: rgb(253,77,22)
      &__elipse:hover
        -webkit-box-shadow: -20px 30px 23px 0px rgba(0,0,0,0.8)
        -moz-box-shadow: -20px 30px 23px 0px rgba(0,0,0,0.8)
        box-shadow: -5px 10px 23px 0px rgba(0,0,0,0.8)
</style>
