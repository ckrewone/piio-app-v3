<template>
    <v-footer absolute class="footer--background" style="z-index: 10; color: black">
        <v-flex class="text-md-center footer" xs12>
            <v-flex class="footer--inline-block footer__prefix">
            {{ new Date().getFullYear() }} -- Powered by
            </v-flex>
            <v-flex class="footer__name footer--inline-block">
            <v-img :src="name" ></v-img>
            </v-flex>
        </v-flex>
    </v-footer>
</template>

<script>
  import name from '../assets/cone.svg';

  export default {
    name: 'FooterComponent',
    data() {
      return {
        name
      };
    }
  };
</script>

<style lang="sass" scoped>
    .footer
        margin-left: -35px
        &__prefix
            font-size: 17px
            margin-bottom: 20px
        &__name
            position: absolute
            top: 0
            margin-top: -10px
            margin-left: 5px
            height: 40px
            width: 70px
        &--background
            background: rgba(0, 0, 0, 0)
        &--inline-block
            display: inline-block
</style>