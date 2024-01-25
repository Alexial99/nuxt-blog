<template>
  <v-card
    class="mx-auto"
    max-width="344"
  >
    <v-img
      src="https://cdn.vuetifyjs.com/images/cards/sunshine.jpg"
      height="200px"
      cover
    />

    <v-card-title>
      {{ getStyledString }}
      <p>input text {{ inputText }}</p>
      checkbox {{ checkbox }}
    </v-card-title>
    <v-card-text>
      <span>
        <slot />
      </span>
    </v-card-text>
  </v-card>
  <TestComponent
    v-model:inputText="inputText"
    v-model:checkbox="checkbox"
  />
</template>
<script setup lang="ts">
const inputText = ref('')
const checkbox = ref(true)
const getStyledString = computed(() => {
  return inputText.value.toUpperCase()
})
</script>
<style scoped>
div.component {
    background: honeydew;
}
</style>
