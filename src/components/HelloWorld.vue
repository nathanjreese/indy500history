<script setup>
import { ref } from 'vue'

defineProps({
  msg: String,
})

const count = ref(0)
const test_value = import.meta.env.VITE_TEST_VALUE
const test_env = import.meta.env.VITE_TEST_ENV
</script>

<template>
  <h1>{{ msg }}</h1>

  <div class="card">
    <button type="button" @click="count++">1ST IS: {{ test_value }}</button>
    <p>
      Edit
      <code>components/HelloWorld.vue</code> ENV TEST IS: {{ test_env }}
    </p>
  </div>

  <p>
    Check out
    <a href="https://vuejs.org/guide/quick-start.html#local" target="_blank"
      >create-vue</a
    >, the official Vue + Vite starter
  </p>
  <p>
    Install
    <a href="https://github.com/vuejs/language-tools" target="_blank">Volar</a>
    in your IDE for a better DX
  </p>
  <p class="read-the-docs">Click on the Vite and Vue logos to learn more</p>
</template>

<style scoped>
.read-the-docs {
  color: #888;
}
</style>
