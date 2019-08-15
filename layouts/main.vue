<template>
  <v-flex class="base">
    <transition name="fade">
    <v-card :class="getFirstCardClass" color="rgb(254,105,36)" :elevation="elevCounters[0]"></v-card>
    </transition>
    <v-card :class="getSecondCardClass" color="rgb(253,77,22)" :elevation="elevCounters[1]"></v-card>
    <v-card :class="getThirdCardClass" color="rgb(191,62,0)" :elevation="elevCounters[2]"></v-card>
    <v-card :class="getFourthCardClass" color="rgb(255,255,255)" :elevation="elevCounters[3]"></v-card>
    <v-card :class="getFifthCardClass" color="rgb(196,196,196)" :elevation="elevCounters[4]"></v-card>
    <v-card :class="getSixthCardClass" color="rgb(110,110,110)" :elevation="elevCounters[5]"></v-card>
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
    computed: {
      getFirstCardClass (){
        return this.getCardClass + '__first'
      },
      getSecondCardClass (){
        return this.getCardClass + '__second'
      },
      getThirdCardClass (){
        return this.getCardClass + '__third'
      },
      getFourthCardClass (){
        return this.getCardClass + '__fourth'
      },
      getFifthCardClass (){
        return this.getCardClass + '__fifth'
      },
      getSixthCardClass (){
        return this.getCardClass + '__sixth'
      },
      getCardClass (){
        return this.urlForm ? 'card-form' : 'card'
      },
      urlForm (){
        return this.$route.path === '/login' || this.$route.path === '/register'
      }
    }
  };
</script>
<style scoped lang="sass">
  .fade-enter-active, .fade-leave-active
    transition: margin-top .5s
  .fade-enter, .fade-leave-to
    opacity: 0
  .base
    overflow-y: hidden
  @media screen and (max-width: 700px)
    .card-form
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
    .card-form
      &__first
        z-index: 10
        position: fixed
        overflow: hidden
        transform: rotate(4deg)
        width: 130vw
        margin-left: -10px
        margin-top: -200px
        height: 300px
      &__second
        z-index: 9
        position: fixed
        overflow: hidden
        transform: rotate(5deg)
        width: 130vw
        margin-left: -10px
        margin-top: -140px
        height: 300px
      &__third
        z-index: 8
        position: fixed
        overflow: hidden
        transform: rotate(8deg)
        width: 130vw
        margin-left: -10px
        margin-top: -50px
        height: 300px
      &__fourth
        z-index: 7
        position: fixed
        overflow: hidden
        transform: rotate(-8deg)
        width: 130vw
        margin-left: -10px
        margin-top: 90vh
        height: 1700px
      &__fifth
        z-index: 6
        position: fixed
        overflow: hidden
        transform: rotate(-6deg)
        width: 130vw
        margin-left: -10px
        margin-top: 85vh
        height: 300px
      &__sixth
        z-index: 5
        position: fixed
        overflow: hidden
        width: 100vw
        height: 100vh
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
        height: 1700px
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
    .card-form
      &__first
        z-index: 10
        position: absolute
        transform: rotate(3deg)
        width: 130vw
        margin-left: -100px
        margin-top: -500px
        height: 600px
      &__second
        z-index: 9
        position: absolute
        transform: rotate(6deg)
        width: 130vw
        margin-top: -350px
        margin-left: -100px
        height: 500px
      &__third
        z-index: 8
        position: fixed
        overflow: hidden
        transform: rotate(7deg)
        width: 130vw
        margin-left: -100px
        margin-top: -100px
        height: 300px
      &__fourth
        z-index: 7
        position: fixed
        overflow: hidden
        transform: rotate(-6deg)
        width: 130vw
        margin-left: -10px
        margin-top: 90vh
        height: 2500px
      &__fifth
        z-index: 6
        position: fixed
        overflow: hidden
        transform: rotate(-8deg)
        width: 130vw
        margin-left: -10px
        margin-top: 85vh
        height: 300px
      &__sixth
        z-index: 5
        position: fixed
        overflow: hidden
        width: 100vw
        height: 100vh
    .card
      &__first
        z-index: 10
        position: absolute
        transform: rotate(6deg)
        width: 130vw
        margin-left: -100px
        margin-top: -400px
        height: 600px
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
        height: 2500px
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
