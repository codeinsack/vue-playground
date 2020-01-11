<template>
  <div class="hello">
    <p>{{ someVar }}</p>
    <button @click="$emit('increment-counter', 0.2)">Click me</button>
    <custom-button></custom-button>
  </div>
</template>

<script>
import CustomButton from "./CustomButton";

export default {
  name: 'HelloWorld',
  components: {
    CustomButton,
  },
  props: {
    someVar: {
      type: String,
      validator(value) {
        return ['success', 'warning', 'danger'].indexOf(value) !== -1
      }
    },
  }
}
</script>

<style scoped>
.hello {
  background-color: cadetblue;
  color: white;
}
</style>
