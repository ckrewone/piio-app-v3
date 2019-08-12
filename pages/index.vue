<template>
    <v-flex @resize="resize">
        <v-flex>
            <v-flex v-show="validScreenSize">
                <v-btn class="play" color="rgb(254,105,36)" elevation="15" fixed icon large>
                    <v-icon :size="buttonSize" color="white">fas fa-play</v-icon>
                </v-btn>
                <v-btn class="info" color="rgb(191,62,0)" fixed large rounded>info</v-btn>
                <v-flex class="logo logo__name">
                    <v-img :src="logo" size="100"></v-img>
                    <v-flex class="logo logo__app">app <span class="logo__version">v3</span></v-flex>
                </v-flex>
                <v-flex class="logo logo__elipse">
                </v-flex>
            </v-flex>
        </v-flex>
        <v-layout wrap>
            <v-flex class="not-supported text-md-center" v-show="!validScreenSize" xs12>
              <v-flex class="not-supported__emoji">
                <v-icon dark size="100">far fa-dizzy</v-icon>
              </v-flex>
                <v-divider class="not-supported__divider"></v-divider>
                <span class="not-supported__text">Resolution is not supported jet</span>
            </v-flex>
        </v-layout>
    </v-flex>
</template>

<script>
  import logo from '../assets/piio.svg';

  export default {
    layout: 'main',
    created() {
      window.addEventListener('resize', () => {
        this.validScreenSize = window.innerWidth / window.innerHeight > 0.60;
      });
    },
    destroyed() {
      window.removeEventListener('resize', this.handleResize);
    },
    data() {
      return {
        logo,
        buttonSize: window.innerWidth > 1200 ? 30 : 20,
        validScreenSize: true
      };
    },
    computed: {
      indexClass() {
        return !this.validScreenSize ? 'index index--not-supported' : 'index';
      },
    },
    methods: {
      resize(event) {
        console.log(event);
      }
    }
  };
</script>


<style lang="sass" scoped>
    .not-supported
        font-family: Roboto, sans-serif
        z-index: 9999
        background: rgba(0, 0, 0, 0.5)
        margin-top: 40vh
        margin-left: 10px
        margin-right: 10px
        padding: 5vh 10px 10vh 10px
        text-align: center
        border-radius: 10px
        font-size: 40px
        color: white
        &__divider
          padding-top: 1vh
          padding-bottom: 1vh
        &__emoji
          padding-bottom: 2vh

    @media screen and (max-width: 1200px) and (min-width: 700px)
        .logo
            z-index: 10
            position: fixed
            top: 30vh
            left: 60vw
            &__name
                width: 400px
                margin-left: -330px
                margin-top: -200px
            &__app
                color: white
                font-size: 20px
                font-weight: 100
                margin-left: 30px
                margin-top: 40px
            &__version
                font-size: 12px
            &__elipse
                z-index: 9 !important
                height: 140px
                margin-top: -70px
                margin-left: -150px
                width: 180px
                border-radius: 90px / 70px
                -moz-border-radius: 100px / 50px
                transform: rotate(45deg)
                -webkit-transform: rotate(45deg)
                -moz-transform: rotate(45deg)
                -o-transform: rotate(45deg)
                -webkit-box-shadow: -20px 30px 23px 0px rgba(0, 0, 0, 0.5)
                -moz-box-shadow: -20px 30px 23px 0px rgba(0, 0, 0, 0.5)
                box-shadow: -5px 10px 23px 0px rgba(0, 0, 0, 0.5)
                background: rgb(253, 77, 22)
        .play
            z-index: 11
            position: absolute
            left: 50vw
            top: 80vh
            margin-top: -50px
            margin-left: -50px
            width: 100px !important
            height: 100px !important
        .info
            z-index: 10
            top: 30px
            right: 30px
            bottom: 20vh
    @media screen and (min-width: 1200px)
        .logo
            z-index: 10
            position: fixed
            top: 50vh
            left: 50vw
            &__name
                width: 600px
                margin-left: -400px
                margin-top: -270px
            &__app
                z-index: 10
                color: white
                font-size: 30px
                font-weight: 100
                margin-left: 130px
                margin-top: 90px
            &__version
                font-size: 12px
            &__elipse
                z-index: 9 !important
                height: 240px
                margin-top: -70px
                margin-left: -140px
                width: 280px
                border-radius: 140px / 120px
                -moz-border-radius: 100px / 50px
                transform: rotate(45deg)
                -webkit-transform: rotate(45deg)
                -moz-transform: rotate(45deg)
                -o-transform: rotate(45deg)
                -webkit-box-shadow: -20px 30px 23px 0px rgba(0, 0, 0, 0.5)
                -moz-box-shadow: -20px 30px 23px 0px rgba(0, 0, 0, 0.5)
                box-shadow: -5px 10px 23px 0px rgba(0, 0, 0, 0.5)
                background: rgb(253, 77, 22)
        .play
            z-index: 11
            position: fixed
            top: 87vh
            left: 50vw
            margin-top: -60px
            margin-left: -60px !important
            width: 120px !important
            height: 120px !important
        .info
            z-index: 10
            top: 30px
            right: 30px
            bottom: 20vh
</style>
