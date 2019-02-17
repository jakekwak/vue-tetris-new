<template>
  <div :style="style" :class="display" class="cell"></div>
</template>

<script>
  import stageComputed from './stageComputed'

  export default {
    name: 'cell',
    props: ['stage', 'data', 'pos'],
    mixins: [stageComputed],
    computed: {
      display () { return this.data.class },
      style () {
        return {
          width: this.cellSize + 'px',
          height: this.cellSize + 'px',
          left: this.pos[0] * this.cellSize + 'px',
          bottom: this.pos[1] * this.cellSize + 'px'
        }
      }
    }
  }
</script>

<style scoped>


  .cell {
    position: absolute;
    box-sizing: border-box;
    border-style: outset;
    border-width: 3px;
    border-top-color: rgba(255, 255, 255, 0.3);
    border-left-color: rgba(255, 255, 255, 0.3);
  }
  .cell.I {
    background-color: red;
    border-right-color: red;
    border-bottom-color: red;
  }
  .cell.O {
    background-color: blue;
    border-right-color: blue;
    border-bottom-color: blue;
  }
  .cell.T {
    background-color: orange;
    border-right-color: orange;
    border-bottom-color: orange;
  }
  .cell.S {
    background-color: lime;
    border-right-color: lime;
    border-bottom-color: lime;
  }
  .cell.Z {
    background-color: cyan;
    border-right-color: cyan;
    border-bottom-color: cyan;
  }
  .cell.J {
    background-color: white;
    border-right-color: white;
    border-bottom-color: white;
  }
  .cell.L {
    background-color: magenta;
    border-right-color: magenta;
    border-bottom-color: magenta;
  }

</style>
