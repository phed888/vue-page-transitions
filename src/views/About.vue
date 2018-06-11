<template>
  <div class="about page">
    <h1>This is an about page</h1>
    <ImageCarousel v-bind:screens="screens"></ImageCarousel>
  </div>
</template>

<script>
import ImageCarousel from '../components/ImageCarousel'
import aboutJSON from '../data/project-data/about.json'

export default {
  name: 'About',
  components: 'ImageCarousel',
  data() {
    return {
      screens: aboutJSON
    }
  }
}
</script>

