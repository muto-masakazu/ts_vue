<template>
  <div id="app">
    <transition appear>
      <router-view/>
    </transition>
  </div>
</template>

<script lang="ts">
import Vue from 'vue'
export default class App extends Vue{
  
}
</script>


<style lang="scss">
#app {
  .v-leave-to {
    -webkit-transition: all 1.5s;
    -moz-transition: all 1.5s;
    -ms-transition: all 1.5s;
    -o-transition: all 1.5s;
    transition: all 1.5s;
    opacity: 0;
  }
  .v-enter-active {
    -webkit-transition: all 1.5s;
    -moz-transition: all 1.5s;
    -ms-transition: all 1.5s;
    -o-transition: all 1.5s;
    transition: all 1.5s;
    opacity: 1;
  }
  height: 100vh;
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  a {
    font-weight: bold;
    color: #2c3e50;
    &.router-link-exact-active {
      color: #42b983;
    }
  }
}


</style>
