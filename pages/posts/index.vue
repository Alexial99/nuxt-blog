<template>
  <div>
    <h1>Posts</h1>
    <post v-for="post in posts" :key="post.user" :post="post" @buttonClick="onButtonClick" />
  </div>
</template>
<script setup lang="ts">
import { IPost } from '@/shared/model/post.model'
const posts = [{ user: 'user1', age: 20 }, { user: 'user2', age: 20 }]
function onButtonClick (post: IPost) {
  console.log(post)
}
</script>
