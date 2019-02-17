<template>
  <div class="app">
    <tetris></tetris>
  </div>
</template>

<script>
import tetris from './tetris/tetris.vue'
import 'animate.css/animate.css'

export default {
  name: 'app',
  data () {
    return {}
  },
  components: {tetris},
}

</script>

<style>

</style>
