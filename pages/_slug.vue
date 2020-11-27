<template>
<div id="article">
    <div class="w-full relative">
        <h1 class="absolute text-5xl text-bold bottom-3 left-3">{{post.title}}</h1>
      <img class="flex-1 w-90" :src="post.feature_image" alt="">
</div>
  <div class="w-full  flex items-center justify-center">
    <article class=" p-1">
        
        <section class="prose lg:prose-xl" v-html="post.html"></section>
    </article>
  </div>
</div>
</template>

<script>
import { getSinglePost } from '../api/posts';
export default {
    async asyncData ({params}) {
        const post = await getSinglePost(params.slug);
        return {post:post}
    } 
}
</script>

<style>

</style>