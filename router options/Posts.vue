<template>
  <h2>Posts</h2>
  <router-link to="/posts/new">New Post</router-link>
  <ul>
    <li v-for="post in posts" :key="post.id">
      <router-link :to="`/posts/${post.id}`">
        {{ post.title }}
      </router-link>
    </li>
  </ul>
  <router-view :posts="posts" />
</template>

<script>
import { testPosts } from '../microblog/testPosts'

export default {
  data() {
    return {
      posts: testPosts
    }
  }
}
</script>

<style scoped>
</style>