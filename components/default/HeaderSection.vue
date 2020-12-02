<template>
  <header class="bg-blue-500">
      <nav class="flex align-center justify-between p-3">
          <div class=""><nuxt-link to="/">NB</nuxt-link></div>
          <div class="">
              <nuxt-link to="/blog">Blog</nuxt-link>
          </div>
      </nav>
  </header>
</template>

<script>
export default {
    data () {
        return {
            links: [
                {text: "NB", to: "/", left: true},
                {text: "Blog", to: "/blog", left: false},
            ]
        }
    }
}
</script>

<style>

</style>