<template>
  <ul id="nav">
    <router-link v-for="data in nav" :key="data.url" tag="li" :to="data.url" >{{ data.pageName }}</router-link>
  </ul>
</template>

<script>
import navJSON from '../data/nav.json'

export default {
  name: 'LeftNav',
  data() {
    return {
      nav: navJSON
    }
  }
}
</script>

<style>
#nav {
  position: absolute;
  width: 80px;
  left: -100px;
  list-style: none;
  top: 30px;
}

#nav li {
  cursor: pointer;
  margin: 10px 0;
}

#nav a {
  font-weight: bold;
  color: #2c3e50;
}

#nav a.router-link-exact-active {
  color: #42b983;
}
</style>
