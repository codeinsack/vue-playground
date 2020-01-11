<template>
  <div class="hello">
    <button @click="$emit('increment-counter', 0.2)">Click me</button>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
}
</script>

<style scoped>
.hello {
  background-color: cadetblue;
  color: white;
}
</style>
