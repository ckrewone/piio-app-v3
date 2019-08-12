<template>
    <v-layout wrap v-show="show">
        <v-flex class="not-supported text-md-center" xs12>
            <v-flex class="not-supported__emoji">
                <v-icon dark size="100">far fa-dizzy</v-icon>
            </v-flex>
            <v-divider class="not-supported__divider"></v-divider>
            <span class="not-supported__text">{{this.message}}</span>
        </v-flex>
    </v-layout>
</template>

<script>
  export default {
    name: 'NotSupportedComponent',
    props: {
      show: Boolean
    },
    data() {
      return {
        message: 'Resolution is not supported jet'
      }
    }
  };
</script>

<style scoped lang="sass">
    .not-supported
        font-family: Roboto, sans-serif
        z-index: 9999
        background: rgba(0, 0, 0, 0.5)
        margin-top: 30vh
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
</style>