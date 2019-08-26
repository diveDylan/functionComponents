<template>
  <div id="app">
    <f-button
    class="f-button"
    style="color: red"
    type="primary"
    v-show="buttonText != 3"
    @click="add"
    >{{ buttonText }}</f-button>
  </div>
</template>

<script>
import FButton from './components/FButton.vue'

export default {
  name: 'app',
  data() {
    return {
      buttonText: 2
    }
  },
  components: {
    FButton
  },
  mounted() {
     let timer = setTimeout(() => {
      this.buttonText = 3
      clearTimeout(timer)
    }, 1000);
  },
  methods: {
    add() {
      this.buttonText ++
    }
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
.f-button {
  background: red
}
</style>
