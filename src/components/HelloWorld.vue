<script setup>
import { ref } from 'vue'
const props = defineProps({
  element: {
    type: Object,
    default: {}
  },
});


</script>

<template>
  <!-- 这里不能填写注释 -->
  <div>{{ props.element }}</div>
</template>

<style scoped>
a {
  color: #42b983;
}
</style>
