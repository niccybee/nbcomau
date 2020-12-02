<template>
  <main class="flex items-center flex-col bg-blue-100 min-h-screen">
      <div class="md:p-4 lg:p-4 sm:p-2"><h1 class="text-6xl">Blog Page</h1></div>
      <div class="grid lg:grid-cols-4 md:grid-cols-3 sm:grid-cols-1 gap-2 w-full lg:max-w-6xl">
          <nuxt-link v-for="post in posts" :key="post.uuid" :to="post.slug">
          <article class="p-3 m-2 max-w-md border border-solid rounded-md bg-white">
              <img :src="post.feature_image">
              <h3 class="font-bold">{{post.title}}</h3>
              <p>{{post.excerpt}}</p>
             
          </article>
          </nuxt-link>
      </div>
  </main>
</template>

<script>
import {getPosts} from '../api/posts'

export default {
    async asyncData() {
        const posts = await getPosts();
        return {posts: posts}
    }

}
</script>

<style>

</style>