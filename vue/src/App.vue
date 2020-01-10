<template>
  <div id="app">
    <img src="./assets/logo.png">
    <button @click="camera()">take picture</button>
    <img id="myImage" alt="">
    <router-view/>
  </div>
</template>

<script>
import {cameraTakePicture} from '../static/cordovaplugin'
export default {
  name: 'App',
  methods: {
    camera () {
      cameraTakePicture()
    }
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
