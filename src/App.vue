<template>
  <div id="app">
    <Bingo/>
  </div>
</template>

<script>
import Bingo from './components/Bingo.vue'

export default {
  name: 'App',
  components: {
    Bingo
  }
}
</script>

<style lang="scss">
@import "@/scss/style.scss";
</style>
