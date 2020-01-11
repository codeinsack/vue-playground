<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    <hello-world v-on:increment-counter="incrementCounter" />
    <div>{{ counter }}</div>
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'

export default {
  name: 'app',
  components: {
    HelloWorld
  },
  data() {
    return {
      counter: 0,
    }
  },
  methods: {
    incrementCounter: function (amount) {
      console.log('amount', amount);
      this.counter += amount;
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
</style>
