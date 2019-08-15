<template>
    <v-flex class="base">
        <v-flex>
            <v-flex v-show="validScreenSize">
                <v-btn to="/login" class="play" color="rgb(254,105,36)" elevation="15" fixed icon large>
                    <v-icon :size="buttonSize" color="white">fas fa-play</v-icon>
                </v-btn>
                <v-btn class="info" color="rgb(191,62,0)" fixed large rounded>info</v-btn>
                <logo/>
            </v-flex>
        </v-flex>
        <not-supported-component :show="!validScreenSize"/>
        <footer-component/>
    </v-flex>
</template>

<script>
  import NotSupportedComponent from '../components/NotSupportedComponent';
  import FooterComponent from '../components/FooterComponent';
  import Logo from '../components/Logo';

  export default {
    components: { Logo, FooterComponent, NotSupportedComponent },
    layout: 'main',
    created() {
      window.addEventListener('resize', () => {
        this.validScreenSize = window.outerWidth / window.outerHeight > 0.60;
      });
    },
    destroyed() {
      window.removeEventListener('resize', this.handleResize);
    },
    data() {
      return {
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
