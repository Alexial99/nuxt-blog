<template>
  <div>
    <h3>{{ post.user }}</h3>
    <span>{{ post.age }}</span>
    <button @click="onButtonClick">
      ТЫК
    </button>
  </div>
</template>
<script setup lang="ts">
import { IPost } from '@/shared/model/post.model'
interface IProps {
    post: IPost,
    isActive?: boolean,
}
const props = withDefaults(defineProps<IProps>(), {
  isActive: false
})

// eslint-disable-next-line func-call-spacing
const emit = defineEmits<{
    (e: 'buttonClick', post: IPost): void,
    (e: 'anotherClick'): void
}>()

const onButtonClick = () => {
  emit('buttonClick', props.post)
}
</script>
