<template>
  <main :class="$style.main">
    Hello World! Check network for fetching the css file for App
  </main>
</template>

<script lang="ts">
import { defineComponent } from 'vue';

export default defineComponent({
  name: 'App',
});
</script>
<style module>
:global(.some-class) {
  color: red;
}

.main {
  background-color: #f0f0f0;
}
</style>
