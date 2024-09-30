<template>
  <div class="content" @click="color = !color">
    <h1>Rsbuild with Vue</h1>
    <p>Start building amazing things with Rsbuild.</p>
  </div>
</template>

<script setup lang="ts">
import { ref } from 'vue'

const color = ref(true)
</script>

<style scoped>
.content {
  display: flex;
  min-height: 100vh;
  line-height: 1.1;
  text-align: center;
  flex-direction: column;
  justify-content: center;
}

.content h1 {
  font-size: 3.6rem;
  font-weight: 700;
  /* ok */
  /* color: v-bind("color ? 'red': 'green'"); */

  /* no ok */
  /* color: v-bind('color ? "red": "green"'); */
}

.content p {
  font-size: 1.2rem;
  font-weight: 400;
  opacity: 0.5;
}
</style>
