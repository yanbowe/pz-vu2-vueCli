<template>
  <div>
    <h3 class="text-red-400">{{ msg }}</h3>
    <p class="bg-blue-400">
      Recommended IDE setup:
      <a href="https://code.visualstudio.com/" target="_blank">VSCode</a>
      +
      <a href="https://github.com/johnsoncodehk/volar" target="_blank">Volar</a>
    </p>

    <p>
      See
      <code>README.md</code>
      for more information.
    </p>

    <p>
      <a href="https://vitejs.dev/guide/features.html" target="_blank">Vite Docs</a>
      |
      <a href="https://v3.vuejs.org/" target="_blank">Vue 3 Docs</a>
    </p>

    <button type="button" @click="count++">count is: {{ count }}</button>
    <p>
      Edit
      <code>components/HelloWorld.vue</code>
      to test hot module replacement.
    </p>
    <h1 class="text-30px flex-center">{{ str }}</h1>
  </div>
</template>

<script lang="ts">
import { defineComponent, ref } from '@vue/composition-api';

export default defineComponent({
  props: {
    msg: {
      type: String,
      default: ''
    }
  },
  setup() {
    const count = ref<number>(0);
    const str = ref<string>('composition-api');
    return {
      count,
      str
    };
  }
});
</script>

<style scoped></style>
