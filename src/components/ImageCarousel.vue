<template>
  <div class="screens">
    {{ videos.length }}
  </div>
</template>

<script>
export default {
  name: 'ImageCarousel',
  props: ['screens']
}
</script>

<style>
  .screens {
    border: 1px solid red;
  }
  .screen {
    display: flex;
  }
  .screen-image {
    width: 75%;
    border: 1px solid green;
    padding: 15px;
  }
  .screen-descr {
    border: 1px solid orange;
    padding: 15px;
    overflow: hidden;
    width: 25%
  }
</style>
