<template>
  <div class="component">
    <label for="text">text</label>
    <input
      id="text"
      type="text"
      :value="inputText"
      @input="onFormInput"
    >
    <label for="checkbox"> checked</label>
    <input
      id="checkbox"
      type="checkbox"
      :checked="checkbox"
      @change="onCheckboxInput"
    >
    <v-expansion-panels>
      <v-expansion-panel
        title="click here"
      >
        <!--        <v-expansion-panel-text>
          <iframe
            src="https://giphy.com/embed/15wC7XdIXN5q8o6fr9"
            width="200"
            height="200"
            class="giphy-embed"
            allowFullScreen
          />

          <iframe
            src="https://giphy.com/embed/5n067EUZwH8cvtRfGz"
            height="200"
            class="giphy-embed"
            allowFullScreen
          />
        </v-expansion-panel-text>-->
      </v-expansion-panel>
    </v-expansion-panels>
  </div>
</template>
<script setup lang="ts">
defineProps(['inputText', 'checkbox'])
const emit = defineEmits(['update:inputText', 'update:checkbox'])
const onFormInput = (event: InputEvent) => {
  emit('update:inputText', (event.target as HTMLInputElement).value)
}
const onCheckboxInput = (event: InputEvent) => {
  emit('update:checkbox', (event.target as HTMLInputElement).checked)
}
</script>
<style scoped>
div.component {
    padding: 10px;
}
.component input{
    border: 1px solid black;
}
</style>
