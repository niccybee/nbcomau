<template>
  <div>
    <header-section/>
    <Nuxt />
  </div>
</template>

<script>
import HeaderSection from '@/components/default/HeaderSection'
export default {
  components: {
    HeaderSection
  }
}
</script>

<style>
html {
  font-size: 16px;
  -ms-text-size-adjust: 100%;
  -webkit-text-size-adjust: 100%;
  -moz-osx-font-smoothing: grayscale;
  -webkit-font-smoothing: antialiased;
  box-sizing: border-box;
}


</style>
