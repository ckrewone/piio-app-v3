<template>
  <v-flex class="base">
    <v-card class="card__first" color="rgb(254,105,36)" :elevation="elevCounters[0]"></v-card>
    <v-card class="card__second" color="rgb(253,77,22)" :elevation="elevCounters[1]"></v-card>
    <v-card class="card__third" color="rgb(191,62,0)" :elevation="elevCounters[2]"></v-card>
    <v-card class="card__fourth" color="rgb(255,255,255)" :elevation="elevCounters[3]"></v-card>
    <v-card class="card__fifth" color="rgb(196,196,196)" :elevation="elevCounters[4]"></v-card>
    <v-card class="card__sixth" color="rgb(110,110,110)" :elevation="elevCounters[5]"></v-card>
    <nuxt/>
  </v-flex>
</template>

<script>
  export default {
    data() {
      return {
        elevCounters: [15, 8, 2, 2, 8, 15],
      };
    },
  };
</script>
<style scoped lang="sass">
  .base
    overflow-y: hidden
  @media screen and (max-width: 700px)
    .card
      &__first
        z-index: 10
        position: fixed
        overflow: hidden
        transform: rotate(6deg)
        width: 130vw
        margin-left: -10px
        margin-top: -150px
        height: 300px
      &__second
        z-index: 9
        position: fixed
        overflow: hidden
        transform: rotate(12deg)
        width: 130vw
        margin-left: -10px
        margin-top: -60px
        height: 300px
      &__third
        z-index: 8
        position: fixed
        overflow: hidden
        transform: rotate(15deg)
        width: 130vw
        margin-left: -10px
        margin-top: 60px
        height: 300px
      &__fourth
        z-index: 7
        position: fixed
        overflow: hidden
        transform: rotate(-12deg)
        width: 130vw
        margin-left: -10px
        margin-top: 600px
        height: 700px
      &__fifth
        z-index: 6
        position: fixed
        overflow: hidden
        transform: rotate(-15deg)
        width: 130vw
        margin-left: -10px
        margin-top: 500px
        height: 300px
      &__sixth
        z-index: 5
        position: fixed
        overflow: hidden
        width: 100vw
        height: 100vh
  @media screen and (max-width: 1200px) and (min-width: 700px)
    .card
      &__first
        z-index: 10
        position: fixed
        overflow: hidden
        transform: rotate(6deg)
        width: 130vw
        margin-left: -10px
        margin-top: -200px
        height: 300px
      &__second
        z-index: 9
        position: fixed
        overflow: hidden
        transform: rotate(12deg)
        width: 130vw
        margin-left: -10px
        margin-top: -100px
        height: 300px
      &__third
        z-index: 8
        position: fixed
        overflow: hidden
        transform: rotate(15deg)
        width: 130vw
        margin-left: -10px
        margin-top: 10px
        height: 300px
      &__fourth
        z-index: 7
        position: fixed
        overflow: hidden
        transform: rotate(-12deg)
        width: 130vw
        margin-left: -10px
        margin-top: 400px
        height: 700px
      &__fifth
        z-index: 6
        position: fixed
        overflow: hidden
        transform: rotate(-15deg)
        width: 130vw
        margin-left: -10px
        margin-top: 300px
        height: 300px
      &__sixth
        z-index: 5
        position: fixed
        overflow: hidden
        width: 100vw
        height: 100vh
  @media screen and (min-width: 1200px)
    .card
      &__first
        z-index: 10
        position: absolute
        transform: rotate(6deg)
        width: 130vw
        margin-left: -100px
        margin-top: -100px
        height: 300px
      &__second
        z-index: 9
        position: absolute
        transform: rotate(12deg)
        width: 130vw
        margin-top: -150px
        margin-left: -100px
        height: 500px
      &__third
        z-index: 8
        position: fixed
        overflow: hidden
        transform: rotate(15deg)
        width: 130vw
        margin-left: -100px
        margin-top: 150px
        height: 300px
      &__fourth
        z-index: 7
        position: fixed
        overflow: hidden
        transform: rotate(-12deg)
        width: 130vw
        margin-left: -10px
        margin-top: 700px
        height: 600px
      &__fifth
        z-index: 6
        position: fixed
        overflow: hidden
        transform: rotate(-15deg)
        width: 130vw
        margin-left: -10px
        margin-top: 600px
        height: 300px
      &__sixth
        z-index: 5
        position: fixed
        overflow: hidden
        width: 100vw
        height: 100vh
</style>
