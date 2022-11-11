<script setup>
import Title from './components/Title.vue'
import ContentContainer from './components/ContentContainer.vue'
import Footer from './components/Footer.vue'
</script>

<template>
  <header>
    <div class="wrapper">
      <Title msg="Raster and Vector Images" />
    </div>
  </header>

  <main>
    <ContentContainer />
  </main>

  <Footer />
</template>

<style scoped>
header {
  line-height: 1.5;
}

.logo {
  display: block;
  margin: 0 auto 2rem;
}
</style>
