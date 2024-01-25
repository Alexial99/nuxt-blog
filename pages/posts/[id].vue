<template>
  <div>
    <h3>{{ route.params.id }}</h3>
    <span> hi my route param {{ route.params.id }}</span>
  </div>
</template>
<script setup lang="ts">
const route = useRoute()
console.log(route.params.id)
</script>
