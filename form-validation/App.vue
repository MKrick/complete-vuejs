<template>
  <my-button
    background="darkslateblue"
    color="white"
    :disabled="!valid"
  />
</template>

<script>
import MyButton from './MyButton.vue'
export default {
  components: {
    MyButton
  },

  data() {
    return {
      valid: true
    }
  }
}
</script>

<style scoped>
button {
  background: none;
  color: black;
  border: none;
  border-radius: 5px;
  padding: 10px 40px;
  font-size: 16px;
  cursor: pointer;
}
button:disabled {
  opacity: 0.5;
}
button:hover {
  filter: brightness(125%)
}

</style>