<template>
  <h1>{{ msg }}</h1>

  <p>
    <a href="https://vitejs.dev/guide/features.html" target="_blank">Vite Documentation</a> |
    <a href="https://v3.vuejs.org/" target="_blank">Vue 3 Documentation</a>
  </p>

  <button @click="state.count ++ ">count is: {{ state.count }}</button>
  <button @click="refValue ++ ">obj.id is: {{ refValue }}</button>
  <p>
    Edit
    <code>components/HelloWorld.vue</code> to test hot module replacement.
  </p>


</template>

<script setup>
import { defineProps, reactive, computed, ref } from 'vue'

const refValue = ref(1)

defineProps({
  msg: String
})


// data
const state = reactive({ count: 1, })


// computed
const negativeCount = computed(() => -state.count )


</script>

<style scoped>
a {
  color: #42b983;
}
</style>