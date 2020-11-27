<template>
  <main>
      <div><h1 class="text-6xl">Blog Page</h1></div>
      <div>
          <nuxt-link v-for="post in posts" :key="post.uuid" :to="post.slug">
          <article class="p-3 m-2 max-w-md border border-solid rounded-md">
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