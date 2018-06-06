<template>
  <div id="app">
    <!-- <ul id="nav">
      <router-link tag="li" to="/">Home</router-link>
      <router-link tag="li" to="/about">About</router-link>
    </ul> -->
    <LeftNav></LeftNav>
    <div class="page-container">
      <transition name="page-change" mode="out-in">
      <router-view/>
    </transition>
    </div>
  </div>
</template>

<script>
import LeftNav from './components/LeftNav';
export default {
  components: {
    LeftNav
  }
}
</script>


<style>
html,body {
  background-color: #eee;
  margin: 0;
  height: 100%;
}
#app {
  font-family: Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  background-color: #fff;
  color: #222;
  height: 100%;
  width: 75%;
  margin: 0 auto;
  position: relative;
}

.page-container {
  overflow: hidden;
}

.page {
  padding: 30px;
}

.page-change-enter, 
.page-change-leave-to {
  opacity: 0;
  transform: translateX(-30%)
}

.page-change-leave, 
.page-change-enter-to {
  opacity: 1;
  transform: translateX(0)
}

.page-change-enter-active,
.page-change-leave-active {
  transition: all .3s;
}
</style>
