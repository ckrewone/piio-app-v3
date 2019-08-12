<template>
    <v-flex class="base">
        <v-flex>
            <v-flex v-show="validScreenSize">
                <v-btn class="play" color="rgb(254,105,36)" elevation="15" fixed icon large>
                    <v-icon :size="buttonSize" color="white">fas fa-play</v-icon>
                </v-btn>
                <v-btn class="info" color="rgb(191,62,0)" fixed large rounded>info</v-btn>
                <v-flex class="logo">
                    <v-flex class="logo__name">
                        <v-img :src="logo" class="logo__name--z-index" size="100"></v-img>
                    </v-flex>
                    <v-flex class="logo__app">app <span class="logo__version">v3</span></v-flex>
                    <v-flex class="logo__elipse"></v-flex>
                </v-flex>
            </v-flex>
        </v-flex>
        <not-supported-component :show="!validScreenSize"/>
        <footer-component></footer-component>
    </v-flex>
</template>

<script>
  import logo from '../assets/piio.svg';
  import NotSupportedComponent from '../components/NotSupportedComponent';
  import FooterComponent from '../components/FooterComponent';

  export default {
    components: { FooterComponent, NotSupportedComponent },
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
    }
  };
</script>


<style lang="sass" scoped>
    .base
        font-family: "Roboto Thin", Arial, sans-serif
    @media screen and (max-width: 1200px) and (min-width: 700px)
        .logo
            z-index: 10
            position: fixed
            top: 30vh
            left: 50vw
            margin-top: -100px
            margin-left: -120px
            height: 200px
            width: 300px
            &__name
                z-index: 8 !important
                margin-left: -70px
                margin-top: -70px
                &--z-index
                    z-index: 10
            &__app
                position: absolute
                top: 0
                left: 0
                margin-top: 40%
                margin-left: 70%
            &__version
                font-size: 10px
            &__elipse
                z-index: 9 !important
                position: absolute
                top: 0
                left: 0
                margin-left: 30px
                height: 140px
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
            top: 55vh
            left: 50vw
            margin-top: -125px
            margin-left: -200px
            height: 250px
            width: 400px
            &__name
                margin-left: -70px
                margin-top: -70px
                &--z-index
                    z-index: 10
                    width: 400px
            &__app
                position: absolute
                top: 0
                left: 0
                margin-top: 45%
                margin-left: 72%
                font-size: 25px
            &__version
                font-size: 16px
            &__elipse
                z-index: 9 !important
                position: absolute
                top: 0
                left: 0
                margin-left: 45px
                height: 220px
                width: 260px
                border-radius: 130px / 110px
                -moz-border-radius: 130px / 110px
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
